# Home Assistant Config

[![Maintained][maintenance-img]][github-url]
[![HA Version](https://img.shields.io/badge/Home%20Assistant-2026.5.4-41BDF5?style=flat-square&logo=homeassistant&logoColor=white)](https://github.com/home-assistant/core/releases/tag/2026.5.4)
[![Last Commit][last-commit-img]][github-url]
[![Commit Activity][commit-activity-img]][github-url]
[![CI][ci-img]][github-url]
[![License][license-img]][license-url]
[![Stars][stars-img]][github-url]
[![Docs][docs-img]][docs-url]

> 2018년부터 운영 중인 개인 Home Assistant 설정. 1인 가구, 한국어 자동화 중심. (2026-05-31 갱신)

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?logo=buymeacoffee&logoColor=000)](https://www.buymeacoffee.com/my7nmfcm92k)
[![Language](https://img.shields.io/badge/lang-한국어%20·%20English-success)](https://saya6k.github.io/home-assistant-config)

📚 **전체 문서: [saya6k.github.io/home-assistant-config][docs-url]**

---

## 한눈에 보기

<p>
  <img src="https://img.shields.io/badge/entities-2008-1f6feb" alt="Entities">
  <img src="https://img.shields.io/badge/integrations-100%2B-1f6feb" alt="Integrations">
  <img src="https://img.shields.io/badge/automations-49-1f6feb" alt="Automations">
  <img src="https://img.shields.io/badge/add--ons-23-1f6feb" alt="Add-ons">
  <img src="https://img.shields.io/badge/HACS_integrations-17-1f6feb" alt="HACS Integrations">
  <img src="https://img.shields.io/badge/HACS_plugins-8-1f6feb" alt="HACS Plugins">
</p>

<details>
<summary><strong>📦 애드온</strong> (23)</summary>

| 이름 | 버전 | 상태 |
| --- | --- | --- |
| Advanced SSH & Web Terminal | `23.0.9` | started |
| ESPHome Device Builder | `2026.5.1` | started |
| Git pull | `9.0.1` | unknown |
| HASS MCP Proxy | `1.0.20` | started |
| Home Detector | `0.0.13` | started |
| iSponsorBlockTV add-on | `2.6.2` | started |
| Let's Encrypt | `6.3.2` | stopped |
| LLM Conversation Agent | `1.14.5` | started |
| Matter Server | `8.5.0` | started |
| Mosquitto broker | `7.1.0` | started |
| Music Assistant | `2.8.8` | started |
| NGINX Home Assistant SSL proxy | `4.2.0` | started |
| OpenTelemetry Collector | `0.12.14` | started |
| OpenThread Border Router | `3.0.0` | started |
| openWakeWord | `2.1.0` | started |
| Rematters | `0.1.28` | started |
| rethink | `0.1.0` | unknown |
| Samba share | `12.6.1` | started |
| Shelly Manager | `1.1.4` | started |
| Studio Code Server | `6.0.1` | started |
| Supertonic | `2.0.0` | started |
| Wardrowbe | `1.4.0` | started |
| Zensical | `0.1.0` | started |

</details>

<details>
<summary><strong>🧩 HACS · 커스텀 통합</strong> (17)</summary>

- [Anniversaries](https://github.com/pinkywafer/Anniversaries)
- [Dawarich](https://github.com/AlbinLind/dawarich-home-assistant)
- [Discord Game](https://github.com/LordBoos/discord_game)
- [Dyson](https://github.com/libdyson-wg/ha-dyson)
- [HACS](https://github.com/hacs/integration)
- [Koreader](https://github.com/hudsonbrendon/ha-koreader)
- [Kr Component Kit](https://github.com/redchupa/kr_component_kit)
- [Life360](https://github.com/pnbruckner/ha-life360)
- [Openid Connect/Sso Authentication](https://github.com/christiaangoossens/hass-oidc-auth)
- [Remote Logger For Home Assistant](https://github.com/rhizomatics/remote_logger)
- [Restore Persistent Notification](https://github.com/andreadegiovine/homeassistant-restore-persistent-notifications)
- [Spook 👻 Your Homie](https://github.com/frenck/spook)
- [Steam Wishlist](https://github.com/boralyl/steam-wishlist)
- [Truenas](https://github.com/tomaae/homeassistant-truenas)
- [Voice Satellite](https://github.com/jxlarrea/voice-satellite-card-integration)
- [Voice Satellite   Llm Tools](https://github.com/jxlarrea/voice-satellite-card-llm-tools)
- [Washdata](https://github.com/3dg1luk43/ha_washdata)

</details>

<details>
<summary><strong>🎨 HACS · Lovelace 플러그인</strong> (8)</summary>

- [Auto Entities](https://github.com/thomasloven/lovelace-auto-entities)
- [Button Card](https://github.com/custom-cards/button-card)
- [Card Mod](https://github.com/thomasloven/lovelace-card-mod)
- [Decluttering Card](https://github.com/custom-cards/decluttering-card)
- [Homeii Flow](https://github.com/r11a/homeii-music-flow)
- [Hui Element](https://github.com/thomasloven/lovelace-hui-element)
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [Template Entity Row](https://github.com/thomasloven/lovelace-template-entity-row)

</details>

### 플랫폼

<p>
  <img src="https://img.shields.io/badge/HAOS-2026.5.4-41BDF5?logo=homeassistant&logoColor=white" alt="HAOS">
  <img src="https://img.shields.io/badge/host-Generic_x86--64-555?logo=intel&logoColor=white" alt="Generic x86-64">
  <img src="https://img.shields.io/badge/Recorder-MariaDB-003545?logo=mariadb&logoColor=white" alt="MariaDB">
  <img src="https://img.shields.io/badge/otelcol-OpenTelemetry-425CC7?logo=opentelemetry&logoColor=white" alt="OpenTelemetry Collector">
  <img src="https://img.shields.io/badge/Prometheus-Metrics-E6522C?logo=prometheus&logoColor=white" alt="Prometheus">
  <img src="https://img.shields.io/badge/Grafana-Dashboards-F46800?logo=grafana&logoColor=white" alt="Grafana">
  <img src="https://img.shields.io/badge/Loki-Logs-F46800?logo=grafana&logoColor=white" alt="Loki">
  <img src="https://img.shields.io/badge/NGINX-SSL%20Proxy-009639?logo=nginx&logoColor=white" alt="NGINX">
  <img src="https://img.shields.io/badge/TLS-Let's%20Encrypt-003A70?logo=letsencrypt&logoColor=white" alt="Let's Encrypt">
  <img src="https://img.shields.io/badge/AdGuard-DNS-68BC71?logo=adguard&logoColor=white" alt="AdGuard">
</p>

### 프로토콜 · HACS

<p>
  <img src="https://img.shields.io/badge/Matter-2A2A2A?logo=matter&logoColor=white" alt="Matter">
  <img src="https://img.shields.io/badge/Thread-Border%20Router-FF6B00" alt="Thread">
  <img src="https://img.shields.io/badge/MQTT-Mosquitto-660066?logo=mqtt&logoColor=white" alt="MQTT">
  <img src="https://img.shields.io/badge/ESPHome-000000?logo=esphome&logoColor=white" alt="ESPHome">
  <img src="https://img.shields.io/badge/HACS-41BDF5?logo=homeassistantcommunitystore&logoColor=white" alt="HACS">
</p>

### 음성과 AI

<p>
  <img src="https://img.shields.io/badge/Claude-Anthropic-D97757?logo=anthropic&logoColor=white" alt="Claude">
  <img src="https://img.shields.io/badge/GPT-OpenAI-412991?logo=openai&logoColor=white" alt="GPT">
  <img src="https://img.shields.io/badge/Gemini-Google-4285F4?logo=googlegemini&logoColor=white" alt="Gemini">
  <img src="https://img.shields.io/badge/Open%20Router-000000" alt="Open Router">
  <img src="https://img.shields.io/badge/Ollama-Local-000000?logo=ollama&logoColor=white" alt="Ollama">
  <img src="https://img.shields.io/badge/Whisper-STT-74AA9C?logo=openai&logoColor=white" alt="Whisper">
  <img src="https://img.shields.io/badge/Supertonic--MNN-TTS-7C3AED" alt="Supertonic-MNN">
  <img src="https://img.shields.io/badge/MCP-Tools-FF6B6B" alt="MCP">
</p>

### 서비스

<p>
  <img src="https://img.shields.io/badge/Paperless--ngx-문서-17541F" alt="Paperless">
  <img src="https://img.shields.io/badge/Pocket_ID-OIDC-1976D2" alt="Pocket ID">
  <img src="https://img.shields.io/badge/Music_Assistant-1E88E5?logo=musicassistant&logoColor=white" alt="Music Assistant">
  <img src="https://img.shields.io/badge/Jellyfin-00A4DC?logo=jellyfin&logoColor=white" alt="Jellyfin">
  <img src="https://img.shields.io/badge/Plex-E5A00D?logo=plex&logoColor=white" alt="Plex">
</p>

---

## 문서 / Documentation

소스는 [`docs/`](./docs/) — zensical로 빌드되어 GitHub Pages에 배포됩니다.

| 영역 | 한국어 | English |
| --- | --- | --- |
| 하드웨어 | [hardware.md](./docs/hardware.md) | [en/hardware.md](./docs/en/hardware.md) |
| 플랫폼 | [platform/](./docs/platform/) | [en/platform/](./docs/en/platform/) |
| 통합 | [integrations/](./docs/integrations/) | [en/integrations/](./docs/en/integrations/) |
| 자동화 | [automations.md](./docs/automations.md) | [en/automations.md](./docs/en/automations.md) |
| 대시보드 | [dashboards.md](./docs/dashboards.md) | [en/dashboards.md](./docs/en/dashboards.md) |
| 음성과 AI | [voice-and-ai.md](./docs/voice-and-ai.md) | [en/voice-and-ai.md](./docs/en/voice-and-ai.md) |
| 옵저버빌리티 | [observability.md](./docs/observability.md) | [en/observability.md](./docs/en/observability.md) |
| 에너지 | [energy.md](./docs/energy.md) | [en/energy.md](./docs/en/energy.md) |
| 서비스 | [services/](./docs/services/) | [en/services/](./docs/en/services/) |
| 보관소 · 참고 | [retired.md](./docs/retired.md) · [resources.md](./docs/resources.md) | [en/retired.md](./docs/en/retired.md) · [en/resources.md](./docs/en/resources.md) |

## 도메인별 엔티티

| Domain | Count |
| --- | --- |
| automations | 49 |
| binary_sensors | 221 |
| device_trackers | 17 |
| lights | 14 |
| media_players | 16 |
| sensors | 988 |
| switches | 168 |
| others | 535 |
| **Total** | **2008** |

## 화면

<p align="center">
  <img src="./www/lovelace/overview.png" alt="Overview" width="32%">
  <img src="./www/lovelace/mobile.png" alt="Mobile" width="32%">
  <img src="./www/lovelace/energy.png" alt="Energy" width="32%">
</p>

## License

MIT — see [LICENSE](LICENSE). `secrets.yaml` 은 포함되지 않습니다.

> [!CAUTION]
> 이 설정은 매일 진화합니다. 문서가 항상 최신은 아닐 수 있습니다.

<!-- Footnotes -->

[github-url]: https://github.com/saya6k/home-assistant-config
[license-url]: https://github.com/saya6k/home-assistant-config/blob/main/LICENSE
[docs-url]: https://saya6k.github.io/home-assistant-config

[maintenance-img]: https://img.shields.io/maintenance/yes/2026?style=flat-square
[last-commit-img]: https://img.shields.io/github/last-commit/saya6k/home-assistant-config?style=flat-square
[commit-activity-img]: https://img.shields.io/github/commit-activity/m/saya6k/home-assistant-config?style=flat-square
[ci-img]: https://img.shields.io/github/actions/workflow/status/saya6k/home-assistant-config/release.yml?style=flat-square&label=CI
[license-img]: https://img.shields.io/github/license/saya6k/home-assistant-config?style=flat-square
[stars-img]: https://img.shields.io/github/stars/saya6k/home-assistant-config?style=flat-square
[docs-img]: https://img.shields.io/badge/docs-saya6k.github.io-1f6feb?style=flat-square&logo=github

<!--
Generated by the [readme custom integration](https://github.com/custom-components/readme).
Service: readme.generate
-->
