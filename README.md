<a href="https://kjsoo-portfolio.vercel.app/">
  <img width="700" height="200" alt="김준수 포트폴리오 바로가기" src="https://github.com/user-attachments/assets/1b674927-d8ee-4288-9057-3f8551fc50c7" />
</a>

## 성장하는 개발자, 김준수입니다.

끊임없는 노력으로 서로 다른 언어와 사람을 연결하는 개발자입니다.<br>
웹 백엔드, 클라우드 등 보이지 않는 곳을 지탱하는 기술을 배워왔고<br>
최근에는 하네스 엔지니어링, 멀티 에이전틱 시스템 등 AI 신기술에 관심이 많습니다. 

📮 [kjsoo1901@gmail.com](mailto:kjsoo1901@gmail.com) · 🔗 [Portfolio](https://kjsoo-portfolio.vercel.app/) · 💼 [LinkedIn](https://www.linkedin.com/in/junsoo-kim-dev/)



<br>

## Activities

- **삼성 청년 SW·AI 아카데미 16기** `2026.07 ~ 재학 중`
- 경희대학교 SW융합학과 데이터사이언스 트랙 `2019.03 ~ 2026.02`
- AWS Academy — Cloud Architecting / Cloud Foundations / ML Foundations `2025.03 ~ 2025.07`
- 네이버 부스트캠프 웹·모바일 8기 백엔드 `2023.07 ~ 2023.12`
- 전술C4I운용·정비병 복무 `2020.11 ~ 2022.05`
- 알고리즘 동아리 GoGo `2019.06 ~ 2020.08`

**Certificates** 
<br>· AWS Solutions Architect – Associate `2026.08` 
<br>· 정보처리기사 `2025.09` 
<br>· SQL Developer `2024.04`

<br>

## Projects

### 🧭 [MyAnalyst](https://github.com/Junsoo-Kim/MyAnalyst) — RAG 기반 기업 분석 보고서 자동 생성 서비스

> `2025.03 ~ 2025.12` · **개인 프로젝트** · 캡스톤디자인 · 졸업논문 우수 발표 · [시연 영상](https://youtu.be/0xeEq4bg_60)

증권사 보고서의 주관성·비실시간성 문제를 RAG로 해결. 기획부터 배포까지 단독 수행.

- Spring Boot(API) / FastAPI(RAG) / React(FE) 3-서버 구조 설계
- 데이터 성격에 따라 PostgreSQL · Milvus · Redis 를 분리 운영
- AWS Academy 수료 경험을 토대로 AWS 기반 배포 진행
- 생성 결과물을 실제 증권사 보고서와 비교 검증 — 핵심 정보 Recall 0.50 (실제 보고서 평균 0.45)

### 🌙 [별숲 ByeolSoop](https://github.com/boostcampwm2023/web08-ByeolSoop) — 3D 밤하늘 감정 다이어리 ⭐27

> `2023.10 ~ 2023.12` · 팀 4명 · **백엔드 담당** · 네이버 부스트캠프 8기 그룹 프로젝트 · [시연 영상](https://youtu.be/yJT54SBMT_8?si=Es9PJdqxZJMTcYFd)

일기를 3D 밤하늘의 별로 그리고, 감정 분석 결과에 따라 별 색이 바뀌는 다이어리 서비스.

- 액세스 토큰 탈취를 서버가 막을 수 없다는 한계 때문에 Stateless JWT를 Stateful 방식으로 전환, 리프레시 토큰 페이로드에 토큰·클라이언트 IP를 저장해 중복 로그인까지 차단
- JwtAuthGuard · PrivateDiaryGuard 커스텀 가드로 타인의 일기 접근을 요청 단계에서 통제
- 매 테스트마다 DB를 초기화하던 구조를 트랜잭션 롤백 방식으로 바꿔 테스트 시간 50% 이상 단축

### 📈 [VIN](https://github.com/Junsoo-Kim/VIN) — 리스크 헷지 기반 ETF 추천 서비스

> `2024.09 ~ 2024.12` · 팀 3명 · **팀 리더 / 풀스택 개발** · 경희대학교 캡스톤디자인 ·  [시연 영상](https://youtu.be/FWQwvUAIn-Y?si=5F7Ps3m5IbhlS0md)

한국·미국 ETF 1,100여 개의 상관관계를 분석해, 개인 투자자에게 헷지 조합을 추천.

- 주가 데이터의 비선형성 때문에 피어슨·스피어만 상관계수를 그대로 쓸 수 없었던 문제 — 부호는 스피어만, 값은 피어슨을 쓰는 방식으로 두 지표의 한계를 상호 보완
- Apache Airflow DAG로 Spring Boot ↔ Python 분석 워크플로우 연결 — 수집·전처리·분석·후처리가 순차적으로 필요해, 일반 Python 웹서버 대신 워크플로우 엔진을 REST로 트리거하는 구조 채택
- LLM에 리커트 척도를 적용해 서술형 설문 응답의 편차를 줄이고, −100 ~ 100 범위의 투자 위험 감수 성향 점수 산출

### 🧑‍🏫 [Setuk-AI](https://github.com/Junsoo-Kim/Setuk-AI) — 교사 세부능력특기사항 작성 AI 하네스

> `2026.06 ~ 2026.08` · **개인 프로젝트** · [사용 가이드](https://github.com/Junsoo-Kim/Setuk-AI)

학생 활동 보고서를 통해 규정을 지킨 세특 초안을 완벽하게 생성하는, LLM 위에 얹는 하네스

- 프롬프트 한 덩어리 대신 데이터 구조화 → 초안 작성 → 검증 → 평가 4단계로 분리해, 각 단계를 독립적으로 수정·교체할 수 있는 구조 설계
- 세특 작성 규정을 rules.json으로 외부화하고, 글자 수·표현 검사를 린터 스크립트로 자동화해 출력이 규정을 벗어나는 경우를 기계적으로 걸러냄
- 학생 1명당 세션 1개로 컨텍스트를 격리 — 학생 간 정보 교차 오염을 막고 토큰 사용량 절감

<br>

## Skills

#### Language & Framework
![Java](https://img.shields.io/badge/Java-007396.svg?&style=for-the-badge&logo=OpenJDK&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F.svg?&style=for-the-badge&logo=Spring%20Boot&logoColor=white)
<br>
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6.svg?&style=for-the-badge&logo=TypeScript&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E.svg?&style=for-the-badge&logo=NestJS&logoColor=white)
<br>
![Python](https://img.shields.io/badge/Python-3776AB.svg?&style=for-the-badge&logo=Python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688.svg?&style=for-the-badge&logo=FastAPI&logoColor=white)

#### Database
![MySQL](https://img.shields.io/badge/MySQL-4479A1.svg?&style=for-the-badge&logo=MySQL&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1.svg?&style=for-the-badge&logo=PostgreSQL&logoColor=white)
![Milvus](https://img.shields.io/badge/Milvus-00A1EA.svg?&style=for-the-badge&logo=Milvus&logoColor=white)

#### Infra & Tools
![AWS](https://img.shields.io/badge/AWS-232F3E.svg?&style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED.svg?&style=for-the-badge&logo=Docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF.svg?&style=for-the-badge&logo=githubactions&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639.svg?&style=for-the-badge&logo=Nginx&logoColor=white)
