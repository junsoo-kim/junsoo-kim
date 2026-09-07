<a href="https://kjsoo-portfolio.vercel.app/">
  <img width="700" height="200" alt="김준수 포트폴리오 바로가기" src="https://github.com/user-attachments/assets/1b674927-d8ee-4288-9057-3f8551fc50c7" />
</a>

## 성장하는 개발자, 김준수입니다.

끊임없는 노력으로 서로 다른 언어와 사람을 연결하는 개발자입니다.<br>
웹 백엔드, 클라우드 등 보이지 않는 곳을 지탱하는 기술을 배워왔고<br>
최근에는 하네스 엔지니어링, 멀티 에이전틱 시스템 등 AI 신기술에 관심이 많습니다. 

📮 [kjsoo1901@gmail.com](mailto:kjsoo1901@gmail.com) · 🔗 [Portfolio](https://kjsoo-portfolio.vercel.app/) · 💼 [LinkedIn](https://www.linkedin.com/in/%EC%A4%80%EC%88%98-%EA%B9%80-7a31952a4/)



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
- 임베딩 유사도 검색만으로는 놓치던 수치·고유명사 문서를 잡기 위해 BM25 하이브리드 검색을 직접 구축 — 정답 문서 회수율 Hit@10 0.73 → 0.98
- 생성 결과를 스스로 검증하는 LangGraph 루프(채점 → 생성 → 환각 채점 → 재검색)를 추가해 근거 있는 문장 비율 77.5% → 95.5%
- 자원 경합으로 서비스 전체가 멈춘 장애 이후 백엔드·AI·데이터 계층을 VPC 내로 분리, 보안그룹 체인을 Terraform 11개 모듈로 코드화

### 🌙 [별숲 ByeolSoop](https://github.com/boostcampwm2023/web08-ByeolSoop) — 3D 밤하늘 감정 다이어리 ⭐27

> `2023.10 ~ 2023.12` · 팀 4명 · **백엔드 담당** · 네이버 부스트캠프 8기 그룹 프로젝트 · [시연 영상](https://youtu.be/yJT54SBMT_8?si=Es9PJdqxZJMTcYFd)

일기를 3D 밤하늘의 별로 그리고, 감정 분석 결과에 따라 별 색이 바뀌는 다이어리 서비스.

- OWASP Top 10 기준으로 점검하다 탈취된 액세스 토큰을 서버가 끊을 방법이 없다는 걸 확인, 리프레시 토큰을 Redis에 사용자 단위로 보관하고 발급 토큰·접속 IP를 매 요청 대조하는 Stateful 구조로 재설계
- JwtAuthGuard 위에 PrivateDiaryGuard로 인가를 한 겹 더 쌓아 정상 토큰으로도 타인의 일기 접근을 차단, 리소스 존재 여부가 드러나지 않도록 403 대신 404로 응답
- 4인 팀 안에서 풀리지 않던 기술 난관을 다른 팀과의 코드 리뷰로 확인·해결하며 FE·BE 상태 코드 처리 흐름을 조율

### 📈 [VIN](https://github.com/Junsoo-Kim/VIN) — 리스크 헷지 기반 ETF 추천 서비스

> `2024.09 ~ 2024.12` · 팀 3명 · **팀 리더 / 풀스택 개발** · 경희대학교 캡스톤디자인 ·  [시연 영상](https://youtu.be/FWQwvUAIn-Y?si=5F7Ps3m5IbhlS0md)

한국·미국 ETF 1,100여 개의 상관관계를 분석해, 개인 투자자에게 헷지 조합을 추천.

- 목록 조회 후 종목마다 상세를 다시 조회해 쿼리가 3N+2로 늘어나던 구조를 연관관계별 Fetch 전략 이원화로 해결 — 종목 50개 기준 152 → 2쿼리, 응답 0.1093s → 0.0112s(9.8배)
- 매수 이력 적재를 Kafka로 비동기 분리한 뒤 생긴 "조용한 유실" 위험을 지수 백오프 재시도 + DLT 보상 레코드로 차단 — 동시 매수 30건 유실률 0%, 실패 3건 전부 복구
- 분산 락을 걸었는데도 드물게 정합성이 깨지던 문제를 추적해 락 해제가 트랜잭션 커밋보다 먼저 실행되는 Spring AOP 프록시 순서 문제였음을 밝혀내고, 락·트랜잭션 빈을 물리적으로 분리해 해결

### 🧑‍🏫 [Setuk-AI](https://github.com/Junsoo-Kim/Setuk-AI) — 교사 세부능력특기사항 작성 AI 하네스

> `2026.06 ~ 2026.08` · **개인 프로젝트** · [사용 가이드](https://github.com/Junsoo-Kim/Setuk-AI)

학생 활동 보고서를 통해 규정을 지킨 세특 초안을 완벽하게 생성하는, LLM 위에 얹는 하네스

- 프롬프트 한 덩어리 대신 입력 → 사실 구조화 → 초안 → 평가 4단계로 분리해, 근거가 부족하면 AI가 지어내지 않고 멈춰 되묻도록 설계
- 세특 작성 규정을 rules.json으로 외부화하고 글자 수·표현 위반을 린터로 기계적으로 걸러내며, 핵심 안전장치 문구는 자동 테스트로 고정해 지침 문서에만 존재하다 조용히 사라지지 않게 함
- 설치 부담과 품질 요구라는 서로 다른 사용자 피드백을 한 아키텍처에 욱여넣지 않고 웹 업로드형(A) · VSCode(B) · LangGraph 기반(C) 3개 배포 트랙으로 분리 — 교사 80명 이상 실사용

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

#### Data
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1.svg?&style=for-the-badge&logo=PostgreSQL&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D.svg?&style=for-the-badge&logo=Redis&logoColor=white)
<br>
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20.svg?&style=for-the-badge&logo=ApacheKafka&logoColor=white)
![Milvus](https://img.shields.io/badge/Milvus-00A1EA.svg?&style=for-the-badge&logo=Milvus&logoColor=white)
<br>
![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE.svg?&style=for-the-badge&logo=ApacheAirflow&logoColor=white)

#### Infra & Tools
![AWS](https://img.shields.io/badge/AWS-232F3E.svg?&style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC.svg?&style=for-the-badge&logo=Terraform&logoColor=white)
<br>
![Docker](https://img.shields.io/badge/Docker-2496ED.svg?&style=for-the-badge&logo=Docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF.svg?&style=for-the-badge&logo=githubactions&logoColor=white)
