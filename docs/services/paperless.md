---
title: Paperless-ngx
---

# Paperless-ngx

[Paperless-ngx](https://docs.paperless-ngx.com) — 문서 스캔/인덱스/아카이브를 다루는 커뮤니티 기반 문서 관리 시스템.

## 운영 위치

**원격 TrueNAS** (사이트-투-사이트 VPN 너머). 로컬 HA는 [`paperless_ngx` HA 통합](https://www.home-assistant.io/integrations/paperless_ngx/) 으로 원격 인스턴스의 API 를 호출합니다 — URL/토큰은 `secrets.yaml` 에 저장.

이전엔 HA 애드온으로 운영했지만 로컬을 stateless 로 정리하면서 옮겼습니다.
