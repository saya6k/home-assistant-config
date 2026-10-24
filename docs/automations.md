---
title: 자동화
---

# 자동화

`automations.yaml`에 정의된 **49개**의 자동화. 한국어 자동화가 다수이며, 모드(`single`/`restart`/`queued`/`parallel`)에 따라 동시 실행 정책이 다릅니다.

전체 자동화 원본은 [`automations.yaml`](https://github.com/saya6k/home-assistant-config/blob/main/automations.yaml) 에서 확인할 수 있습니다.

## 요약 (이름 / 모드 / 상태)

| 이름                                                      | Mode       | 상태        |
| --------------------------------------------------------- | ---------- | ----------- |
| 17TRACK 택배 알림                                         | `single`   | on          |
| Apple TV 재생시 영화 장면 활성화                          | `single`   | on          |
| HA Startup                                                | `single`   | on          |
| Notify LG ThinQ Notifications                             | `single`   | on          |
| Notify Personal Agenda                                    | `single`   | on          |
| Notify Study Interruption                                 | `single`   | on          |
| Notify to brush Teeth                                     | `single`   | on          |
| Notify Work Agenda                                        | `single`   | on          |
| TTS 캐시 지우기                                           | `single`   | on          |
| 거실 버튼 조명 제어                                       | `restart`  | on          |
| 고농도 이산화탄소 환기 알림                               | `single`   | on          |
| 구청에서 온 알림 처리 및 확인 요청                        | `parallel` | on          |
| 귀가 시 환영 및 보조 기능 활성화                          | `single`   | on          |
| 기상 특보 수신 및 알림                                    | `single`   | on          |
| 긴급 상황 알림: 재난별 지침 전송                          | `single`   | on          |
| 날씨 이미지 시각화 생성 및 업데이트                       | `single`   | on          |
| 새 이메일 도착 알림                                       | `queued`   | on          |
| 샤워 시 플레이리스트 재생                                 | `single`   | on          |
| 수면 장면 활성화                                          | `single`   | on          |
| 스트레칭 루틴 및 워킹 훈련 실행 (16주 캣워크 완벽 체화형) | `single`   | unavailable |
| 스트레칭 루틴 실행                                        | `single`   | on          |
| 스팀 위시리스트 세일 알림                                 | `single`   | on          |
| 시스템 로그 알림                                          | `queued`   | off         |
| 식사 준비 완료 시 식사 장면 활성화                        | `single`   | on          |
| 야간 화장실 이용간 조명 제어                              | `single`   | on          |
| 오늘 강수 예보 알림                                       | `single`   | on          |
| 외출 모드 활성화 시 조명 끄기                             | `single`   | on          |
| 유튜브 최신 영상 알림                                     | `parallel` | on          |
| 이메일 수신 시 운송장 번호 추출 및 트래킹 추가            | `queued`   | on          |
| 인증서 만료시 재발급                                      | `single`   | on          |
| 일산화탄소 감지 알림                                      | `single`   | on          |
| 일어나면 기상장면 활성화                                  | `single`   | on          |
| 자동 백업 완료 후 HA 코어 자동 업데이트                   | `single`   | on          |
| 재난문자 수신시 지속적인 알림 메시지 생성                 | `single`   | on          |
| 주방 진입 시 조명 장면 활성화                             | `single`   | on          |
| 주요 기념일 7일 전 알림                                   | `single`   | on          |
| 집에 사람이 없을 때 자리 비움 장면 활성화                 | `single`   | on          |
| 창문 닫힘 시 공조 자동 제어 (닫힘)                        | `single`   | on          |
| 창문 열림 시 공조 자동 제어 (열림)                        | `single`   | on          |
| 침대에서 침대에 누워 있다고 알림                          | `single`   | on          |
| 침실 6버튼 스마트 스위치 제어                             | `queued`   | on          |
| 침실 이산화탄소 농도 알림                                 | `single`   | on          |
| 커피 머신 물 부족 오류 발생 시 거실에서 음성 알림         | `single`   | on          |
| 커피 머신 원두 없음 오류 알림                             | `single`   | on          |
| 커피 머신 추출 완료 알림                                  | `single`   | on          |
| 핫 세일 알림 (위시리스트 체크)                            | `parallel` | on          |
| 현관 감지 시 조명 자동 켜기                               | `single`   | on          |
| 화장실 습도 50% 미만일 때 제습기 끄기                     | `single`   | on          |
| 화장실 습도 70% 초과 시 제습기 켜기                       | `single`   | on          |

## 자동화별 상세

> 이 아래 항목들은 자동화 ID 기준 정렬. 일부는 한글 이름과 영문 별칭이 혼재합니다.

## ESPHome Auto-Update

- **ID**: 1714009521553
- **Alias**: ESPHome Auto-Update
- **Description**: Trigger: The automation triggers when any ESPHome device is marked as 'on' for an update. Action: Once triggered, it calls script esphome_update_all_devices, which starts the update process for each device. Mode: Like the script, it's set to 'single' to handle updates one by one.

## Washer State On

- **ID**: 1717333060399
- **Alias**: Washer State On
- **Description**:

## HA Startup

- **ID**: 1717334579267
- **Alias**: HA Startup
- **Description**: Notify and perform actions on HA startup

## Apply Welcome Scene when Person Enter Zone

- **ID**: 1722165897301
- **Alias**: Apply Welcome Scene when Person Enter Zone
- **Description**:

## Bathroom Occupancy Light Control

- **ID**: 1728370793546
- **Alias**: Bathroom Occupancy Light Control
- **Description**:

## Kitchen Occupancy Light Control

- **ID**: 1732863830358
- **Alias**: Kitchen Occupancy Light Control
- **Description**:

## Notify Steam Wishlist on Sales

- **ID**: 1737078076689
- **Alias**: Notify Steam Wishlist on Sales
- **Description**:

## Purge Log Filesize

- **ID**: 1737747451172
- **Alias**: Purge Log Filesize
- **Description**: Purge Log when file size exceed 50mb

## Track Floor Cleaning by Robot Vacuum

- **ID**: 1738794001846
- **Alias**: Track Floor Cleaning by Robot Vacuum
- **Description**:

## Notify Seoul Teukbo

- **ID**: 1739462792155
- **Alias**: Notify Seoul Teukbo
- **Description**:

## iOS Action - Run Vacuum Yes

- **ID**: 1739748588995
- **Alias**: iOS Action - Run Vacuum Yes
- **Description**:

## Apply Away Scene when no person is home

- **ID**: 1739844963798
- **Alias**: Apply Away Scene when no person is home
- **Description**:

## Play Playlist on Shower Scene

- **ID**: 1739846179022
- **Alias**: Play Playlist on Shower Scene
- **Description**: Play Spotify playlist

## Play Playlist on Cooking Scene

- **ID**: 1739846462573
- **Alias**: Play Playlist on Cooking Scene
- **Description**: Play Spotify playlist

## Notify LG ThinQ Notifications

- **ID**: 1739846798671
- **Alias**: Notify LG ThinQ Notifications
- **Description**:

## Update Datetime every 10 minutes

- **ID**: 1740397060235
- **Alias**: Update Datetime every 10 minutes
- **Description**:

## TTS on door opening with persons at home

- **ID**: 1741577306708
- **Alias**: TTS on door opening with persons at home
- **Description**:

## Notify to brush Teeth

- **ID**: 1750997515323
- **Alias**: Notify to brush Teeth
- **Description**:

## Notify Work Agenda

- **ID**: 1751020435496
- **Alias**: Notify Work Agenda
- **Description**:

## Notify Personal Agenda

- **ID**: 1751020560204
- **Alias**: Notify Personal Agenda
- **Description**:

## Notify Study Interruption

- **ID**: 1751025981451
- **Alias**: Notify Study Interruption
- **Description**:

## 핫 세일 알림 (위시리스트 체크)

- **ID**: 1753928991880
- **Alias**: 핫 세일 알림 (위시리스트 체크)
- **Description**: 핫 세일 상품을 위시리스트에 대응하여 알림을 전송합니다. 이 자동화는 세일 상품이 위시리스트에 있는 경우에만 알림을 제공합니다.

## 침대에서 침대에 누워 있다고 알림

- **ID**: 1753930331307
- **Alias**: 침대에서 침대에 누워 있다고 알림
- **Description**: 침대에 누워 있고, 집이 일정 조건을 충족할 때 조명과 음악으로 편안한 환경 조성.

## 유튜브 최신 영상 저장 및 알림

- **ID**: 1753948404845
- **Alias**: 유튜브 최신 영상 저장 및 알림
- **Description**:

## 새 이메일 도착 알림

- **ID**: 1753958558668
- **Alias**: 새 이메일 도착 알림
- **Description**:

## 아침 알림 및 시작 준비

- **ID**: 1753959217336
- **Alias**: 아침 알림 및 시작 준비
- **Description**: 아침 일찍 일어나기 위한 맞춤 알림과 환경 설정 자동화입니다.

## 배터리 부족 알림

- **ID**: 1754101151958
- **Alias**: 배터리 부족 알림
- **Description**: 주요 기기의 배터리가 30% 미만으로 떨어지면 알림을 보냅니다.

## TTS 캐시 지우기

- **ID**: 1754101632706
- **Alias**: TTS 캐시 지우기
- **Description**: 매일 오전 1시에 TTS 캐시를 지웁니다.

## 막차 알림

- **ID**: 1754998962612
- **Alias**: 막차 알림
- **Description**: 다수 센서의 '마지막 차량 정보'를 확인하고, 막차 여부가 확인되면 알림을 보냄.

## 구청에서 온 알림 처리 및 확인 요청

- **ID**: 1754999423567
- **Alias**: 구청에서 온 알림 처리 및 확인 요청
- **Description**: District office에서 전달된 알림을 처리하여 사용자에게 알림과 필수 확인 요청을 수행하는 자동화

## Let's Encrypt 자동 시작 – 인증서 만료 시

- **ID**: 1755190192909
- **Alias**: Let's Encrypt 자동 시작 – 인증서 만료 시
- **Description**: 인증서 유효성 검사 실패(is_valid: false) 시 Let's Encrypt Addon(core_letsencrypt)를 시작합니다.
