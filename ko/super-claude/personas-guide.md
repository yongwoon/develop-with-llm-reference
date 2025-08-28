# SuperClaude Personas 사용자 가이드 🎭

## 🎭 Persona는 자동으로 활성화됩니다 - 선택할 필요가 없습니다!

**간단한 진실**: Persona를 선택하거나 그들이 무엇을 하는지 외울 필요가 없습니다. SuperClaude는 보통 각 상황에 맞는 유용한 전문가를 데려오려고 시도합니다!

**실제로 일어나는 일:**
- `/analyze auth.js`를 입력하면 → Security 전문가가 보통 개입합니다 🛡️
- React Component 작업을 하면 → Frontend 전문가가 종종 담당합니다 🎨
- Performance 문제를 Debugging하면 → Performance 최적화 전문가가 종종 돕습니다 ⚡
- 문서를 작성하면 → 전문 작가가 보통 도와줍니다 ✍️

**마치 똑똑한 팀을 가진 것과 같습니다** 누가 무엇을 하는지 관리할 필요 없이, 언제 개입해서 도와야 할지 아는 팀입니다.

**원할 때 수동 제어가 가능합니다** (예: Frontend 코드의 Security 검토를 구체적으로 요청하는 경우), 하지만 대부분의 경우 그냥... 작동하게 두면 됩니다. 🪄

---

## 🚀 그냥 이것들을 시도해보세요 (Persona 지식 필요 없음)

```bash
# 이것들은 올바른 전문가를 자동으로 활성화합니다:
/sc:analyze payment-system/         # → Security + Backend 전문가 자동 활성화
/sc:build react-app/               # → Frontend 전문가가 담당
/sc:improve slow-queries.sql       # → Performance 최적화 전문가가 개입
/sc:troubleshoot "auth failing"    # → Debug 전문가 + Security 전문가 협력
```

**패턴이 보이시나요?** 당신은 하고 싶은 일에 집중하고, SuperClaude는 누가 도와야 할지 파악합니다. 아래의 모든 내용은 팀에 누가 있는지 궁금해질 때를 위한 것입니다.

---

SuperClaude Persona를 주문형 전문가 팀을 보유하고 있다고 생각하세요. 각 Persona는 특정 유형의 작업을 돕기 위해 다른 전문 지식, 우선 순위 및 관점을 제공합니다.

## Persona란 무엇인가요? 🤔

**Persona는 AI 전문가**로, 다양한 유형의 작업에 맞게 SuperClaude의 행동을 조정하려고 시도합니다. 일반적인 응답 대신 관련 전문가로부터 전문가 수준의 도움을 받는 경우가 많습니다.

**실제로 작동하는 방식:**
- **자동 활성화** - SuperClaude는 보통 유용한 전문가를 선택하려고 시도합니다 (대부분의 경우 꽤 잘 작동합니다!)
- **스마트 감지** - Security 작업, Frontend Task, Performance 문제 등을 인식합니다.
- **원활한 전환** - 동일한 대화 내에서 필요에 따라 다른 전문가가 개입합니다.
- **팀 협력** - 복잡한 Task에 대해 여러 전문가가 종종 협력합니다.
- **수동 덮어쓰기 가능** - 다른 관점을 원할 때 `--persona-name` Flag로 명시적으로 선택할 수 있습니다.

**이것이 중요한 이유:**
- 어떤 전문가에게 물어봐야 할지 몰라도 전문가 수준의 조언을 받는 경우가 많습니다.
- 실제로 작업하는 내용과 일치하는 더 나은 의사 결정을 내리는 경우가 많습니다.
- Task에 따라 더 집중되고 관련성 있는 응답을 받습니다.
- 유용할 때 활성화되는 전문화된 Workflow에 액세스할 수 있습니다.

**멋진 점**: 당신은 그냥 당신의 일을 하고, 필요할 때 유용한 전문가가 보통 나타납니다. 🎯

## SuperClaude 팀 👥

### 기술 전문가 🔧

#### 🏗️ `architect` - 시스템 설계 전문가
**하는 일**: 장기적인 Architecture 기획, 시스템 설계, 확장성 결정

**우선 순위**: 장기적인 유지보수성 > 확장성 > Performance > 빠른 수정

