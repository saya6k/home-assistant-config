---
title: Automations
---

# Automations

**50** automations defined in `automations.yaml`. Most aliases are in Korean. The `mode` attribute (`single` / `restart` / `queued` / `parallel`) controls concurrency.

The raw source lives at [`automations.yaml`](https://github.com/saya6k/home-assistant-config/blob/main/automations.yaml).

## Summary (name / mode / state)

| Name                                           | Mode       | State |
| ---------------------------------------------- | ---------- | ----- |
| 17TRACK 택배 알림                              | `single`   | on    |
| Apple TV 재생시 영화 장면 활성화               | `single`   | off   |
| HA Startup                                     | `single`   | on    |
| LG 기기 상태/오류 알림                         | `single`   | on    |
| Notify Personal Agenda                         | `single`   | on    |
| Notify Study Interruption                      | `restart`  | on    |
| Notify to brush Teeth                          | `single`   | on    |
| Notify Work Agenda                             | `single`   | on    |
| TTS 캐시 지우기                                | `single`   | on    |
| 개인 일정 시작 30분 전 알림                    | `single`   | on    |
| 거실 버튼 조명 제어                            | `restart`  | on    |
| 거실 옷장 문 열림 5분 알림                     | `parallel` | on    |
| 건조대 열림 시 제습기 빨래건조 모드            | `restart`  | on    |
| 고농도 이산화탄소 환기 알림                    | `single`   | on    |
| 귀가 시 환영 및 보조 기능 활성화               | `single`   | on    |
| 기상 특보 수신 및 알림                         | `single`   | on    |
| 긴급 상황 알림: 재난별 지침 전송               | `single`   | on    |
| 날씨 이미지 시각화 생성 및 업데이트            | `single`   | off   |
| 매월 반복 집안일 추가                          | `single`   | on    |
| 매일 반복 집안일 추가                          | `single`   | on    |
| 배달 앱 알림 알려주기                          | `queued`   | on    |
| 샤워 시 플레이리스트 재생                      | `single`   | on    |
| 수면 장면 활성화                               | `single`   | on    |
| 아이폰 메시지 읽어주기                         | `queued`   | on    |
| 아이폰 전화 받을지 묻기                        | `single`   | on    |
| 아침 액자 이미지 변경                          | `single`   | on    |
| 야간 화장실 이용간 조명 제어                   | `single`   | on    |
| 오늘 강수 예보 알림                            | `single`   | on    |
| 외출 모드 활성화 시 조명 끄기                  | `single`   | on    |
| 이메일 수신 시 운송장 번호 추출 및 트래킹 추가 | `queued`   | on    |
| 인증서 만료시 재발급                           | `single`   | on    |
| 일산화탄소 감지 알림                           | `single`   | on    |
| 일어나면 기상장면 활성화                       | `single`   | on    |
| 재난문자 수신시 지속적인 알림 메시지 생성      | `single`   | on    |
| 주말 반복 집안일 추가                          | `single`   | on    |
| 주방 진입 시 조명 장면 활성화                  | `single`   | on    |
| 주요 기념일 7일 전 알림                        | `single`   | on    |
| 집에 들어옴 알림                               | `single`   | on    |
| 집에 사람이 없을 때 자리 비움 장면 활성화      | `single`   | on    |
| 창문 닫힘 시 공조 자동 제어 (닫힘)             | `single`   | on    |
| 창문 열림 시 공조 자동 제어 (열림)             | `single`   | on    |
| 침대에서 침대에 누워 있다고 알림               | `single`   | on    |
| 침실 6버튼 스마트 스위치 제어                  | `queued`   | on    |
| 침실 이산화탄소 농도 알림                      | `single`   | on    |
| 침실 창문 한쪽만 닫힘 3분 알림                 | `restart`  | on    |
| 커피 머신 오류 알림 (종합)                     | `single`   | on    |
| 핫 세일 알림 (위시리스트 체크)                 | `parallel` | on    |
| 현관 감지 시 조명 자동 켜기                    | `single`   | on    |
| 화장실 습도 50% 미만일 때 제습기 끄기          | `single`   | on    |
| 화장실 습도 70% 초과 시 제습기 켜기            | `single`   | on    |

See [`automations.yaml`](https://github.com/saya6k/home-assistant-config/blob/main/automations.yaml) for each automation's triggers, conditions, and description.
