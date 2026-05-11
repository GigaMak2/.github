# 실시간 역경매 서비스

> 구매자가 원하는 물품을 등록하면, 판매자들이 경쟁적으로 가격을 낮춰 입찰하는 **역경매(Reverse Auction)** 서비스입니다.

```
구매자  →  경매 등록 (최대 희망가 설정)
판매자  →  입찰 (더 낮은 가격 경쟁)
마감    →  최저가 판매자 자동 낙찰
```

---

## 1. 조원 소개

자기소개 추가 바람

---

## 2. 프로젝트 개요

**개발 기간**: 2026.04.07 ~ 2026.05.14

### 핵심 차별점 — AI 상담 챗봇

별도 AI 채팅방에서 **DeepSeek V3** 기반 AI가 실시간 시세, 판매자 신뢰도, 경쟁 입찰 현황 등을 분석해드립니다.
DB의 실제 거래 데이터를 **Tool Calling + RAG**로 실시간 조회하므로 hallucination 없이 플랫폼 데이터를 정확하게 안내합니다.

---

## 3. 기술 스택

<div align="center">

### **Language**
<img src="https://img.shields.io/badge/java-007396?style=for-the-badge&logo=openjdk&logoColor=white"> <img src="https://img.shields.io/badge/gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white">

### **Backend**
<img src="https://img.shields.io/badge/spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white"> <img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"> <img src="https://img.shields.io/badge/Spring%20Data%20JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white"> <img src="https://img.shields.io/badge/Spring%20AI-6DB33F?style=for-the-badge&logo=spring&logoColor=white"> <img src="https://img.shields.io/badge/Spring%20WebFlux-6DB33F?style=for-the-badge&logo=spring&logoColor=white"> <img src="https://img.shields.io/badge/QueryDSL-0078D4?style=for-the-badge&logo=github&logoColor=white">

### **Security**
<img src="https://img.shields.io/badge/springsecurity-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white"> <img src="https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=jsonwebtokens&logoColor=white">

### **Real-time**
<img src="https://img.shields.io/badge/WebSocket-010101?style=for-the-badge&logo=socket.io&logoColor=white"> <img src="https://img.shields.io/badge/SSE-FF6C37?style=for-the-badge&logo=server&logoColor=white">

### **Database**
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"> <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white"> <img src="https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white"> <img src="https://img.shields.io/badge/Kibana-005571?style=for-the-badge&logo=kibana&logoColor=white"> <img src="https://img.shields.io/badge/Flyway-CC0200?style=for-the-badge&logo=flyway&logoColor=white">

### **Message Queue**
<img src="https://img.shields.io/badge/Amazon%20EventBridge-FF4F8B?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/Amazon%20SQS-FF4F8B?style=for-the-badge&logo=amazonsqs&logoColor=white">

### **AI Model**
<img src="https://img.shields.io/badge/DeepSeek%20V3-4D6BFE?style=for-the-badge&logo=deepseek&logoColor=white"> <img src="https://img.shields.io/badge/OpenAI%20Embedding-412991?style=for-the-badge&logo=openai&logoColor=white">

### **Infra / Cloud**
<img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/Amazon%20EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white"> <img src="https://img.shields.io/badge/Amazon%20ECS-FF9900?style=for-the-badge&logo=amazonecs&logoColor=white"> <img src="https://img.shields.io/badge/Amazon%20ECR-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/Amazon%20RDS-527FFF?style=for-the-badge&logo=amazonrds&logoColor=white"> <img src="https://img.shields.io/badge/Amazon%20S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white"> <img src="https://img.shields.io/badge/AWS%20Lambda-FF9900?style=for-the-badge&logo=awslambda&logoColor=white"> <img src="https://img.shields.io/badge/CloudFront-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/Route%2053-8C4FFF?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/ElastiCache-C925D1?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/NAT%20Gateway-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/AWS%20IAM-DD344C?style=for-the-badge&logo=amazonaws&logoColor=white">

### **CI/CD**
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"> <img src="https://img.shields.io/badge/Github%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white">

