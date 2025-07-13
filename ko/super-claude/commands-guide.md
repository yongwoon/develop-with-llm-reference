# SuperClaude Commands 가이드 🛠️

## 💡 너무 깊이 생각하지 마세요 - SuperClaude가 도와드립니다

**17개 Command에 대한 진실**: 이 Command들을 모두 외울 필요는 없습니다. 그냥 `/sc:analyze`나 `/sc:implement`로 시작해보고 어떤 일이 일어나는지 확인하세요!

**일반적인 작동 방식은 다음과 같습니다:**

- Claude Code에 `/`를 입력 → 사용 가능한 Command 표시
- `/sc:analyze`, `/sc:build`, `/sc:improve`와 같은 기본 Command 사용
- **SuperClaude는 각 상황에 맞는 유용한 Tool과 전문가를 선택하려고 시도합니다**
- 익숙해질수록 더 많은 Command가 유용해집니다

**자동 활성화는 정말 멋집니다** 🪄 - SuperClaude는 사용자가 하려는 작업을 감지하고 관련 전문가(Security 전문가, Performance 최적화 전문가 등)를 직접 관리하지 않아도 활성화하려고 시도합니다. 보통 잘 작동합니다! 😊

---

## "그냥 한번 시도해보세요" 빠른 목록 🚀

**여기서 시작하세요** (읽을 필요 없음):

```bash
/sc:help                    # 사용 가능한 기능 확인
/sc:analyze src/            # 코드를 스마트하게 분석 시도
/sc:workflow feature-100-prd.md  # PRD로부터 단계별 구현 Workflow 생성
/sc:implement user-auth     # Feature 및 Component 생성 (v2 /build 대체)
/sc:build                   # 지능적인 Project 빌드 시도
/sc:improve messy-file.js   # 코드 정리 시도
/sc:troubleshoot "error"    # 문제 해결 지원 시도
```

**솔직히 이 정도면 시작하기에 충분합니다.** 아래의 모든 내용은 다른 어떤 Tool들이 있는지 궁금해질 때를 위한 것입니다. 🛠️

---

모든 16개 SuperClaude 슬래시 Command에 대한 실용적인 가이드입니다. 어떤 것이 잘 작동하고 어떤 것이 아직 미흡한지에 대해 솔직하게 알려드립니다.

## 빠른 참조 📋

_(이것을 외울 필요는 정말 없습니다 - 유용해 보이는 것을 선택하세요)_

| Command            | 목적                | 자동 활성화                 | 가장 적합한 용도                       |
| ------------------ | ------------------- | --------------------------- | -------------------------------------- |
| `/sc:analyze`      | 스마트 코드 분석    | Security/Performance 전문가 | 문제 찾기, Codebase 이해               |
| `/sc:build`        | 지능적인 빌드       | Frontend/Backend 전문가     | Compilation, Bundling, Deployment 준비 |
| `/sc:implement`    | Feature 구현        | 특정 Domain 전문가          | Feature, Component, API, Service 생성  |
| `/sc:improve`      | 자동 코드 정리      | 품질 전문가                 | Refactoring, 최적화, 품질 수정         |
| `/sc:troubleshoot` | 문제 조사           | Debug 전문가                | Debugging, 문제 조사                   |
| `/sc:test`         | 스마트 테스팅       | QA 전문가                   | Test 실행, Coverage 분석               |
| `/sc:document`     | 자동 문서화         | 글쓰기 전문가               | README 파일, 코드 주석, 가이드         |
| `/sc:git`          | 향상된 git Workflow | DevOps 전문가               | 스마트 Commit, Branch 관리             |
| `/sc:design`       | System 설계 지원    | Architecture 전문가         | Architecture 기획, API 설계            |
| `/sc:explain`      | 학습 보조           | 교육 전문가                 | 개념 학습, 코드 이해                   |
| `/sc:cleanup`      | 부채 감소           | Refactoring 전문가          | Dead code 제거, 파일 정리              |
| `/sc:load`         | Context 이해        | 분석 전문가                 | Project 분석, Codebase 이해            |
| `/sc:estimate`     | 스마트 견적         | 기획 전문가                 | 시간/노력 기획, 복잡도 분석            |
| `/sc:spawn`        | 복잡한 Workflow     | Orchestration System        | 다단계 작업, Workflow 자동화           |
| `/sc:task`         | Project 관리        | 기획 System                 | 장기 Feature 기획, Task 추적           |
| `/sc:workflow`     | 구현 기획           | Workflow System             | PRD로부터 단계별 Workflow 생성         |
| `/sc:index`        | Command 탐색        | 도움말 System               | Task에 맞는 Command 찾기               |

