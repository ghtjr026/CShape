# C++ 중급 개발자를 위한 C# 학습 로드맵

이 로드맵은 **C++ 중급 개발자이지만 C#은 초보인 개발자**를 대상으로 한다.  
목표는 단순 문법 학습이 아니라, **C#으로 실무 Web API 및 서비스 아키텍처를 설계하고 구현할 수 있는 수준**에 도달하는 것이다.

---

## 최종 목표

- C# 언어 문법과 런타임 특성을 이해한다
- C++과 다른 C#의 철학(GC, async, DI)을 체득한다
- ASP.NET Core 기반 Web API를 설계·구현할 수 있다
- DI, 로깅, 설정, 테스트가 포함된 실무 코드 작성이 가능하다
- C++식 과도한 수명/메모리 관리 사고에서 벗어난다

---

## 전체 학습 단계 개요

### Phase 0 — C# 기본 개념 & 사고방식 전환
**목표**
- C#이 C++와 근본적으로 다른 언어임을 인지
- 문법보다 “관리되는 언어”의 사고방식 습득

**핵심 내용**
- 값 타입 vs 참조 타입
- `class`, `struct`, `record`
- `null`, nullable reference (`T?`)
- 프로퍼티 (`get/set`)
- C++의 수명 관리와 C#의 GC 차이

---

### Phase 1 — 객체지향 설계 (C# 스타일)
**목표**
- 상속 중심 설계에서 interface 중심 설계로 전환

**핵심 내용**
- `interface`
- `virtual / override / sealed`
- 의존성 역전 개념
- C++ 다형성과 C# 다형성의 차이

---

### Phase 2 — 컬렉션 & LINQ
**목표**
- STL + algorithm 사고를 LINQ 기반 사고로 치환

**핵심 내용**
- `List<T>`, `Dictionary<TKey, TValue>`
- `IEnumerable<T>` 개념
- LINQ (`Where`, `Select`, `First`, `Any`)
- 지연 실행(deferred execution)
- 성능과 가독성의 균형

---

### Phase 3 — 메모리 모델 & 수명 관리
**목표**
- GC가 해주는 것과 개발자가 책임져야 할 것을 명확히 구분

**핵심 내용**
- Garbage Collector 동작 개념
- `IDisposable`
- `using` / `await using`
- event / static으로 인한 메모리 누수
- C++ RAII와의 차이

---

### Phase 4 — 비동기 프로그래밍 & 동시성
**목표**
- 스레드 기반 사고에서 async/await 기반 사고로 전환

**핵심 내용**
- `Task`, `Task<T>`
- `async / await`
- `CancellationToken`
- async deadlock 개념
- CPU 작업 vs I/O 작업 구분

---

### Phase 5 — ASP.NET Core Web API
**목표**
- C# 서버 애플리케이션의 기본 구조 이해

**핵심 내용**
- Controller
- Routing
- Middleware
- Request pipeline
- HTTP 요청 처리 흐름

---

### Phase 6 — 실무 필수 인프라 요소
**목표**
- “동작하는 코드”에서 “운영 가능한 코드”로 확장

**핵심 내용**
- Dependency Injection (DI Container)
- 로깅 (`ILogger`)
- 설정 관리 (`appsettings.json`)
- Options 패턴
- Health Check 엔드포인트

---

### Phase 7 — 테스트 & 통합 실습
**목표**
- C#으로 실무 프로젝트를 수행할 수 있는 상태 도달

**핵심 내용**
- 단위 테스트 개념
- 통합 테스트 (WebApplicationFactory)
- API 테스트 전략
- 실무 미니 프로젝트 구성

---

## ⚠️ C++ 개발자가 주의해야 할 핵심 포인트

- GC는 메모리 누수를 자동으로 해결해주지 않는다
- interface는 선택이 아니라 기본이다
- async는 스레드가 아니다
- struct는 성능 최적화 수단이 아니라 설계 도구다
- `IEnumerable<T>`는 데이터가 아니라 실행 규약이다
- 예외는 흐름 제어 용도가 아니다
- DI는 프레임워크 사용의 핵심이다

---

## ✅ 로드맵 완료 후 기대 상태

- C# Web API 프로젝트를 혼자 설계하고 구현 가능
- C++ 기반 시스템과 자연스럽게 연동 가능
- C# 코드 리뷰 및 아키텍처 논의 가능
- 실무 환경에서 즉시 투입 가능한 수준

---

## 📌 권장 학습 방식

- 문법 위주의 학습 지양
- 작은 Web API 프로젝트를 지속적으로 확장
- C++에서 작성했던 구조를 C#으로 재구성하며 학습
