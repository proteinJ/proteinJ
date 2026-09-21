<div align="center">

# 박재현 · Jaehyun Park

**백엔드 개발자** &nbsp;·&nbsp; 동아대학교 컴퓨터공학 &nbsp;·&nbsp; 부산

인증·공간 데이터·실시간 통신을 다루는 Spring Boot 서버를 만듭니다.<br/>
필요하면 클라이언트(iOS·Flutter)와 AI 파이프라인까지 직접 붙여서 끝까지 굴려 봅니다.

[![Gmail](https://img.shields.io/badge/jaehyun516@naver.com-03C75A?style=flat-square&logo=naver&logoColor=white)](mailto:jaehyun516@naver.com)
[![GitHub](https://img.shields.io/badge/@proteinJ-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/proteinJ)

</div>

---

## About

- 서버가 주력입니다. **Spring Boot + PostgreSQL/PostGIS + Redis** 조합으로 JWT 인증, 위치 기반 조회, WebSocket 실시간 브로드캐스트를 직접 설계하고 구현했습니다.
- 팀 프로젝트에서는 백엔드를, 개인 프로젝트에서는 **기획 → 스키마 설계 → 서버 → 앱**까지 혼자 맡아 봤습니다.
- 클라이언트(SwiftUI·Flutter)와 AI/데이터(YOLO·OCR·LSTM)도 필요한 만큼은 직접 붙여 왔습니다. 전문 영역이라고 말하지는 않지만, API 계약을 사이에 두고 양쪽 사정을 모르는 채로 설계하지는 않습니다.
- 기술 선택에는 이유를 남기는 편입니다. 예를 들어 반경 검색에 PostGIS를 쓴 건 `ST_DWithin`이 GiST 인덱스를 타기 때문이고, 이미지 스토리지로 Cloudflare R2를 고른 건 egress 요금이 없어서입니다.

---

## Tech Stack

**Backend** — 주력

![Java](https://img.shields.io/badge/Java%2017·21-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot%203.x-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security%20+%20JWT-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA%20·%20QueryDSL-59666C?style=flat-square&logo=hibernate&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket%20·%20STOMP-010101?style=flat-square&logo=socketdotio&logoColor=white)

**Database & Infra**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![PostGIS](https://img.shields.io/badge/PostGIS-336791?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)
![Docker](https://img.shields.io/badge/Docker%20Compose-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Swagger](https://img.shields.io/badge/SpringDoc%20OpenAPI-85EA2D?style=flat-square&logo=swagger&logoColor=black)

**Client** — 서버와 붙일 수 있는 수준

![Swift](https://img.shields.io/badge/Swift%20·%20SwiftUI-F05138?style=flat-square&logo=swift&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter%20·%20Riverpod-02569B?style=flat-square&logo=flutter&logoColor=white)
![Unity](https://img.shields.io/badge/Unity%20·%20C%23-000000?style=flat-square&logo=unity&logoColor=white)

**AI / Data** — 서비스에 붙여 본 경험

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO%20(Ultralytics)-00FFFF?style=flat-square&logo=yolo&logoColor=black)
![TensorFlow](https://img.shields.io/badge/Keras%20·%20LSTM-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini%20·%20Vision%20AI-4285F4?style=flat-square&logo=google&logoColor=white)

---

## Projects

### 🐾 꼬동 (KKODONG) — 반려견 산책 소셜 *(개인 · 개발 중)*
> 견주 커뮤니티가 아니라 **강아지끼리 친구를 맺어주는** 산책 소셜 서비스. 기획·설계·서버·앱을 혼자 맡았습니다.

[![Server](https://img.shields.io/badge/kkodong--server-6DB33F?style=flat-square&logo=github&logoColor=white)](https://github.com/proteinJ/kkodong-server)

- **서버** Spring Boot 3.5 / PostgreSQL + PostGIS / Redis / Flyway / Cloudflare R2 — 약 15,200줄 + 테스트 5,200줄
- **iOS** Swift · SwiftUI · MVVM — 약 11,600줄, 배경 제거는 Apple Vision 프레임워크로 **온디바이스 처리**(서버 비용 0)
- 거리 기반 추천 후보 조회를 `ST_DWithin` + GiST 인덱스로 처리, Refresh Token·로그아웃 블랙리스트는 Redis
- 기획서·시장조사·의사결정 기록·API 명세·DB 스키마·추천 알고리즘을 전부 `docs/`에 문서화
- 가설 검증을 위해 부산 온천천 15km 구간을 직접 답사하고, 결과에 따라 **핵심 기능 하나를 스스로 폐기**한 뒤 설계를 다시 짰습니다

### 🏃 Baton — 소셜 러닝 트래킹 플랫폼 *(팀 · 백엔드 담당)*
> "혼자 뛰지 말고, 같이 뛰자" — GPS 러닝 기록, 실시간 그룹 러닝, 스팟 체크인, 소셜 피드

[![Backend](https://img.shields.io/badge/Backend-runApp-6DB33F?style=flat-square&logo=github&logoColor=white)](https://github.com/proteinJ/runApp)
[![Frontend](https://img.shields.io/badge/Frontend-Flutter-02569B?style=flat-square&logo=github&logoColor=white)](https://github.com/HC1ab/Baton_runapp_frontend)

- Java 17 / Spring Boot 3.4 / PostgreSQL + PostGIS / Redis / QueryDSL — 전체 197커밋 중 **144커밋 담당**
- GPS 좌표 리스트를 PostGIS `LineString`으로 저장, 하버사인 공식으로 거리 검증 후 유효하지 않은 기록은 폐기
- **WebSocket + STOMP + Redis Pub/Sub** 으로 그룹 러닝 참여자 실시간 위치 브로드캐스트
- JWT Access/Refresh 이중 토큰 — Refresh는 Redis 저장, 로그아웃 Access는 블랙리스트 등록
- `@LoginMember` 커스텀 애노테이션 + ArgumentResolver 로 Stateless 환경에서 인증 객체 주입
- GitHub Actions CI/CD — PostGIS·Redis 서비스 컨테이너를 띄워 테스트한 뒤 자동 배포
- 카카오 소셜 로그인, 레벨·칭호 시스템(`exp = 250n² + 250n`), 스케줄러 기반 그룹 상태 전이

### 📢 엄마의 잔소리 (Mom's Nagging) — AI 시간표 인식 등교 도우미 *(팀 · 백엔드 + AI)*
> 시간표 이미지를 올리면 AI가 일정을 등록하고, 출발할 타이밍에 맞춰 잔소리 알림을 보냅니다

[![Repo](https://img.shields.io/badge/Mom's%20Nagging-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/proteinJ/Mom-s-Nagging)

- **Spring Boot + FastAPI 모노레포** — 비즈니스 서버와 AI 서버를 분리하고 Docker Compose로 일괄 구동
- 파이프라인: **YOLO**(시간표 표 객체 검출) → **Google Vision AI**(OCR) → **Gemini 2.5 Flash**(데이터 정제) → 일정 자동 등록
- 네이버 길찾기 API로 이동 시간을 계산해, 이동 시간의 0.8배 시점에 알림 발송
- 시간표 셀 검출용 YOLO 모델은 2,000장 규모 데이터셋을 직접 구축해 학습·튜닝 (`timeTable_Model_Lab`)

### ⛵ SafeSail — 해양 디지털 트윈 / 항해 보조 *(팀 · 수집 서버 담당)*
> 실제 기상 데이터를 반영한 Unity 시뮬레이터에서 운항 데이터를 수집하고, 항로·위험구역 API를 검증

[![Collector](https://img.shields.io/badge/navlog--collector-6DB33F?style=flat-square&logo=github&logoColor=white)](https://github.com/proteinJ/navlog-collector)
[![Unity](https://img.shields.io/badge/ICT--Unity-000000?style=flat-square&logo=github&logoColor=white)](https://github.com/ICT-Smart-Shipping-Logistics/ICT-Unity)

- **Java 21 / Spring Boot 3.x / PostgreSQL + PostGIS / Redis / Docker** 기반 ML 학습용 데이터 수집 파이프라인
- 로그인 없이 **UUID 기반 클라이언트 식별**, 운항 로그(VesselLog·EnvironmentLog·EventLog) 도메인 분리 설계
- 기상청·국립해양조사원 API를 1시간 주기 스케줄러로 배치 수집
- Unity 클라이언트가 REST + WebSocket(`wss://.../nav/ws`)으로 항로·경로 이탈·위험구역 안내를 실시간 수신

### 🧰 spring-boot-boilerplate — 재사용 백엔드 템플릿 *(개인)*
[![Repo](https://img.shields.io/badge/spring--boot--boilerplate-6DB33F?style=flat-square&logo=github&logoColor=white)](https://github.com/proteinJ/spring-boot-boilerplate)

> 새 프로젝트마다 인증·에러 처리를 다시 짜지 않으려고 만든 스타터

- JWT 인증 전체 흐름 — 회원가입/로그인/로그아웃, **Refresh Token 회전**(재사용 방지), Redis TTL 7일
- `BusinessException` + `ErrorCode` enum + `GlobalExceptionHandler` 로 전역 예외 응답 포맷 통일
- `ApiResponse<T>` 공통 래퍼 + Swagger UI Authorize 연동

---

## 이런 걸 해봤습니다

| 분야 | 경험 |
|---|---|
| **인증** | JWT Access/Refresh 이중 토큰, Refresh 회전, Redis 블랙리스트, 카카오·Apple 소셜 로그인 |
| **공간 데이터** | PostGIS `Point`/`LineString` 매핑, `ST_DWithin` + GiST 반경 검색, 하버사인 거리 계산 |
| **실시간** | WebSocket + STOMP 구독 채널, Redis Pub/Sub 브로드캐스트, 폴링 기반 피드 |
| **인프라** | Docker Compose 로컬 환경, GitHub Actions CI/CD(서비스 컨테이너 테스트), Flyway 마이그레이션 |
| **설계·협업** | 도메인별 패키지 분리, API 명세 선확정 후 병렬 개발, 스키마·의사결정 문서화 |
| **AI 연동** | YOLO 데이터셋 구축·학습, Vision OCR + LLM 정제 파이프라인, LSTM 위험도 예측, FastAPI 서빙 |

---

<div align="center">

**함께 만들 일이 있다면 편하게 연락 주세요**

[![Email](https://img.shields.io/badge/jaehyun516@naver.com-03C75A?style=for-the-badge&logo=maildotru&logoColor=white)](mailto:jaehyun516@naver.com)
[![GitHub](https://img.shields.io/badge/github.com/proteinJ-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/proteinJ)

</div>