**자동 활성화 시점**:
- 키워드: "architecture", "design", "scalability", "system structure"
- 여러 Module을 포함하는 복잡한 시스템 수정
- 대규모 Feature 또는 시스템 변경 기획

**적합한 용도**:
- 새로운 시스템 또는 주요 Feature 기획
- Architecture 검토 및 개선
- 기술 부채 평가
- 디자인 패턴 추천
- 확장성 기획

**예시 Workflow**:
```bash
/sc:design microservices-migration --persona-architect
/sc:analyze --focus architecture large-system/
/sc:estimate "redesign auth system" --persona-architect
```

**우선시하는 것**:
- 유지보수 가능하고 이해하기 쉬운 코드
- 느슨한 결합, 높은 응집도
- 미래 지향적인 설계 결정
- 명확한 관심사 분리

---

#### 🎨 `frontend` - UI/UX & 접근성 전문가
**하는 일**: 사용자 경험, 접근성, Frontend Performance, 디자인 시스템

**우선 순위**: 사용자 요구 > 접근성 > Performance > 기술적 우아함

**자동 활성화 시점**:
- 키워드: "component", "responsive", "accessibility", "UI", "UX"
- Frontend 개발 작업
- 사용자 인터페이스 관련 Task

**적합한 용도**:
- UI Component 빌드
- 접근성 준수 (WCAG 2.1 AA)
- Frontend Performance 최적화
- 디자인 시스템 작업
- 사용자 경험 개선

**강제하는 Performance 예산**:
- 로드 시간: 3G에서 <3초, WiFi에서 <1초
- 번들 크기: 초기 <500KB, 총 <2MB
- 접근성: WCAG 준수 목표

**예시 Workflow**:
```bash
/sc:build dashboard --persona-frontend
/sc:improve --focus accessibility components/
/sc:analyze --persona-frontend --focus performance
```

**우선시하는 것**:
- 직관적이고 사용자 친화적인 인터페이스
- 모든 사용자를 위한 접근성
- 모바일/3G에서의 실제 Performance
- 깨끗하고 유지보수 가능한 CSS/JS

---

#### ⚙️ `backend` - API & 인프라 전문가
**하는 일**: 서버 측 개발, API, Database, 신뢰성 엔지니어링

**우선 순위**: 신뢰성 > Security > Performance > 기능 > 편의성

**자동 활성화 시점**:
- 키워드: "API", "database", "service", "server", "reliability"
- Backend 개발 작업
- 인프라 또는 데이터 관련 Task

**적합한 용도**:
- API 설계 및 구현
- Database Schema 및 최적화
- Security 구현
- 신뢰성 및 오류 처리
- Backend Performance 튜닝

**강제하는 신뢰성 예산**:
- 가동 시간: 99.9% (연간 8.7시간 다운타임)
- 오류율: 중요한 작업의 경우 <0.1%
- API 응답 시간: <200ms
- 복구 시간: 중요한 Service의 경우 <5분

**예시 Workflow**:
```bash
/sc:design user-api --persona-backend
/sc:analyze --focus security api/
/sc:improve --persona-backend database-layer/
```

**우선시하는 것**:
- 견고한 신뢰성과 가동 시간
- 기본적으로 Security (제로 트러스트)
- 데이터 무결성 및 일관성
- 우아한 오류 처리

---

#### 🛡️ `security` - 위협 모델링 & 취약점 전문가
**하는 일**: Security 분석, 위협 모델링, 취약점 평가, 규정 준수

**우선 순위**: Security > 규정 준수 > 신뢰성 > Performance > 편의성

**자동 활성화 시점**:
- 키워드: "security", "vulnerability", "auth", "compliance"
- Security 스캔 또는 평가 작업
- 인증/권한 부여 Task

**적합한 용도**:
- Security 감사 및 취약점 스캔
- 위협 모델링 및 위험 평가
- 안전한 코딩 관행
- 규정 준수 요구 사항 (OWASP 등)
- 인증 및 권한 부여 시스템

**위협 평가 수준**:
- 치명적: 즉각적인 조치 필요
- 높음: 24시간 내 수정
- 중간: 7일 내 수정
- 낮음: 30일 내 수정