**Pro tip**: 유용해 보이는 것을 그냥 시도해보세요. SuperClaude는 보통 각 상황에 맞는 유용한 전문가와 Tool을 활성화하려고 시도합니다! 🎯

## 개발 Command 🔨

### `/workflow` - 구현 Workflow 생성기 🗺️

**기능**: PRD 및 Feature 요구사항을 분석하여 포괄적인 단계별 구현 Workflow를 생성합니다.

**유용한 점**: PRD를 가져와 전문가 가이드, 종속성 매핑, Task Orchestration을 포함한 구조화된 구현 계획으로 분해합니다! 🎯

**사용 시점**:

- PRD 또는 사양서로 새로운 Feature를 시작할 때
- 명확한 구현 Roadmap이 필요할 때
- 구현 전략에 대한 전문가 가이드가 필요할 때
- 여러 종속성이 있는 복잡한 Feature를 기획할 때

**마법**: Feature 요구사항에 따라 적절한 전문가 Persona(Architect, Security, Frontend, Backend) 및 MCP Server(패턴용 Context7, 복잡한 분석용 Sequential)를 자동으로 활성화합니다.

**예시**:

```bash
/sc:workflow docs/feature-100-prd.md --strategy systematic --c7 --sequential
/sc:workflow "user authentication system" --persona security --output detailed
/sc:workflow payment-api --strategy mvp --risks --dependencies
```

**결과물**:

- **Roadmap 형식**: 타임라인이 포함된 단계별 구현 계획
- **Tasks 형식**: 정리된 Epic, Story, 실행 가능한 Task
- **Detailed 형식**: 시간 추정치가 포함된 단계별 지침
- **Risk Assessment**: 잠재적 문제 및 완화 전략
- **Dependency Mapping**: 내부 및 외부 종속성
- **Expert Guidance**: 특정 Domain의 모범 사례 및 패턴

### `/implement` - Feature 구현

**기능**: 지능적인 전문가 활성화를 통해 Feature, Component 및 기능을 구현합니다.

**유용한 점**: SuperClaude는 구현하는 내용에 따라 적절한 전문가(Frontend, Backend, Security)와 Tool을 자동으로 활성화합니다! 🎯

**사용 시점**:

- 새로운 Feature 또는 Component 생성 (v2의 `/build` 기능 대체)
- API, Service 또는 Module 구현
- 최신 Framework으로 UI Component 빌드
- 비즈니스 로직 및 통합 개발

**기본 구문**:

```bash
/sc:implement user authentication system      # 전체 Feature 구현
/sc:implement --type component LoginForm      # 특정 Component 생성
/sc:implement --type api user-management      # API Endpoint 빌드
/sc:implement --framework react dashboard     # Framework별 구현
```

**유용한 Flag**:

- `--type component|api|service|feature|module` - 구현 유형
- `--framework react|vue|express|django|etc` - 대상 Framework
- `--safe` - 보수적인 구현 접근 방식
- `--iterative` - 검증을 통한 단계별 개발
- `--with-tests` - Test 구현 포함
- `--documentation` - 코드와 함께 문서 생성

**실제 예시**:

```bash
/sc:implement user authentication --type feature --with-tests
/sc:implement dashboard component --type component --framework react
/sc:implement REST API for orders --type api --safe
/sc:implement payment processing --type service --iterative
/sc:implement search functionality --framework vue --documentation
```

