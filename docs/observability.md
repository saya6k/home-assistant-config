---
title: 옵저버빌리티
---

# 옵저버빌리티

Home Assistant 자체와 가정의 시스템들을 어떻게 관측하고 알람하는지 정리합니다.

> [!NOTE]
> 예전에는 로컬 OpenTelemetry Collector(`otelcol`) 애드온이 HA 의 `/api/prometheus` 를 스크래핑해 원격 Prometheus/Loki/Tempo 로 보냈지만, 지금은 애드온도 `prometheus:` 설정도 없습니다. ([보관소](./retired.md) 참조)
> 아래는 HA 안에서 확인되는 수집 수단만 다룹니다.

## Recorder DB 지표 (SQL 통합)

원격 MariaDB 의 상태를 [SQL 통합](https://www.home-assistant.io/integrations/sql/) 센서로 직접 조회합니다.

| 센서                                              | 내용                           |
| ------------------------------------------------- | ------------------------------ |
| Home Assistant RDB Size                           | DB 크기                        |
| Home Assistant RDB Slow Queries                   | 느린 쿼리 누적                 |
| Home Assistant RDB Threads Running / Connected    | 실행 중 / 연결된 스레드        |
| Home Assistant RDB Buffer Pool Hit Rate           | InnoDB 버퍼 풀 적중률          |
| Home Assistant RDB Innodb buffer pool pages dirty | 디스크에 아직 쓰지 않은 페이지 |
| Home Assistant RDB Created tmp disk tables        | 디스크 임시 테이블 생성 수     |
| Home Assistant RDB Queries                        | 누적 쿼리 수                   |
| Home Assistant RDB Queries Per Second             | 위 값의 `derivative` 헬퍼      |

## 호스트 / 서비스 상태

| 통합                              | 관측 대상                                                                                                |
| --------------------------------- | -------------------------------------------------------------------------------------------------------- |
| System Monitor, CPU Speed         | Raspberry Pi 5 의 CPU·메모리·디스크·네트워크                                                             |
| Raspberry Pi Power Supply Checker | 전원 부족(저전압) 감지                                                                                   |
| Uptime, Version                   | HA 가동 시간, 설치/최신 버전                                                                             |
| Certificate Expiry                | 외부 도메인 인증서 만료일                                                                                |
| Ping, Speedtest.net               | 인터넷 연결, 회선 속도                                                                                   |
| UniFi Network                     | 두 사이트의 게이트웨이·스위치·AP·클라이언트                                                              |
| TrueNAS CE (커스텀)               | 원격 TrueNAS 의 풀·디스크·서비스 상태                                                                    |
| Template                          | `System Check Home-Assistant`, `System Check Unifi`, `Any Alert`, `Count Alerts True`, `Any Battery Low` |

## 침입 / 보안 모니터링

- `http:` 블록이 없어 HA 기본 로그인 보호만 동작 ([네트워크](./platform/network.md#침입-차단) 참조)
- 외부 IPS는 현재 미운영 (이전 CrowdSec 구성은 [보관소](./retired.md) 참조)

## 알림 / 경보 파이프라인

`packages/alerts.yaml` 의 `alert:` 엔티티가 상태 이상을 반복 알림으로 보냅니다. 모두 iOS `time-sensitive` 푸시이고, 정상으로 돌아오면 `done_message: clear_notification` 으로 알림을 지웁니다.

| 구역    | Alert                           | 대상 엔티티                        | 채널                |
| ------- | ------------------------------- | ---------------------------------- | ------------------- |
| Error   | Ping lost                       | `binary_sensor.ping_google`        | iPhone (5분 → 60분) |
| Error   | UniFi site offline (사이트 2곳) | 각 게이트웨이 `*_state` 센서       | iPhone (5분 → 60분) |
| Warning | 공부 시간!                      | `binary_sensor.study_interruption` | MacBook             |

그 외 알림은 자동화에서 직접 보냅니다 — `notify.mobile_app_*`, `notify.send_message`, `persistent_notification`. 자세한 목록은 [자동화](./automations.md):

- 일산화탄소 감지 알림
- 인증서 만료시 재발급
- LG 기기 상태/오류 알림
- 커피 머신 오류 알림 (종합)