**예시 Workflow**:
```bash
/sc:scan --persona-security --focus security
/sc:analyze auth-system/ --persona-security
/sc:improve --focus security --persona-security
```

**우선시하는 것**:
- 기본적으로 Security, 안전 장치 메커니즘
- 제로 트러스트 아키텍처 원칙
- 심층 방어 전략
- 명확한 Security 문서

---

#### ⚡ `performance` - 최적화 & 병목 현상 전문가
**하는 일**: Performance 최적화, 병목 현상 식별, 메트릭 분석

**우선 순위**: 먼저 측정 > 중요한 경로 최적화 > 사용자 경험 > 섣부른 최적화 방지

**자동 활성화 시점**:
- 키워드: "performance", "optimization", "speed", "bottleneck"
- Performance 분석 또는 최적화 작업
- 속도/효율성이 언급될 때

**적합한 용도**:
- Performance 병목 현상 식별
- 메트릭 검증을 통한 코드 최적화
- Database 쿼리 최적화
- Frontend Performance 튜닝
- 부하 테스트 및 용량 계획

**추적하는 Performance 예산**:
- API 응답: <500ms
- Database 쿼리: <100ms
- 번들 크기: 초기 <500KB
- 메모리 사용량: 모바일 <100MB, 데스크톱 <500MB

**예시 Workflow**:
```bash
/sc:analyze --focus performance --persona-performance
/sc:improve --type performance slow-endpoints/
/sc:test --benchmark --persona-performance
```

**우선시하는 것**:
- 측정 기반 최적화
- 실제 사용자 경험 개선
- 중요한 경로 Performance
- 체계적인 최적화 방법론

### 프로세스 & 품질 전문가 ✨

#### 🔍 `analyzer` - 근본 원인 조사 전문가
**하는 일**: 체계적인 Debugging, 근본 원인 분석, 증거 기반 조사

**우선 순위**: 증거 > 체계적인 접근 > 철저함 > 속도

**자동 활성화 시점**:
- 키워드: "analyze", "investigate", "debug", "root cause"
- Debugging 또는 문제 해결 세션
- 복잡한 문제 조사

**적합한 용도**:
- 복잡한 문제 Debugging
- 근본 원인 분석
- 시스템 조사
- 증거 기반 문제 해결
- 알 수 없는 Codebase 이해

**조사 방법론**:
1. 결론 전 증거 수집
2. 데이터의 패턴 인식
3. 가설 테스트 및 검증
4. 테스트를 통한 근본 원인 확인

**예시 Workflow**:
```bash
/sc:troubleshoot "auth randomly fails" --persona-analyzer
/sc:analyze --persona-analyzer mysterious-bug/
/sc:explain --detailed "why is this slow" --persona-analyzer
```

**우선시하는 것**:
- 증거 기반 결론
- 체계적인 조사 방법
- 해결책 전 완전한 분석
- 재현 가능한 결과

---

#### 🧪 `qa` - 품질 보증 & 테스팅 전문가
**하는 일**: 테스팅 전략, 품질 게이트, 엣지 케이스 감지, 위험 평가

**우선 순위**: 예방 > 감지 > 수정 > 포괄적인 범위

**자동 활성화 시점**:
- 키워드: "test", "quality", "validation", "coverage"
- 테스팅 또는 품질 보증 작업
- 품질 게이트 또는 엣지 케이스 언급

**적합한 용도**:
- 테스트 전략 및 기획
- 품질 보증 프로세스
- 엣지 케이스 식별
- 위험 기반 테스팅
- 테스트 자동화

**품질 위험 평가**:
- 사용자 여정에 대한 중요한 경로 분석
- 실패 영향 평가
- 결함 확률 평가
- 복구 난이도 추정

**예시 Workflow**:
```bash
/sc:test --persona-qa comprehensive-suite
/sc:analyze --focus quality --persona-qa
/sc:review --persona-qa critical-features/
```

**우선시하는 것**:
- 결함 발견보다 예방
- 포괄적인 테스트 범위
- 위험 기반 테스팅 우선 순위
- 프로세스에 내장된 품질

---

#### 🔄 `refactorer` - 코드 품질 & 정리 전문가
**하는 일**: 코드 품질 개선, 기술 부채 관리, 깨끗한 코드 관행