**자동 활성화 패턴**:

- **Frontend**: UI Component, React/Vue/Angular → Frontend Persona + Magic MCP
- **Backend**: API, Service, Database → Backend Persona + Context7
- **Security**: 인증, 결제, 민감 데이터 → Security Persona + Validation
- **복잡한 Feature**: 다단계 구현 → Sequential MCP + Architect Persona

**주의할 점**:

- 더 나은 결과를 위해 `--type`을 지정하세요 (component vs service vs feature)
- 특정 기술 스택으로 작업할 때 `--framework`를 사용하세요
- Production 코드에는 `--safe`를, 복잡한 Feature에는 `--iterative`를 시도해보세요
- 기억하세요: 이것은 실제 코드 구현을 위해 v2의 `/build`를 대체합니다

---

### `/build` - Project 빌드

**기능**: 스마트한 오류 처리로 Project를 빌드, Compile 및 Package합니다.

**쉬운 방법**: 그냥 `/sc:build`를 입력하면 SuperClaude가 빌드 시스템을 파악하려고 시도합니다! 🎯

**사용 시점**:

- Project를 Compile/Bundle해야 할 때 (그냥 `/sc:build` 시도)
- 빌드 프로세스가 실패하고 Debugging에 도움이 필요할 때
- 빌드 최적화 설정 (필요한 것을 감지하려고 시도)
- Deployment 준비

**기본 구문**:

```bash
/sc:build                          # 현재 Project 빌드
/sc:build --type prod              # Production 빌드
/sc:build --clean                  # 클린 빌드 (오래된 Artifact 제거)
/sc:build --optimize               # 최적화 활성화
/sc:build src/                     # 특정 Directory 빌드
```

**유용한 Flag**:

- `--type dev|prod|test` - 빌드 유형
- `--clean` - 빌드 전 정리
- `--optimize` - 빌드 최적화 활성화
- `--verbose` - 상세 빌드 출력 표시

**실제 예시**:

```bash
/sc:build --type prod --optimize   # 최적화된 Production 빌드
/sc:build --clean --verbose        # 상세 출력을 포함한 클린 빌드
/sc:build src/components           # Component 폴더만 빌드
```

**주의할 점**:

- 일반적인 빌드 Tool(npm, webpack 등)에서 가장 잘 작동합니다
- 매우 맞춤화된 빌드 설정에서는 어려움을 겪을 수 있습니다
- 빌드 Tool이 PATH에 있는지 확인하세요

---

### `/design` - System & Component 설계

**기능**: System Architecture, API 설계 및 Component 사양을 생성합니다.

**사용 시점**:

- 새로운 Feature 또는 System 기획
- API 또는 Database 설계 필요
- Component Architecture 생성
- System 관계 문서화

**기본 구문**:

```bash
/sc:design user-auth-system        # 사용자 인증 System 설계
/sc:design --type api auth         # API 부분만 설계
/sc:design --format spec payment   # 공식 사양서 생성
```

**유용한 Flag**:

- `--type architecture|api|component|database` - 설계 초점
- `--format diagram|spec|code` - 출력 형식
- `--iterative` - 반복을 통해 설계 구체화

**실제 예시**:

```bash
/sc:design --type api user-management    # 사용자 관리 API 설계
/sc:design --format spec chat-system     # 채팅 System 사양서 생성
/sc:design --type database ecommerce     # Database Schema 설계
```

**주의할 점**:

- 코드 생성보다는 개념적입니다
- 출력 품질은 요구사항을 얼마나 명확하게 설명하는지에 따라 달라집니다
- 기획 단계에 적합하며, 구현 세부사항에는 덜 적합합니다

## 분석 Command 🔍

### `/analyze` - 코드 분석

**기능**: 코드 품질, Security, Performance 및 Architecture에 대한 포괄적인 분석.

