# AGENTS.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Home Assistant configuration repository for a comprehensive smart home setup running on Home Assistant OS 18.4 on a Raspberry Pi 5 (Home Assistant Core currently `2026.11.0b1`, beta channel). The configuration manages 2000+ entities across multiple domains including climate control, security, media, voice, and energy monitoring. This is a production system actively used since 2018.

## Key Architecture

### Configuration Structure

- **Split Configuration**: Main `configuration.yaml` uses packages pattern with `!include_dir_named ./packages/`
- **Packages Directory** (`packages/`): Modular YAML files for specific functionality
  - `alerts.yaml`: `alert:` definitions (ping lost, UniFi site offline, study interruption) pushed to the iPhone/MacBook mobile apps
  - `anniversaries.yaml`: Anniversary template sensors from the `edwin_d/anniversary.yaml` blueprint; names and dates come from `!secret anniversary_{1,2,3}_{name,date}`
  - `citybikes.yaml`: City bike availability tracking
  - `flux.yaml`: Flux circadian color temperature (brightness adjustment disabled)
  - `matrix.yaml`: Matrix integration draft, fully commented out
- **Automations**: Stored in `automations.yaml` (~46 automations, primarily in Korean)
- **Scripts**: Stored in `scripts.yaml` (~20 scripts, including the LLM tool scripts built from `saya6k/*_llm_tool.yaml` blueprints)
- **Scenes**: Stored in `scenes.yaml`
- **Blueprints** (`blueprints/`): Organized under `automation/`, `script/`, and `template/` subdirectories with vendor-named folders (`saya6k/`, `censay/`, `music-assistant/`, `TheFes/`, `edwin_d/`, `homeassistant/`)

### Data Storage

- **Recorder**: Uses an **external MariaDB on a remote TrueNAS** (reached over a site-to-site VPN; connection string in `secrets.yaml`). Local HA is intentionally stateless.
  - Auto-purge and auto-repack enabled
  - 120-second commit interval for performance (also helps absorb VPN latency)
  - Excludes high-frequency / low-value domains: `camera`, `sun`, `time_date`, `todo`, `update`, `worldclock`, `event`, `weather.`
  - Entity-glob exclusions for clocks, dates, uptime, load averages, anniversary/expiry sensors, version sensors, and derived `any_*`/`all_*`/`count_*`/`overview_*` helpers
- **Monitoring**: No metrics/log exporter runs locally (no `prometheus:` integration, no otelcol add-on). Recorder DB health comes from `sql` integration sensors (`Home Assistant RDB Size`, slow queries, threads) plus a `derivative` queries-per-second sensor; host health from System Monitor, Uptime, Certificate Expiry, Version, and RPi Power.

### Custom Components

`custom_components/` holds 17 custom integrations. HACS is no longer installed — custom integrations and Lovelace plugins are installed through Home Assistant's built-in **Marketplace** (`marketplace` integration). `ancs` is installed manually.

**Korean-specific integrations:**

- `kr_public_data`: Korean public data (KEPCO, fuel prices, weather/alerts, transit, AirKorea, disaster info)
- `chzzk`: Naver CHZZK live-streaming presence
- `naver_map`: Naver Map
- `pweb_amano`: Amano parking system

**Home / appliance management:**

- `dyson_local`: Local control for Dyson devices
- `localthings`: Local control for Samsung appliances (microwave)
- `wardrowbe`: Wardrobe/closet management
- `xbloom`: xBloom coffee machine
- `life360`: Location tracking
- `ancs`: iPhone notifications (ANCS) over Bluetooth

**Utilities:**

- `jinja_files`: Renders every `templates/**/*.j2` into the matching path (`jinja_files.render`); generates `README.md` and parts of `docs/`
- `spook` (+ `spook_calibration`, `spook_inverse`, `spook_time_in_state`): Advanced toolbox with additional services
- `restore_persistent_notifications`: Persists notifications across restarts
- `truenas_ce`: TrueNAS CE monitoring

### ESPHome Devices

ESPHome configurations are in `esphome/` directory:

- `esp-wallpad.yaml`: Hyundai HT wall pad bridge (M5Stack Atom, RS-485)
- `esp-subphone.yaml`: Subphone/intercom integration
- `archive/`: Retired device configurations (e.g. `living-room-assistant.yaml`, `nano-c6.yaml`)
- `fonts/`: Bundled fonts for display devices (not tracked in this repo)
- `esphome/` is also a separate git repo on the HA server with its own `secrets.yaml`
- Other ESPHome devices adopted in HA (Voice PE, Echo Show 5/8 and a YUPP mirror running TECHO5/YUPP firmware, a TDS meter) have no YAML in this repo

### Frontend

