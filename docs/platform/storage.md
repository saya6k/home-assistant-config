---
title: 스토리지
---

# 스토리지

상태 데이터와 빈번하게 갱신되는 런타임 파일을 어떻게 나눠 저장하는지 정리합니다.

## Recorder = 원격 MariaDB 단일 계층

| 계층     | 사용 도구        | 위치               | 보관 기간 / 목적                                          |
| -------- | ---------------- | ------------------ | --------------------------------------------------------- |
| Recorder | **원격 MariaDB** | TrueNAS (VPN 너머) | 모든 상태/이벤트. 그래프, 히스토리, 자동화 트리거 평가용. |

로컬 SQLite (`home-assistant_v2.db`) 는 사용하지 않습니다 — `recorder.db_url` 이 원격 MariaDB 를 가리키므로 HA Core 가 SQLite 를 거의 건드리지 않으며, 로컬은 의도적으로 stateless로 운영됩니다.

> 이전엔 로컬 MariaDB 애드온을 썼으나, 로컬을 stateless로 운영하면서 원격 TrueNAS의 MariaDB로 이전했습니다. ([retired](../retired.md) 참조)

Recorder DB 자체의 상태(크기, 느린 쿼리, 스레드 수)는 SQL 통합 센서로 수집합니다 — [옵저버빌리티](../observability.md) 참조.

## Recorder (원격 MariaDB)

`configuration.yaml`의 `recorder:` 블록:

- 외부 MariaDB URL은 `secrets.yaml` 의 `recorder_mariadb_homeassistant_remote_url` — TrueNAS의 MariaDB jail/VM 인스턴스를 사이트-투-사이트 VPN 너머로 가리킴
- `auto_purge: true`, `auto_repack: true`
- `commit_interval: 120` — write throughput 우선 (VPN latency 보상)
- `db_max_retries: 15`, `db_retry_wait: 5` — VPN 일시 끊김 대비 재시도 정책

### 제외 도메인

고빈도·저가치 도메인은 Recorder에서 제외해 DB 크기를 억제합니다.

```yaml
exclude:
  domains:
    - camera # idle/recording 토글 노이즈
    - sun # 천문, 예측 가능
    - time_date # 시계
    - todo # 체크 여부만
    - update # 업데이트 알림 on/off
    - worldclock
    - event # transient
    - weather. # forecast attribute의 5분 갱신
```

### 제외 엔티티 글롭

- `sensor.clock*`, `sensor.date*`, `sensor.time*`, `sensor.uptime*`
- `sensor.load_*m` — 1m/5m/15m 평균 (system_monitor가 별도로 처리)
- `sensor.anniversary_*`, `sensor.*cert_expiry`
- `sensor.home_assistant_versions*`, `binary_sensor.home_assistant_versions*`
- 헬퍼 파생값: `binary_sensor.any_*`, `binary_sensor.all_*`, `sensor.count_*`, `sensor.overview_*`, `binary_sensor.*_approach`
- 명시 엔티티: `sensor.moon_phase`, `binary_sensor.workday_sensor`

## `.storage/` 운영 규칙

- 기본적으로 모두 비공개 (`gitignore`)
- 단, **Lovelace 대시보드 설정** 4종은 저장소에 포함 — 대시보드 UI를 코드와 함께 버전 관리하기 위함
  - `.storage/lovelace`
  - `.storage/lovelace_dashboards`
  - `.storage/lovelace_resources`
  - `.storage/lovelace.*` (대시보드별 파일)

## 빈번 갱신 / 머신 상태 파일

다음 파일들은 디스크에 보관하되 git에는 반영하지 않습니다 — 매 재시작이나 동작마다 갱신되어 diff 노이즈를 만들기 때문.

- `.HA_VERSION`
- `.ha_run.lock`
- `ip_bans.yaml`
- `home-assistant.log`, `home-assistant.log.fault`
