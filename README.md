# 📰 SpringBoot News Platform

> 카테고리 기반 기사 관리와 댓글·신고·반응 기능을 포함한  
> **Spring Boot 기반 뉴스 서비스 플랫폼**

---

## 📌 프로젝트 개요

- 개발 기간 : 2025.07 (1주 소요)
- 형태 : 팀 프로젝트
- 역할 : Backend 설계 및 주요 도메인 구현
- 목표 : 기사·댓글·신고 흐름이 분리된 구조 설계와 관리 기능 구현

---

## 🎯 설계 목표

단순 게시판 형태가 아닌,  
**기사 작성 → 승인 → 노출 → 댓글 → 신고 → 관리자 처리**  
까지 이어지는 흐름을 고려한 구조 설계를 목표로 개발했습니다.

---

## 🛠 기술 스택

### Backend
- Java
- Spring Boot
- MyBatis
- MVC 패턴 기반 설계

### Database
- RDBMS (MyBatis Mapper 사용)

### Frontend
- Thymeleaf
- HTML/CSS

---

## 🏗 아키텍처 설계

```
Controller → Service → Mapper(MyBatis) → DB
```

- Controller : 요청/응답 처리
- Service : 비즈니스 로직 분리
- Mapper : SQL 분리 관리
- DTO 기반 데이터 전달

👉 **계층 분리를 통해 역할과 책임을 명확히 구분**

---

## 📦 핵심 기능

### 📰 1. 기사 관리

- 카테고리별 기사 조회 (정치/경제/사회/스포츠/연예)
- 기자 등록 및 기사 작성
- 관리자 승인 후 노출 구조

> 승인 프로세스를 통해 단순 게시판과 차별화

---

### 💬 2. 댓글 시스템

- 기사별 댓글 등록
- 반응(좋아요/감정 표현) 기능
- 댓글 목록 동적 조회

> 단순 댓글 저장이 아닌,  
> 기사-댓글 관계를 고려한 구조 설계

---

### 🚨 3. 신고 및 관리자 처리

- 기사/댓글 신고 기능
- 관리자 페이지에서 신고 관리
- 승인/삭제 처리 구조

> 사용자 기능과 관리자 기능을 분리 설계

---

### 👤 4. 사용자 기능

- 회원가입 / 로그인
- 마이페이지
- 기사 작성 이력 조회

---

## 📊 설계 포인트

### ✔ 계층 분리

- Controller와 Service 분리
- Mapper를 통한 SQL 분리
- DTO 사용으로 Entity 직접 노출 방지

---

### ✔ 도메인 분리

- News
- Comment
- Reporter
- Report
- Sports
- Users

→ 기능 중심이 아닌 **도메인 중심 패키지 분리**

---

### ✔ 확장 고려

- 카테고리 확장 가능 구조
- 신고 기능 모듈화
- 관리자 승인 흐름 분리

---

## 🚀 실행 방법

```bash
git clone https://github.com/Ahn0204/springboot-news-platform.git
cd springboot-news-platform
./gradlew build
./gradlew bootRun
```

---

## 💡 개선 및 확장 가능성

- JWT 기반 인증 도입
- Spring Security 적용
- 댓글 비동기 처리 (Ajax)
- 캐싱 적용
- API 서버화 전환

---

## 🧠 프로젝트 회고

- 계층 분리 설계의 중요성 체감
- 관리자/사용자 역할 분리 구조 경험
- 게시글과 댓글 관계 설계 경험
- 유지보수성을 고려한 SQL 분리 설계 학습

---

## 👤 Contributor

안성진  
Backend Developer
