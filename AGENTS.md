# AGENTS.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Home Assistant configuration repository for a comprehensive smart home setup running on Home Assistant OS (currently version `2026.5.4`). The configuration manages 2000+ entities across multiple domains including climate control, security, media, voice, and energy monitoring. This is a production system actively used since 2018.

## Key Architecture

### Configuration Structure

- **Split Configuration**: Main `configuration.yaml` uses packages pattern with `!include_dir_named ./packages/`
- **Packages Directory** (`packages/`): Modular YAML files for specific functionality
  - `alerts_and_notifications.yaml`: Alert definitions and notification rules
  - `citybikes.yaml`: City bike availability tracking
  - `flux.yaml`: Adaptive lighting configuration (brightness adjustment disabled)
  - `xbloom.yaml`: xBloom coffee machine integration (recipes, scripts, sensors)
- **Automations**: Stored in `automations.yaml` (47 automations, primarily in Korean)
- **Scripts**: Stored in `scripts.yaml`
- **Scenes**: Stored in `scenes.yaml`
- **Blueprints** (`blueprints/`): Organized under `automation/`, `script/`, and `template/` subdirectories with vendor-named folders (e.g. `Blackshome/`, `luuquangvu/`, `music-assistant/`, `homeassistant/`)

### Data Storage

- **Recorder**: Uses an **external MariaDB on a remote TrueNAS** (reached over a site-to-site VPN; connection string in `secrets.yaml`). Local HA is intentionally stateless.
  - Auto-purge and auto-repack enabled
  - 120-second commit interval for performance (also helps absorb VPN latency)
  - Excludes high-frequency / low-value domains: `camera`, `sun`, `time_date`, `todo`, `update`, `worldclock`, `event`, `weather.`
  - Entity-glob exclusions for clocks, dates, uptime, load averages, anniversary/expiry sensors, version sensors, and derived `any_*`/`all_*`/`count_*`/`overview_*` helpers
- **Long-term Observability**: A local OpenTelemetry Collector (`otelcol`) sidecar scrapes HA's `/api/prometheus` endpoint + collects system/addon logs, then ships everything as OTLP to a **remote otelcol gateway running on TrueNAS**. From there: metrics → Prometheus, logs → Loki, traces → Tempo, visualized in Grafana. All backends live on the remote TrueNAS.

### Custom Components

The system uses 18+ custom integrations in `custom_components/`:

**Korean-specific integrations:**

- `kr_component_kit`: Korean home/utility integrations kit
- `chzzk`: Naver CHZZK live-streaming presence

**Home / appliance management:**

- `dyson_local`: Local control for Dyson devices
- `ha_washdata`: Washing machine data integration
- `wardrowbe`: Wardrobe/closet management
- `xbloom`: xBloom coffee machine
- `life360`: Family location tracking
- `dawarich`: Self-hosted location history
- `anniversaries`: Date-based anniversary sensors

**Voice / AI:**

- `voice_satellite`: Voice satellite endpoint
- `voice_satellite_llm_tools`: LLM tool integration for voice satellite

**Utilities:**

- `hacs`: Home Assistant Community Store (manages custom components)
- `spook`: Advanced toolbox with additional services
- `restore_persistent_notifications`: Persists notifications across restarts
- `truenas`: TrueNAS NAS monitoring
- `cyclist`: Cycling-related sensors
- `steam_wishlist`: Steam wishlist tracking
- `discord_game`: Discord game presence

### ESPHome Devices

ESPHome configurations are in `esphome/` directory:

- `esp-wallpad.yaml`: Wall-mounted control panel integration
- `esp-subphone.yaml`: Subphone/intercom integration
- `respeaker-voice-eada78.yaml`: ReSpeaker-based voice satellite
- `archive/`: Retired device configurations (e.g. `living-room-assistant.yaml`, `xvf3800.yaml`, `nano-c6.yaml`)
- `fonts/`: Bundled fonts for display devices
- `esphome/` is also a separate git repo with its own `secrets.yaml`

### Frontend

- **Lovelace**: Storage mode only (UI-managed dashboards in `.storage/`); no `ui-lovelace.yaml` is used
- **Themes**: Custom themes in `themes/` directory (e.g. `Frosted Glass Light/`)
- **Custom Cards**: Lovelace custom cards installed via HACS
- **Extra Modules**: `card-mod` is registered via `frontend.extra_module_url` in `configuration.yaml`; other modules (Bubble Card, brand icons, etc.) are loaded via the dashboard config

### Add-ons

The system runs many Home Assistant add-ons, including:

