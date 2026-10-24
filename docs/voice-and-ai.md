---
title: 음성과 AI
---

# 음성과 AI

음성 입력을 받아 LLM에 라우팅하고, TTS로 응답하는 전체 파이프라인입니다.

## 데이터 흐름

```
[ Voice PE / 모바일 ]
        │ Wyoming
        ▼
   ┌────────────┐
   │   Whisper  │  (STT)
   └─────┬──────┘
         │ 텍스트
         ▼
   ┌──────────────┐
   │  Conversation│  ← LLM 선택: Anthropic / OpenAI / Gemini / Open Router / Ollama (LLM Conversation Agent)
   │   Pipeline   │  ← LLM Tools: voice_satellite_llm_tools (날씨·이미지·YouTube)
   └─────┬────────┘
         │ 텍스트 + 액션
         ▼
   ┌────────────────┐
   │ Supertonic-MNN │  (TTS, MNN 추론 엔진)
   └─────┬──────────┘
         │ 오디오
         ▼
  스피커(Voice PE / Edifier MR5 / JBL Flip 4)
```

## 입력 디바이스

- **Home Assistant Voice Preview Edition** × 2 — Wi-Fi, ESPHome 펌웨어
- **Voice Satellite 커스텀 컴포넌트** — 태블릿/폰/브라우저를 위성으로 사용

## STT / 추론

- **Whisper** (HA Wyoming 표준) — CPU 추론

## 대화 에이전트

- **Anthropic Conversation** — Claude
- **OpenAI Conversation** — GPT
- **Google Generative AI** — Gemini (`gemini-2.0-flash` 등)
- **Open Router** — 라우팅 백업
- **LLM Conversation Agent** 애드온 — 로컬 Ollama 라우팅
- **OpenAI-to-Ollama Bridge** 애드온 — OpenAI API 호출을 Ollama로 변환

> [!TIP]
> 어떤 어시스턴트가 어떤 대화 에이전트를 쓰는지는 `.storage/assist_pipeline.pipelines`에 정의됩니다.

## LLM 도구 / 액션 확장

- **`voice_satellite_llm_tools`** 커스텀 컴포넌트가 다음 도구를 제공:
  - 날씨/예보 검색
  - 금융 시세
  - 이미지 검색
  - YouTube 비디오 검색 + 화면 표시
- **MCP / MCP Server** 통합 — Model Context Protocol 기반 외부 도구 연동
- **HASS MCP Proxy** 애드온 — MCP 호출 라우팅
- **Voice Match** 애드온 — 화자 식별

## TTS

| 엔진                 | 용도                                      |
| -------------------- | ----------------------------------------- |
| Supertonic-MNN       | 메인 — Alibaba MNN 추론 엔진 기반, 저지연 |
| Google Translate TTS | 폴백 / 다국어                             |

TTS 캐시는 `tts/` 디렉터리에 저장되고, 자동화 **TTS 캐시 지우기** 가 매일 오전 1시에 비웁니다. 이전에 사용하던 Piper는 [보관소](./retired.md) 참조.

## 자동화 연계

음성 입력으로 트리거되거나 LLM이 호출하는 주요 자동화 — 자세한 목록은 [자동화](./automations.md):

- 귀가 시 환영 및 보조 기능 활성화
- 야간 화장실 이용간 조명 제어
- 커피 머신 추출 완료 알림
- 침실 6버튼 스마트 스위치 제어
- 응급 상황 알림 / 재난 안내