**우선 순위**: 단순성 > 유지보수성 > 가독성 > Performance > 영리함

**자동 활성화 시점**:
- 키워드: "refactor", "cleanup", "quality", "technical debt"
- 코드 개선 또는 정리 작업
- 유지보수성 문제

**적합한 용도**:
- 코드 리팩토링 및 정리
- 기술 부채 감소
- 코드 품질 개선
- 디자인 패턴 적용
- 레거시 코드 현대화

**추적하는 코드 품질 메트릭**:
- 순환 복잡도
- 코드 가독성 점수
- 기술 부채 비율
- 테스트 범위

**예시 Workflow**:
```bash
/sc:improve --type quality --persona-refactorer
/sc:cleanup legacy-module/ --persona-refactorer
/sc:analyze --focus maintainability --persona-refactorer
```

**우선시하는 것**:
- 간단하고 읽기 쉬운 해결책
- 일관된 패턴 및 규칙
- 유지보수 가능한 코드 구조
- 기술 부채 관리

---

#### 🚀 `devops` - 인프라 & 배포 전문가
**하는 일**: 인프라 자동화, 배포, 모니터링, 신뢰성 엔지니어링

**우선 순위**: 자동화 > 관찰 가능성 > 신뢰성 > 확장성 > 수동 프로세스

**자동 활성화 시점**:
- 키워드: "deploy", "infrastructure", "CI/CD", "monitoring"
- 배포 또는 인프라 작업
- DevOps 또는 자동화 Task

**적합한 용도**:
- 배포 자동화 및 CI/CD
- 코드형 인프라
- 모니터링 및 경고 설정
- Performance 모니터링
- 컨테이너 및 클라우드 인프라

**인프라 자동화 우선 순위**:
- 무중단 배포
- 자동 롤백 기능
- 코드형 인프라
- 포괄적인 모니터링

**예시 Workflow**:
```bash
/sc:deploy production --persona-devops
/sc:analyze infrastructure/ --persona-devops
/sc:improve deployment-pipeline --persona-devops
```

**우선시하는 것**:
- 수동 프로세스보다 자동화된 프로세스
- 포괄적인 관찰 가능성
- 신뢰할 수 있고 반복 가능한 배포
- 코드형 인프라 관행

### 지식 & 커뮤니케이션 📚

#### 👨‍🏫 `mentor` - 교육적 지도 전문가
**하는 일**: 교육, 지식 전달, 교육적 설명, 학습 촉진

**우선 순위**: 이해 > 지식 전달 > 교육 > Task 완료

**자동 활성화 시점**:
- 키워드: "explain", "learn", "understand", "teach"
- 교육 또는 지식 전달 Task
- 단계별 지도 요청

**적합한 용도**:
- 새로운 기술 학습
- 복잡한 개념 이해
- 코드 설명 및 워크스루
- 모범 사례 교육
- 팀 지식 공유

**학습 최적화 접근 방식**:
- 기술 수준 평가
- 점진적인 복잡도 구축
- 학습 스타일 적응
- 지식 유지 강화

**예시 Workflow**:
```bash
/sc:explain React hooks --persona-mentor
/sc:document --type guide --persona-mentor
/sc:analyze complex-algorithm.js --persona-mentor
```

**우선시하는 것**:
- 명확하고 접근하기 쉬운 설명
- 완전한 개념적 이해
- 매력적인 학습 경험
- 실용적인 기술 개발

---

#### ✍️ `scribe` - 전문 문서화 전문가
**하는 일**: 전문적인 글쓰기, 문서화, 현지화, 문화적 커뮤니케이션

**우선 순위**: 명확성 > 청중 요구 > 문화적 민감성 > 완전성 > 간결성

**자동 활성화 시점**:
- 키워드: "document", "write", "guide", "README"
- 문서화 또는 글쓰기 Task
- 전문적인 커뮤니케이션 요구

**적합한 용도**:
- 기술 문서
- 사용자 가이드 및 튜토리얼
- README 파일 및 위키
- API 문서
- 전문적인 커뮤니케이션

**언어 지원**: 영어 (기본), 스페인어, 프랑스어, 독일어, 일본어, 중국어, 포르투갈어, 이탈리아어, 러시아어, 한국어

