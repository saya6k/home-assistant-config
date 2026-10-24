---
title: Home
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

A personal Home Assistant setup, running since 2018. Currently **2008 entities**, **17 HACS integrations**, and **23 add-ons**.

> [!CAUTION]
> A home keeps evolving. **This documentation may be out of date** — best effort to keep it fresh. (Auto-regenerated via `jinja2docs.render`.)

## System at a glance

```
┌─ Hardware       │ Piesia AD742A + Raspberry Pi 5, UniFi (local + remote), Matter/Thread/Wi-Fi
├─ Platform       │ HAOS (local, stateless) · Remote TrueNAS (Recorder MariaDB, observability backends)
├─ Integrations   │ 100+ built-in + 17 custom components + 3 ESPHome devices
├─ Automations    │ 49 automations (mostly Korean) · scenes/scripts
├─ Dashboards     │ Lovelace storage mode + Mushroom/Bubble Card/Card Mod
├─ Voice & AI     │ Whisper · Supertonic-MNN · Ollama · Voice Satellite · multiple LLM agents
├─ Observability  │ otelcol agent (local) ─VPN─▶ otelcol gateway (remote) ─▶ Prometheus / Loki / Tempo ─▶ Grafana
├─ Backups        │ 3× local + 1× remote TrueNAS + 1× Nabu Casa Cloud
└─ Services       │ Paperless-ngx · Pocket ID  (both on remote TrueNAS)
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

## Documentation

- [Hardware](./hardware.md) — devices, hubs, appliances, networking
- Platform
  - [Overview](./platform/index.md)
  - [Network](./platform/network.md) — AdGuard · NGINX · UniFi · auth
  - [Storage](./platform/storage.md) — MariaDB · `.storage`
  - [Backups](./platform/backups.md)
  - [Add-ons](./platform/add-ons.md) — 23 installed
- Integrations
  - [Overview](./integrations/index.md) — 100+ integrations
  - [Custom components](./integrations/custom-components.md) — 17 HACS integrations
  - [ESPHome](./integrations/esphome.md) — wall pad, intercom, voice satellite
- [Automations](./automations.md) — 49 total
- [Dashboards](./dashboards.md)
- [Voice & AI](./voice-and-ai.md)
- [Observability](./observability.md)
- [Energy](./energy.md)
- [Services](./services/index.md) — Paperless-ngx, Pocket ID
- [Retired](./retired.md) · [Inspiration](./resources.md)

## License

This repository is distributed under the [MIT License](https://github.com/saya6k/home-assistant-config/blob/main/LICENSE). `secrets.yaml` is not included.
