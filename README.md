# 👋 Backend Developer 강문구입니다!

---

## 🚀 About Me

- 🔭 클라우드 기반 분산 시스템 아키텍처 설계 및 구현
- 💡 OAuth2, JWT 기반 인증/인가 시스템 구축
- 🏗️ AWS ECS, AWS Elastic Cache, Confluent cloud를 활용한 MSA 환경 구성

---

## 🛠️ Tech Stack

### Backend
![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=spring-security&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-59666C?style=for-the-badge&logo=hibernate&logoColor=white)

### Database & Cache
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)

### Message Queue & Event
![Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apache-kafka&logoColor=white)
![Confluent](https://img.shields.io/badge/Confluent-0D1117?style=for-the-badge&logo=confluent&logoColor=white)

### DevOps & Cloud
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)

### Tools & Collaboration
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white)

---

## 💼 Projects & Experience

<details open>
<summary><b>🎨 OOTD 추천 서비스 (2025.08.29 - 2025.10.24)</b></summary>

<br>

> Spring Boot 기반 패션 추천 플랫폼  
> https://www.notion.so/ohgiraffers/55TD-207649136c1180288dabfeb1877485d6
> 
> https://github.com/SB03-OOTD-Team5/OOTD-Team5

**주요 구현 사항:**
- 🔐 OAuth2 소셜 로그인 (Google, Kakao) 및 JWT 기반 인증 시스템
- 🏗️ AWS ECS 멀티 서버 환경 + Nginx 리버스 프록시 구성
- ⚡ Redis를 활용한 분산 서버 환경에서의 JWT 토큰 공유
- 🌐 AWS Cloud Map을 활용한 서비스 디스커버리

**Tech Stack:**
`Spring Boot` `Spring Security` `PostgreSQL` `Redis` `Kafka` `AWS ECS` `Nginx` `Docker`