**유용한 점**: SuperClaude는 어떤 종류의 분석이 필요한지 감지하려고 시도하며 보통 관련 전문가를 선택합니다! 🔍

**사용 시점**:

- 익숙하지 않은 Codebase 이해 (어떤 폴더든 가리키기만 하면 됨)
- Security 취약점 찾기 (Security 전문가가 보통 개입)
- Performance 병목 현상 찾기 (Performance 전문가가 보통 도움)
- 코드 품질 평가 (품질 전문가가 종종 담당)

**기본 구문**:

```bash
/sc:analyze src/                   # 전체 src Directory 분석
/sc:analyze --focus security       # Security 문제에 집중
/sc:analyze --depth deep app.js    # 특정 파일의 심층 분석
```

**유용한 Flag**:

- `--focus quality|security|performance|architecture` - 분석 초점
- `--depth quick|deep` - 분석 깊이
- `--format text|json|report` - 출력 형식

**실제 예시**:

```bash
/sc:analyze --focus security --depth deep     # 심층 Security 분석
/sc:analyze --focus performance src/api/      # API의 Performance 분석
/sc:analyze --format report .                 # 분석 보고서 생성
```

**주의할 점**:

- 대규모 Codebase에서는 시간이 걸릴 수 있습니다
- Security 분석은 꽤 좋지만, Performance 분석은 다양합니다
- 일반적인 언어(JS, Python 등)에서 가장 잘 작동합니다

---

### `/troubleshoot` - 문제 조사

**기능**: 체계적인 Debugging 및 문제 조사.

**사용 시점**:

- 무언가 고장 났는데 이유를 모를 때
- 체계적인 Debugging 접근 방식이 필요할 때
- 오류 메시지가 혼란스러울 때
- Performance 문제 조사

**기본 구문**:

```bash
/sc:troubleshoot "login not working"     # 로그인 문제 조사
/sc:troubleshoot --logs error.log        # 오류 로그 분석
/sc:troubleshoot performance             # Performance 문제 해결
```

**유용한 Flag**:

- `--logs <file>` - 로그 파일 분석 포함
- `--systematic` - 구조화된 Debugging 접근 방식 사용
- `--focus network|database|frontend` - 초점 영역

**실제 예시**:

```bash
/sc:troubleshoot "API returning 500" --logs server.log
/sc:troubleshoot --focus database "slow queries"
/sc:troubleshoot "build failing" --systematic
```

**주의할 점**:

- 구체적인 오류 설명과 함께 더 잘 작동합니다
- 가능하면 관련 오류 메시지와 로그를 포함하세요
- 처음에는 명백한 것을 제안할 수 있습니다 (보통 좋은 현상입니다!)

---

### `/explain` - 교육적 설명

**기능**: 코드, 개념 및 기술을 교육적인 방식으로 설명합니다.

**사용 시점**:

- 새로운 기술이나 패턴 학습
- 복잡한 코드 이해
- 팀원을 위한 명확한 설명 필요
- 까다로운 개념 문서화

**기본 구문**:

```bash
/sc:explain async/await               # async/await 개념 설명
/sc:explain --code src/utils.js       # 특정 코드 파일 설명
/sc:explain --beginner React hooks    # 초보자 친화적인 설명
```

**유용한 Flag**:

- `--beginner` - 더 간단한 설명
- `--advanced` - 기술적 깊이
- `--code <file>` - 특정 코드 설명
- `--examples` - 실제 예시 포함

**실제 예시**:

```bash
/sc:explain --beginner "what is REST API"
/sc:explain --code src/auth.js --advanced
/sc:explain --examples "React context patterns"
```

**주의할 점**:

- 잘 알려진 개념에 대해서는 훌륭하지만, 매우 전문적인 주제에 대해서는 어려움을 겪을 수 있습니다
- 모호한 "이 Codebase 설명해줘"보다 구체적인 질문에 더 좋습니다
- 자신의 경험 수준에 대한 Context를 포함하세요

## 품질 Command ✨

### `/improve` - 코드 향상

