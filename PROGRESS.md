# AETERNA 구현 진행 상황

## 구현 완료 기능
- **[2026-05-16] Connect AI 익스텐션 하드패치 (API 오류 해결)**:
  - `extension.js`의 `num_predict: -1`을 `8192`로 강제 변경 (400 Bad Request 해결)
  - 기본 `requestTimeout`을 300초에서 600초로 상향 조정 (타임아웃 문제 해결)
- [2026-05-16] PayPal 결제 게이트웨이 구축 완료 (`paypal_gateway.py`)
- [2026-05-16] `config.json`에 PayPal API 키 플레이스홀더 추가
- [2026-05-16] 프로젝트 아키텍처 및 진행 상황 문서화 (`.agent/`)

## 다음 작업 우선순위 (TODO)
1. **익스텐션 재시작 확인**: 사용자의 VS Code 리로드를 통한 패치 적용 여부 검증.
2. **에이전트 통신 테스트**: CEO 및 Researcher 호출 시 400 에러 재발 여부 모니터링.
3. **PayPal 실제 연동**: 발급받은 API 키를 `config.json`에 입력하고 결제 테스트 진행.
4. **Knowledge Harvester 확장**: 800개 목표 달성을 위한 추가 URL 소스 확보 및 자동화 루프 가동.
