---
title: 애드온
---

# 애드온

현재 **23** 개의 애드온이 등록되어 있으며, 다음 카테고리로 분류할 수 있습니다.

## 개발 / 운영

| 이름                                                                                                      | 버전     | 상태    |
| --------------------------------------------------------------------------------------------------------- | -------- | ------- |
| [Advanced SSH & Web Terminal](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_ssh) | `23.0.9` | started |
| [Git pull](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_git_pull)                   | `9.0.1`  | unknown |
| [Samba share](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_samba)                   | `12.6.1` | started |
| [Studio Code Server](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_vscode)       | `6.0.1`  | started |

## 네트워크 / 보안

| 이름                                                                                                             | 버전    | 상태    |
| ---------------------------------------------------------------------------------------------------------------- | ------- | ------- |
| [Let's Encrypt](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_letsencrypt)                  | `6.3.2` | stopped |
| [NGINX Home Assistant SSL proxy](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_nginx_proxy) | `4.2.0` | started |

## 디바이스 / 프로토콜

| 이름                                                                                                                    | 버전       | 상태    |
| ----------------------------------------------------------------------------------------------------------------------- | ---------- | ------- |
| [ESPHome Device Builder](https://my.home-assistant.io/redirect/supervisor_addon/?addon=5c53de3b_esphome)                | `2026.5.1` | started |
| [Matter Server](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_matter_server)                       | `8.5.0`    | started |
| [Mosquitto broker](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_mosquitto)                        | `7.1.0`    | started |
| [OpenThread Border Router](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_openthread_border_router) | `3.0.0`    | started |
| [Shelly Manager](https://my.home-assistant.io/redirect/supervisor_addon/?addon=26aa648f_shelly-manager)                 | `1.1.4`    | started |

## 미디어 / 음성

| 이름                                                                                                             | 버전    | 상태    |
| ---------------------------------------------------------------------------------------------------------------- | ------- | ------- |
| [iSponsorBlockTV add-on](https://my.home-assistant.io/redirect/supervisor_addon/?addon=932a64e5_isponsorblocktv) | `2.6.2` | started |
| [Music Assistant](https://my.home-assistant.io/redirect/supervisor_addon/?addon=d5369777_music_assistant)        | `2.8.8` | started |
| [Supertonic](https://my.home-assistant.io/redirect/supervisor_addon/?addon=local_supertonic)                     | `2.0.0` | started |

## AI / 자동화

| 이름                                                                                                                 | 버전     | 상태    |
| -------------------------------------------------------------------------------------------------------------------- | -------- | ------- |
| [HASS MCP Proxy](https://my.home-assistant.io/redirect/supervisor_addon/?addon=3d1b46f3_hass_mcpproxy)               | `1.0.20` | started |
| [LLM Conversation Agent](https://my.home-assistant.io/redirect/supervisor_addon/?addon=local_llm_conversation_agent) | `1.14.5` | started |
| [rethink](https://my.home-assistant.io/redirect/supervisor_addon/?addon=local_rethink)                               | `0.1.0`  | unknown |

## 서비스 / 생산성

| 이름                                                                                                 | 버전     | 상태    |
| ---------------------------------------------------------------------------------------------------- | -------- | ------- |
| [Home Detector](https://my.home-assistant.io/redirect/supervisor_addon/?addon=ba53f40c_homedetector) | `0.0.13` | started |
| [Wardrowbe](https://my.home-assistant.io/redirect/supervisor_addon/?addon=local_wardrowbe)           | `1.4.0`  | started |
| [Zensical](https://my.home-assistant.io/redirect/supervisor_addon/?addon=local_zensical)             | `0.1.0`  | started |

## 모니터링 / 데이터

| 이름                                                                                                      | 버전      | 상태    |
| --------------------------------------------------------------------------------------------------------- | --------- | ------- |
| [OpenTelemetry Collector](https://my.home-assistant.io/redirect/supervisor_addon/?addon=b69c5888_otelcol) | `0.12.14` | started |

## 기타 (분류 미지정)

> 새 애드온이 설치되면 여기에 표시됩니다. `templates/docs/platform/add-ons.md.j2` 의 `categories` 맵에 추가하면 적절한 섹션으로 이동합니다.

| 이름         | 슬러그               | 버전     | 상태    |
| ------------ | -------------------- | -------- | ------- |
| openWakeWord | `core_openwakeword`  | `2.1.0`  | started |
| Rematters    | `995e941b_rematters` | `0.1.28` | started |

자세한 음성/AI 파이프라인은 [음성과 AI](../voice-and-ai.md), 옵저버빌리티 스택은 [옵저버빌리티](../observability.md) 참조.