**기능**: 코드 품질, Performance 및 유지보수성에 대한 체계적인 개선.

**사용 시점**:

- 지저분한 코드 Refactoring
- Performance 최적화
- 모범 사례 적용
- 오래된 코드 현대화

**기본 구문**:

```bash
/sc:improve src/legacy/            # 레거시 코드 개선
/sc:improve --type performance     # Performance에 집중
/sc:improve --safe src/utils.js    # 안전하고 위험이 낮은 개선만
```

**유용한 Flag**:

- `--type quality|performance|maintainability|style` - 개선 초점
- `--safe` - 위험이 낮은 변경만 적용
- `--preview` - 변경될 내용을 실행하지 않고 표시

**실제 예시**:

```bash
/sc:improve --type performance --safe src/api/
/sc:improve --preview src/components/LegacyComponent.js
/sc:improve --type style . --safe
```

**주의할 점**:

- 항상 `--preview`를 먼저 사용하여 변경될 내용을 확인하세요
- `--safe`는 친구입니다 - 위험한 Refactoring을 방지합니다
- 전체 Codebase보다는 작은 파일/Module에서 가장 잘 작동합니다

---

### `/cleanup` - 기술 부채 감소

**기능**: Dead code, 사용하지 않는 Import를 제거하고 파일 구조를 정리합니다.

**사용 시점**:

- Codebase가 복잡하게 느껴질 때
- 사용하지 않는 Import/변수가 많을 때
- 파일 구성이 지저분할 때
- 주요 Refactoring 전

**기본 구문**:

```bash
/sc:cleanup src/                   # src Directory 정리
/sc:cleanup --dead-code            # Dead code 제거에 집중
/sc:cleanup --imports package.js   # 특정 파일의 Import 정리
```

**유용한 Flag**:

- `--dead-code` - 사용하지 않는 코드 제거
- `--imports` - Import 문 정리
- `--files` - 파일 구조 재구성
- `--safe` - 보수적인 정리만

**실제 예시**:

```bash
/sc:cleanup --dead-code --safe src/utils/
/sc:cleanup --imports src/components/
/sc:cleanup --files . --safe
```

**주의할 점**:

- 공격적일 수 있으므로 변경 사항을 항상 신중하게 검토하세요
- 모든 Dead code를 잡지 못할 수 있습니다 (특히 동적 Import)
- 전체 Project보다는 작은 섹션에서 실행하는 것이 좋습니다

---

### `/test` - 테스팅 & 품질 보증

**기능**: Test를 실행하고, Coverage 보고서를 생성하며, Test 품질을 유지합니다.

**사용 시점**:

- Test Suite 실행
- Test Coverage 확인
- Test 보고서 생성
- 지속적인 테스팅 설정

**기본 구문**:

```bash
/sc:test                           # 모든 Test 실행
/sc:test --type unit               # Unit Test만 실행
/sc:test --coverage                # Coverage 보고서 생성
/sc:test --watch src/              # 개발용 Watch 모드
```

**유용한 Flag**:

- `--type unit|integration|e2e|all` - Test 유형
- `--coverage` - Coverage 보고서 생성
- `--watch` - Watch 모드에서 Test 실행
- `--fix` - 실패하는 Test를 자동으로 수정 시도

**실제 예시**:

```bash
/sc:test --type unit --coverage
/sc:test --watch src/components/
/sc:test --type e2e --fix
```

**주의할 점**:

- Test Framework이 올바르게 구성되어 있어야 합니다
- Coverage 보고서는 기존 Test 설정에 따라 다릅니다
- `--fix`는 실험적입니다 - 변경되는 내용을 검토하세요

## 문서화 Command 📝

### `/document` - 집중 문서화

**기능**: 특정 Component, 함수 또는 Feature에 대한 문서를 생성합니다.

**사용 시점**:

- README 파일 필요
- API 문서 작성
- 코드 주석 추가
- 사용자 가이드 생성

**기본 구문**:

