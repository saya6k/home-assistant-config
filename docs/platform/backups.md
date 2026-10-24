---
title: 백업
---

# 백업

> 로컬은 stateless 운영이라, **HA 설정 + Recorder DB** 가 복구의 핵심입니다. 다음 5개 보관처에 분산 저장합니다.

## 보관처 (3 로컬 + 1 원격 + 1 클라우드)

| #   | 위치            | 종류                       | 비고                                  |
| --- | --------------- | -------------------------- | ------------------------------------- |
| 1   | 로컬 HA 호스트  | HA 기본 백업               | `/backup`                             |
| 2   | 로컬 호스트 #2  | HA 백업 사본               | rotational 보관                       |
| 3   | 로컬 호스트 #3  | HA 백업 사본               | rotational 보관                       |
| 4   | 원격 TrueNAS    | HA 백업 + Recorder DB 덤프 | VPN 너머. ZFS snapshot 으로 추가 보호 |
| 5   | Nabu Casa Cloud | HA 백업                    | 오프사이트 안전망                     |

이전엔 Google Drive 통합으로 백업 사본을 올렸으나 더 이상 사용하지 않습니다. ([retired](../retired.md) 참조)

## 사용 통합

- [Backup](https://www.home-assistant.io/integrations/backup/) — HA 기본 백업
- [Home Assistant Cloud (Nabu Casa)](https://www.home-assistant.io/cloud/) — 클라우드 백업 대상

## 자동화

- **자동 백업 완료 후 HA 코어 자동 업데이트** — 백업 성공 이벤트를 받아 코어 업데이트를 트리거. `automations.yaml` 참조.

## 복구 순서 (재구성 시)

1. **HAOS 새로 설치** — 베어메탈 또는 가상 머신
2. **Nabu Casa Cloud 백업** 복원 (가장 최근 보관처) 또는 **TrueNAS** 의 백업 다운로드 후 복원
3. `secrets.yaml` 의 외부 비밀번호/토큰 갱신 필요 여부 확인:
   - 원격 MariaDB 접속 자격증명
   - VPN 연결 상태
   - Nabu Casa, GitHub PAT, HACS, LLM API 키
4. 원격 TrueNAS의 **MariaDB Recorder DB** 가 살아있는지 확인 — 정상이면 HA 가 자동으로 다시 연결
5. otelcol sidecar 가 원격 gateway에 연결되어 메트릭/로그 흐름 회복 확인

## 권장 점검

- 매 분기 1회 복구 리허설 (테스트 인스턴스에 복원만 시도)
- ZFS snapshot 보존 기간 확인
- Nabu Casa 가입 만료 임박 알림 (자동화로 처리 가능)