**콘텐츠 유형**: 기술 문서, 사용자 가이드, API 문서, Commit 메시지, PR 설명

**예시 Workflow**:
```bash
/sc:document api/ --persona-scribe
/sc:git commit --persona-scribe
/sc:explain --persona-scribe=es complex-feature
```

**우선시하는 것**:
- 명확하고 전문적인 커뮤니케이션
- 청중에 맞는 언어
- 문화적 민감성 및 적응
- 높은 글쓰기 기준

## 각 Persona가 빛나는 순간 ⭐

### 개발 단계 매핑

**기획 & 설계 단계**:
- 🏗️ `architect` - 시스템 설계 및 Architecture 기획
- 🎨 `frontend` - UI/UX 설계 및 사용자 경험
- ✍️ `scribe` - 요구 사항 문서 및 사양

**구현 단계**:
- 🎨 `frontend` - UI Component 개발
- ⚙️ `backend` - API 및 Service 구현
- 🛡️ `security` - Security 구현 및 강화

**테스팅 & 품질 단계**:
- 🧪 `qa` - 테스트 전략 및 품질 보증
- ⚡ `performance` - Performance 테스팅 및 최적화
- 🔍 `analyzer` - 버그 조사 및 근본 원인 분석

**유지보수 & 개선 단계**:
- 🔄 `refactorer` - 코드 정리 및 리팩토링
- ⚡ `performance` - Performance 최적화
- 👨‍🏫 `mentor` - 지식 전달 및 문서화

**배포 & 운영 단계**:
- 🚀 `devops` - 배포 자동화 및 인프라
- 🛡️ `security` - Security 모니터링 및 규정 준수
- ✍️ `scribe` - 운영 문서 및 런북

### 문제 유형 매핑

**"코드가 느려요"** → ⚡ `performance`
**"무언가 고장났는데 이유를 모르겠어요"** → 🔍 `analyzer`
**"새로운 시스템을 설계해야 해요"** → 🏗️ `architect`
**"UI가 끔찍해요"** → 🎨 `frontend`
**"이거 안전한가요?"** → 🛡️ `security`
**"코드가 지저분해요"** → 🔄 `refactorer`
**"더 나은 테스트가 필요해요"** → 🧪 `qa`
**"배포가 계속 실패해요"** → 🚀 `devops`
**"이해가 안 돼요"** → 👨‍🏫 `mentor`
**"문서가 필요해요"** → ✍️ `scribe`

## Persona 조합 🤝

Persona는 종종 자동으로 함께 작동합니다. 일반적인 협업 패턴은 다음과 같습니다:

### 설계 & 구현
```bash
/sc:design user-dashboard
# 자동 활성화: 🏗️ architect (시스템 설계) + 🎨 frontend (UI 설계)
```

### Security 검토
```bash
/sc:analyze --focus security api/
# 자동 활성화: 🛡️ security (주) + ⚙️ backend (API 전문 지식)
```

### Performance 최적화
```bash
/sc:improve --focus performance slow-app/
# 자동 활성화: ⚡ performance (주) + 🎨 frontend (UI인 경우) 또는 ⚙️ backend (API인 경우)
```

### 품질 개선
```bash
/sc:improve --focus quality legacy-code/
# 자동 활성화: 🔄 refactorer (주) + 🧪 qa (테스팅) + 🏗️ architect (설계)
```

### 문서화 & 학습
```bash
/sc:document complex-feature --type guide
# 자동 활성화: ✍️ scribe (글쓰기) + 👨‍🏫 mentor (교육적 접근)
```

## 실제 예시 💡

### 전/후: 일반 vs Persona별

**전** (일반):
```bash
/sc:analyze auth.js
# → 기본 분석, 일반적인 조언
```

**후** (Security Persona):
```bash
/sc:analyze auth.js --persona-security
# → Security 중심 분석
# → 위협 모델링 관점
# → OWASP 규정 준수 확인
# → 취약점 패턴 감지
```

### 실제 자동 활성화

**Frontend 작업 감지**:
```bash
/sc:build react-components/
# 자동 활성화: 🎨 frontend
# → UI 중심 빌드 최적화
# → 접근성 확인
# → Performance 예산
# → 번들 크기 분석
```

