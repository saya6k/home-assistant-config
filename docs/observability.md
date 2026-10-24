---
title: 옵저버빌리티
---

# 옵저버빌리티

Home Assistant 자체와 가정의 시스템들을 어떻게 관측하고 알람하는지 정리합니다.

## 통합 수집 파이프라인 (OpenTelemetry Collector)

옵저버빌리티 백엔드는 **전부 원격 TrueNAS** 에 있습니다. HA 호스트엔 가벼운 sidecar agent 만 실행되고, 모든 시그널은 사이트-투-사이트 VPN 너머의 **otelcol gateway** 로 OTLP 로 전달됩니다.

```
[ 로컬 HA 사이트 ]                              [ 원격 TrueNAS ]

HA Core (/api/prometheus)  ─┐
시스템 / 애드온 stdout 로그 ─┼─▶ otelcol agent ─VPN/OTLP─▶ otelcol gateway ─┬─▶ Prometheus (메트릭)
journald / 시스템 로그       ─┘    (sidecar)                                  ├─▶ Grafana Loki  (로그)
                                                                              └─▶ Grafana Tempo (추적)
                                                                                     │
                                                                                     ▼
                                                                                  Grafana
```

- **otelcol agent** (로컬, HA sidecar): 메트릭 스크래핑(`prometheus` receiver) + 로그 수집(`filelog`/`journald` receiver) + 자기 자신의 trace 도 수집. OTLP exporter 로 원격 gateway 전송.
- **otelcol gateway** (원격 TrueNAS): 여러 agent 의 OTLP 시그널을 받아 백엔드별로 라우팅. 인증·rate limit·buffer 가 여기 모임.
- **Prometheus** (원격): 메트릭 TSDB.
- **Grafana Loki** (원격): 로그 인덱스 + 저장.
- **Grafana Tempo** (원격): 분산 추적 저장.
- **Grafana** (원격): Prometheus + Loki + Tempo 를 데이터 소스로. 시각화·알람.

이 구조의 장점은 **로컬 HA 가 stateless** 라는 점 — HA 호스트가 사라지거나 재설치돼도 옵저버빌리티 데이터는 원격에 그대로 남고, 새 HA 인스턴스가 부팅되면 agent 만 다시 붙으면 흐름이 회복됩니다.

## 침입 / 보안 모니터링

- HA의 `http.ip_ban_enabled` + `login_attempts_threshold` 가 1차 방어
- 외부 IPS는 현재 미운영 (이전 CrowdSec 구성은 [보관소](./retired.md) 참조)

## 알림 / 경보 파이프라인

`packages/alerts_and_notifications.yaml`이 다음을 정의합니다.

| 레벨    | 채널                                | 비고                       |
| ------- | ----------------------------------- | -------------------------- |
| Fatal   | Discord + iOS Critical + Persistent | 시스템 장애, 보안 사고     |
| Error   | Discord + Mobile push               | 자동화 실패, 통합 오프라인 |
| Warning | Mobile push                         | 배터리 부족, 인증서 임박   |
| Info    | Persistent notification             | 정보성                     |

알림 라우팅에 사용되는 주요 자동화 — 자세한 목록은 [자동화](./automations.md):

- 배터리 부족 알림
- 시스템 로그 알림
- 인증서 만료시 재발급
- 자동 백업 완료 후 HA 코어 자동 업데이트

## 대시보드 (Grafana)

> [!NOTE]
> 아래는 다른 사용자의 예시 스크린샷이며, 자체 대시보드 캡처로 교체 필요.

<p align="center">
  <img src="https://github.com/denysdovhan/home-assistant-config/assets/3459374/c687d08c-10c1-453c-b5b6-74c4e8cf8600" alt="Energy Usage" width="48%">
  <img src="https://github.com/denysdovhan/home-assistant-config/assets/3459374/51dfc5c6-f7bf-4218-8bf0-8cc4ffe9c951" alt="Internet Security" width="48%">
</p>