### **Monitoring**
<img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white"> <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white"> <img src="https://img.shields.io/badge/Grafana%20Alloy-F46800?style=for-the-badge&logo=grafana&logoColor=white"> <img src="https://img.shields.io/badge/CloudWatch-FF4F8B?style=for-the-badge&logo=amazonaws&logoColor=white"> <img src="https://img.shields.io/badge/K6-7D64FF?style=for-the-badge&logo=k6&logoColor=white">

### **Test**
<img src="https://img.shields.io/badge/JUnit5-25A162?style=for-the-badge&logo=junit5&logoColor=white"> <img src="https://img.shields.io/badge/Mockito-25A162?style=for-the-badge&logo=java&logoColor=white"> <img src="https://img.shields.io/badge/Testcontainers-9B489A?style=for-the-badge&logo=docker&logoColor=white"> <img src="https://img.shields.io/badge/Spring%20REST%20Docs-6DB33F?style=for-the-badge&logo=spring&logoColor=white"> <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white">

### **Open API**
<img src="https://img.shields.io/badge/Google%20OAuth2-4285F4?style=for-the-badge&logo=google&logoColor=white"> <img src="https://img.shields.io/badge/Kakao%20OAuth2-FFCD00?style=for-the-badge&logo=kakao&logoColor=black"> <img src="https://img.shields.io/badge/Naver%20OAuth2-03C75A?style=for-the-badge&logo=naver&logoColor=white">

### **Collaboration**
<img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=github&logoColor=white"> <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white"> <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white"> <img src="https://img.shields.io/badge/Draw.io-F08705?style=for-the-badge&logo=diagramsdotnet&logoColor=white"> <img src="https://img.shields.io/badge/ERDCloud-4A90D9?style=for-the-badge&logo=cloud&logoColor=white"> <img src="https://img.shields.io/badge/CodeRabbit-FF4500?style=for-the-badge&logo=rabbit&logoColor=white">

</div>

---

## 4. 아키텍처

사진 첨부 예정

---

## 5. ERD

사진 첨부 예정

---

## 6. 패키지 구조

```
com.example.auction/
├── common/
│   ├── config/       # Security, Redis, QueryDSL, WebSocket, Spring AI, pgvector
│   ├── dto/          # BaseResponse, PageResponse
│   ├── entity/       # BaseEntity (생성일, 수정일, 삭제일)
│   └── exception/    # GlobalExceptionHandler, ServiceErrorException
│
└── domain/
    ├── auth/         # 회원가입, 로그인, 토큰 갱신, 소셜 로그인
    ├── user/         # 마이페이지, 비밀번호 변경, 회원 탈퇴
    ├── auction/      # 경매 CRUD, 검색 (ES + pgvector), EventBridge 연동
    │   ├── result/   # 낙찰 결과 조회
    │   └── search/   # Elasticsearch 도큐먼트, 검색 서비스
    ├── bid/          # 입찰 생성 (분산락), 입찰 조회
    ├── category/     # 카테고리 트리 조회, 관리자 CRUD
    ├── review/       # 리뷰 CRUD, S3 Presigned URL, RAG 임베딩 연동
    ├── chat/         # AI 채팅방 CRUD, 메시지 목록 (커서 페이징), Redis 컨텍스트
    ├── ai/           # SSE 스트리밍, Tool Calling 8종, RAG 2종, 임베딩 서비스
    ├── userchat/     # 유저간 실시간 채팅 (WebSocket + Redis Pub/Sub)
    └── notification/ # Redis Pub/Sub 알림 발행
```

### 도메인 상태 흐름

```
경매 상태
  READY ──► ACTIVE ──► DONE   (낙찰)
    │              └──► NO_BID (유찰)
    └──► CANCELLED (READY 상태 + 시작 10분 전까지)

낙찰 흐름
  Lambda 실행
    → auction_results 생성
    → Redis Pub/Sub 발행
    → AuctionEmbedListener
    → pgvector 임베딩 저장 (RAG 검색 가능)
```

---

## 7. [API 명세서](https://www.notion.so/API-35df7cf0a20c80b885a0dd708f506cbb?showMoveTo=true&saveParent=true)

---

## 8. 주요 기능

