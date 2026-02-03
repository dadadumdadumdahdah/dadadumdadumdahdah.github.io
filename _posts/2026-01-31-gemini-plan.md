---
layout: post
title: "토이프로젝트1: 1-2. Gemini said"
date: 2026-01-31 16:38:00 +0900
categories: 
    - 토이프로젝트
tags:
  - Backend
  - 백엔드
last_modified_at: 2026-02-03 20:38:46 +0900
---


# 🚀 2026년 백엔드 이직을 위한 3개월 집중 성장 로드맵 

2026년 이미 1월이 지나가고 있지만, 상반기(3~4월) 또는 하반기(9월) 채용 시즌을 목표로 한다면 지금이 시작하기에 가장 좋은 시기입니다. 본인의 실력이 부족하다고 느끼신다면 이론만 파는 것보다 **'실무와 가장 유사한 환경에서 문제를 해결해보는 경험'**이 가장 빠른 성장 방법입니다.

채용 시장에서 백엔드 주니어/미들급에게 가장 요구하는 역량은 **데이터 무결성, 동시성 제어, 그리고 대용량 트래픽 처리 경험**입니다. 이를 녹여낼 수 있는 **'선착순 티켓 예매 서비스'**를 토이프로젝트 주제로 제안하며, 12주(3개월) 완성형 몰입 계획표를 공유합니다.

---

## 1. 추천 토이프로젝트: 대규모 트래픽을 가정한 "콘서트 티켓 예매 시스템"

단순한 쇼핑몰보다 '좌석'이라는 한정된 자원을 두고 발생하는 **동시성 문제(Concurrency)**를 해결하는 과정이 백엔드 개발자로서의 역량을 어필하기에 훨씬 유리합니다.

* **핵심 기술 스택:** Java 17+, Spring Boot 3.x, Spring Data JPA, MySQL, Redis, Docker
* **어필 포인트:** 동시성 제어(Lock), 대기열 시스템 구현, 쿼리 최적화, 테스트 코드 작성

---

## 2. 📅 3개월 집중 학습 & 프로젝트 병행 로드맵

이론 공부(Input)와 프로젝트 구현(Output)의 비율을 **3:7**로 가져가세요. 막히는 부분만 찾아서 공부하는 것이 가장 빠릅니다.

### Phase 1: 기반 다지기 & 설계 (1~4주 차)
*목표: 기본 CRUD를 넘어선 탄탄한 설계와 API 개발 시작*

| 주차 | 프로젝트(Action) | 필수 학습 키워드(Study) |
| :-- | :-- | :-- |
| **1주** | **요구사항 분석 및 설계**<br>- UseCase 작성<br>- ERD 설계 (정규화/비정규화 고민)<br>- API 명세서 작성 (Swagger/Notion) | REST API 디자인 원칙<br>RDB 설계 (1:N, N:M 관계 이해)<br>Git Flow 전략 |
| **2주** | **환경 설정 및 회원 도메인**<br>- Spring Boot 3.x 프로젝트 세팅<br>- 회원가입/로그인 (JWT 구현) | Spring Security 구조<br>JWT (Access/Refresh Token)<br>BCrypt 암호화 |
| **3주** | **공연/좌석 도메인 개발 (CRUD)**<br>- 공연 등록, 날짜별 좌석 생성<br>- 기본적인 조회 API 구현 | JPA 영속성 컨텍스트<br>Fetch Join (N+1 문제 방지)<br>DTO 변환 및 Validation |
| **4주** | **예매 로직 구현 (기초)**<br>- 좌석 선택 및 임시 배정<br>- 결제 전 상태 관리 | 트랜잭션(@Transactional)의 전파 레벨<br>격리 수준(Isolation Level) 기초 |

### Phase 2: 핵심 문제 해결 & 심화 (5~8주 차)
*목표: 이 프로젝트의 꽃인 '동시성 문제'를 해결하고 테스트로 검증*

| 주차 | 프로젝트(Action) | 필수 학습 키워드(Study) |
| :-- | :-- | :-- |
| **5주** | **동시성 제어 1 (DB Lock)**<br>- 동시에 같은 좌석 예약 시도 시나리오<br>- 비관적 락(Pessimistic Lock) 적용해보기 | **Race Condition(경쟁 상태)**<br>Database Lock (Shared vs Exclusive)<br>Deadlock(교착 상태) 해결 |
| **6주** | **동시성 제어 2 (Redis)**<br>- Redis를 활용한 분산 락 구현 (Redisson)<br>- 성능 비교 (DB 락 vs Redis 락) | Redis 자료구조<br>In-memory DB의 특징<br>분산 환경에서의 정합성 |
| **7주** | **대기열 시스템 구현 (선택/심화)**<br>- 트래픽 폭주 시 대기 순번 부여<br>- WebSocket 또는 Polling으로 순서 알림 | Kafka 또는 Redis Pub/Sub<br>비동기 처리 (@Async)<br>스케줄러 |
| **8주** | **테스트 코드 작성**<br>- JUnit5, Mockito 활용 단위/통합 테스트<br>- 동시성 테스트 케이스 작성 필수 | TDD 개념<br>Jacoco (코드 커버리지)<br>Test Container |

### Phase 3: 배포 & 최적화 (9~12주 차)
*목표: 실제 서비스 가능한 수준으로 배포하고 성능 튜닝*

| 주차 | 프로젝트(Action) | 필수 학습 키워드(Study) |
| :-- | :-- | :-- |
| **9주** | **인프라 구축 (CI/CD)**<br>- Docker Compose로 DB/App 컨테이너화<br>- GitHub Actions로 자동 배포 파이프라인 | Docker/Docker Compose<br>CI/CD 개념<br>AWS EC2/RDS 기초 |
| **10주** | **성능 튜닝 & 모니터링**<br>- 슬로우 쿼리 분석 및 인덱스 적용<br>- JMeter/nGrinder로 부하 테스트 | Database Index 원리<br>Query Plan 분석<br>Pinpoint 또는 Prometheus/Grafana |
| **11주** | **리팩토링 & 문서화**<br>- SOLID 원칙 기반 코드 리팩토링<br>- **README 작성 (가장 중요)** | 객체지향 설계 원칙 (SOLID)<br>디자인 패턴 (Strategy, Facade 등) |
| **12주** | **이력서/포트폴리오 작성**<br>- 프로젝트에서의 '문제-해결-성과' 정리<br>- 모의 면접 질문 리스트 뽑기 | 기술 면접 예상 질문<br>STAR 기법 자기소개서 |

---

## 3. 💡 멘토의 조언 (이것만은 꼭!)

1.  **"왜?"에 집착하세요:** 단순히 Redis를 썼다가 아니라, *"DB 부하를 줄이기 위해 Redis 캐싱을 도입했고, 그 결과 응답 속도가 00ms 단축되었다"*는 식의 근거가 중요합니다.
2.  **기록이 곧 실력입니다:** 개발하며 마주친 에러, 고민했던 점들을 블로그(Velog, Tistory 등)에 '트러블 슈팅' 로그로 남기세요. 면접관은 코드보다 그 과정을 보고 싶어 합니다.
3.  **완벽주의를 버리세요:** 처음부터 완벽한 아키텍처는 없습니다. 일단 돌아가게 만들고(Make it work), 올바르게 고치고(Make it right), 빠르게 만드세요(Make it fast).

---