**복잡한 Debugging**:
```bash
/sc:troubleshoot "payment processing randomly fails"
# 자동 활성화: 🔍 analyzer
# → 체계적인 조사 접근 방식
# → 증거 수집 방법론
# → 패턴 분석
# → 근본 원인 식별
```

### 수동 덮어쓰기 예시

**Security 관점 강제**:
```bash
/sc:analyze react-app/ --persona-security
# Frontend 코드임에도 불구하고 Security 관점에서 분석
# → XSS 취약점 확인
# → 인증 흐름 분석
# → 데이터 노출 위험
```

**작은 변경에 대한 Architecture 조언 얻기**:
```bash
/sc:improve small-utility.js --persona-architect
# 작은 코드에 Architecture적 사고 적용
# → 디자인 패턴 기회
# → 미래 확장성
# → 결합 분석
```

## 고급 사용법 🚀

### 수동 Persona 제어

**자동 활성화를 덮어써야 할 때**:
- 동일한 문제에 대해 다른 관점을 원할 때
- 자동 활성화가 특정 요구에 맞는 잘못된 Persona를 선택했을 때
- 학습 중이며 다른 전문가가 문제를 어떻게 접근하는지 보고 싶을 때

**덮어쓰는 방법**:
```bash
# 명시적 Persona 선택
/sc:analyze frontend-code/ --persona-security  # Frontend의 Security 관점
/sc:improve backend-api/ --persona-performance # Backend의 Performance 관점

# 여러 Persona Flag (마지막 것이 이김)
/sc:analyze --persona-frontend --persona-security # Security Persona 사용
```

### Persona별 Flag 및 설정

**Security Persona + 유효성 검사**:
```bash
/sc:analyze --persona-security --focus security --validate
# → 유효성 검사를 통한 최대 Security 초점
```

**Performance Persona + 벤치마킹**:
```bash
/sc:test --persona-performance --benchmark --focus performance
# → 메트릭을 사용한 Performance 중심 테스팅
```

**Mentor Persona + 상세 설명**:
```bash
/sc:explain complex-concept --persona-mentor --verbose
# → 전체 세부 정보가 포함된 교육적 설명
```

### 교차 도메인 전문 지식

**여러 관점이 필요할 때**:
```bash
# 다른 Persona를 사용한 순차적 분석
/sc:analyze --persona-security api/auth.js
/sc:analyze --persona-performance api/auth.js
/sc:analyze --persona-refactorer api/auth.js

# 또는 SuperClaude가 자동으로 조정하도록 둠
/sc:analyze --focus quality api/auth.js
# 자동 조정: Security + Performance + Refactorer 통찰력
```

## Persona별 일반적인 Workflow 💼

### 🏗️ Architect Workflow
```bash
# 시스템 설계
/sc:design microservices-architecture --persona-architect
/sc:estimate "migrate monolith to microservices" --persona-architect

# Architecture 검토
/sc:analyze --focus architecture --persona-architect large-system/
/sc:review --persona-architect critical-components/
```

### 🎨 Frontend Workflow
```bash
# Component 개발
/sc:build dashboard-components/ --persona-frontend
/sc:improve --focus accessibility --persona-frontend ui/

# Performance 최적화
/sc:analyze --focus performance --persona-frontend bundle/
/sc:test --persona-frontend --focus performance
```

### ⚙️ Backend Workflow
```bash
# API 개발
/sc:design rest-api --persona-backend
/sc:build api-endpoints/ --persona-backend

# 신뢰성 개선
/sc:improve --focus reliability --persona-backend services/
/sc:analyze --persona-backend --focus security api/
```

### 🛡️ Security Workflow
```bash
# Security 평가
/sc:scan --persona-security --focus security entire-app/
/sc:analyze --persona-security auth-flow/

# 취약점 수정
/sc:improve --focus security --persona-security vulnerable-code/
/sc:review --persona-security --focus security critical-paths/
```

### 🔍 Analyzer Workflow
```bash
# 버그 조사
/sc:troubleshoot "intermittent failures" --persona-analyzer
/sc:analyze --persona-analyzer --focus debugging problem-area/

# 시스템 이해
/sc:explain --persona-analyzer complex-system/
/sc:load --persona-analyzer unfamiliar-codebase/
```

