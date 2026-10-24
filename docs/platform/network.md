---
title: 네트워크
---

# 네트워크

## 라우팅 및 무선

로컬 사이트 ↔ 원격 TrueNAS 사이트가 사이트-투-사이트 VPN 으로 묶여 있습니다. 하드웨어 상세는 [하드웨어 → Network Devices](../hardware.md#network-devices) 참조.

### 로컬 사이트

| 장비                | 역할                       |
| ------------------- | -------------------------- |
| UniFi Gateway Fiber | 메인 라우터 (광 회선 종단) |
| UniFi US-8-60W      | 백본 스위치 (PoE)          |
| UniFi UAP-AC-Lite   | Wi-Fi AP                   |

### 원격 사이트 (TrueNAS 가 있는 곳)

| 장비                      | 역할                                          |
| ------------------------- | --------------------------------------------- |
| UniFi NextGen Gateway Pro | 원격 사이트 라우터, 로컬과 site-to-site VPN   |
| UniFi CloudKey 2 Plus     | 컨트롤러 (로컬 호스팅, 모든 사이트 통합 관리) |

Home Assistant 측은 [UniFi Network 통합](https://www.home-assistant.io/integrations/unifi/)으로 장치/클라이언트/포트 상태를 수집합니다.

## DNS / 광고 차단

- **AdGuard Home 애드온** — 내부 DNS 리졸버. 클라이언트별 필터링 적용.

## 외부 노출

- **NGINX Home Assistant SSL Proxy** 애드온이 80/443 종단을 담당
- **Let's Encrypt** 애드온이 ACME 챌린지 처리. 인증서 만료 임박 시 자동화 `Let's Encrypt 자동 시작`이 트리거 (참고: [자동화](../automations.md))
- `configuration.yaml`의 `http:` 블록은 `cors_allowed_origins`, `trusted_proxies`, `ip_ban_enabled`, `login_attempts_threshold` 를 모두 `secrets.yaml` 기반으로 설정

## 인증

- Home Assistant 기본 인증
- 실험적: [`hass-oidc-auth`](https://github.com/christiaangoossens/hass-oidc-auth) CI에서 빌드 검증, **원격 TrueNAS 의 [Pocket ID](../services/pocket-id.md)** 와 OIDC 페어링 계획 (현재 `configuration.yaml`에는 주석 상태)

## 침입 차단

HA `http.ip_ban_enabled` + `login_attempts_threshold` 가 기본 방어선입니다. 외부 IPS는 현재 미운영 (이전 CrowdSec 구성은 [보관소](../retired.md) 참조).
