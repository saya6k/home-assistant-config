---
title: Home
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

A personal Home Assistant setup, running since 2018. Currently **3113 entities**, **14 custom integrations**, and **17 add-ons**.

> [!CAUTION]
> A home keeps evolving. **This documentation may be out of date** — best effort to keep it fresh. (Auto-regenerated via `jinja_files.render`.)

## System at a glance

```
┌─ Hardware       │ Raspberry Pi 5 (HAOS), UniFi (local + remote), Matter/Thread/Wi-Fi
├─ Platform       │ HAOS (local, stateless) · Remote TrueNAS (Recorder MariaDB, backups)
├─ Integrations   │ 100+ built-in + 14 custom integrations (Marketplace) + 6 ESPHome devices
├─ Automations    │ 50 automations (mostly Korean) · scripts/scenes
├─ Dashboards     │ Lovelace storage mode + smarthome3d-card (3D dashboard)
├─ Voice & AI     │ HA Cloud STT · Supertonic TTS · OpenAI/Claude/Gemini/llama.cpp · LLM tool scripts
├─ Observability  │ SQL-based recorder DB metrics · System Monitor · alert package
├─ Backups        │ Daily automatic backups → local + remote TrueNAS + Nabu Casa Cloud (3 kept)
└─ Services       │ Paperless-ngx · Pocket ID  (both on remote TrueNAS)
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

## Documentation

- [Hardware](./hardware.md) — devices, hubs, appliances, networking
- Platform
  - [Overview](./platform/index.md)
  - [Network](./platform/network.md) — AdGuard · NGINX · UniFi · auth
  - [Storage](./platform/storage.md) — MariaDB · `.storage`
  - [Backups](./platform/backups.md)
  - [Add-ons](./platform/add-ons.md) — 17 installed
- Integrations
  - [Overview](./integrations/index.md) — 100+ integrations
  - [Custom components](./integrations/custom-components.md) — 14 total
  - [ESPHome](./integrations/esphome.md) — wall pad, intercom, voice devices
- [Automations](./automations.md) — 50 total
- [Dashboards](./dashboards.md)
- [Voice & AI](./voice-and-ai.md)
- [Observability](./observability.md)
- [Energy](./energy.md)
- [Services](./services/index.md) — Paperless-ngx, Pocket ID
- [Retired](./retired.md) · [Inspiration](./resources.md)

## License

This repository is distributed under the [MIT License](https://github.com/saya6k/home-assistant-config/blob/main/LICENSE). `secrets.yaml` is not included.