```bash
/sc:document src/api/auth.js       # 인증 Module 문서화
/sc:document --type api            # API 문서화
/sc:document --style brief README  # 간략한 README 파일
```

**유용한 Flag**:

- `--type inline|external|api|guide` - 문서 유형
- `--style brief|detailed` - 상세 수준
- `--template` - 특정 문서 Template 사용

**실제 예시**:

```bash
/sc:document --type api src/controllers/
/sc:document --style detailed --type guide user-onboarding
/sc:document --type inline src/utils/helpers.js
```

**주의할 점**:

- 전체 Project보다는 특정 파일/함수에서 더 좋습니다
- 품질은 코드가 얼마나 잘 구조화되어 있는지에 따라 달라집니다
- Project의 문서 스타일에 맞게 일부 편집이 필요할 수 있습니다

## Project 관리 Command 📊

### `/estimate` - Project 견적

**기능**: 개발 Task에 대한 시간, 노력 및 복잡도를 견적합니다.

**사용 시점**:

- 새로운 Feature 기획
- Sprint 기획
- Project 복잡도 이해
- 리소스 할당

**기본 구문**:

```bash
/sc:estimate "add user authentication"    # 인증 Feature 견적
/sc:estimate --detailed shopping-cart     # 상세 내역
/sc:estimate --complexity user-dashboard  # 복잡도 분석
```

**유용한 Flag**:

- `--detailed` - Task의 상세 내역
- `--complexity` - 기술적 복잡도에 집중
- `--team-size <n>` - 견적에 팀 규모 고려

**실제 예시**:

```bash
/sc:estimate --detailed "implement payment system"
/sc:estimate --complexity --team-size 3 "migrate to microservices"
/sc:estimate "add real-time chat" --detailed
```

**주의할 점**:

- 견적은 대략적입니다 - 절대적인 것이 아니라 시작점으로 사용하세요
- 명확하고 구체적인 Feature 설명과 함께 더 잘 작동합니다
- 기술 스택에 대한 팀의 경험을 고려하세요

---

### `/task` - 장기 Project 관리

**기능**: 복잡하고 여러 Session에 걸친 개발 Task 및 Feature를 관리합니다.

**사용 시점**:

- 며칠/몇 주가 걸리는 Feature 기획
- 대규모 Project 분해
- 여러 Session에 걸친 진행 상황 추적
- 팀 작업 조정

**기본 구문**:

```bash
/sc:task create "implement user dashboard"  # 새 Task 생성
/sc:task status                            # Task 상태 확인
/sc:task breakdown "payment integration"    # 하위 Task로 분해
```

**유용한 Flag**:

- `create` - 새 장기 Task 생성
- `status` - 현재 Task 상태 확인
- `breakdown` - 큰 Task를 작은 Task로 분해
- `--priority high|medium|low` - Task 우선순위 설정

**실제 예시**:

```bash
/sc:task create "migrate from REST to GraphQL" --priority high
/sc:task breakdown "e-commerce checkout flow"
/sc:task status
```

**주의할 점**:

- 아직 실험적입니다 - Session 간에 안정적으로 유지되지 않을 때가 있습니다 😅
- 실제 Project 관리보다는 기획에 더 적합합니다
- 요구사항을 구체적으로 명시할 때 가장 잘 작동합니다

---

### `/spawn` - 복잡한 작업 Orchestration

**기능**: 복잡한 다단계 작업 및 Workflow를 조정합니다.

**사용 시점**:

- 여러 Tool/System을 포함하는 작업
- 병렬 Workflow 조정
- 복잡한 Deployment 프로세스
- 다단계 데이터 처리

**기본 구문**:

```bash
/sc:spawn deploy-pipeline          # Deployment Orchestration
/sc:spawn --parallel migrate-data  # 병렬 데이터 마이그레이션
/sc:spawn setup-dev-environment    # 복잡한 개발 환경 설정
```

**유용한 Flag**:

- `--parallel` - 가능할 때 작업을 병렬로 실행
- `--sequential` - 순차적 실행 강제
- `--monitor` - 작업 진행 상황 모니터링