- **Development**: Studio Code Server, Advanced SSH & Web Terminal, File editor
- **Monitoring (local add-ons)**: `otelcol` agent only — Grafana, Loki, Tempo, Prometheus all run remotely on TrueNAS.
- **Services**: MariaDB, Mosquitto (MQTT), Node-RED, ESPHome Device Builder, Matter Server
- **AI/ML**: Ollama, Open WebUI, Whisper, Claude Terminal, Supertonic-MNN (TTS)
- **Media**: Jellyfin, Plex, Music Assistant, iSponsorBlockTV
- **Productivity**: Paperless-ngx, Calibre-web
- **Security**: AdGuard Home
- **MCP Servers**: Multiple Model Context Protocol servers for AI integrations

## Common Commands

### Configuration Validation

Home Assistant configuration check (before restart):

```bash
ha core check
```

### Service Management

Restart Home Assistant:

```bash
ha core restart
```

Rebuild Home Assistant container:

```bash
ha core rebuild
```

Check Home Assistant logs:

```bash
ha core logs
```

### Add-on Management

List all add-ons:

```bash
ha addons
```

Restart specific add-on (e.g., ESPHome):

```bash
ha addons restart 5c53de3b_esphome
```

Check add-on logs:

```bash
ha addons logs 5c53de3b_esphome
```

### ESPHome

Validate ESPHome configuration:

```bash
esphome config esphome/esp-wallpad.yaml
```

Compile ESPHome firmware:

```bash
esphome compile esphome/esp-wallpad.yaml
```

Upload to device:

```bash
esphome upload esphome/esp-wallpad.yaml
```

### Code Quality

Run pre-commit checks (yamllint, prettier, etc.):

```bash
pre-commit run --all-files
```

## Important Patterns

### Secrets Management

- Secrets stored in `secrets.yaml` (not in repo)
- Use `!secret key_name` syntax in YAML files
- Fake examples in `secrets.fake.yaml`
- ESPHome has separate `esphome/secrets.yaml`

### Entity Naming

- Korean language is used extensively for entity names and automations
- Entities follow `domain.descriptive_name` pattern
- Use `homeassistant.customize` in packages for friendly names and icons

### Energy Monitoring

The system tracks energy usage across multiple domains:

- Total utilities: electricity, gas, water
- Per-domain energy: HVAC, lights, media players, cookers
- Korean electricity billing handled via packages and template sensors

### Notification System

Alerts defined in `packages/alerts_and_notifications.yaml`:

- Multi-level alerts: Fatal, Error, Warning, Info
- Multiple notification channels: Discord, mobile devices, persistent notifications
- Korean language messages
- Supports iOS critical notifications for urgent alerts

### Authentication & HTTP

- `http:` block uses secrets for `cors_allowed_origins`, `trusted_proxies`, `use_x_forwarded_for`, `ip_ban_enabled`, and `login_attempts_threshold`
- An `alarm_control_panel` (`Security System`, manual platform) is defined directly in `configuration.yaml` with `armed_away`, `armed_home`, `armed_night`, and `armed_vacation` states

## Working with This Repository

### Before Making Changes

1. Always validate configuration with `ha core check`
2. Run pre-commit hooks with `pre-commit run --all-files`
3. Test changes in development environment if possible
4. This is a production system - changes affect active home automation

### File Locations

- Core configs: Root directory (`configuration.yaml`, `automations.yaml`, `scripts.yaml`, `scenes.yaml`)
- Modular configs: `packages/` directory
- Custom integrations: `custom_components/`
- ESPHome devices: `esphome/`
- Dashboards: managed in storage mode under `.storage/`
- Blueprints: `blueprints/{automation,script,template}/`
- TTS cache: `tts/`
- Voice satellite assets: `voice_satellite/` (models, sounds)

### Database Monitoring

MariaDB (Recorder) size monitored via a dedicated sensor.

## Development Notes

- **Language**: Mix of English (config structure) and Korean (entity names, automations, notifications)
- **Platform**: Home Assistant OS (Generic x86-64 board, per `.storage/core.config_entries`)
- **Integration Count**: 100+ integrations (default + custom)
- **Storage**: Local HA is stateless. Recorder runs on a remote MariaDB on TrueNAS (over VPN). Long-term metrics/logs/traces live on remote Prometheus/Loki/Tempo (via local otelcol → remote otelcol gateway). The local `home-assistant_v2.db` SQLite file is not used.
- **Update Strategy**: Semantic release automation configured (`.releaserc`)
- **Git**: Pre-commit hooks enforce YAML linting and formatting (`yamllint`, `prettier`)
- **CLAUDE.md**: Symlink to `AGENTS.md` — edit `AGENTS.md` only
