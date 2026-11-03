---
title: 홈
---

# Home Assistant Config

<p>
  <a href="https://github.com/saya6k/home-assistant-config"><img src="https://img.shields.io/maintenance/yes/2026?style=flat-square" alt="Maintained"></a>
  <a href="https://github.com/home-assistant/core/releases/tag/2026.10.4"><img src="https://img.shields.io/badge/Home%20Assistant-2026.10.4-41BDF5?style=flat-square&logo=homeassistant&logoColor=white" alt="HA Version"></a>
  <a href="https://github.com/saya6k/home-assistant-config"><img src="https://img.shields.io/github/last-commit/saya6k/home-assistant-config?style=flat-square" alt="Last Commit"></a>
  <a href="https://github.com/saya6k/home-assistant-config"><img src="https://img.shields.io/github/commit-activity/m/saya6k/home-assistant-config?style=flat-square" alt="Commit Activity"></a>
  <a href="https://github.com/saya6k/home-assistant-config/actions"><img src="https://img.shields.io/github/actions/workflow/status/saya6k/home-assistant-config/release.yml?style=flat-square&label=CI" alt="CI"></a>
  <a href="https://github.com/saya6k/home-assistant-config/blob/main/LICENSE"><img src="https://img.shields.io/github/license/saya6k/home-assistant-config?style=flat-square" alt="License"></a>
  <a href="https://github.com/saya6k/home-assistant-config/stargazers"><img src="https://img.shields.io/github/stars/saya6k/home-assistant-config?style=flat-square" alt="Stars"></a>
</p>

<p>
  <a href="https://www.buymeacoffee.com/my7nmfcm92k"><img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?logo=buymeacoffee&logoColor=000" alt="Buy Me a Coffee"></a>
</p>

2018년부터 운영 중인 개인 Home Assistant 설정입니다. 현재 **3113개 엔티티**, **14개 커스텀 통합**, **17개 애드온**으로 구성되어 있습니다.

> [!CAUTION]
> 가정 환경은 계속 진화합니다. **이 문서가 최신이 아닐 수 있다는 점을 감안해 주세요** — 가능한 한 자주 갱신하려 노력하고 있습니다. (`jinja_files.render` 로 자동 갱신)

## 시스템 한눈에 보기

```
┌─ 하드웨어   │ Raspberry Pi 5 (HAOS), UniFi (로컬+원격), Matter/Thread/Wi-Fi
├─ 플랫폼     │ HAOS (로컬, stateless) · 원격 TrueNAS (Recorder MariaDB, 백업)
├─ 통합       │ 100+ 기본 통합 + 14 커스텀 통합 (Marketplace) + ESPHome 디바이스 6대
├─ 자동화     │ 50 자동화 (한국어 중심) · 스크립트/장면 다수
├─ 대시보드   │ Lovelace storage 모드 + smarthome3d-card (3D 대시보드)
├─ 음성·AI    │ HA Cloud STT · Supertonic TTS · OpenAI/Claude/Gemini/llama.cpp · LLM 도구 스크립트
├─ 옵저버빌리티│ SQL 통합 기반 RDB 지표 · System Monitor · alert 패키지
├─ 백업       │ 매일 자동 백업 → 로컬 + 원격 TrueNAS + Nabu Casa Cloud (3개 보관)
└─ 서비스     │ Paperless-ngx · Pocket ID  (모두 원격 TrueNAS)
```

## Insights

| Domain          |    Value |
| --------------- | -------: |
| automations     |       50 |
| binary_sensors  |      265 |
| device_trackers |       16 |
| lights          |       17 |
| media_players   |       21 |
| sensors         |     1356 |
| switches        |      429 |
| others          |      959 |
| **Total**       | **3113** |

## 문서 내비게이션

- [하드웨어](./hardware.md) — 디바이스, 허브, 가전, 네트워크 장비
- 플랫폼
  - [개요](./platform/index.md)
  - [네트워크](./platform/network.md) — AdGuard · NGINX · UniFi · 인증
  - [스토리지](./platform/storage.md) — MariaDB · `.storage`
  - [백업](./platform/backups.md)
  - [애드온](./platform/add-ons.md) — 17 등록
- 통합
  - [개요](./integrations/index.md) — 100+ 통합 목록
  - [커스텀 컴포넌트](./integrations/custom-components.md) — 14개
  - [ESPHome](./integrations/esphome.md) — 월패드, 인터폰, 음성 디바이스
- [자동화](./automations.md) — 50개
- [대시보드](./dashboards.md)
- [음성과 AI](./voice-and-ai.md)
- [옵저버빌리티](./observability.md)
- [에너지](./energy.md)
- [서비스](./services/index.md) — Paperless-ngx, Pocket ID
- [보관소](./retired.md) · [참고 자료](./resources.md)

## 라이선스

이 저장소는 [MIT 라이선스](https://github.com/saya6k/home-assistant-config/blob/main/LICENSE)로 배포됩니다. `secrets.yaml`은 포함되지 않습니다.