**실제 예시**:

```bash
/sc:spawn --parallel "test and deploy to staging"
/sc:spawn setup-ci-cd --monitor
/sc:spawn --sequential database-migration
```

**주의할 점**:

- 가장 복잡한 Command - 약간의 미흡함을 예상하세요
- 임시 작업보다는 잘 정의된 Workflow에 더 적합합니다
- 올바르게 작동하려면 여러 번의 반복이 필요할 수 있습니다

## 버전 관리 Command 🔄

### `/git` - 향상된 Git 작업

**기능**: 지능적인 Commit 메시지 및 Workflow 최적화를 통한 Git 작업.

**사용 시점**:

- 더 나은 메시지로 Commit 만들기
- Branch 관리
- 복잡한 git Workflow
- Git 문제 해결

**기본 구문**:

```bash
/sc:git commit                     # 자동 생성된 메시지로 스마트 Commit
/sc:git --smart-commit add .       # 스마트 메시지로 추가 및 Commit
/sc:git branch feature/new-auth    # 새 Branch 생성 및 전환
```

**유용한 Flag**:

- `--smart-commit` - 지능적인 Commit 메시지 생성
- `--branch-strategy` - Branch 이름 규칙 적용
- `--interactive` - 복잡한 작업을 위한 대화형 모드

**실제 예시**:

```bash
/sc:git --smart-commit "fixed login bug"
/sc:git branch feature/user-dashboard --branch-strategy
/sc:git merge develop --interactive
```

**주의할 점**:

- 스마트 Commit 메시지는 꽤 좋지만 검토하세요
- 일반적인 git Workflow를 따르고 있다고 가정합니다
- 나쁜 git 습관을 고쳐주지는 않지만, 더 쉽게 만들어줍니다

## 유틸리티 Command 🔧

### `/index` - Command 탐색

**기능**: Task에 맞는 올바른 Command를 찾도록 도와줍니다.

**사용 시점**:

- 어떤 Command를 사용해야 할지 모를 때
- 사용 가능한 Command 탐색
- Command 기능에 대해 학습

**기본 구문**:

```bash
/sc:index                          # 모든 Command 나열
/sc:index testing                  # 테스팅 관련 Command 찾기
/sc:index --category analysis      # 분석 카테고리의 Command
```

**유용한 Flag**:

- `--category <cat>` - Command 카테고리별 필터링
- `--search <term>` - Command 설명 검색

**실제 예시**:

```bash
/sc:index --search "performance"
/sc:index --category quality
/sc:index git
```

**주의할 점**:

- 간단하지만 발견에 유용합니다
- 16개 Command를 모두 기억하려고 하는 것보다 낫습니다

---

### `/load` - Project Context 로딩

**기능**: 더 나은 이해를 위해 Project Context를 로드하고 분석합니다.

**사용 시점**:

- 익숙하지 않은 Project에서 작업 시작
- Project 구조를 이해해야 할 때
- 주요 변경 전
- 팀원 온보딩

**기본 구문**:

```bash
/sc:load                           # 현재 Project Context 로드
/sc:load src/                      # 특정 Directory Context 로드
/sc:load --deep                    # Project 구조의 심층 분석
```

**유용한 Flag**:

- `--deep` - 포괄적인 Project 분석
- `--focus <area>` - 특정 Project 영역에 집중
- `--summary` - Project 요약 생성

**실제 예시**:

```bash
/sc:load --deep --summary
/sc:load src/components/ --focus architecture
/sc:load . --focus dependencies
```

**주의할 점**:

- 대규모 Project에서는 시간이 걸릴 수 있습니다
- 개발 중보다는 Project 시작 시에 더 유용합니다
- 온보딩에 도움이 되지만 좋은 문서를 대체할 수는 없습니다

## Command 팁 & 패턴 💡

### 효과적인 Flag 조합