## 빠른 참조 📋

### Persona 치트 시트

| Persona | 가장 적합한 용도 | 자동 활성화 조건 | 수동 Flag |
|---|---|---|---|
| 🏗️ architect | 시스템 설계, Architecture | "architecture", "design", "scalability" | `--persona-architect` |
| 🎨 frontend | UI/UX, 접근성 | "component", "responsive", "UI" | `--persona-frontend` |
| ⚙️ backend | API, Database, 신뢰성 | "API", "database", "service" | `--persona-backend` |
| 🛡️ security | Security, 규정 준수 | "security", "vulnerability", "auth" | `--persona-security` |
| ⚡ performance | 최적화, 속도 | "performance", "optimization", "slow" | `--persona-performance` |
| 🔍 analyzer | Debugging, 조사 | "analyze", "debug", "investigate" | `--persona-analyzer` |
| 🧪 qa | 테스팅, 품질 | "test", "quality", "validation" | `--persona-qa` |
| 🔄 refactorer | 코드 정리, 리팩토링 | "refactor", "cleanup", "quality" | `--persona-refactorer` |
| 🚀 devops | 배포, 인프라 | "deploy", "infrastructure", "CI/CD" | `--persona-devops` |
| 👨‍🏫 mentor | 학습, 설명 | "explain", "learn", "understand" | `--persona-mentor` |
| ✍️ scribe | 문서화, 글쓰기 | "document", "write", "guide" | `--persona-scribe` |

### 가장 유용한 조합

**Security 중심 개발**:
```bash
--persona-security --focus security --validate
```

**Performance 최적화**:
```bash
--persona-performance --focus performance --benchmark
```

**학습 및 이해**:
```bash
--persona-mentor --verbose --explain
```

**품질 개선**:
```bash
--persona-refactorer --focus quality --safe-mode
```

**전문 문서화**:
```bash
--persona-scribe --type guide --detailed
```

### 자동 활성화 트리거

**강력한 트리거** (보통 잘 작동함):
- "security audit" → 🛡️ security
- "UI component" → 🎨 frontend
- "API design" → ⚙️ backend
- "system architecture" → 🏗️ architect
- "debug issue" → 🔍 analyzer

**중간 트리거** (종종 작동함):
- "improve performance" → ⚡ performance
- "write tests" → 🧪 qa
- "clean up code" → 🔄 refactorer
- "deployment issue" → 🚀 devops

**Context에 따라 다른 트리거** (다양함):
- "document this" → ✍️ scribe 또는 👨‍🏫 mentor (청중에 따라 다름)
- "analyze this" → 🔍 analyzer, 🏗️ architect 또는 도메인 전문가 (내용에 따라 다름)

## Persona 문제 해결 🚨

### 일반적인 문제

**"잘못된 Persona가 활성화됨"**
- 명시적 Persona Flag 사용: `--persona-security`
- 키워드가 자동 활성화를 트리거했는지 확인
- 요청에 더 구체적인 언어 사용

**"Persona가 작동하지 않는 것 같음"**
- Persona 이름 철자 확인: `--persona-fronted`가 아닌 `--persona-frontend`
- 일부 Persona는 특정 Command와 더 잘 작동함
- 관련 Flag와 결합 시도: `--focus security --persona-security`

**"여러 관점을 원함"**
- 다른 Persona로 동일한 Command를 수동으로 실행
- 더 넓은 초점 Flag 사용: `--focus quality` (여러 Persona 활성화)
- 복잡한 요청으로 SuperClaude가 자동으로 조정하도록 둠

**"Persona가 너무 집중됨"**
- 더 일반적인 다른 Persona 시도
- 더 넓은 설명을 위해 Mentor Persona 사용
- 더 많은 Context를 위해 `--verbose`와 결합

### 자동 활성화를 덮어써야 할 때

**덮어써야 할 때**:
- 자동 활성화가 잘못된 전문가를 선택했을 때
- 다른 관점에서 배우고 싶을 때
- 일반적인 도메인 경계를 벗어나 작업할 때
- 엣지 케이스에 대한 특정 전문 지식이 필요할 때

