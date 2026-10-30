---
title: 음성과 AI
---

# 음성과 AI

음성 입력을 받아 LLM에 라우팅하고, TTS로 응답하는 전체 파이프라인입니다.

## 데이터 흐름

```
[ Voice PE / Echo Show / 거울 / 모바일 ]
        │ Assist satellite
        ▼
   ┌──────────────────────┐
   │ Home Assistant Cloud │  (STT)
   └─────┬────────────────┘
         │ 텍스트
         ▼
   ┌──────────────┐
   │  Conversation│  ← 기본 파이프라인: OpenAI · 그 외 Anthropic / Gemini / OpenRouter / llama.cpp
   │   Pipeline   │  ← LLM 도구: 스크립트 · MCP 서버
   └─────┬────────┘
         │ 텍스트 + 액션
         ▼
   ┌────────────────┐
   │   Supertonic   │  (TTS, Wyoming)
   └─────┬──────────┘
         │ 오디오
         ▼
  위성 디바이스 스피커
```

## Assist 파이프라인

`.storage/assist_pipeline.pipelines` 에 정의되며, 모두 한국어(`ko`)입니다.

| 파이프라인                 | 대화 에이전트                | STT                  | TTS                  |
| -------------------------- | ---------------------------- | -------------------- | -------------------- |
| **Voice Assistant** (기본) | OpenAI                       | Home Assistant Cloud | Supertonic           |
| Home Assistant Cloud       | Home Assistant (내장 인텐트) | Home Assistant Cloud | Home Assistant Cloud |
| Deep Research              | Home Assistant (내장 인텐트) | —                    | —                    |
| Test                       | llama.cpp (로컬 Gemma 모델)  | Home Assistant Cloud | Supertonic           |

## 입력 디바이스

- **Home Assistant Voice Preview Edition** — Wi-Fi, ESPHome 펌웨어
- **Echo Show 5 / Echo Show 8 (1세대)** — TECHO5 커스텀 펌웨어로 HA 에 ESPHome 디바이스로 연결, 위성 2개씩 노출
- **YUPP 스마트 거울** — 같은 방식의 ESPHome 디바이스
- **모바일 앱** — iPhone, MacBook

## 대화 에이전트

- **OpenAI** — 기본 파이프라인
- **Anthropic** — Claude
- **Google Gemini**
- **OpenRouter**
- **llama.cpp** — OpenAI 호환 엔드포인트 2개 (자가 호스팅 서버, DeepSeek API)

## LLM 도구 / 액션 확장

- **LLM 도구 스크립트** (`scripts.yaml`) — 대화 에이전트에 노출되는 스크립트
  - 블루프린트 기반: `music-assistant/llm_voice_script.yaml`, `saya6k/mealie_llm_tool.yaml`, `saya6k/jellyfin_apple_tv_llm_tool.yaml`, `saya6k/youtube_apple_tv_llm_tool.yaml`, `saya6k/apple_tv_apps_llm_tool.yaml`
  - 직접 작성: Entity History, Entity Attributes, 카메라 분석, 집 상태 보고서, 메시지 방송, 에어컨 제어 등
- **MCP Client** (`mcp`) — 외부 MCP 서버를 도구로 연결: CRW Web Tools, Memory, ESPHome Device Builder, multi-service-mcp
- **MCP Server** (`mcp_server`) — HA 와 일부 커스텀 통합(Chzzk, Wardrowbe, xBloom, 한국 공공데이터 등)을 MCP 로 노출
- **AI Task** — 자동화에서 이미지 생성 등에 사용 (예: `날씨 이미지 시각화 생성 및 업데이트`)

## TTS

| 엔진                 | 용도                                  |
| -------------------- | ------------------------------------- |
| Supertonic           | 메인 — 로컬 애드온, Wyoming 으로 연결 |
| Home Assistant Cloud | Cloud 파이프라인용                    |
| ElevenLabs           | 보조                                  |
| Google Translate TTS | 폴백 / 다국어                         |

TTS 캐시는 `tts/` 디렉터리에 저장되고, 자동화 **TTS 캐시 지우기** 가 매주 월요일 오전 1시에 비웁니다. Whisper 애드온은 설치되어 있지만 정지 상태입니다(STT 는 Cloud 사용). 이전에 사용하던 Piper, Ollama, Voice Satellite 는 [보관소](./retired.md) 참조.

## 자동화 연계

음성 입력으로 트리거되거나 LLM이 호출하는 주요 자동화 — 자세한 목록은 [자동화](./automations.md):

- 귀가 시 환영 및 보조 기능 활성화
- 야간 화장실 이용간 조명 제어
- 커피 머신 오류 알림 (종합)
- 침실 6버튼 스마트 스위치 제어
- 긴급 상황 알림: 재난별 지침 전송