```bash
# 안전한 개선 Workflow
/sc:improve --preview src/component.js    # 변경될 내용 확인
/sc:improve --safe src/component.js       # 안전한 변경만 적용

# 포괄적인 분석
/sc:analyze --focus security --depth deep
/sc:test --coverage
/sc:document --type api

# 스마트 git Workflow
/sc:git add .
/sc:git --smart-commit --branch-strategy

# Project 이해 Workflow
/sc:load --deep --summary
/sc:analyze --focus architecture
/sc:document --type guide
```

### 일반적인 Workflow

**새 Project 온보딩**:

```bash
/sc:load --deep --summary
/sc:analyze --focus architecture
/sc:test --coverage
/sc:document README
```

**버그 조사**:

```bash
/sc:troubleshoot "specific error message" --logs
/sc:analyze --focus security
/sc:test --type unit affected-component
```

**코드 품질 개선**:

```bash
/sc:analyze --focus quality
/sc:improve --preview src/
/sc:cleanup --safe
/sc:test --coverage
```

**배포 전 체크리스트**:

```bash
/sc:test --type all --coverage
/sc:analyze --focus security
/sc:build --type prod --optimize
/sc:git --smart-commit
```

### Command 문제 해결

**Command가 예상대로 작동하지 않나요?**

- `--help`를 추가하여 모든 옵션을 확인해보세요
- 가능하면 `--preview` 또는 `--safe` Flag를 사용하세요
- 더 작은 범위(전체 Project 대신 단일 파일)로 시작하세요

**분석이 너무 오래 걸리나요?**

- `--focus`를 사용하여 범위를 좁히세요
- 심층 분석 대신 `--depth quick`을 시도해보세요
- 더 작은 Directory를 먼저 분석하세요

**빌드/Test Command가 실패하나요?**

- Tool이 PATH에 있는지 확인하세요
- 구성 파일이 예상 위치에 있는지 확인하세요
- 기본 Command를 직접 먼저 실행해보세요

**어떤 Command를 사용해야 할지 모르겠나요?**

- `/index`를 사용하여 사용 가능한 Command를 찾아보세요
- 위의 빠른 참조 표를 보세요
- 가장 구체적인 Command를 먼저 시도한 다음 더 넓은 Command를 시도하세요

---

## 최종 참고 사항 📝

**이 Command들에 대한 진짜 진실** 💯:

- **그냥 시도해보세요** - 이 가이드를 먼저 공부할 필요 없습니다
- **기본부터 시작하세요** - `/analyze`, `/build`, `/improve`가 대부분의 요구를 충족합니다
- **자동 활성화가 작동하게 두세요** - SuperClaude는 보통 유용한 전문가를 선택합니다
- **자유롭게 실험하세요** - 먼저 어떤 일이 일어날지 보고 싶다면 `--preview`를 사용하세요

**아직 미흡한 점:**

- 복잡한 Orchestration(spawn, task)은 약간 불안정할 수 있습니다
- 일부 분석은 Project 설정에 크게 의존합니다
- 일부 Command의 오류 처리가 더 개선될 수 있습니다

**계속해서 나아지고 있습니다:**

- 사용자 피드백을 바탕으로 Command를 적극적으로 개선합니다
- 최신 Command(analyze, improve)가 더 잘 작동하는 경향이 있습니다
- 자동 활성화는 계속해서 더 똑똑해지고 있습니다

**이것을 외우느라 스트레스 받지 마세요** 🧘‍♂️

- SuperClaude는 사용하면서 발견할 수 있도록 설계되었습니다
- `/`를 입력하여 사용 가능한 Command를 확인하세요
- Command는 `--help`를 사용할 때 할 수 있는 일을 제안합니다
- 지능적인 라우팅이 대부분의 복잡성을 처리합니다

**도움이 필요하신가요?** 막혔다면 GitHub issue를 확인하거나 새로 만드세요! 🚀

---

_즐거운 코딩 되세요! 그냥 이 가이드의 대부분을 건너뛰고 직접 해보면서 배울 수 있다는 것을 기억하세요. 🎯_
