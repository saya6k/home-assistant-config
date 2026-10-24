---
title: 홈
---

# Home Assistant Config

<p>
  <a href="https://github.com/saya6k/home-assistant-config"><img src="https://img.shields.io/maintenance/yes/2026?style=flat-square" alt="Maintained"></a>
  <a href="https://github.com/home-assistant/core/releases/tag/2026.5.4"><img src="https://img.shields.io/badge/Home%20Assistant-2026.5.4-41BDF5?style=flat-square&logo=homeassistant&logoColor=white" alt="HA Version"></a>
  <a href="https://github.com/saya6k/home-assistant-config"><img src="https://img.shields.io/github/last-commit/saya6k/home-assistant-config?style=flat-square" alt="Last Commit"></a>
  <a href="https://github.com/saya6k/home-assistant-config"><img src="https://img.shields.io/github/commit-activity/m/saya6k/home-assistant-config?style=flat-square" alt="Commit Activity"></a>
  <a href="https://github.com/saya6k/home-assistant-config/actions"><img src="https://img.shields.io/github/actions/workflow/status/saya6k/home-assistant-config/release.yml?style=flat-square&label=CI" alt="CI"></a>
  <a href="https://github.com/saya6k/home-assistant-config/blob/main/LICENSE"><img src="https://img.shields.io/github/license/saya6k/home-assistant-config?style=flat-square" alt="License"></a>
  <a href="https://github.com/saya6k/home-assistant-config/stargazers"><img src="https://img.shields.io/github/stars/saya6k/home-assistant-config?style=flat-square" alt="Stars"></a>
</p>

<p>
  <a href="https://www.buymeacoffee.com/my7nmfcm92k"><img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?logo=buymeacoffee&logoColor=000" alt="Buy Me a Coffee"></a>
</p>

2018년부터 운영 중인 개인 Home Assistant 설정입니다. 현재 **2008개 엔티티**, **17개 HACS 통합**, **23개 애드온**으로 구성되어 있습니다.

> [!CAUTION]
> 가정 환경은 계속 진화합니다. **이 문서가 최신이 아닐 수 있다는 점을 감안해 주세요** — 가능한 한 자주 갱신하려 노력하고 있습니다. (`jinja2docs.render` 로 자동 갱신)

## 시스템 한눈에 보기

```
┌─ 하드웨어   │ Piesia AD742A + Raspberry Pi 5, UniFi (로컬+원격), Matter/Thread/Wi-Fi
├─ 플랫폼     │ HAOS (로컬, stateless) · 원격 TrueNAS (Recorder MariaDB, 옵저버빌리티 백엔드)
├─ 통합       │ 100+ 기본 통합 + 17 커스텀 컴포넌트 + ESPHome 디바이스 3종
├─ 자동화     │ 49 자동화 (한국어 중심) · 시나리오/장면 다수
├─ 대시보드   │ Lovelace storage 모드 + Mushroom/Bubble Card/Card Mod
├─ 음성·AI    │ Whisper · Supertonic-MNN · Ollama · Voice Satellite · LLM 대화 에이전트 다중
├─ 옵저버빌리티│ otelcol agent (로컬) ─VPN─▶ otelcol gateway (원격) ─▶ Prometheus / Loki / Tempo ─▶ Grafana
├─ 백업       │ 로컬 3개 + 원격 TrueNAS 1개 + Nabu Casa Cloud 1개
└─ 서비스     │ Paperless-ngx · Pocket ID  (모두 원격 TrueNAS)
```

## Insights

| Domain          |    Value |
| --------------- | -------: |
| automations     |       49 |
| binary_sensors  |      221 |
| device_trackers |       17 |
| lights          |       14 |
| media_players   |       16 |
| sensors         |      988 |
| switches        |      168 |
| others          |      535 |
| **Total**       | **2008** |

## 문서 내비게이션

- [하드웨어](./hardware.md) — 디바이스, 허브, 가전, 네트워크 장비
- 플랫폼
  - [개요](./platform/index.md)
  - [네트워크](./platform/network.md) — AdGuard · NGINX · UniFi · 인증
  - [스토리지](./platform/storage.md) — MariaDB · `.storage`
  - [백업](./platform/backups.md)
  - [애드온](./platform/add-ons.md) — 23 등록
- 통합
  - [개요](./integrations/index.md) — 100+ 통합 목록
  - [커스텀 컴포넌트](./integrations/custom-components.md) — 17 HACS 통합
  - [ESPHome](./integrations/esphome.md) — 월패드, 인터폰, 음성 위성
- [자동화](./automations.md) — 49개
- [대시보드](./dashboards.md)
- [음성과 AI](./voice-and-ai.md)
- [옵저버빌리티](./observability.md)
- [에너지](./energy.md)
- [서비스](./services/index.md) — Paperless-ngx, Pocket ID
- [보관소](./retired.md) · [참고 자료](./resources.md)

## 라이선스

이 저장소는 [MIT 라이선스](https://github.com/saya6k/home-assistant-config/blob/main/LICENSE)로 배포됩니다. `secrets.yaml`은 포함되지 않습니다.