**주요 트러블슈팅:**
- [비밀번호 재설정 타임아웃 이슈 해결](https://www.notion.so/ohgiraffers/29b649136c11807aaface4729fbd0df9?source=copy_link) - 비동키 처리를 통해 해결
- [Redis 직렬화 문제 해결](https://www.notion.so/ohgiraffers/Redis-Value-29b649136c1180e091b8da37876ca0bb?source=copy_link) - GenericJackson2JsonRedisSerializer 설정 개선
- [OAuth2 State 저장 문제](https://www.notion.so/ohgiraffers/OAuth-authorization_request_not_found-29b649136c1180fe8b5dcd03f812e01b?source=copy_link) - Stateless 환경에서 쿠키 기반 저장소 구현
- [AWS 요금 환불 요청 경험 ](https://www.notion.so/ohgiraffers/AWS-29b649136c1180c79428e57b2e901287?source=copy_link) - 문의를 통해 크레딧 115$ 지급 받음

---

### 🎯 Highlights

**🏛️ 분산 시스템 아키텍처 설계**
```
┌─────────────┐
│   사용자    │
└──────┬──────┘
       │
┌──────▼──────────────┐
│  Nginx (ECS)        │ ← Elastic IP
│  리버스 프록시      │
└──────┬──────────────┘
       │
┌──────▼──────────────┐
│  Cloud Map          │ ← Service Discovery
│  backend.internal   │
└──────┬──────────────┘
       │
┌──────┴───────┐
│              │
▼              ▼
Backend 1   Backend 2
```

**🔐 인증/인가 시스템**
- **OAuth2 + JWT 하이브리드 방식**
  - Access Token (1시간) + Refresh Token (7일)
  - HttpOnly Cookie + localStorage 보안 계층화
  - Redis 기반 토큰 무효화 전략

**⚡ 성능 최적화**
- **비동기 처리로 응답시간 95% 개선**
  - Before: 10~30초 (메일 발송 대기)
  - After: 0.5~1초 (즉시 응답)
  
- **Redis를 통한 분산 환경 JWT 관리**
  - 멀티 서버 환경에서 토큰 정보 공유
  - 토큰 무효화 전략 구현

**💰 비용 최적화**
- **AWS 인프라 비용 50% 절감**
  - NAT Gateway 2개 → 1개 ($90/월 → $45/월)
  - RDS 인스턴스 타입 최적화
  - 불필요한 Multi-AZ 옵션 제거

</details>

---

<details>
<summary><b>📰 Monew - 모두의 뉴스 (2025.07.09 - 2025.07.30)</b></summary>

<br>

> Spring Boot 기반 뉴스 통합 플랫폼  
> https://www.notion.so/ohgiraffers/5-207649136c1180968b6bf8028b42b212
> 
> https://github.com/5josama/sb03-monew-team5

**프로젝트 소개:**
여러 뉴스 API를 통합하여 사용자에게 맞춤형 뉴스를 제공하고, 댓글을 통해 의견을 나눌 수 있는 소셜 기능을 갖춘 뉴스 플랫폼

**담당 역할:** 댓글 시스템 백엔드 개발 (CRUD + 좋아요 + 커서 페이지네이션)

**주요 구현 사항:**
- 💬 **댓글 CRUD 시스템**
  - 댓글 등록/조회/수정/삭제 (논리/물리 삭제 분리)
  - 사용자 권한 검증 로직 구현
  
- 📄 **Querydsl 기반 커서 페이지네이션**
  - 동적 정렬 조건 처리 (`createdAt`, `likeCount`)
  - JPQL → Querydsl 마이그레이션으로 유지보수성 향상
  - 대용량 댓글 목록 효율적 조회

- ❤️ **댓글 좋아요 기능**
  - `likedByMe` 필드를 통한 사용자별 좋아요 여부 판단
  - N+1 쿼리 문제 해결 (fetch join 활용)

- 🔔 **이벤트 기반 알림 시스템**
  - `ApplicationEventPublisher`를 활용한 서비스 간 결합도 분리

**Tech Stack:**
`Spring Boot` `JPA` `Querydsl` `MapStruct` `PostgreSQL` `Spring Events`

**주요 성과:**

| 지표 | 개선 결과 |
|:----:|:--------:|
| 📊 쿼리 최적화 | **N+1 문제 해결** (fetch join) |
| 🔄 코드 품질 | **Querydsl 마이그레이션** (동적 쿼리) |
| 🏗️ 아키텍처 | **이벤트 기반 설계** (결합도↓) |
| 🎯 테스트 커버리지 | **단위/통합 테스트 작성** |

---

### 🎯 Technical Highlights

**⚡ 성능 최적화**

**N+1 쿼리 해결로 성능 대폭 개선**
- Before: 300+ 쿼리 (100개 댓글 기준)
- After: 2개 쿼리 (fetch join 적용)
- **쿼리 수 99% 감소** 🎯

```java
// 최적화 전: N+1 문제 발생
List<Comment> comments = commentRepository.findAll(); // 1번 쿼리
for (Comment comment : comments) {
    comment.getUser().getName();     // N번 쿼리
    comment.getArticle().getTitle(); // N번 쿼리
    // 총 1 + 2N번의 쿼리 실행
}

// 최적화 후: Fetch Join 적용
List<Comment> comments = queryFactory
    .selectFrom(comment)
    .join(comment.user).fetchJoin()
    .join(comment.article).fetchJoin()
    .fetch(); // 1번의 조인 쿼리로 모든 데이터 로딩
```

**Querydsl 동적 쿼리로 유지보수성 향상**
- 정렬 조건별 중복 코드 제거
- 컴파일 타임 검증으로 안정성 확보
- 동적 조건 처리로 확장성 개선

---

### 📝 Development Process

**구현한 주요 기능**

**1. 댓글 등록 (POST /api/comments)**
```java
@PostMapping
public ResponseEntity<CommentResponse> createComment(
        @RequestHeader("User-Id") Long userId,
        @RequestBody CommentCreateRequest request) {
    CommentResponse response = commentService.createComment(userId, request);
    return ResponseEntity.ok(response);
}
```
- ✅ 사용자 인증 및 권한 검증
- ✅ DTO 검증 (MapStruct)
- ✅ 단위/통합 테스트 작성

**2. 댓글 조회 - 커서 페이지네이션 (GET /api/comments)**
```java
@GetMapping
public ResponseEntity<CursorPageResponse<CommentResponse>> getComments(
        @RequestParam Long articleId,
        @RequestParam(required = false) String cursor,
        @RequestParam(defaultValue = "createdAt") String sortBy,
        @RequestParam(defaultValue = "10") int size) {
    // ...
}
```
- ✅ 동적 정렬 (createdAt, likeCount)
- ✅ Querydsl 기반 커서 처리
- ✅ likedByMe 필드 포함

**3. 댓글 수정 (PUT /api/comments/{id})**
```java
@PutMapping("/{id}")
public ResponseEntity<CommentResponse> updateComment(
        @PathVariable Long id,
        @RequestHeader("User-Id") Long userId,
        @RequestBody CommentUpdateRequest request) {
    // 작성자 검증 로직 포함
}
```
- ✅ 작성자 본인 확인
- ✅ 논리 삭제된 댓글 수정 불가

**4. 댓글 삭제 - 논리/물리 분리**
```java
// 논리 삭제 (Soft Delete)
@DeleteMapping("/{id}/soft")
public ResponseEntity<Void> softDeleteComment(...) {
    comment.softDelete();
    // deletedAt 필드만 업데이트
}

// 물리 삭제 (Hard Delete) - 관리자 전용
@DeleteMapping("/{id}/hard")
public ResponseEntity<Void> hardDeleteComment(...) {
    commentRepository.delete(comment);
    // DB에서 완전 삭제
}
```

**5. 댓글 좋아요 (POST /api/comments/{id}/like)**
```java
@PostMapping("/{id}/like")
public ResponseEntity<LikeResponse> likeComment(
        @PathVariable Long id,
        @RequestHeader("User-Id") Long userId) {
    LikeResponse response = commentService.likeComment(id, userId);
    
    // 이벤트 발행 (비동기 알림)
    eventPublisher.publishEvent(
        new CommentLikedEvent(id, userId)
    );
    
    return ResponseEntity.ok(response);
}
```
- ✅ 이벤트 기반 알림 발송

</details>

---

<details>
<summary><b>🏢 HRBANK - HR Management System (2025.06.04 - 2025.06.13)</b></summary>

<br>

> Spring Boot 기반 인적자원 관리 시스템  
> https://www.notion.so/ohgiraffers/5-207649136c1180e79ab9d2751a0a9b1b
> 
> https://github.com/Codeit-Basic-Project-Team-5/sb3-hrbank-team5

**프로젝트 소개:**
기업의 인적자원을 체계적으로 관리하고 모니터링하기 위한 HR Management System

**담당 역할:** 
- 데이터 백업 관리 시스템 개발
- DB 관리 총괄 (데이터베이스 생성, Schema 설계)
- 프로젝트 회의 주관

**주요 구현 사항:**

- 🔄 **자동 백업 시스템**
  - Spring Scheduler 기반 주기적 백업 (1시간 간격)
  - 데이터 변경 여부 확인을 통한 불필요한 백업 방지
  - CSV 파일 형식으로 전체 직원 정보 저장

- 📋 **백업 이력 관리**
  - 커서 기반 페이지네이션 구현
  - 작업자, 시작 시간, 상태별 필터링 기능
  - 시작/종료 시간 기준 양방향 정렬 (ASC/DESC)

- 💾 **백업 파일 관리**
  - 백업 파일 다운로드 기능
  - UTF-8 BOM 추가로 엑셀 한글 인코딩 문제 해결
  - 백업 실패 시 에러 로그 파일 자동 생성

- 🗄️ **데이터베이스 설계 및 관리**
  - 전체 Schema 설계 및 테이블 구조 정의
  - 데이터베이스 생성 및 초기 설정
  - DB 관련 이슈 총괄 관리

**Tech Stack:**
`Spring Boot` `Spring Batch` `Spring Scheduler` `JPA` `PostgreSQL` `JPQL`

**주요 성과:**

| 지표 | 달성 내용 |
|:----:|:--------:|
| 🔄 자동화 | **1시간 주기 자동 백업** |
| 📊 데이터 관리 | **CSV 파일 기반 백업** |
| 🎯 페이지네이션 | **양방향 정렬 커서 구현** |
| 🛠️ DB 설계 | **전체 Schema 설계 완료** |

---


### 📝 Development Process

**구현한 주요 기능**

**1. 자동 백업 스케줄링 - 스마트 백업 판단**
```java
@Scheduled(cron = "0 0 * * * *")  // 매 시간마다 실행
public void performScheduledBackup() {
    // 1. 마지막 백업 시간 조회 (완료된 백업만)
    Optional<DataBackup> lastBackup = dataBackupRepository
        .findAll()
        .stream()
        .filter(backup -> backup.getEndedAt() != null)
        .max(Comparator.comparing(DataBackup::getEndedAt));
    
    // 2. 변경된 데이터 확인
    if (lastBackup.isPresent()) {
        Instant lastBackupTime = lastBackup.get().getEndedAt();
        boolean hasChanges = employeeRepository
            .existsByModifiedAtAfter(lastBackupTime);
        
        if (!hasChanges) {
            createSkippedBackup("No changes since last backup");
            return;
        }
    }
    
    // 3. 백업 수행
    performBackup();
}
```

**2. 백업 이력 조회 - 양방향 정렬 커서 페이지네이션**
```java
@GetMapping("/api/backups")
public ResponseEntity<CursorPageResponse<BackupResponse>> getBackups(
        @RequestParam(required = false) String cursor,
        @RequestParam(required = false) Long idAfter,
        @RequestParam(defaultValue = "startedAt") String sortField,
        @RequestParam(defaultValue = "DESC") String sortDirection,
        @RequestParam(defaultValue = "10") int size) {
    
    CursorPageResponse<BackupResponse> response = 
        backupService.getBackupsWithCursor(cursor, idAfter, sortField, sortDirection, size);
    
    return ResponseEntity.ok(response);
}
```
- ✅ 4가지 정렬 조건 지원 (startedAt/endedAt × ASC/DESC)
- ✅ 작업자, 상태별 필터링
- ✅ NULL 값 처리 (endedAt 기준 정렬 시)

**3. 백업 파일 다운로드**
```java
@GetMapping("/api/backups/{id}/download")
public ResponseEntity<Resource> downloadBackup(@PathVariable Long id) {
    DataBackup backup = backupRepository.findById(id)
        .orElseThrow(() -> new BackupNotFoundException(id));
    
    File file = new File(backup.getFilePath());
    Resource resource = new FileSystemResource(file);
    
    return ResponseEntity.ok()
        .header(HttpHeaders.CONTENT_DISPOSITION, 
            "attachment; filename=\"" + backup.getFileName() + ".csv\"")
        .contentType(MediaType.parseMediaType("text/csv"))
        .body(resource);
}
```
- ✅ CSV 파일 다운로드
- ✅ 한글 파일명 지원
- ✅ 파일 존재 여부 검증

---

### 🔥 Problem Solving

**트러블슈팅 하이라이트**

<details>
<summary><b>🔴 오름차순 정렬 시 무한 스크롤 발생</b></summary>

### 문제
- **정상 동작**: 내림차순(DESC) 정렬
- **문제 발생**: 오름차순(ASC) 정렬에서 동일한 데이터가 무한 반복 조회
- **증상**: 커서가 다음 페이지로 진행되지 않고 첫 번째 페이지 데이터 반복

### 원인 분석

**근본 원인:**
커서 기반 페이지네이션에서 정렬 방향에 따른 조건문 차이를 고려하지 않음

**잘못된 쿼리 (내림차순에만 적합):**
```sql
-- 기존 코드
WHERE d.startedAt < CAST(:cursor AS java.time.Instant)
   OR (d.startedAt = CAST(:cursor AS java.time.Instant) 
       AND d.id <= :idAfter)
ORDER BY d.startedAt DESC
```

**문제점:**
- 내림차순(DESC): 다음 데이터는 현재 커서보다 **작은 값**들
- 오름차순(ASC): 다음 데이터는 현재 커서보다 **큰 값**들
- 조건문(`<`)은 내림차순 전용이므로 오름차순에서 작동 안 함

### 해결 방법

**1단계: 정렬 방향별 쿼리 분리**
```java
// Repository에 4개의 메서드 생성
@Query("SELECT d FROM DataBackup d WHERE ...")
Page<DataBackup> findAllWithCursorStartedAtDesc(...);

@Query("SELECT d FROM DataBackup d WHERE ...")
Page<DataBackup> findAllWithCursorStartedAtAsc(...);

@Query("SELECT d FROM DataBackup d WHERE ...")
Page<DataBackup> findAllWithCursorEndedAtDesc(...);

@Query("SELECT d FROM DataBackup d WHERE ...")
Page<DataBackup> findAllWithCursorEndedAtAsc(...);
```

**2단계: 올바른 쿼리 조건 적용**
```sql
-- 오름차순용 (수정)
WHERE d.startedAt > CAST(:cursor AS java.time.Instant)  -- < 에서 > 로 변경
   OR (d.startedAt = CAST(:cursor AS java.time.Instant) 
       AND d.id >= :idAfter)  -- <= 에서 >= 로 변경
ORDER BY d.startedAt ASC
```

**3단계: Service 로직 개선**
```java
public Page<DataBackup> getBackupsWithCursor(
        String cursor, Long idAfter, String sortField, String sortDirection, int size) {
    
    if ("startedAt".equals(sortField)) {
        if ("DESC".equalsIgnoreCase(sortDirection)) {
            return repository.findAllWithCursorStartedAtDesc(cursor, idAfter, size);
        } else {
            return repository.findAllWithCursorStartedAtAsc(cursor, idAfter, size);
        }
    } else if ("endedAt".equals(sortField)) {
        if ("DESC".equalsIgnoreCase(sortDirection)) {
            return repository.findAllWithCursorEndedAtDesc(cursor, idAfter, size);
        } else {
            return repository.findAllWithCursorEndedAtAsc(cursor, idAfter, size);
        }
    }
    
    throw new IllegalArgumentException("Invalid sort field: " + sortField);
}
```

**4단계: NULL 값 처리**
```sql
-- endedAt DESC: NULL 값 포함 (진행 중인 백업)
WHERE (d.endedAt < :cursor OR d.endedAt IS NULL)
ORDER BY d.endedAt DESC

-- endedAt ASC: NULL 값 제외 (완료된 백업만)
WHERE d.endedAt > :cursor 
  AND d.endedAt IS NOT NULL
ORDER BY d.endedAt ASC
```

### 결과
- ✅ 4가지 정렬 조건 모두 정상 작동
- ✅ 무한 스크롤 문제 완전 해결
- ✅ NULL 값 올바르게 처리

</details>

<details>
<summary><b>🔴 마지막 페이지 요소 누락</b></summary>

### 문제
페이지네이션 조회 시 가장 마지막 요소가 조회되지 않음

### 원인
다음 페이지 존재 여부 확인을 위해 `size+1` 개를 조회했지만, 마지막 요소 처리 로직 누락

### 해결
```java
// 조회 결과에서 hasNext 판단
List<DataBackup> content = result.getContent();
boolean hasNext = content.size() > size;

// 마지막 페이지가 아닐 경우에만 마지막 요소 제거
if (hasNext) {
    content.remove(content.size() - 1);
}

return new CursorPageResponse<>(
    content, 
    hasNext, 
    hasNext ? getNextCursor(content) : null
);
```

**결과:** 모든 데이터 정상 조회 ✅

</details>

<details>
<summary><b>🔴 totalElements 오류</b></summary>

### 문제
검색 조건 적용 시 전체 개수가 아닌 조건에 맞는 개수가 반환되지 않음

### 원인
Repository 메서드가 `List<DataBackup>` 타입을 반환하여 전체 개수 정보 손실

### 해결
```java
// Before: List 반환
List<DataBackup> findAllWithCursor(...);

// After: Page 반환
@Query("SELECT d FROM DataBackup d WHERE ... ")
Page<DataBackup> findAllWithCursor(...);

// Service에서 totalElements 추출
Page<DataBackup> page = repository.findAllWithCursor(...);
Long totalElements = page.getTotalElements();
```

**결과:** 정확한 전체 개수 반환 ✅

</details>

<details>
<summary><b>🔴 중복 백업 생성 문제</b></summary>

### 문제
한 번 백업 후 재실행 시 "건너뜀" 처리되지 않고 중복 백업 생성

### 원인
백업 필요성 판단 로직에서 **진행 중인 백업 상태**를 고려하지 않음

### 해결
```java
// Before: 모든 백업 대상으로 최신 시간 조회
Optional<DataBackup> lastBackup = repository.findAll()
    .stream()
    .max(Comparator.comparing(DataBackup::getEndedAt));

// After: 완료된 백업만 대상으로 조회
Optional<DataBackup> lastBackup = repository.findAll()
    .stream()
    .filter(backup -> backup.getEndedAt() != null)  // 완료된 것만
    .max(Comparator.comparing(DataBackup::getEndedAt));
```

**결과:** 중복 백업 방지 ✅

</details>

<details>
<summary><b>🔴 엑셀에서 한글 인코딩 깨짐</b></summary>

### 문제
CSV 파일 다운로드 후 엑셀에서 열람 시 한글이 깨져서 표시됨

### 원인
엑셀이 UTF-8 파일을 열 때 BOM(Byte Order Mark) 없이는 인코딩을 제대로 인식하지 못함

### 해결
```java
try (BufferedWriter writer = new BufferedWriter(
        new OutputStreamWriter(
            new FileOutputStream(file), StandardCharsets.UTF_8))) {
    
    // UTF-8 BOM 추가
    writer.write('\uFEFF');
    
    // CSV 데이터 작성
    writer.write("ID,이름,부서,직책\n");
    employees.forEach(emp -> {
        writer.write(emp.toCsvLine());
    });
}
```

**UTF-8 BOM이란?**
- `\uFEFF`: UTF-8 파일의 시작을 알리는 특수 문자
- 엑셀이 이 문자를 인식하면 자동으로 UTF-8로 파일을 읽음

**결과:** 엑셀에서 한글 정상 표시 ✅

</details>

</details>

---

## 📚 Key Learnings

### 기술적 성장

1. **JPA 성능 최적화**
   - N+1 문제 발견 및 해결 능력 향상
   - Fetch Join 활용법 습득

2. **Querydsl 활용**
   - 동적 쿼리 작성 능력 향상
   - 타입 세이프 쿼리의 장점 체감
   - 복잡한 조건 처리 경험

3. **아키텍처 설계**
   - 이벤트 기반 아키텍처 도입 경험
   - 서비스 간 결합도 관리 방법 학습

4. **테스트 작성**
   - 단위/통합 테스트 작성 습관화
   - Mock 객체 활용 능력 향상
   - 테스트 커버리지 중요성 이해

### 협업 스킬

- **코드 리뷰**: 팀원 피드백을 적극 수용하고 개선
- **문서화**: 상세한 PR 작성으로 리뷰 효율성 향상
- **커뮤니케이션**: 기술적 의사결정 과정 공유

---

## 💬 Let's Connect!

<div align="center">

[![NaverMail Badge](https://img.shields.io/badge/Mail-03C75A?style=flat-square&logo=Naver&logoColor=white&link=mailto:sprtms5325@naver.com)](mailto:sprtms5325@naver.com)

---

**⭐ 방문해주셔서 감사합니다! ⭐**

![footer](https://capsule-render.vercel.app/api?type=waving&color=gradient&height=150&section=footer)

</div>
