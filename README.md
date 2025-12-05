# Home Assistant Config

![Project Maintenance][maintenance-shield]
[![GitHub Workflow Status][github-img]][github-url]
[![Last Commit][last-commit-img]][github-url]
[![Commit Activity][commit-activity-img]][github-url]
[![License][license-img]][license-url]
[![GitHub Stars][stars-img]][github-url]

[![HA Version](https://img.shields.io/badge/Running%20Home%20Assistant-2025.12.0%20-darkblue)](https://github.com/home-assistant/home-assistant/core/releases/tag/2025.12.0)

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/my7nmfcm92k)

This is my Home Assistant configuration, updated on 2025-12-04.

I started using Home Assistant in 2018. Now, it has grown significantly, with a total of 1953 entities for now.

> [!CAUTION]
> I constantly improve my home. It evolves as I add new devices and services. It's changing as my daily routines are changing.
> Please, keep in mind **this documentation might be outdated** in covering some details. However, I'll try my best to keep this updated.

This repository publish it's documentation. Go to: [Documentation][docs-url]

Or you can directly go to:

[Hardware](./docs/hardware.md) |
[Configuration](./docs/config/index.md) |
[Services](./docs/config/services.md) |
[Retired](./docs/retired.md) |
[Inspiration](./docs/resources.md)

## Table of Content

[Insights](#insights) |
[Integrations](#integrations) |
[Automations](#automations) |
[Add-Ons](#add-ons) |
[Dashboards](#dashboards) |
[Custom Integrations](#custom-integrations) |

----

## Insights

Domain | Value
-- | --
automations | 39
binary_sensors | 202
device_trackers | 14
lights | 13
media_players | 9
sensors | 1079
switches | 162
switches | 162
others | 435
**Total** | **1953**

## Integrations

Integration | Name
--|--
[<img src="https://brands.home-assistant.io/_/seventeentrack/icon.png" height="24"/>](https://brands.home-assistant.io/_/seventeentrack/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/seventeentrack/icon.png" height="24"/>](https://brands.home-assistant.io/_/seventeentrack/icon.png#gh-light-mode-only) | [17TRACK](https://home-assistant.io/integrations/seventeentrack)
[<img src="https://brands.home-assistant.io/_/alert/icon.png" height="24"/>](https://brands.home-assistant.io/_/alert/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/alert/icon.png" height="24"/>](https://brands.home-assistant.io/_/alert/icon.png#gh-light-mode-only) | [alert](https://home-assistant.io/integrations/alert)
[<img src="https://brands.home-assistant.io/_/alpha_vantage/icon.png" height="24"/>](https://brands.home-assistant.io/_/alpha_vantage/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/alpha_vantage/icon.png" height="24"/>](https://brands.home-assistant.io/_/alpha_vantage/icon.png#gh-light-mode-only) | [Alpha Vantage](https://home-assistant.io/integrations/alpha_vantage)
[<img src="https://brands.home-assistant.io/_/anthropic/icon.png" height="24"/>](https://brands.home-assistant.io/_/anthropic/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/anthropic/icon.png" height="24"/>](https://brands.home-assistant.io/_/anthropic/icon.png#gh-light-mode-only) | [Anthropic Conversation](https://home-assistant.io/integrations/anthropic)
[<img src="https://brands.home-assistant.io/_/icloud/icon.png" height="24"/>](https://brands.home-assistant.io/_/icloud/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/icloud/icon.png" height="24"/>](https://brands.home-assistant.io/_/icloud/icon.png#gh-light-mode-only) | [Apple iCloud](https://home-assistant.io/integrations/icloud)
[<img src="https://brands.home-assistant.io/_/apple_tv/icon.png" height="24"/>](https://brands.home-assistant.io/_/apple_tv/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/apple_tv/icon.png" height="24"/>](https://brands.home-assistant.io/_/apple_tv/icon.png#gh-light-mode-only) | [Apple TV](https://home-assistant.io/integrations/apple_tv)
[<img src="https://brands.home-assistant.io/_/automation/icon.png" height="24"/>](https://brands.home-assistant.io/_/automation/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/automation/icon.png" height="24"/>](https://brands.home-assistant.io/_/automation/icon.png#gh-light-mode-only) | [Automation](https://home-assistant.io/integrations/automation)
[<img src="https://brands.home-assistant.io/_/backup/icon.png" height="24"/>](https://brands.home-assistant.io/_/backup/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/backup/icon.png" height="24"/>](https://brands.home-assistant.io/_/backup/icon.png#gh-light-mode-only) | [Backup](https://home-assistant.io/integrations/backup)
[<img src="https://brands.home-assistant.io/_/bitcoin/icon.png" height="24"/>](https://brands.home-assistant.io/_/bitcoin/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/bitcoin/icon.png" height="24"/>](https://brands.home-assistant.io/_/bitcoin/icon.png#gh-light-mode-only) | [Bitcoin](https://home-assistant.io/integrations/bitcoin)
[<img src="https://brands.home-assistant.io/_/bluetooth/icon.png" height="24"/>](https://brands.home-assistant.io/_/bluetooth/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/bluetooth/icon.png" height="24"/>](https://brands.home-assistant.io/_/bluetooth/icon.png#gh-light-mode-only) | [Bluetooth](https://home-assistant.io/integrations/bluetooth)
[<img src="https://brands.home-assistant.io/_/bluetooth/icon.png" height="24"/>](https://brands.home-assistant.io/_/bluetooth/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/bluetooth/icon.png" height="24"/>](https://brands.home-assistant.io/_/bluetooth/icon.png#gh-light-mode-only) | [Bluetooth](https://home-assistant.io/integrations/bluetooth)
[<img src="https://brands.home-assistant.io/_/caldav/icon.png" height="24"/>](https://brands.home-assistant.io/_/caldav/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/caldav/icon.png" height="24"/>](https://brands.home-assistant.io/_/caldav/icon.png#gh-light-mode-only) | [CalDAV](https://home-assistant.io/integrations/caldav)
[<img src="https://brands.home-assistant.io/_/calendar/icon.png" height="24"/>](https://brands.home-assistant.io/_/calendar/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/calendar/icon.png" height="24"/>](https://brands.home-assistant.io/_/calendar/icon.png#gh-light-mode-only) | [Calendar](https://home-assistant.io/integrations/calendar)
[<img src="https://brands.home-assistant.io/_/cert_expiry/icon.png" height="24"/>](https://brands.home-assistant.io/_/cert_expiry/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/cert_expiry/icon.png" height="24"/>](https://brands.home-assistant.io/_/cert_expiry/icon.png#gh-light-mode-only) | [Certificate Expiry](https://home-assistant.io/integrations/cert_expiry)
[<img src="https://brands.home-assistant.io/_/command_line/icon.png" height="24"/>](https://brands.home-assistant.io/_/command_line/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/command_line/icon.png" height="24"/>](https://brands.home-assistant.io/_/command_line/icon.png#gh-light-mode-only) | [Command Line](https://home-assistant.io/integrations/command_line)
[<img src="https://brands.home-assistant.io/_/default_config/icon.png" height="24"/>](https://brands.home-assistant.io/_/default_config/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/default_config/icon.png" height="24"/>](https://brands.home-assistant.io/_/default_config/icon.png#gh-light-mode-only) | [Default Config](https://home-assistant.io/integrations/default_config)
[<img src="https://brands.home-assistant.io/_/discord/icon.png" height="24"/>](https://brands.home-assistant.io/_/discord/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/discord/icon.png" height="24"/>](https://brands.home-assistant.io/_/discord/icon.png#gh-light-mode-only) | [Discord](https://home-assistant.io/integrations/discord)
[<img src="https://brands.home-assistant.io/_/dnsip/icon.png" height="24"/>](https://brands.home-assistant.io/_/dnsip/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/dnsip/icon.png" height="24"/>](https://brands.home-assistant.io/_/dnsip/icon.png#gh-light-mode-only) | [DNS IP](https://home-assistant.io/integrations/dnsip)
[<img src="https://brands.home-assistant.io/_/downloader/icon.png" height="24"/>](https://brands.home-assistant.io/_/downloader/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/downloader/icon.png" height="24"/>](https://brands.home-assistant.io/_/downloader/icon.png#gh-light-mode-only) | [Downloader](https://home-assistant.io/integrations/downloader)
[<img src="https://brands.home-assistant.io/_/co2signal/icon.png" height="24"/>](https://brands.home-assistant.io/_/co2signal/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/co2signal/icon.png" height="24"/>](https://brands.home-assistant.io/_/co2signal/icon.png#gh-light-mode-only) | [Electricity Maps](https://home-assistant.io/integrations/co2signal)
[<img src="https://brands.home-assistant.io/_/esphome/icon.png" height="24"/>](https://brands.home-assistant.io/_/esphome/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/esphome/icon.png" height="24"/>](https://brands.home-assistant.io/_/esphome/icon.png#gh-light-mode-only) | [ESPHome](https://home-assistant.io/integrations/esphome)
[<img src="https://brands.home-assistant.io/_/feedreader/icon.png" height="24"/>](https://brands.home-assistant.io/_/feedreader/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/feedreader/icon.png" height="24"/>](https://brands.home-assistant.io/_/feedreader/icon.png#gh-light-mode-only) | [Feedreader](https://home-assistant.io/integrations/feedreader)
[<img src="https://brands.home-assistant.io/_/flux/icon.png" height="24"/>](https://brands.home-assistant.io/_/flux/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/flux/icon.png" height="24"/>](https://brands.home-assistant.io/_/flux/icon.png#gh-light-mode-only) | [Flux](https://home-assistant.io/integrations/flux)
[<img src="https://brands.home-assistant.io/_/frontend/icon.png" height="24"/>](https://brands.home-assistant.io/_/frontend/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/frontend/icon.png" height="24"/>](https://brands.home-assistant.io/_/frontend/icon.png#gh-light-mode-only) | [Frontend](https://home-assistant.io/integrations/frontend)
[<img src="https://brands.home-assistant.io/_/generic/icon.png" height="24"/>](https://brands.home-assistant.io/_/generic/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/generic/icon.png" height="24"/>](https://brands.home-assistant.io/_/generic/icon.png#gh-light-mode-only) | [Generic Camera](https://home-assistant.io/integrations/generic)
[<img src="https://brands.home-assistant.io/_/github/icon.png" height="24"/>](https://brands.home-assistant.io/_/github/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/github/icon.png" height="24"/>](https://brands.home-assistant.io/_/github/icon.png#gh-light-mode-only) | [GitHub](https://home-assistant.io/integrations/github)
[<img src="https://brands.home-assistant.io/_/gdacs/icon.png" height="24"/>](https://brands.home-assistant.io/_/gdacs/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/gdacs/icon.png" height="24"/>](https://brands.home-assistant.io/_/gdacs/icon.png#gh-light-mode-only) | [Global Disaster Alert and Coordination System](https://home-assistant.io/integrations/gdacs)
[<img src="https://brands.home-assistant.io/_/google_drive/icon.png" height="24"/>](https://brands.home-assistant.io/_/google_drive/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/google_drive/icon.png" height="24"/>](https://brands.home-assistant.io/_/google_drive/icon.png#gh-light-mode-only) | [Google Drive](https://home-assistant.io/integrations/google_drive)
[<img src="https://brands.home-assistant.io/_/google_generative_ai_conversation/icon.png" height="24"/>](https://brands.home-assistant.io/_/google_generative_ai_conversation/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/google_generative_ai_conversation/icon.png" height="24"/>](https://brands.home-assistant.io/_/google_generative_ai_conversation/icon.png#gh-light-mode-only) | [Google Generative AI Conversation](https://home-assistant.io/integrations/google_generative_ai_conversation)
[<img src="https://brands.home-assistant.io/_/google_translate/icon.png" height="24"/>](https://brands.home-assistant.io/_/google_translate/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/google_translate/icon.png" height="24"/>](https://brands.home-assistant.io/_/google_translate/icon.png#gh-light-mode-only) | [Google Translate text-to-speech](https://home-assistant.io/integrations/google_translate)
[<img src="https://brands.home-assistant.io/_/history/icon.png" height="24"/>](https://brands.home-assistant.io/_/history/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/history/icon.png" height="24"/>](https://brands.home-assistant.io/_/history/icon.png#gh-light-mode-only) | [History](https://home-assistant.io/integrations/history)
[<img src="https://brands.home-assistant.io/_/holiday/icon.png" height="24"/>](https://brands.home-assistant.io/_/holiday/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/holiday/icon.png" height="24"/>](https://brands.home-assistant.io/_/holiday/icon.png#gh-light-mode-only) | [Holiday](https://home-assistant.io/integrations/holiday)
[<img src="https://brands.home-assistant.io/_/homeassistant/icon.png" height="24"/>](https://brands.home-assistant.io/_/homeassistant/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/homeassistant/icon.png" height="24"/>](https://brands.home-assistant.io/_/homeassistant/icon.png#gh-light-mode-only) | [Home Assistant Core Integration](https://home-assistant.io/integrations/homeassistant)
[<img src="https://brands.home-assistant.io/_/http/icon.png" height="24"/>](https://brands.home-assistant.io/_/http/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/http/icon.png" height="24"/>](https://brands.home-assistant.io/_/http/icon.png#gh-light-mode-only) | [HTTP](https://home-assistant.io/integrations/http)
[<img src="https://brands.home-assistant.io/_/imap/icon.png" height="24"/>](https://brands.home-assistant.io/_/imap/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/imap/icon.png" height="24"/>](https://brands.home-assistant.io/_/imap/icon.png#gh-light-mode-only) | [IMAP](https://home-assistant.io/integrations/imap)
[<img src="https://brands.home-assistant.io/_/jellyfin/icon.png" height="24"/>](https://brands.home-assistant.io/_/jellyfin/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/jellyfin/icon.png" height="24"/>](https://brands.home-assistant.io/_/jellyfin/icon.png#gh-light-mode-only) | [Jellyfin](https://home-assistant.io/integrations/jellyfin)
[<img src="https://brands.home-assistant.io/_/lastfm/icon.png" height="24"/>](https://brands.home-assistant.io/_/lastfm/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/lastfm/icon.png" height="24"/>](https://brands.home-assistant.io/_/lastfm/icon.png#gh-light-mode-only) | [Last.fm](https://home-assistant.io/integrations/lastfm)
[<img src="https://brands.home-assistant.io/_/lg_thinq/icon.png" height="24"/>](https://brands.home-assistant.io/_/lg_thinq/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/lg_thinq/icon.png" height="24"/>](https://brands.home-assistant.io/_/lg_thinq/icon.png#gh-light-mode-only) | [LG ThinQ](https://home-assistant.io/integrations/lg_thinq)
[<img src="https://brands.home-assistant.io/_/local_calendar/icon.png" height="24"/>](https://brands.home-assistant.io/_/local_calendar/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/local_calendar/icon.png" height="24"/>](https://brands.home-assistant.io/_/local_calendar/icon.png#gh-light-mode-only) | [Local Calendar](https://home-assistant.io/integrations/local_calendar)
[<img src="https://brands.home-assistant.io/_/local_ip/icon.png" height="24"/>](https://brands.home-assistant.io/_/local_ip/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/local_ip/icon.png" height="24"/>](https://brands.home-assistant.io/_/local_ip/icon.png#gh-light-mode-only) | [Local IP Address](https://home-assistant.io/integrations/local_ip)
[<img src="https://brands.home-assistant.io/_/local_todo/icon.png" height="24"/>](https://brands.home-assistant.io/_/local_todo/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/local_todo/icon.png" height="24"/>](https://brands.home-assistant.io/_/local_todo/icon.png#gh-light-mode-only) | [Local To Do](https://home-assistant.io/integrations/local_todo)
[<img src="https://brands.home-assistant.io/_/logger/icon.png" height="24"/>](https://brands.home-assistant.io/_/logger/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/logger/icon.png" height="24"/>](https://brands.home-assistant.io/_/logger/icon.png#gh-light-mode-only) | [Logger](https://home-assistant.io/integrations/logger)
[<img src="https://brands.home-assistant.io/_/lovelace/icon.png" height="24"/>](https://brands.home-assistant.io/_/lovelace/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/lovelace/icon.png" height="24"/>](https://brands.home-assistant.io/_/lovelace/icon.png#gh-light-mode-only) | [Lovelace](https://home-assistant.io/integrations/lovelace)
[<img src="https://brands.home-assistant.io/_/matter/icon.png" height="24"/>](https://brands.home-assistant.io/_/matter/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/matter/icon.png" height="24"/>](https://brands.home-assistant.io/_/matter/icon.png#gh-light-mode-only) | [Matter](https://home-assistant.io/integrations/matter)
[<img src="https://brands.home-assistant.io/_/media_extractor/icon.png" height="24"/>](https://brands.home-assistant.io/_/media_extractor/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/media_extractor/icon.png" height="24"/>](https://brands.home-assistant.io/_/media_extractor/icon.png#gh-light-mode-only) | [Media extractor](https://home-assistant.io/integrations/media_extractor)
[<img src="https://brands.home-assistant.io/_/mobile_app/icon.png" height="24"/>](https://brands.home-assistant.io/_/mobile_app/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/mobile_app/icon.png" height="24"/>](https://brands.home-assistant.io/_/mobile_app/icon.png#gh-light-mode-only) | [Mobile App](https://home-assistant.io/integrations/mobile_app)
[<img src="https://brands.home-assistant.io/_/mcp/icon.png" height="24"/>](https://brands.home-assistant.io/_/mcp/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/mcp/icon.png" height="24"/>](https://brands.home-assistant.io/_/mcp/icon.png#gh-light-mode-only) | [Model Context Protocol](https://home-assistant.io/integrations/mcp)
[<img src="https://brands.home-assistant.io/_/mcp_server/icon.png" height="24"/>](https://brands.home-assistant.io/_/mcp_server/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/mcp_server/icon.png" height="24"/>](https://brands.home-assistant.io/_/mcp_server/icon.png#gh-light-mode-only) | [Model Context Protocol Server](https://home-assistant.io/integrations/mcp_server)
[<img src="https://brands.home-assistant.io/_/moon/icon.png" height="24"/>](https://brands.home-assistant.io/_/moon/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/moon/icon.png" height="24"/>](https://brands.home-assistant.io/_/moon/icon.png#gh-light-mode-only) | [Moon](https://home-assistant.io/integrations/moon)
[<img src="https://brands.home-assistant.io/_/mqtt/icon.png" height="24"/>](https://brands.home-assistant.io/_/mqtt/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/mqtt/icon.png" height="24"/>](https://brands.home-assistant.io/_/mqtt/icon.png#gh-light-mode-only) | [MQTT](https://home-assistant.io/integrations/mqtt)
[<img src="https://brands.home-assistant.io/_/music_assistant/icon.png" height="24"/>](https://brands.home-assistant.io/_/music_assistant/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/music_assistant/icon.png" height="24"/>](https://brands.home-assistant.io/_/music_assistant/icon.png#gh-light-mode-only) | [Music Assistant](https://home-assistant.io/integrations/music_assistant)
[<img src="https://brands.home-assistant.io/_/my/icon.png" height="24"/>](https://brands.home-assistant.io/_/my/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/my/icon.png" height="24"/>](https://brands.home-assistant.io/_/my/icon.png#gh-light-mode-only) | [My Home Assistant](https://home-assistant.io/integrations/my)
[<img src="https://brands.home-assistant.io/_/netatmo/icon.png" height="24"/>](https://brands.home-assistant.io/_/netatmo/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/netatmo/icon.png" height="24"/>](https://brands.home-assistant.io/_/netatmo/icon.png#gh-light-mode-only) | [Netatmo](https://home-assistant.io/integrations/netatmo)
[<img src="https://brands.home-assistant.io/_/notify/icon.png" height="24"/>](https://brands.home-assistant.io/_/notify/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/notify/icon.png" height="24"/>](https://brands.home-assistant.io/_/notify/icon.png#gh-light-mode-only) | [notify](https://home-assistant.io/integrations/notify)
[<img src="https://brands.home-assistant.io/_/open_router/icon.png" height="24"/>](https://brands.home-assistant.io/_/open_router/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/open_router/icon.png" height="24"/>](https://brands.home-assistant.io/_/open_router/icon.png#gh-light-mode-only) | [Open Router](https://home-assistant.io/integrations/open_router)
[<img src="https://brands.home-assistant.io/_/otbr/icon.png" height="24"/>](https://brands.home-assistant.io/_/otbr/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/otbr/icon.png" height="24"/>](https://brands.home-assistant.io/_/otbr/icon.png#gh-light-mode-only) | [Open Thread Border Router](https://home-assistant.io/integrations/otbr)
[<img src="https://brands.home-assistant.io/_/openai_conversation/icon.png" height="24"/>](https://brands.home-assistant.io/_/openai_conversation/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/openai_conversation/icon.png" height="24"/>](https://brands.home-assistant.io/_/openai_conversation/icon.png#gh-light-mode-only) | [OpenAI Conversation](https://home-assistant.io/integrations/openai_conversation)
[<img src="https://brands.home-assistant.io/_/oralb/icon.png" height="24"/>](https://brands.home-assistant.io/_/oralb/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/oralb/icon.png" height="24"/>](https://brands.home-assistant.io/_/oralb/icon.png#gh-light-mode-only) | [Oral-B](https://home-assistant.io/integrations/oralb)
[<img src="https://brands.home-assistant.io/_/paperless_ngx/icon.png" height="24"/>](https://brands.home-assistant.io/_/paperless_ngx/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/paperless_ngx/icon.png" height="24"/>](https://brands.home-assistant.io/_/paperless_ngx/icon.png#gh-light-mode-only) | [Paperless-ngx](https://home-assistant.io/integrations/paperless_ngx)
[<img src="https://brands.home-assistant.io/_/ping/icon.png" height="24"/>](https://brands.home-assistant.io/_/ping/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/ping/icon.png" height="24"/>](https://brands.home-assistant.io/_/ping/icon.png#gh-light-mode-only) | [Ping (ICMP)](https://home-assistant.io/integrations/ping)
[<img src="https://brands.home-assistant.io/_/plex/icon.png" height="24"/>](https://brands.home-assistant.io/_/plex/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/plex/icon.png" height="24"/>](https://brands.home-assistant.io/_/plex/icon.png#gh-light-mode-only) | [Plex Media Server](https://home-assistant.io/integrations/plex)
[<img src="https://brands.home-assistant.io/_/private_ble_device/icon.png" height="24"/>](https://brands.home-assistant.io/_/private_ble_device/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/private_ble_device/icon.png" height="24"/>](https://brands.home-assistant.io/_/private_ble_device/icon.png#gh-light-mode-only) | [Private BLE Device](https://home-assistant.io/integrations/private_ble_device)
[<img src="https://brands.home-assistant.io/_/prometheus/icon.png" height="24"/>](https://brands.home-assistant.io/_/prometheus/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/prometheus/icon.png" height="24"/>](https://brands.home-assistant.io/_/prometheus/icon.png#gh-light-mode-only) | [Prometheus](https://home-assistant.io/integrations/prometheus)
[<img src="https://brands.home-assistant.io/_/proximity/icon.png" height="24"/>](https://brands.home-assistant.io/_/proximity/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/proximity/icon.png" height="24"/>](https://brands.home-assistant.io/_/proximity/icon.png#gh-light-mode-only) | [Proximity](https://home-assistant.io/integrations/proximity)
[<img src="https://brands.home-assistant.io/_/rpi_power/icon.png" height="24"/>](https://brands.home-assistant.io/_/rpi_power/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/rpi_power/icon.png" height="24"/>](https://brands.home-assistant.io/_/rpi_power/icon.png#gh-light-mode-only) | [Raspberry Pi Power Supply Checker](https://home-assistant.io/integrations/rpi_power)
[<img src="https://brands.home-assistant.io/_/recorder/icon.png" height="24"/>](https://brands.home-assistant.io/_/recorder/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/recorder/icon.png" height="24"/>](https://brands.home-assistant.io/_/recorder/icon.png#gh-light-mode-only) | [Recorder](https://home-assistant.io/integrations/recorder)
[<img src="https://brands.home-assistant.io/_/remote_calendar/icon.png" height="24"/>](https://brands.home-assistant.io/_/remote_calendar/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/remote_calendar/icon.png" height="24"/>](https://brands.home-assistant.io/_/remote_calendar/icon.png#gh-light-mode-only) | [Remote Calendar](https://home-assistant.io/integrations/remote_calendar)
[<img src="https://brands.home-assistant.io/_/rest/icon.png" height="24"/>](https://brands.home-assistant.io/_/rest/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/rest/icon.png" height="24"/>](https://brands.home-assistant.io/_/rest/icon.png#gh-light-mode-only) | [Restful](https://home-assistant.io/integrations/rest)
[<img src="https://brands.home-assistant.io/_/scene/icon.png" height="24"/>](https://brands.home-assistant.io/_/scene/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/scene/icon.png" height="24"/>](https://brands.home-assistant.io/_/scene/icon.png#gh-light-mode-only) | [Scene](https://home-assistant.io/integrations/scene)
[<img src="https://brands.home-assistant.io/_/scrape/icon.png" height="24"/>](https://brands.home-assistant.io/_/scrape/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/scrape/icon.png" height="24"/>](https://brands.home-assistant.io/_/scrape/icon.png#gh-light-mode-only) | [Scrape](https://home-assistant.io/integrations/scrape)
[<img src="https://brands.home-assistant.io/_/script/icon.png" height="24"/>](https://brands.home-assistant.io/_/script/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/script/icon.png" height="24"/>](https://brands.home-assistant.io/_/script/icon.png#gh-light-mode-only) | [Script](https://home-assistant.io/integrations/script)
[<img src="https://brands.home-assistant.io/_/season/icon.png" height="24"/>](https://brands.home-assistant.io/_/season/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/season/icon.png" height="24"/>](https://brands.home-assistant.io/_/season/icon.png#gh-light-mode-only) | [Season](https://home-assistant.io/integrations/season)
[<img src="https://brands.home-assistant.io/_/shell_command/icon.png" height="24"/>](https://brands.home-assistant.io/_/shell_command/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/shell_command/icon.png" height="24"/>](https://brands.home-assistant.io/_/shell_command/icon.png#gh-light-mode-only) | [Shell Command](https://home-assistant.io/integrations/shell_command)
[<img src="https://brands.home-assistant.io/_/shopping_list/icon.png" height="24"/>](https://brands.home-assistant.io/_/shopping_list/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/shopping_list/icon.png" height="24"/>](https://brands.home-assistant.io/_/shopping_list/icon.png#gh-light-mode-only) | [Shopping List](https://home-assistant.io/integrations/shopping_list)
[<img src="https://brands.home-assistant.io/_/smartthings/icon.png" height="24"/>](https://brands.home-assistant.io/_/smartthings/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/smartthings/icon.png" height="24"/>](https://brands.home-assistant.io/_/smartthings/icon.png#gh-light-mode-only) | [SmartThings](https://home-assistant.io/integrations/smartthings)
[<img src="https://brands.home-assistant.io/_/smtp/icon.png" height="24"/>](https://brands.home-assistant.io/_/smtp/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/smtp/icon.png" height="24"/>](https://brands.home-assistant.io/_/smtp/icon.png#gh-light-mode-only) | [SMTP](https://home-assistant.io/integrations/smtp)
[<img src="https://brands.home-assistant.io/_/sql/icon.png" height="24"/>](https://brands.home-assistant.io/_/sql/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/sql/icon.png" height="24"/>](https://brands.home-assistant.io/_/sql/icon.png#gh-light-mode-only) | [SQL](https://home-assistant.io/integrations/sql)
[<img src="https://brands.home-assistant.io/_/steam_online/icon.png" height="24"/>](https://brands.home-assistant.io/_/steam_online/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/steam_online/icon.png" height="24"/>](https://brands.home-assistant.io/_/steam_online/icon.png#gh-light-mode-only) | [Steam](https://home-assistant.io/integrations/steam_online)
[<img src="https://brands.home-assistant.io/_/sun/icon.png" height="24"/>](https://brands.home-assistant.io/_/sun/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/sun/icon.png" height="24"/>](https://brands.home-assistant.io/_/sun/icon.png#gh-light-mode-only) | [Sun](https://home-assistant.io/integrations/sun)
[<img src="https://brands.home-assistant.io/_/hassio/icon.png" height="24"/>](https://brands.home-assistant.io/_/hassio/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/hassio/icon.png" height="24"/>](https://brands.home-assistant.io/_/hassio/icon.png#gh-light-mode-only) | [Supervisor](https://home-assistant.io/integrations/hassio)
[<img src="https://brands.home-assistant.io/_/systemmonitor/icon.png" height="24"/>](https://brands.home-assistant.io/_/systemmonitor/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/systemmonitor/icon.png" height="24"/>](https://brands.home-assistant.io/_/systemmonitor/icon.png#gh-light-mode-only) | [System Monitor](https://home-assistant.io/integrations/systemmonitor)
[<img src="https://brands.home-assistant.io/_/template/icon.png" height="24"/>](https://brands.home-assistant.io/_/template/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/template/icon.png" height="24"/>](https://brands.home-assistant.io/_/template/icon.png#gh-light-mode-only) | [Template](https://home-assistant.io/integrations/template)
[<img src="https://brands.home-assistant.io/_/alarm_control_panel.template/icon.png" height="24"/>](https://brands.home-assistant.io/_/alarm_control_panel.template/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/alarm_control_panel.template/icon.png" height="24"/>](https://brands.home-assistant.io/_/alarm_control_panel.template/icon.png#gh-light-mode-only) | [Template Alarm control panel](https://home-assistant.io/integrations/alarm_control_panel.template)
[<img src="https://brands.home-assistant.io/_/thread/icon.png" height="24"/>](https://brands.home-assistant.io/_/thread/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/thread/icon.png" height="24"/>](https://brands.home-assistant.io/_/thread/icon.png#gh-light-mode-only) | [Thread](https://home-assistant.io/integrations/thread)
[<img src="https://brands.home-assistant.io/_/time_date/icon.png" height="24"/>](https://brands.home-assistant.io/_/time_date/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/time_date/icon.png" height="24"/>](https://brands.home-assistant.io/_/time_date/icon.png#gh-light-mode-only) | [Time & Date](https://home-assistant.io/integrations/time_date)
[<img src="https://brands.home-assistant.io/_/tod/icon.png" height="24"/>](https://brands.home-assistant.io/_/tod/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/tod/icon.png" height="24"/>](https://brands.home-assistant.io/_/tod/icon.png#gh-light-mode-only) | [Times of the Day](https://home-assistant.io/integrations/tod)
[<img src="https://brands.home-assistant.io/_/uptime/icon.png" height="24"/>](https://brands.home-assistant.io/_/uptime/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/uptime/icon.png" height="24"/>](https://brands.home-assistant.io/_/uptime/icon.png#gh-light-mode-only) | [Uptime](https://home-assistant.io/integrations/uptime)
[<img src="https://brands.home-assistant.io/_/version/icon.png" height="24"/>](https://brands.home-assistant.io/_/version/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/version/icon.png" height="24"/>](https://brands.home-assistant.io/_/version/icon.png#gh-light-mode-only) | [Version](https://home-assistant.io/integrations/version)
[<img src="https://brands.home-assistant.io/_/wake_on_lan/icon.png" height="24"/>](https://brands.home-assistant.io/_/wake_on_lan/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/wake_on_lan/icon.png" height="24"/>](https://brands.home-assistant.io/_/wake_on_lan/icon.png#gh-light-mode-only) | [Wake on LAN](https://home-assistant.io/integrations/wake_on_lan)
[<img src="https://brands.home-assistant.io/_/withings/icon.png" height="24"/>](https://brands.home-assistant.io/_/withings/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/withings/icon.png" height="24"/>](https://brands.home-assistant.io/_/withings/icon.png#gh-light-mode-only) | [Withings](https://home-assistant.io/integrations/withings)
[<img src="https://brands.home-assistant.io/_/workday/icon.png" height="24"/>](https://brands.home-assistant.io/_/workday/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/workday/icon.png" height="24"/>](https://brands.home-assistant.io/_/workday/icon.png#gh-light-mode-only) | [Workday](https://home-assistant.io/integrations/workday)
[<img src="https://brands.home-assistant.io/_/waqi/icon.png" height="24"/>](https://brands.home-assistant.io/_/waqi/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/waqi/icon.png" height="24"/>](https://brands.home-assistant.io/_/waqi/icon.png#gh-light-mode-only) | [World air quality index](https://home-assistant.io/integrations/waqi)
[<img src="https://brands.home-assistant.io/_/youtube/icon.png" height="24"/>](https://brands.home-assistant.io/_/youtube/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/youtube/icon.png" height="24"/>](https://brands.home-assistant.io/_/youtube/icon.png#gh-light-mode-only) | [YouTube](https://home-assistant.io/integrations/youtube)
[<img src="https://brands.home-assistant.io/_/zodiac/icon.png" height="24"/>](https://brands.home-assistant.io/_/zodiac/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/zodiac/icon.png" height="24"/>](https://brands.home-assistant.io/_/zodiac/icon.png#gh-light-mode-only) | [Zodiac](https://home-assistant.io/integrations/zodiac)
## Automations

> [!TIP]
> If you want to see my automation details other than list, go to [Automations](./docs/config/automations.md)

> [!TIP]
> Or if you want to see `automations.yaml`, click [automations.yaml](./automations.yaml)

Name | Description
-- | --
17TRACK 택배 알림 | mode: single
ASHRAE 55 Adaptive Climate Control | mode: single
ESPHome Auto-Update | mode: single
HA Startup | mode: single
Notify LG ThinQ Notifications | mode: single
Notify Personal Agenda | mode: single
Notify Seoul Teukbo | mode: single
Notify Study Interruption | mode: single
Notify to brush Teeth | mode: single
Notify Work Agenda | mode: single
TTS 캐시 지우기 | mode: single
update_youtube_watching_thumbnail | mode: 
Washer State On | mode: single
거실 장면 스위치 버튼 제어 | mode: single
고농도 이산화탄소 환기 알림 | mode: single
구청에서 온 알림 처리 및 확인 요청 | mode: parallel
귀가 시 환영 및 보조 기능 활성화 | mode: single
긴급 상황 알림: 재난별 지침 전송 | mode: single
막차 알림 | mode: single
배터리 부족 알림 | mode: single
새 이메일 도착 알림 | mode: queued
샤워 시 플레이리스트 재생 | mode: single
수면 장면 활성화 | mode: single
스팀 위시리스트 세일 알림 | mode: parallel
식사 준비 완료 시 식사 장면 활성화 | mode: single
식탁 닫히면 조명 끄기 | mode: single
아침 알림 및 시작 준비 | mode: single
안전 안내 알림 | mode: single
야간 화장실 이용간 조명 제어 | mode: single
오늘 강수 예보 알림 | mode: single
유튜브 최신 영상 저장 및 알림 | mode: parallel
이메일 수신 시 운송장 번호 추출 및 트래킹 추가 | mode: queued
집에 사람이 없을 때 자리 비움 장면 활성화 | mode: single
창문 열림 시 강우 예보 알림 | mode: single
창문 열림 시 공조 자동 제어 | mode: single
침대에서 침대에 누워 있다고 알림 | mode: single
침실 이산화탄소 농도 알림 | mode: single
핫 세일 알림 (위시리스트 체크) | mode: parallel
화장실 습도 40% 미만일 때 제습기 끄기 | mode: single

## Add-Ons

> [!TIP]
> If you want to see services I'm running as add-ons, go to [Services](./docs/config/services.md)

> [!TIP]
>  If you want to see how I built my grafana dashboards, go to [Monitoring](./docs/config/monitoring.md)

Name | Version | Description
-- | -- | --
[AdGuard Home](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_adguard) | 6.0.1 | started
[AdGuardHome Sync](https://my.home-assistant.io/redirect/supervisor_addon/?addon=486a4ea9_adguardhome-sync) | 0.2.1 | started
[Amniotic](https://my.home-assistant.io/redirect/supervisor_addon/?addon=da51adea_amniotic) | 1.0.8 | unknown
[Argon ONE OLED Display](https://my.home-assistant.io/redirect/supervisor_addon/?addon=8b81119a_argon_one_oled_display) | 1.16.2 | started
[DbStats](https://my.home-assistant.io/redirect/supervisor_addon/?addon=8bce8ef4_dbstats) | 0.5.12 | started
[Documentation Viewer](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a6d311c0_doc-viewer) | 1.0.2 | started
[ESPHome Device Builder](https://my.home-assistant.io/redirect/supervisor_addon/?addon=5c53de3b_esphome) | 2025.11.3 | started
[File editor](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_configurator) | 5.8.0 | started
[Firefly iii](https://my.home-assistant.io/redirect/supervisor_addon/?addon=db21ed7f_fireflyiii) | 6.4.9 | started
[Git pull](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_git_pull) | 8.0.1 | stopped
[Grafana](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_grafana) | 12.1.0 | started
[Grafana Loki](https://my.home-assistant.io/redirect/supervisor_addon/?addon=71dadad1_grafana-loki) | 4.0.1 | started
[Grafana Promtail](https://my.home-assistant.io/redirect/supervisor_addon/?addon=71dadad1_grafana-promtail) | 4.0.0 | started
[Grocy](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_grocy) | 0.24.0 | started
[HA COPS](https://my.home-assistant.io/redirect/supervisor_addon/?addon=670b30ea_ha-cops) | 1.39 | started
[HAOS Kiosk Display](https://my.home-assistant.io/redirect/supervisor_addon/?addon=4c8b21d0_haoskiosk) | 1.1.1 | unknown
[HassOS I2C Configurator](https://my.home-assistant.io/redirect/supervisor_addon/?addon=2ad4c73a_hassosi2cconfiguratoraddon) | 0.14 | stopped
[Home Detector](https://my.home-assistant.io/redirect/supervisor_addon/?addon=ba53f40c_homedetector) | 0.0.11 | started
[iSponsorBlockTV add-on](https://my.home-assistant.io/redirect/supervisor_addon/?addon=932a64e5_isponsorblocktv) | 2.3.0 | started
[KNXD daemon](https://my.home-assistant.io/redirect/supervisor_addon/?addon=ecaeb50e_knxd) | 0.6.1 | started
[Let's Encrypt](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_letsencrypt) | 5.4.9 | stopped
[Mailfilter](https://my.home-assistant.io/redirect/supervisor_addon/?addon=32b8266a_mailfilter) | 4.2.3 | started
[Mailserver](https://my.home-assistant.io/redirect/supervisor_addon/?addon=32b8266a_mailserver) | 5.0.1 | started
[MariaDB](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_mariadb) | 2.7.2 | started
[Matter Server](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_matter_server) | 8.1.1 | started
[MCP Proxy Server](https://my.home-assistant.io/redirect/supervisor_addon/?addon=adfd7a46_mcp_proxy_server) | 0.4.1 | started
[Mosquitto broker](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_mosquitto) | 6.5.2 | started
[MQTT Explorer](https://my.home-assistant.io/redirect/supervisor_addon/?addon=2ad4c73a_mqtt-explorer) | browser-1.0.1 | started
[Music Assistant](https://my.home-assistant.io/redirect/supervisor_addon/?addon=d5369777_music_assistant) | 2.6.3 | unknown
[Music Assistant (BETA)](https://my.home-assistant.io/redirect/supervisor_addon/?addon=d5369777_music_assistant_beta) | 2.7.0b17 | started
[NanoNVR](https://my.home-assistant.io/redirect/supervisor_addon/?addon=f3d82367_nanonvr) | 1.5.1 | started
[NGINX Home Assistant SSL proxy](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_nginx_proxy) | 3.14.0 | started
[Node-RED](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_nodered) | 20.2.3 | started
[Ollama](https://my.home-assistant.io/redirect/supervisor_addon/?addon=76e18fb5_ollama) | 0.13.1 | started
[OpenThread Border Router](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_openthread_border_router) | 2.15.2 | started
[Paperless-ngx](https://my.home-assistant.io/redirect/supervisor_addon/?addon=ca5234a0_paperless-ngx) | 3.1.1 | started
[phpMyAdmin](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_phpmyadmin) | 0.13.0 | started
[Picture Element Editor](https://my.home-assistant.io/redirect/supervisor_addon/?addon=6b81e8b5_picture_element_editor) | 1.0.0 | started
[Playwright](https://my.home-assistant.io/redirect/supervisor_addon/?addon=8165a4b1_playwright) | 0.2.3 | started
[Pocket ID](https://my.home-assistant.io/redirect/supervisor_addon/?addon=c80c7555_pocket-id) | 1.1.25 | started
[Puppet](https://my.home-assistant.io/redirect/supervisor_addon/?addon=0f1cc410_puppet) | 2.4.3 | started
[Roundcube](https://my.home-assistant.io/redirect/supervisor_addon/?addon=32b8266a_roundcube) | 1.1.1 | started
[Samba share](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_samba) | 12.5.4 | started
[Shelly Manager](https://my.home-assistant.io/redirect/supervisor_addon/?addon=26aa648f_shelly-manager) | 2024.09.26 | started
[stt-fallback](https://my.home-assistant.io/redirect/supervisor_addon/?addon=47701997_stt-fallback) | 1.0.0 | started
[Studio Code Server](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_vscode) | 6.0.1 | started
[Terminal & SSH](https://my.home-assistant.io/redirect/supervisor_addon/?addon=core_ssh) | 9.20.1 | started
[Tika-Gotenberg](https://my.home-assistant.io/redirect/supervisor_addon/?addon=ca5234a0_tika-gotenberg) | 0.1.0 | started
[Traccar](https://my.home-assistant.io/redirect/supervisor_addon/?addon=a0d7b954_traccar) | 0.25.0 | started
[VictoriaMetrics](https://my.home-assistant.io/redirect/supervisor_addon/?addon=8f49de54_victoria_metrics) | 1.130.0 | started
[⏯️ Invidious](https://my.home-assistant.io/redirect/supervisor_addon/?addon=c532faa4_invidious) | 1.0.0 | error

## Dashboards

> [!TIP]
> If you want to see how I built my dashboards other than list, go to [Dashboards](./docs/config/dashboards)

<table>
    <tr>
        <td>
            <img alt="Lovelace Dashboard" src="www/lovelace/overview.png"><br>
            Overview on Desktop
        </td>
        <td>
            <img alt="Mobile Dashboard" src="www/lovelace/mobile.png"><br>
            Overview on Mobile
        </td>
        <td>
        <img alt="Mobile Dashboard" src="www/lovelace/living-room-subview.png"><br>
        Living Room Subview as Sample
        </td>
    </tr>
    <tr>
        <td>
            <img alt="Monitoring Dashboard" src="www/lovelace/system.png"><br>
            System Dashboard
        </td>
        <td>
        <img alt="Climate Dashboard" src="www/lovelace/climate.png"><br>
        Climate Dashboard
        </td>
        <td>
            <img alt="Energy Dashboard" src="www/lovelace/energy.png"><br>
            Energy Dashboard
        </td>
    </tr>
</table>

### Lovelace Plugins

Name | Description
-- | --
[Apexcharts Card](https://github.com/RomRider/apexcharts-card) | 📈 A Lovelace card to display advanced graphs and charts based on ApexChartsJS for Home Assistant
[Auto Entities](https://github.com/thomasloven/lovelace-auto-entities) | 🔹Automatically populate the entities-list of lovelace cards
[Bha Icon Pack](https://github.com/hulkhaugen/hass-bha-icons) | Additional icons for Home Assistant to accompany the MDI icons
[Bubble Card](https://github.com/Clooos/Bubble-Card) | Bubble Card is a minimalist card collection for Home Assistant with a nice pop-up touch.
[Button Card](https://github.com/custom-cards/button-card) | ❇️ Lovelace button-card for home assistant
[Card Mod](https://github.com/thomasloven/lovelace-card-mod) | 🔹 Add CSS styles to (almost) any lovelace card
[Clock Weather Card](https://github.com/pkissling/clock-weather-card) | A Home Assistant Card indicating today's date/time, along with an iOS inspired weather forecast for the next days with animated icons
[Custom Brand Icons](https://github.com/elax46/custom-brand-icons) | Custom brand icons for Home Assistant
[Decluttering Card](https://github.com/custom-cards/decluttering-card) | 🧹 Declutter your lovelace configuration with the help of this card
[Device Card](https://github.com/homeassistant-extras/device-card) | Device Card to summarize device information in Home Assistant
[Energy Entity Row](https://github.com/zeronounours/lovelace-energy-entity-row) | Lovelace HA entity row to integrate with energy-date-selection
[Energy Flow Card Plus](https://github.com/flixlix/energy-flow-card-plus) | An upgraded Energy Distribution Card for Home Assistant, with added features like Individual Devices and refined UI enhancements, while maintaining the Energy Dashboard's original design.
[Entity Progress Card](https://github.com/francois-le-ko4la/lovelace-entity-progress-card) | Entity progress card for Home Assistant
[Expander Card](https://github.com/MelleD/lovelace-expander-card) | Expander card for HomeAssistant
[Flex Cells Card](https://github.com/michalowskil/flex-cells-card) | A Lovelace card for Home Assistant that lets you add icons, text, entities, attributes, or input controls in flexible cell layouts — fully configurable from a visual editor, so no documentation is required to get started.
[Flex Table   Highly Customizable, Data Visualization](https://github.com/custom-cards/flex-table-card) | Highly Flexible Lovelace Card - arbitrary contents/columns/rows, regex matched, perfect to show appdaemon created content and anything breaking out of the entity_id + attributes concept
[Grocy Tasks And Chores Card](https://github.com/FamousWolf/grocy-tasks-chores) | Custom Home Assistant card for displaying tasks and chores from Grocy. This card requires the custom Grocy integration to be installed in Home Assistant.
[Ha Map Card Korea Radar](https://github.com/hwajin-me/ha-map-card-korea-radar) | Integrates a Korea rain radar overlay in the Home Assistant custom map card
[Html Jinja2 Template Card](https://github.com/PiotrMachowski/Home-Assistant-Lovelace-HTML-Jinja2-Template-card) | This card displays provided Jinja2 template as an HTML content of a card. It uses exactly the same engine as Home Assistant in Developer tools.
[Hui Element](https://github.com/thomasloven/lovelace-hui-element) | 🔹 Use built-in elements in the wrong place
[Ingress Webpage Card](https://github.com/lovelylain/ha-addon-iframe-card) | HA webpage card with addon ingress support.
[Logbook Card](https://github.com/royto/logbook-card) | Logbook card for Home Assistant UI Lovelace
[Lovelace Grocy Chores Card](https://github.com/isabellaalstrom/lovelace-grocy-chores-card) | A card to track chores and tasks in Grocy.
[Lovelace Home Feed Card](https://github.com/gadgetchnnel/lovelace-home-feed-card) | A custom Lovelace card for displaying a combination of persistent notifications, calendar events, and entities in the style of a feed.
[Lovelace Weather Icons](https://github.com/scinos/lovelace-weather-icons) | Official weather icons from Home Assistant
[Map Card](https://github.com/nathan-gs/ha-map-card) | A Map Card for Home Assistant
[Maxi Media Player](https://github.com/punxaphil/maxi-media-player) | Media card for Home Assistant UI with a focus on managing multiple media players, but not excluding single player setups.
[Meal Plan Card   Lovelace Style](https://github.com/firstof9/lovelace-grocy-meal-plan-card) | Meal Plan Card for Home Assistant Grocy integration
[Mediocre Hass Media Player Cards](https://github.com/antontanderup/mediocre-hass-media-player-cards) | Media Player Cards for Homeassistant.
[Mini Graph Card](https://github.com/kalkih/mini-graph-card) | Minimalistic graph card for Home Assistant Lovelace UI
[Modern Circular Gauge](https://github.com/selvalt7/modern-circular-gauge) | Modern circular gauge card for Home Assistant
[Multiple Entity Row](https://github.com/benct/lovelace-multiple-entity-row) | Show multiple entity states and attributes on entity rows in Home Assistant's Lovelace UI
[Mushroom](https://github.com/piitaya/lovelace-mushroom) | Build a beautiful Home Assistant dashboard easily
[My Cards Bundle](https://github.com/AnthonMS/my-cards) | Bundle of my custom Lovelace cards for Home Assistant. Includes: my-slider, my-slider-v2, my-button
[Navbar Card](https://github.com/joseluis9595/lovelace-navbar-card) | Custom lovelace card that displays a bottom nav in mobile devices, and a side nav in desktop devices for easy navigation.
[Nintendo Wishlist Card](https://github.com/custom-cards/nintendo-wishlist-card) | Displays a card showing Nintendo Switch games that are on sale from your wish list.
[Paper Buttons Row](https://github.com/jcwillox/lovelace-paper-buttons-row) | Adds highly configurable buttons that use actions and per-state styling.
[Simple Swipe Card](https://github.com/nutteloost/simple-swipe-card) | A swipeable container for multiple cards with touch and mouse gesture support.
[Simple Tabs Card](https://github.com/agoberg85/home-assistant-simple-tabs) | A simple and configurable tabs card for Home Assistant Dashboards.
[Simple Weather Card](https://github.com/kalkih/simple-weather-card) | Minimalistic weather card for Home Assistant
[Stack In Card](https://github.com/custom-cards/stack-in-card) | 🛠 group multiple cards into one card without the borders
[Tabbed Card](https://github.com/kinghat/tabbed-card) | a custom card for home assistant that utilizes tabs to segregate individual cards.
[Template Entity Row](https://github.com/thomasloven/lovelace-template-entity-row) | 🔹 Display whatever you want in an entities card row.
[Timeflow Card](https://github.com/Rishi8078/TimeFlow-Card) | A beautiful countdown timer card for Home Assistant with animated progress circle and intelligent time formatting
[Todo Swipe Card](https://github.com/nutteloost/todo-swipe-card) | A specialized swipe card for todo lists in Home Assistant with custom styling
[Upcoming Media Card](https://github.com/custom-cards/upcoming-media-card) | 📺 A card to display upcoming episodes and movies from services like: Plex, Kodi, Radarr, Sonarr, and Trakt.
[Weather Card](https://github.com/bramkragten/weather-card) | Weather Card with animated icons for Home Assistant Lovelace
[Weather Chart Card](https://github.com/mlamberts78/weather-chart-card) | Custom weather card with charts.
[Week Planner Card](https://github.com/FamousWolf/week-planner-card) | Custom Home Assistant card displaying a responsive overview or multiple days with events from one of multiple calendars
[Yet Another Media Player](https://github.com/jianyu-li/yet-another-media-player) | YAMP is a Home Assistant media card for controlling multiple entities with highly customizable actions and ui elements

### Themes

Name | Description
-- | --
[Frosted Glass Theme](https://github.com/wessamlauf/homeassistant-frosted-glass-themes) | ✨ Beautiful and modern Theme for Home Assistant 
[Visionos & Ios 26 Liquid Glass Theme](https://github.com/Nezz/homeassistant-visionos-theme) | Theme inspired by visionOS for Home Assistant

## Custom Integration

Name | Description
-- | --
[<img src="https://brands.home-assistant.io/_/gas_station_korea/icon.png" height="24"/>](https://brands.home-assistant.io/_/gas_station_korea/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/gas_station_korea/icon.png" height="24"/>](https://brands.home-assistant.io/_/gas_station_korea/icon.png#gh-light-mode-only) [[Kr] Gas Station Oil Price Sensor](https://github.com/GrecHouse/gas_station_korea) | Gas station oil price sensor #HA 주유소 유가 정보 센서
[<img src="https://brands.home-assistant.io/_/kwh_to_won/icon.png" height="24"/>](https://brands.home-assistant.io/_/kwh_to_won/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/kwh_to_won/icon.png" height="24"/>](https://brands.home-assistant.io/_/kwh_to_won/icon.png#gh-light-mode-only) [[KR] 전기요금 계산 센서 (가정용)](https://github.com/dugurs/kwh_to_won) | 한국전력 전기요금 계산기 (가정용)
[<img src="https://brands.home-assistant.io/_/anniversaries/icon.png" height="24"/>](https://brands.home-assistant.io/_/anniversaries/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/anniversaries/icon.png" height="24"/>](https://brands.home-assistant.io/_/anniversaries/icon.png#gh-light-mode-only) [Anniversaries](https://github.com/pinkywafer/Anniversaries) | Anniversary Countdown Sensor for Home Assistant
[<img src="https://brands.home-assistant.io/_/city_gas_bill/icon.png" height="24"/>](https://brands.home-assistant.io/_/city_gas_bill/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/city_gas_bill/icon.png" height="24"/>](https://brands.home-assistant.io/_/city_gas_bill/icon.png#gh-light-mode-only) [City Gas Bill](https://github.com/dugurs/ha-city-gas-bill) | 도시가스요금 계산 홈어시스턴트 통합구성요소
[<img src="https://brands.home-assistant.io/_/discord_game/icon.png" height="24"/>](https://brands.home-assistant.io/_/discord_game/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/discord_game/icon.png" height="24"/>](https://brands.home-assistant.io/_/discord_game/icon.png#gh-light-mode-only) [Discord Game](https://github.com/LordBoos/discord_game) | Home Assistant custom component to get online and game status of Discord users
[<img src="https://brands.home-assistant.io/_/dyson_local/icon.png" height="24"/>](https://brands.home-assistant.io/_/dyson_local/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/dyson_local/icon.png" height="24"/>](https://brands.home-assistant.io/_/dyson_local/icon.png#gh-light-mode-only) [Dyson](https://github.com/libdyson-wg/ha-dyson) | Home Assistant custom integration for Wi-Fi connected Dyson devices
[<img src="https://brands.home-assistant.io/_/price_tracker/icon.png" height="24"/>](https://brands.home-assistant.io/_/price_tracker/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/price_tracker/icon.png" height="24"/>](https://brands.home-assistant.io/_/price_tracker/icon.png#gh-light-mode-only) [E Commerce Integrator](https://github.com/hwajin-me/hs-price-tracker) | Home Assistant - E-commerce price tracker
[<img src="https://brands.home-assistant.io/_/findmy/icon.png" height="24"/>](https://brands.home-assistant.io/_/findmy/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/findmy/icon.png" height="24"/>](https://brands.home-assistant.io/_/findmy/icon.png#gh-light-mode-only) [Findmy](https://github.com/malmeloo/hass-FindMy) | Custom Home Assistant integration for Apple's FindMy network.
[<img src="https://brands.home-assistant.io/_/readme/icon.png" height="24"/>](https://brands.home-assistant.io/_/readme/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/readme/icon.png" height="24"/>](https://brands.home-assistant.io/_/readme/icon.png#gh-light-mode-only) [Generate Readme](https://github.com/custom-components/readme) | Use Jinja and data from Home Assistant to generate your README.md file
[<img src="https://brands.home-assistant.io/_/grocy/icon.png" height="24"/>](https://brands.home-assistant.io/_/grocy/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/grocy/icon.png" height="24"/>](https://brands.home-assistant.io/_/grocy/icon.png#gh-light-mode-only) [Grocy Custom Component](https://github.com/iamkarlson/grocy) | Custom Grocy integration for Home Assistant
[<img src="https://brands.home-assistant.io/_/hacs/icon.png" height="24"/>](https://brands.home-assistant.io/_/hacs/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/hacs/icon.png" height="24"/>](https://brands.home-assistant.io/_/hacs/icon.png#gh-light-mode-only) [HACS](https://github.com/hacs/integration) | HACS gives you a powerful UI to handle downloads of all your custom needs.
[<img src="https://brands.home-assistant.io/_/korea_incubator/icon.png" height="24"/>](https://brands.home-assistant.io/_/korea_incubator/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/korea_incubator/icon.png" height="24"/>](https://brands.home-assistant.io/_/korea_incubator/icon.png#gh-light-mode-only) [Korea Component](https://github.com/hwajin-me/home-assistant-korea-components) | Home Assistant - Korea Components
[<img src="https://brands.home-assistant.io/_/life360/icon.png" height="24"/>](https://brands.home-assistant.io/_/life360/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/life360/icon.png" height="24"/>](https://brands.home-assistant.io/_/life360/icon.png#gh-light-mode-only) [Life360](https://github.com/pnbruckner/ha-life360) | A Home Assistant integration for Life360.
[<img src="https://brands.home-assistant.io/_/radarr_upcoming_media/icon.png" height="24"/>](https://brands.home-assistant.io/_/radarr_upcoming_media/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/radarr_upcoming_media/icon.png" height="24"/>](https://brands.home-assistant.io/_/radarr_upcoming_media/icon.png#gh-light-mode-only) [Radarr Upcoming Media](https://github.com/custom-components/sensor.radarr_upcoming_media) | 🎬 Radarr component to feed Upcoming Media Card.
[<img src="https://brands.home-assistant.io/_/simpleicons/icon.png" height="24"/>](https://brands.home-assistant.io/_/simpleicons/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/simpleicons/icon.png" height="24"/>](https://brands.home-assistant.io/_/simpleicons/icon.png#gh-light-mode-only) [Simpleicons](https://github.com/vigonotion/hass-simpleicons) | Use Simple Icons in Home Assistant
[<img src="https://brands.home-assistant.io/_/sonarr_upcoming_media/icon.png" height="24"/>](https://brands.home-assistant.io/_/sonarr_upcoming_media/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/sonarr_upcoming_media/icon.png" height="24"/>](https://brands.home-assistant.io/_/sonarr_upcoming_media/icon.png#gh-light-mode-only) [Sonarr Upcoming Media](https://github.com/custom-components/sensor.sonarr_upcoming_media) | 📺 Sonarr component to feed Upcoming Media Card.
[<img src="https://brands.home-assistant.io/_/spook/icon.png" height="24"/>](https://brands.home-assistant.io/_/spook/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/spook/icon.png" height="24"/>](https://brands.home-assistant.io/_/spook/icon.png#gh-light-mode-only) [Spook 👻 Your Homie](https://github.com/frenck/spook) | A scary 👻 powerful toolbox 🧰 for Home Assistant 🏡
[<img src="https://brands.home-assistant.io/_/steam_wishlist/icon.png" height="24"/>](https://brands.home-assistant.io/_/steam_wishlist/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/steam_wishlist/icon.png" height="24"/>](https://brands.home-assistant.io/_/steam_wishlist/icon.png#gh-light-mode-only) [Steam Wishlist](https://github.com/boralyl/steam-wishlist) | A home assistant integration that monitors games on sale on your Steam wishlist.
[<img src="https://brands.home-assistant.io/_/truenas/icon.png" height="24"/>](https://brands.home-assistant.io/_/truenas/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/truenas/icon.png" height="24"/>](https://brands.home-assistant.io/_/truenas/icon.png#gh-light-mode-only) [Truenas](https://github.com/tomaae/homeassistant-truenas) | TrueNAS integration for Home Assistant 
[<img src="https://brands.home-assistant.io/_/korea_bus/icon.png" height="24"/>](https://brands.home-assistant.io/_/korea_bus/dark_icon.png#gh-dark-mode-only)[<img src="https://brands.home-assistant.io/_/korea_bus/icon.png" height="24"/>](https://brands.home-assistant.io/_/korea_bus/icon.png#gh-light-mode-only) [버스(대중교통) 도착 정보](https://github.com/luiseok/ha-korea-bus-arrival) | Home Assistant custom component for South Korean bus arrival information

***

Generated by the [custom readme integration](https://github.com/custom-components/readme)

<!-- Footnotes -->

[home-assistant]: https://home-assistant.io

[saya6k]: https://lyz.kr
[docs-url]: https://saya6k.github.io/home-assistant-config

[maintenance-shield]: https://img.shields.io/maintenance/yes/2025.svg
[contributors]: https://github.com/saya6k/home-assistant-config/graphs/contributors

[kanban-board]: https://github.com/users/saya6k/projects/3
[github-url]: https://github.com/saya6k/home-assistant-config
[github-img]: https://img.shields.io/github/actions/workflow/status/saya6k/home-assistant-config/release.yml?style=flat-square
[last-commit-img]: https://img.shields.io/github/last-commit/saya6k/home-assistant-config?style=flat-square
[commit-activity-img]: https://img.shields.io/github/commit-activity/m/saya6k/home-assistant-config?style=flat-square
[license-url]: https://github.com/saya6k/home-assistant-config/blob/main/LICENSE
[license-img]: https://img.shields.io/github/license/saya6k/home-assistant-config?style=flat-square
[twitter-url]: https://twitter.com/saya6k
[twitter-img]: https://img.shields.io/twitter/follow/saya6k?label=Follow
[stars-img]: https://img.shields.io/github/stars/saya6k/home-assistant-config?style=social