---
title: 서비스
---

# 서비스

자가 호스팅 서비스. **로컬 HA가 stateless 로 운영**되면서, 보조 서비스들도 모두 **원격 TrueNAS** 에 옮겨졌습니다. 로컬 HA 는 IMAP·OIDC·API 등 클라이언트로만 연결합니다.

| 서비스                          | 위치         | 용도                            |
| ------------------------------- | ------------ | ------------------------------- |
| [Paperless-ngx](./paperless.md) | 원격 TrueNAS | 문서 디지털화 / OCR             |
| [Pocket ID](./pocket-id.md)     | 원격 TrueNAS | OIDC 인증 공급자 (passkey 기반) |

## HA 통합과의 연계

| 서비스        | HA 통합                                                                                          |
| ------------- | ------------------------------------------------------------------------------------------------ |
| Paperless-ngx | [`paperless_ngx`](https://www.home-assistant.io/integrations/paperless_ngx/) — 원격 URL 로 연결  |
| Pocket ID     | 현재 연동 없음 ([`hass-oidc-auth`](https://github.com/christiaangoossens/hass-oidc-auth) 미사용) |

그 밖에 Jellyfin, Plex, Immich, Mealie, Traccar, Transmission, AdGuard Home 도 HA 밖에서 운영하며 각 HA 통합으로만 연결합니다.

> [!NOTE]
> 이전에 운영했던 Grocy, Firefly III, 자체 메일 서버는 [보관소](../retired.md)에 정리되어 있습니다.
