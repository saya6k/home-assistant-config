---
title: ESPHome
---

# ESPHome 디바이스

`esphome/` 디렉터리에 보관되며, ESPHome Device Builder 애드온으로 빌드/플래시합니다. `esphome/secrets.yaml`은 별도(저장소에서 제외).

| 파일                | 디바이스                | 비고                                               |
| ------------------- | ----------------------- | -------------------------------------------------- |
| `esp-wallpad.yaml`  | 현대HT HNF-I2101 월패드 | M5Stack Atom 으로 RS-485 연결, ESPHome 으로 브리지 |
| `esp-subphone.yaml` | 인터폰(서브폰)          | 출입/벨 이벤트 송출                                |

## 저장소 밖의 ESPHome 디바이스

HA 에는 연결되어 있지만 YAML 이 이 저장소에 없는 디바이스입니다.

| 디바이스                             | 비고                              |
| ------------------------------------ | --------------------------------- |
| Home Assistant Voice Preview Edition | 공식 펌웨어                       |
| Echo Show 5 / Echo Show 8 (1세대)    | TECHO5 커스텀 펌웨어, Assist 위성 |
| YUPP 스마트 거울 (BM-S-21E1)         | YUPP 펌웨어, Assist 위성          |
| YDAI TDS 측정기                      | ESP32, 수질(TDS) 센서             |

## 보관소

`esphome/archive/` 아래 다음 구성이 보관되어 있습니다 — 더 이상 사용하지 않거나 교체된 디바이스.

- `living-room-assistant.yaml`
- `nano-c6.yaml`

## CI 검증

`.github/workflows/esphome-ci.yml` 에서 push마다 `esphome config` 로 모든 `esphome/*.yaml` 파일의 구성을 검증합니다 (실제 빌드는 하지 않음).

## 별도 git 저장소

HA 서버의 `esphome/` 는 메인 저장소 안에 별도 `.git`을 두고 있어, ESPHome 빌더 내부의 git 기능과 분리됩니다.
