---
title: Pocket ID
---

# Pocket ID

[Pocket ID](https://pocket-id.org) — 패스키(passkey) 기반의 가벼운 OIDC provider.

## 운영 위치

**원격 TrueNAS** (사이트-투-사이트 VPN 너머). [`hass-oidc-auth`](https://github.com/christiaangoossens/hass-oidc-auth) 로 HA 로그인을 Pocket ID 에 연동하는 구성은 현재 `configuration.yaml` 에 없습니다 — HA 는 기본 인증만 사용합니다.

이전엔 HA 애드온으로 운영했지만 로컬을 stateless 로 정리하면서 옮겼습니다.
