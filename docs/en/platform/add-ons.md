---
title: Add-ons
---

# Add-ons

Currently **23** add-ons installed, grouped as follows.

## Dev / Ops

| Name                                                                                                      | Version  | State   |
| --------------------------------------------------------------------------------------------------------- | -------- | ------- |
| [Advanced SSH & Web Terminal](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_ssh) | `23.0.9` | started |
| [Git pull](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_git_pull)                   | `9.0.1`  | unknown |
| [Samba share](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_samba)                   | `12.6.1` | started |
| [Studio Code Server](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_vscode)       | `6.0.1`  | started |

## Network / Security

| Name                                                                                                             | Version | State   |
| ---------------------------------------------------------------------------------------------------------------- | ------- | ------- |
| [Let's Encrypt](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_letsencrypt)                  | `6.3.2` | stopped |
| [NGINX Home Assistant SSL proxy](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_nginx_proxy) | `4.2.0` | started |

## Devices / Protocols

| Name                                                                                                                    | Version    | State   |
| ----------------------------------------------------------------------------------------------------------------------- | ---------- | ------- |
| [ESPHome Device Builder](https://my.home-assistant.io/redirect/supervisor_addon/?addon=5c53de3b_esphome)                | `2026.5.1` | started |
| [Matter Server](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_matter_server)                       | `8.5.0`    | started |
| [Mosquitto broker](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_mosquitto)                        | `7.1.0`    | started |
| [OpenThread Border Router](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_openthread_border_router) | `3.0.0`    | started |
| [Shelly Manager](https://my.home-assistant.io/redirect/supervisor_addon/?addon=26aa648f_shelly-manager)                 | `1.1.4`    | started |

## Media / Voice

| Name                                                                                                             | Version | State   |
| ---------------------------------------------------------------------------------------------------------------- | ------- | ------- |
| [iSponsorBlockTV add-on](https://my.home-assistant.io/redirect/supervisor_addon/?addon=932a64e5_isponsorblocktv) | `2.6.2` | started |
| [Music Assistant](https://my.home-assistant.io/redirect/supervisor_addon/?addon=d5369777_music_assistant)        | `2.8.8` | started |
| [Supertonic](https://my.home-assistant.io/redirect/supervisor_addon/?addon=local_supertonic)                     | `2.0.0` | started |

## AI / Automation

| Name                                                                                                                 | Version  | State   |
| -------------------------------------------------------------------------------------------------------------------- | -------- | ------- |
| [HASS MCP Proxy](https://my.home-assistant.io/redirect/supervisor_addon/?addon=3d1b46f3_hass_mcpproxy)               | `1.0.20` | started |
| [LLM Conversation Agent](https://my.home-assistant.io/redirect/supervisor_addon/?addon=local_llm_conversation_agent) | `1.14.5` | started |
| [rethink](https://my.home-assistant.io/redirect/supervisor_addon/?addon=local_rethink)                               | `0.1.0`  | unknown |

## Services / Productivity

| Name                                                                                                 | Version  | State   |
| ---------------------------------------------------------------------------------------------------- | -------- | ------- |
| [Home Detector](https://my.home-assistant.io/redirect/supervisor_addon/?addon=ba53f40c_homedetector) | `0.0.13` | started |
| [Wardrowbe](https://my.home-assistant.io/redirect/supervisor_addon/?addon=local_wardrowbe)           | `1.4.0`  | started |
| [Zensical](https://my.home-assistant.io/redirect/supervisor_addon/?addon=local_zensical)             | `0.1.0`  | started |

## Monitoring / Data

| Name                                                                                                      | Version   | State   |
| --------------------------------------------------------------------------------------------------------- | --------- | ------- |
| [OpenTelemetry Collector](https://my.home-assistant.io/redirect/supervisor_addon/?addon=b69c5888_otelcol) | `0.12.14` | started |

## Uncategorized

> New add-ons land here. Add the slug to the `categories` map in `templates/docs/platform/add-ons.md.j2` (and the English mirror) to move it into the right section.

| Name         | Slug                 | Version  | State   |
| ------------ | -------------------- | -------- | ------- |
| openWakeWord | `core_openwakeword`  | `2.1.0`  | started |
| Rematters    | `995e941b_rematters` | `0.1.28` | started |

See [Voice & AI](../voice-and-ai.md) for the audio/AI pipeline, [Observability](../observability.md) for the metrics/logs/traces stack.