- **Lovelace**: Storage mode only (UI-managed dashboards in `.storage/`); no `ui-lovelace.yaml` is used
- **Themes**: Custom themes in `themes/` directory (`Frosted Glass Light/`)
- **Custom Cards**: Installed via Marketplace into `www/community/` and registered in `.storage/lovelace_resources` (currently `floor3d-card`, `ha-homelab-map`, plus `/local/floor3d/weather.js`)
- **Extra Modules**: None — the old `card-mod` entry under `frontend.extra_module_url` is commented out

### Add-ons

The system runs these Home Assistant add-ons (apps):

- **Development**: Advanced SSH & Web Terminal, CodeMirror, Samba share
- **Devices / protocols**: ESPHome Device Builder, Matter Server, Mosquitto broker, OpenThread Border Router
- **Network**: NGINX Home Assistant SSL proxy, Let's Encrypt (started on demand)
- **Voice / media**: Supertonic (TTS, Wyoming), Whisper (stopped), Music Assistant, YT Music PO Token Generator
- **AI / MCP**: CRW Web Tools, Memory (both exposed to HA through the `mcp` integration)
- **Services**: Wardrowbe, NILM (stopped)

Jellyfin, Plex, Paperless-ngx, Immich, Mealie, AdGuard Home, Traccar, and Transmission run outside this HA host and are reached only through their HA integrations.

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

List all add-ons (`ha addons` still works but is deprecated in favor of `ha apps`):

```bash
ha apps
```

Restart specific add-on (e.g., ESPHome):

```bash
ha apps restart 5c53de3b_esphome
```

Check add-on logs:

```bash
ha apps logs 5c53de3b_esphome
```

### Generated Docs

`README.md` and the docs pages that have a `templates/**/*.j2` counterpart are generated on the HA server by the `jinja_files` integration. Edit the `.j2` template, not the rendered `.md`, then render on the server (existing files are skipped unless `override` is set):

```yaml
action: jinja_files.render
data:
  override: true
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
- No example/fake secrets file in the repo: CI generates mock secrets from `.github/workflows/mock-secrets-config.json` and `mock-esphome-secrets-config.json`. Don't add `*.example.yaml` under `esphome/` — the ESPHome dashboard picks up every top-level YAML there as a device
- ESPHome has separate `esphome/secrets.yaml`
- A pre-push gitleaks hook scans every commit being pushed (including commits made on the HA server, where hooks don't run); install with `pre-commit install`

### Entity Naming

- Korean language is used extensively for entity names and automations
- Entities follow `domain.descriptive_name` pattern
- Use `homeassistant.customize` in packages for friendly names and icons

### Energy Monitoring

The system tracks energy usage across multiple domains:

- Electricity: KEPCO usage/billing via `kr_public_data`, per-circuit power via Shelly EM Mini Gen4 and Shelly Power Strip 4 Gen4
- Gas and water: UI-defined `template` sensors (`Utility Total Gas/Water`, last day/month) feeding `utility_meter` (this day/month)
- Grid carbon intensity via Electricity Maps (`co2signal`)

### Notification System

Alerts defined in `packages/alerts.yaml`:

- `alert:` entities grouped by section comments (Fatal / Error / Warning / Notice); currently ping lost, UniFi site offline (×2), and study interruption
- Delivered to the `mobile_app_*` notifiers with iOS `time-sensitive` interruption level; `done_message: clear_notification` removes the push when resolved
- Korean language messages
- Other notifications (Discord bot, SMTP, persistent notifications) are sent from automations

### Authentication & HTTP

- No `http:` block in `configuration.yaml`; external access goes through the NGINX SSL proxy add-on
- `homeassistant.auth_providers` is the built-in `homeassistant` provider only
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

MariaDB (Recorder) is monitored via `sql` integration sensors (`Home Assistant RDB Size`, slow queries, threads running/connected) and a `derivative` queries-per-second sensor.

## Development Notes

- **Language**: Mix of English (config structure) and Korean (entity names, automations, notifications)
- **Platform**: Home Assistant OS 18.4 on a Raspberry Pi 5 (`rpi5-64` board, 128 GB NVMe data disk)
- **Integration Count**: 100+ integrations (default + custom)
- **Storage**: Local HA is stateless. Recorder runs on a remote MariaDB on TrueNAS (over VPN). The local `home-assistant_v2.db` SQLite file is not used.
- **Backups**: Daily automatic backups to the local disk, the `TrueNAS_Backup` network storage mount, and Home Assistant Cloud; 3 copies retained
- **Update Strategy**: Semantic release automation configured (`.releaserc`)
- **Git**: Pre-commit hooks enforce YAML linting and formatting (`yamllint`, `prettier`)
- **CLAUDE.md**: Symlink to `AGENTS.md` — edit `AGENTS.md` only
