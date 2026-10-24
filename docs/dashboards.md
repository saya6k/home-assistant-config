---
title: 대시보드
---

# 대시보드

Lovelace는 **storage 모드** 로 운영합니다 (`configuration.yaml`의 `lovelace: mode: storage`). 대시보드는 `.storage/lovelace*` 파일로 저장되며 — 이 4종은 `.gitignore` 예외로 저장소에 포함됩니다.

## 디자인 원칙

- **자동화 + 템플릿 우선**: 수동 조작을 최소화. template 센서, group, label, Jinja2 템플릿으로 동적 구성.
- **반응형**: 섹션 폭을 초기 3에서 2로 줄여 월패드 등 작은 화면에서도 보기 좋게.
- **단일 인터페이스**: 좌측 단축 탭 숨김, 모든 정보를 한 Lovelace 화면에서.
- **HomeKit 영감**: 아이폰 사용자에 맞춰 Apple HomeKit 스타일 차용.

## 주요 기능

- **동적 섹션**: Home / Climate / Energy / System 등 목적별 분리.
- **인터랙티브 카드**: 미디어, 조명, 공조 등 직접 제어.
- **커스텀 비주얼**: 커스텀 카드 + 테마 조합.
- **실시간 갱신**: 날씨 예보, 교통, 시스템 상태가 실시간으로 표시.

## 스크린샷

<p align="center">
  <img src="https://raw.githubusercontent.com/saya6k/home-assistant-config/main/www/lovelace/overview.png" alt="Overview" width="32%">
  <img src="https://raw.githubusercontent.com/saya6k/home-assistant-config/main/www/lovelace/mobile.png" alt="Mobile" width="32%">
  <img src="https://raw.githubusercontent.com/saya6k/home-assistant-config/main/www/lovelace/living-room-subview.png" alt="Living Room" width="32%">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/saya6k/home-assistant-config/main/www/lovelace/system.png" alt="System" width="32%">
  <img src="https://raw.githubusercontent.com/saya6k/home-assistant-config/main/www/lovelace/climate.png" alt="Climate" width="32%">
  <img src="https://raw.githubusercontent.com/saya6k/home-assistant-config/main/www/lovelace/energy.png" alt="Energy" width="32%">
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/saya6k/home-assistant-config/main/www/lovelace/music.png" alt="Music" width="32%">
</p>

## Lovelace 플러그인

`configuration.yaml`의 `frontend.extra_module_url`에 `card-mod`가 등록되어 있고, 나머지는 HACS를 통해 `.storage/lovelace_resources`에 등록됩니다. 현재 **8개** 의 HACS 플러그인이 설치되어 있습니다.

| 이름                                                                               | 설명                                    |
| ---------------------------------------------------------------------------------- | --------------------------------------- |
| [Auto Entities](https://github.com/thomasloven/lovelace-auto-entities)             | 🔹 엔티티 목록을 동적으로 채워주는 카드 |
| [Button Card](https://github.com/custom-cards/button-card)                         | ❇️ 강력한 커스텀 버튼 카드              |
| [Card Mod](https://github.com/thomasloven/lovelace-card-mod)                       | 🔹 거의 모든 Lovelace 카드에 CSS 주입   |
| [Decluttering Card](https://github.com/custom-cards/decluttering-card)             | 🧹 반복되는 카드 정의를 템플릿화        |
| [Homeii Flow](https://github.com/r11a/homeii-music-flow)                           | Music Assistant용 프리미엄 카드         |
| [Hui Element](https://github.com/thomasloven/lovelace-hui-element)                 | 🔹 내장 엘리먼트를 자유 위치에          |
| [Mushroom](https://github.com/piitaya/lovelace-mushroom)                           | 🍄 부드러운 톤의 통합 카드 세트         |
| [Template Entity Row](https://github.com/thomasloven/lovelace-template-entity-row) | 🔹 entities 카드의 행을 자유롭게        |

## 테마

`themes/` 디렉터리에 보관되며, `configuration.yaml`의 `frontend.themes`로 로드.

| 이름                | 비고                    |
| ------------------- | ----------------------- |
| Frosted Glass Auto  | 시스템 라이트/다크 추종 |
| Frosted Glass Dark  | 다크 전용               |
| Frosted Glass Light | 라이트 전용             |

## 보조 통합

- **Music Assistant** — 미디어 플레이어 카드 연동
- **alert** — 시스템 알림 카드 직접 표시
