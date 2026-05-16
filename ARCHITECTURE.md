# AETERNA 시스템 아키텍처

## 1. 개요
AETERNA는 초거대 지식 베이스(Second Brain)와 멀티 에이전트 시스템이 결합된 자율형 비즈니스 자동화 플랫폼입니다.

## 2. 핵심 구성 요소
- **CEO Agent**: 전체 워크플로우 제어 및 에이전트 태스크 분배.
- **Researcher Agent**: 외부 데이터 수집 및 지식 정제.
- **Knowledge Base (10_Wiki)**: 800개 이상의 고품질 비즈니스 인사이트 저장소.
- **Payment Infrastructure**: PayPal 기반의 자동 결제 및 정산 모듈.

## 3. 데이터 흐름
1. 사용자의 자연어 입력 수신.
2. CEO 에이전트가 의도 분석 및 하위 태스크 생성.
3. Researcher가 필요 지식 검색 및 생성.
4. 모든 결정 사항은 `.agent/` 내에 기록되어 맥락 유지.
5. 결과물은 Markdown 형식으로 `10_Wiki`에 저장.

## 4. 인프라 패치 (Vibe Healing)
- **Connect AI Extension**: `extension.js`를 직접 패치하여 `num_predict: -1` 오류를 해결하고 타임아웃을 600초로 연장함.
