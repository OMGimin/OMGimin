<div align="center">

# 김지민

### Backend · Full-stack Developer

목적에 맞는 AI 기술을 선택하고,<br>
API와 데이터를 연결해 서비스로 구현합니다.

[Projects](#selected-projects) · [Tech Stack](#tech-stack) · [Development Notes](https://github.com/OMGimin/codex-agent-playbook)

</div>

## About

AI 기능이 실제 서비스에서 쓰일 수 있도록 API, 데이터 저장, 사용자 화면을 연결합니다.
응답이 잘못되거나 요청이 실패했을 때의 처리까지 살피고, 직접 사용하며 발견한 불편을 개선합니다.

## Selected Projects

### 01 · 사랑과 전쟁터

연인 간 갈등을 양측의 입장과 AI 변론·공방·최종 의견으로 돌아보는 웹 서비스입니다.

**역할 · 팀 프로젝트 참여 및 후속 AI 연동·복구 흐름 개발**

- 기존 Spring 서비스에 FastAPI·LangChain/OpenAI를 연결해 실제 AI 응답 생성 기능을 확장했습니다.
- 구조화 응답 검증과 실패 재시도를 보완하고, 저장된 상태를 바탕으로 진행 화면을 복구하도록 구성했습니다.

`Java` `Spring Boot` `Python` `FastAPI` `LangChain` `Vue` `PostgreSQL`

[Repository](https://github.com/OMGimin/mini-web-project)

<details>
<summary>구현과 검증 기록</summary>

[AI 연결 구조](https://github.com/OMGimin/mini-web-project/blob/main/docs/langchain-integration.md) · [검증 기록](https://github.com/OMGimin/mini-web-project/blob/main/docs/langchain-verification.md)

재시도 후 늦게 도착한 이전 응답이 새 결과를 덮어쓰지 않도록 요청 ID·단계·상태를 검사합니다.
[핵심 구현](https://github.com/OMGimin/mini-web-project/blob/6f7b762edd55e2a29978499faae90c85ce0cac2d/backend/src/main/java/com/skala/team6/webmini/trial/TrialGenerationService.java#L233-L246) · [테스트](https://github.com/OMGimin/mini-web-project/blob/6f7b762edd55e2a29978499faae90c85ce0cac2d/backend/src/test/java/com/skala/team6/webmini/trial/TrialGenerationRecoveryAcceptanceTest.java#L66-L119)

</details>

### 02 · LinguaRoute

사용자의 학습 조건과 수강 이력을 바탕으로 강의를 추천하는 기업 외국어교육 플랫폼입니다.

**역할 · AI 추천 서비스 개발 및 API·DB·화면 통합**

- 내부 API에서 조회한 실제 강의 후보를 기준으로 OpenAI 추천 결과의 ID·중복·언어를 검증했습니다.
- AI 호출 실패 시 규칙 기반 추천으로 전환하고, MariaDB 저장과 Vue 결과 화면까지 연결했습니다.

`Python` `FastAPI` `OpenAI` `REST API` `MariaDB` `Vue`

[Repository](https://github.com/OMGimin/linguaroute-msa-project)

<details>
<summary>구현과 검증 기록</summary>

[담당 기능과 기술 선택](https://github.com/OMGimin/linguaroute-msa-project/blob/main/docs/learning-notes/ai-recommendation-development-retrospective.md) · [통합 검증 기록](https://github.com/OMGimin/linguaroute-msa-project/blob/dev/docs/mvp-verification.md)

[핵심 구현](https://github.com/OMGimin/linguaroute-msa-project/blob/ced08531764c2a38947a270ae38066ab6cf37030/recommend-service/app/service/recommend_service.py#L48-L129) · [테스트](https://github.com/OMGimin/linguaroute-msa-project/blob/ced08531764c2a38947a270ae38066ab6cf37030/recommend-service/tests/test_recommendation_service.py#L37-L93)

</details>

### 03 · 설정공방 LoreForge

키워드로 세계관을 만들고, 기존 원고의 설정 충돌을 근거 문단과 함께 살펴보는 창작 웹 서비스입니다.

**역할 · 서비스 기획·개발 및 사용 흐름 개선**

- 긴 원고를 매번 다시 읽는 불편을 줄이기 위해 생성과 검토를 분리하고, 쟁점·근거를 먼저 확인하는 흐름으로 구성했습니다.
- 원문에 이미 설명된 내용을 누락으로 지적하는 문제를 발견해 반대 근거 대조를 보완하고, 관계 그래프의 탐색과 가독성을 개선했습니다.

`Python` `FastAPI` `LangGraph` `Vue` `TypeScript` `SQLite`

[Repository](https://github.com/OMGimin/loreforge)

<details>
<summary>구현과 검증 기록</summary>

[구현 결과와 남은 한계](https://github.com/OMGimin/loreforge/blob/main/docs/RESULTS.md)

채택한 문서만 이어쓰기 기준으로 사용하며, 원문 검토에서는 창작·자동 수정을 실행하지 않습니다.
근거 문단이 존재해도 판단이 틀릴 수 있어 오탐 사례와 기능 검사 결과를 구분해 기록합니다.

</details>

## Tech Stack

프로젝트에서 반복해서 활용한 기술을 중심으로 정리했습니다.

| 분야 | 기술 |
| :--- | :--- |
| Backend | <kbd>Python</kbd> <kbd>FastAPI</kbd> <kbd>Java</kbd> <kbd>Spring Boot</kbd> |
| Frontend | <kbd>JavaScript</kbd> <kbd>Vue</kbd> |
| Database | <kbd>MariaDB</kbd> <kbd>PostgreSQL</kbd> |
| AI / Tools | <kbd>OpenAI API</kbd> <kbd>LangChain</kbd> <kbd>Docker Compose</kbd> <kbd>Git</kbd> |

## Experience & Education

| 기간 | 경험 |
| :--- | :--- |
| 2026.07–현재 | **SKALA · SK AI Leader Academy** — AI·데이터·웹 서비스 개발 교육 및 프로젝트 |
| 2025.07 | **으뜸정보기술 인턴** — SaaS·클라우드 교육 교재 3건 공동 개발 참여 |
| 2024.06–2024.08 | **Google Cloud AI 기반 인재양성 프로그램** — Mindrawing 프로젝트, 최우수 AI 혁신상 팀 수상(2024.09, Google AI 융합혁신기술 전국대회) |
| 2020.03–2026.02 | **조선대학교 컴퓨터공학전공** — 공학사 |

## Currently Exploring

- LLM 기능을 API·데이터·사용자 화면으로 연결하는 서비스 개발
- 잘못된 응답과 실패 상황을 재현하고 개선하는 검증 방식
- 작업·검토·완료 기준을 정리한 개발 워크플로 — [Codex Agent Playbook](https://github.com/OMGimin/codex-agent-playbook)

<sub>프로젝트별 구현 범위, 실행 기록과 남은 한계는 각 저장소 문서에 정리했습니다.</sub>