### 1. 회원 인증
- JWT 기반 Stateless 인증 (Access 30분 / Refresh 7일)
- 소셜 로그인: Google, Kakao, Naver OAuth2
- 로그인 5회 실패 시 5분 계정 잠금 (Redis TTL)
- Refresh Token 탈취 시 즉시 무효화

### 2. 경매
- 등록 즉시 EventBridge Scheduler에 시작/종료 스케줄 자동 등록
- Elasticsearch + PostgreSQL 이중 검색 (Nori 한국어 형태소 분석)
- AWS Lambda가 종료 시각에 자동 낙찰 / 유찰 처리
- Redis 캐싱으로 단건 / 목록 조회 성능 최적화

### 3. 입찰
- Redisson 분산락으로 동시 입찰 경합 방지
- 현재 최저가보다 낮은 가격만 등록 가능
- 입찰 성공 시 실시간 알림 자동 발행 (NEW_BID / LOWEST_BID_UPDATED)

### 4. 실시간 알림
- Redis Pub/Sub → 별도 알림 서버 → SSE로 클라이언트에 실시간 전달

### 5. 유저간 실시간 채팅
- 낙찰 후 구매자-판매자 1:1 채팅방 자동 생성
- WebSocket + STOMP + SockJS 기반, JWT 인증 적용
- Redis Pub/Sub 브로커로 다중 서버 인스턴스 간 메시지 공유

### 6. 리뷰
- 낙찰 경매 당사자(구매자/판매자)만 작성 가능
- 별점(1~5) 필수, 이미지 선택 (S3 Presigned URL → CloudFront CDN)
- 리뷰 작성/수정 후 pgvector 임베딩 자동 저장 → AI RAG 소스로 활용

### 7. AI 상담 챗봇

SSE 스트리밍으로 실시간 응답을 수신하며, Tool Calling과 RAG를 통해 DB의 실제 데이터를 기반으로 답변합니다.

**Tool Calling (8종)**

| Tool | 역할 |
|------|------|
| `getBidsByAuctionId` | 경매 입찰 현황 · 최저가 · 경쟁 분석 |
| `getRecentAuctionResults` | 상품 시세 · 낙찰 이력 조회 |
| `getSellerStats` | 판매자 종합 신뢰도 (낙찰 횟수, 평균 평점) |
| `getSellerReviewInsights` | 판매자 후기 키워드 분석 (RAG) |
| `getMyAuctions` | 내가 등록한 경매 현황 · 현재 최저가 |
| `getMyBids` | 내가 입찰한 경매 현황 · 1위 여부 |
| `getAuctionStatsByCategory` | 카테고리별 낙찰 통계 · 시세 분석 |
| `searchAuctionDescriptions` | 낙찰 경매 상품 설명 의미 검색 (RAG) |

**RAG (2종)**

| 종류 | 대상 | 기법 |
|------|------|------|
| 후기 RAG | 판매자 리뷰 텍스트 | HyDE + Contextual Retrieval + 감성 방향 score 필터 |
| 경매 설명 RAG | 낙찰 경매 상품명+설명 | 코사인 유사도 검색 (Lambda Pub/Sub 파이프라인) |

- **HyDE**: 질문으로 가상 후기를 생성한 후 그 임베딩으로 검색 → P@3 성능 0.83 → 1.00 향상
- **Contextual Retrieval**: 별점을 텍스트에 prepend하여 짧은 후기의 임베딩 품질 개선
- **감성 방향 필터**: 부정 키워드 → score≤2 / 긍정 키워드 → score≥4 자동 필터

### 8. CI/CD

**CI** — main, dev 브랜치 push/PR 시 자동 실행
- JDK 21 (Corretto) + Gradle 빌드 + 전체 테스트 통과 확인

**CD** — 수동 트리거 (배포할 커밋 해시 입력)
- Spring Boot JAR 빌드 → arm64 Docker 이미지 → AWS ECR push
- ECS 태스크 정의 등록 → ECS 서비스 강제 업데이트 (무중단 배포)
- AWS 자격증명: OIDC (키 없이 역할 기반 인증)

---

## 9. [기술적 의사결정 / 트러블 슈팅 / 성능 개선](https://www.notion.so/35df7cf0a20c80119d48fa7435c3824d?source=copy_link)