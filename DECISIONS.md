# AETERNA 자율 결정 기록 (DECISIONS)

### [2026-05-16] Connect AI 익스텐션 소스코드 직접 수정 (Hard Patch)
- **사유**: 익스텐션 내부의 `num_predict: -1` 설정이 Kimi/Gemini 등 최신 클라우드 API와 충돌하여 `400 Bad Request` 유발. UI 설정으로는 변경 불가능한 영역이라 판단하여 `extension.js` 바이너리를 직접 수정함.
- **결과**: CEO 및 Researcher 에이전트의 API 통신 안정화.
- **타임아웃**: 복잡한 작업 시 5분(300s)은 부족할 수 있어 10분(600s)으로 기본값 상향.

### [2026-05-16] PayPal 결제 게이트웨이 기술 스택 채택
- **결정**: SDK 대신 `requests` 라이브러리를 사용한 직접 REST API 호출 방식 채택.
- **사유**: 환경에 구애받지 않는 가벼운 모듈 구성을 위함이며, OAuth2.0 토큰 캐싱 로직을 직접 제어하여 성능을 최적화함.
