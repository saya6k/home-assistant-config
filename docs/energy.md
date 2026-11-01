---
title: 에너지
---

# 에너지

전기·가스·수도 사용량을 추적하고, 한국식 청구서 시뮬레이션을 제공하는 구성입니다.

## 통합

| 통합                         | 출처                      | 측정                                                                   |
| ---------------------------- | ------------------------- | ---------------------------------------------------------------------- |
| 한전 (KEPCO)                 | `kr_public_data` (커스텀) | 전기 사용량, 요금 추정                                                 |
| Shelly                       | 기본 통합 (+ Matter)      | Shelly EM Mini Gen4 ×2, Shelly Power Strip 4 Gen4 — 회로·콘센트별 전력 |
| 유가정보                     | `kr_public_data` (커스텀) | 주변 주유소 유가                                                       |
| Electricity Maps (co2signal) | 기본 통합                 | 전력망의 탄소 강도                                                     |

## 가스 · 수도

가스와 수도는 UI 에서 만든 헬퍼로 집계합니다.

| 헬퍼          | 엔티티                                                                                  |
| ------------- | --------------------------------------------------------------------------------------- |
| Template      | `Utility Total Gas/Water`, `Utility Last Day Gas/Water`, `Utility Last Month Gas/Water` |
| Utility Meter | `Utility This Day Gas/Water`, `Utility This Month Gas/Water`                            |

## 데이터 저장

[스토리지](./platform/storage.md) (Recorder / 원격 MariaDB) 의 장기 통계(long-term statistics)로 보관합니다.

## 대시보드

HA 기본 Energy 대시보드에는 현재 **가스·수도** 소스만 등록되어 있습니다 (전력망·개별 기기 소비는 미등록). 스크린샷은 [대시보드](./dashboards.md) 페이지에 있습니다.

## 관련 자동화

- **창문 열림 시 공조 자동 제어 (열림)** / **창문 닫힘 시 공조 자동 제어 (닫힘)**
- **화장실 습도 50% 미만일 때 제습기 끄기** / **화장실 습도 70% 초과 시 제습기 켜기**
- **건조대 열림 시 제습기 빨래건조 모드**
- **고농도 이산화탄소 환기 알림**

## 정리 권장

- 월별 청구서와 자동 비교 (외부 가계부 서비스로 export)
- 누진세 임계 진입 시 알림
- ESS / 태양광 도입 시 export 메트릭 추가