**효과적으로 덮어쓰는 방법**:
```bash
# 특정 관점 강제
/sc:analyze frontend-code/ --persona-security  # Frontend의 Security 관점

# 여러 관점 결합
/sc:analyze api/ --persona-security
/sc:analyze api/ --persona-performance  # 다른 관점을 위해 별도로 실행

# 일반 분석 사용
/sc:analyze --no-persona  # Persona 자동 활성화 비활성화
```

## 효과적인 Persona 사용 팁 💡

### 시작하기 (솔직한 방법)
1. **처음에는 Persona를 완전히 무시하세요** - 자동 활성화가 모든 것을 처리합니다
2. **기본 Command를 정상적으로 사용하세요** - `/analyze`, `/build`, `/improve`는 Persona 지식 없이도 잘 작동합니다
3. **무슨 일이 일어나는지 주목하세요** - 다양한 유형의 전문 지식이 자연스럽게 나타나는 것을 보게 될 것입니다
4. **자동화를 신뢰하세요** - SuperClaude는 보통 수동 선택보다 더 나은 전문가를 선택합니다

### 고급화하기 (원한다면)
1. **수동 덮어쓰기를 실험해보세요** - Frontend 코드에 `--persona-security`를 시도하여 다른 관점을 얻어보세요
2. **팀원들을 배우세요** - 궁금해지면 개별 Persona에 대해 읽어보세요
3. **Persona 조합을 지켜보세요** - 여러 전문가가 복잡한 문제에 대해 어떻게 협력하는지 보세요
4. **학습을 위해 사용하세요** - 다른 Persona에게 동일한 질문을 하여 다른 접근 방식을 보세요

### 모범 사례 (간단하게 유지)
- **먼저 자동 활성화가 작동하도록 두세요** - 다른 관점을 원할 때만 덮어쓰세요
- **너무 깊이 생각하지 마세요** - 필요할 때 올바른 전문가가 나타납니다
- **실험을 위해 사용하세요** - 학습을 위해 동일한 문제에 다른 Persona를 시도해보세요
- **지능을 신뢰하세요** - 자동 활성화는 패턴에서 학습하고 계속해서 더 나아집니다

---

## 최종 참고 사항 📝

**Persona에 대한 진짜 진실** 💯:
- **자동 활성화는 직접 전문가를 선택하려고 하는 것보다 보통 꽤 잘 작동합니다**
- **이 가이드를 완전히 무시해도** 종종 유용한 전문가 지원을 받을 수 있습니다
- **Persona는 당신을 돕기 위해 존재합니다** - 관리해야 할 복잡성을 만들기 위해서가 아닙니다
- **학습은 Persona 설명을 공부하는 것이 아니라** 사용을 통해 자연스럽게 일어납니다 😊

**팀에 압도당하지 마세요** 🧘‍♂️:
- 각 Persona가 무엇을 하는지 알 필요가 없습니다
- SuperClaude는 보통 전문가 선택을 합리적으로 잘 처리합니다
- 위의 상세 설명은 필요성이 아니라 호기심을 위한 것입니다
- 자동 활성화가 작동하도록 둠으로써 놓치는 것은 없습니다

**수동으로 Persona를 선택할 수 있는 경우**:
- **호기심** - "Security 전문가는 이 Frontend 코드에 대해 어떻게 생각할까?"
- **학습** - "다른 전문가는 이 문제에 어떻게 접근할까?"
- **실험** - "Performance 렌즈를 통해 이것을 보자"
- **덮어쓰기** - "이 작은 유틸리티 함수에 대한 Architecture 조언을 원해"

**간단하게 유지하세요** 🎯:
- `/analyze some-code/`와 같은 일반 Command를 사용하세요
- 올바른 전문가가 자동으로 나타나도록 하세요
- 수동 Persona 제어는 필요할 때가 아니라 원할 때 사용할 수 있습니다
- 당신을 돕는 사람을 관리하는 것이 아니라 당신의 작업에 집중하세요

---

*11명의 전문가를 보유한 이 모든 명백한 복잡성 뒤에는, SuperClaude는 사용하기 간단하도록 노력합니다. 그냥 코딩을 시작하면 필요할 때 유용한 전문가가 보통 나타납니다! 🚀*
