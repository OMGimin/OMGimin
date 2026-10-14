<div align="center">

# 김지민

### AI를 서비스에 연결하는 Backend · Full-stack 개발자

API와 데이터, 화면을 연결하고<br>
AI 응답의 검증과 실패 복구까지 살펴봅니다.

<kbd>Java</kbd> <kbd>Spring Boot</kbd> <kbd>Python</kbd> <kbd>FastAPI</kbd> <kbd>Vue</kbd>

</div>

## Selected Projects

### 01 · 사랑과 전쟁터

**AI 변론·공방·최종 의견을 제공하는 실시간 웹 서비스**

SKALA 팀 프로젝트를 기반으로 개인 저장소에서 LangChain/OpenAI 생성 기능을 확장했습니다.

- Spring → FastAPI → LangChain/OpenAI로 이어지는 AI 생성 흐름
- 구조화 응답 검증, WebSocket/STOMP 이벤트, PostgreSQL 저장
- 생성 실패 시 진행 중지와 명시적 재시도, 저장된 상태를 이용한 화면 복구

`Java` `Spring Boot` `Python` `FastAPI` `LangChain` `Vue` `PostgreSQL`

[Repository](https://github.com/OMGimin/mini-web-project) · [AI 연결 구조](https://github.com/OMGimin/mini-web-project/blob/main/docs/langchain-integration.md) · [검증 기록](https://github.com/OMGimin/mini-web-project/blob/main/docs/langchain-verification.md)

재시도 후 늦게 도착한 이전 응답이 새 결과를 덮어쓰지 않도록 요청 ID·단계·상태를 검사합니다.
[핵심 구현](https://github.com/OMGimin/mini-web-project/blob/6f7b762edd55e2a29978499faae90c85ce0cac2d/backend/src/main/java/com/skala/team6/webmini/trial/TrialGenerationService.java#L233-L246) · [테스트](https://github.com/OMGimin/mini-web-project/blob/6f7b762edd55e2a29978499faae90c85ce0cac2d/backend/src/test/java/com/skala/team6/webmini/trial/TrialGenerationRecoveryAcceptanceTest.java#L66-L119)

### 02 · LinguaRoute

**기업 외국어교육 MSA의 AI 추천 서비스와 통합**

FastAPI 기반 추천 서비스와 서비스 간 통합을 담당했습니다.

- 내부 API로 사용자 권한·수강 이력·활성 강의 후보 조회
- OpenAI 추천 결과의 강의 ID·중복·언어를 서버에서 재검증
- AI 장애 시 규칙 기반 fallback, MariaDB 저장과 Vue 화면 연결

`Python` `FastAPI` `OpenAI` `REST API` `MariaDB` `Vue`

[Repository · 실제 구현(dev)](https://github.com/OMGimin/linguaroute-msa-project/tree/dev) · [담당 기능과 기술 선택](https://github.com/OMGimin/linguaroute-msa-project/blob/main/docs/learning-notes/ai-recommendation-development-retrospective.md) · [통합 검증 기록](https://github.com/OMGimin/linguaroute-msa-project/blob/dev/docs/mvp-verification.md)

공개 dev 구현에서 추천 후보의 ID·중복·언어를 검증하고, AI 호출 실패 시 규칙 기반 추천으로 전환합니다.
[핵심 구현](https://github.com/OMGimin/linguaroute-msa-project/blob/694d828acc362fe604a18643f29d75bb28f8eb0b/recommend-service/app/service/recommend_service.py#L48-L129) · [테스트](https://github.com/OMGimin/linguaroute-msa-project/blob/694d828acc362fe604a18643f29d75bb28f8eb0b/recommend-service/tests/test_recommendation_service.py#L37-L93)

## AI-native Development

[**Codex Agent Playbook**](https://github.com/OMGimin/codex-agent-playbook)에는 AI 도구를 활용하면서 정리한 개인 개발 워크플로와 스킬을 모았습니다. 작업 분담, 검토, 완료 근거를 명확히 하는 데 초점을 두었습니다.

## Tech I Work With

| Area | Technologies |
| :--- | :--- |
| Backend | Java · Spring Boot · Python · FastAPI |
| Frontend | Vue · JavaScript · TypeScript |
| Data & Integration | PostgreSQL · MariaDB · REST API · WebSocket/STOMP |
| AI & Tools | OpenAI · LangChain · Docker Compose · Git |

<sub>프로젝트별 구현 범위, 실행 기록과 남은 한계는 각 저장소 문서에 정리했습니다.</sub>
