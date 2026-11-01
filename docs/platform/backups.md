---
title: 백업
---

# 백업

> 로컬은 stateless 운영이라, **HA 설정 + Recorder DB** 가 복구의 핵심입니다. HA 기본 백업이 매일 아래 3개 보관처에 동시에 저장합니다.

## 보관처

| #   | 위치            | 백업 에이전트           | 비고                                          |
| --- | --------------- | ----------------------- | --------------------------------------------- |
| 1   | 로컬 HA 호스트  | `hassio.local`          | `/backup`                                     |
| 2   | 원격 TrueNAS    | `hassio.TrueNAS_Backup` | Supervisor 네트워크 스토리지 마운트, VPN 너머 |
| 3   | Nabu Casa Cloud | `cloud.cloud`           | 오프사이트 안전망                             |

- **일정**: 매일 자동 백업
- **보존**: 최근 3개

Recorder DB 는 원격 TrueNAS 의 MariaDB 에 있으므로 HA 백업과 별개로 TrueNAS 쪽에서 보호됩니다.

이전엔 Google Drive 통합으로 백업 사본을 올렸으나 더 이상 사용하지 않습니다. ([retired](../retired.md) 참조)

## 사용 통합

- [Backup](https://www.home-assistant.io/integrations/backup/) — HA 기본 백업
- [Home Assistant Cloud (Nabu Casa)](https://www.home-assistant.io/cloud/) — 클라우드 백업 대상

## 복구 순서 (재구성 시)

1. **HAOS 새로 설치** — Raspberry Pi 5 (또는 다른 지원 보드)
2. **Nabu Casa Cloud 백업** 복원, 또는 **TrueNAS** 의 백업 다운로드 후 복원
3. `secrets.yaml` 의 외부 비밀번호/토큰 갱신 필요 여부 확인:
   - 원격 MariaDB 접속 자격증명
   - VPN 연결 상태
   - Nabu Casa, GitHub PAT, LLM API 키
4. 원격 TrueNAS의 **MariaDB Recorder DB** 가 살아있는지 확인 — 정상이면 HA 가 자동으로 다시 연결
5. Supervisor 의 `TrueNAS_Backup` 네트워크 스토리지가 다시 마운트되는지 확인

## 권장 점검

- 매 분기 1회 복구 리허설 (테스트 인스턴스에 복원만 시도)
- ZFS snapshot 보존 기간 확인
- Nabu Casa 가입 만료 임박 알림 (자동화로 처리 가능)
