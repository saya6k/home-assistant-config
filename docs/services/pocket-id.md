---
title: Pocket ID
---

# Pocket ID

[Pocket ID](https://pocket-id.org) — 패스키(passkey) 기반의 가벼운 OIDC provider.

## 운영 위치

**원격 TrueNAS** (사이트-투-사이트 VPN 너머). 로컬 HA 의 OIDC 연동은 [`hass-oidc-auth`](https://github.com/christiaangoossens/hass-oidc-auth) 통해 원격 Pocket ID 인스턴스를 가리킵니다 — `configuration.yaml` 의 OIDC discovery URL 은 현재 주석 처리 상태.

이전엔 HA 애드온으로 운영했지만 로컬을 stateless 로 정리하면서 옮겼습니다.
