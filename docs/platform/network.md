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

- **AdGuard Home** — 내부 DNS 리졸버. HA 애드온이 아니라 원격 호스트에서 운영하며, HA 는 [AdGuard Home 통합](https://www.home-assistant.io/integrations/adguard/)으로 통계와 필터 스위치만 가져옵니다.
- **Cloudflare 통합** — 외부 도메인의 DNS 레코드를 현재 공인 IP 로 갱신.

## 외부 노출

- **NGINX Home Assistant SSL Proxy** 애드온이 80/443 종단을 담당
- **Let's Encrypt** 애드온이 ACME 챌린지 처리. 평소엔 정지 상태이고, 인증서가 유효하지 않으면 자동화 `인증서 만료시 재발급`이 애드온을 시작 (참고: [자동화](../automations.md))
- Certificate Expiry 통합이 외부 도메인 인증서의 만료일을 감시
- `configuration.yaml` 에는 `http:` 블록이 없습니다 — HA 기본값으로 동작

## 인증

- Home Assistant 기본 인증 (`auth_providers: homeassistant` 만 사용)
- [`hass-oidc-auth`](https://github.com/christiaangoossens/hass-oidc-auth) 로 원격 [Pocket ID](../services/pocket-id.md) 와 OIDC 연동하는 방안은 현재 설정에 없습니다

## 침입 차단

`http:` 블록이 없어 HA 기본값으로 동작합니다 — `ip_ban_enabled` 는 켜져 있지만 `login_attempts_threshold` 가 설정되지 않아 로그인 실패로 IP 가 자동 차단되지는 않습니다. 외부 IPS는 현재 미운영 (이전 CrowdSec 구성은 [보관소](../retired.md) 참조).
