# SuperClaude 사용자 가이드 🚀

## 🎯 간단한 진실

**겉보기의 복잡함 뒤에, SuperClaude는 실제로 사용하기 간단합니다.**

모든 Command, Flag, Persona를 배울 필요가 없습니다. 그냥 사용 시작하세요! 🎈

SuperClaude는 당신이 무엇을 필요로 하는지 파악하려는 **지능형 Routing System**을 가지고 있습니다:
- `/analyze some-code/`를 입력하면 → 올바른 분석 Tool을 선택합니다
- Security에 대해 물어보면 → Security 전문가가 자동으로 활성화됩니다
- Frontend 작업을 하면 → UI 전문가가 담당합니다
- 무언가를 Debugging하면 → 조사 모드가 시작됩니다

**학습은 사용 중에 나타납니다** - 설명서를 먼저 공부하지 않고도 자연스럽게 작동하는 것을 발견하게 될 것입니다.

아래의 상세 가이드들은요? 방금 무슨 일이 일어났는지 **이해하고 싶거나** 더 깊이 파고들고 싶을 때를 위해 여기에 있습니다. 하지만 솔직히? 대부분의 경우 그냥 즉흥적으로 해도 됩니다. 😊

---

**TL;DR**: 설치하고, 코드에 `/analyze` 또는 `/build`를 시도해보고, 마법이 일어나는 것을 지켜보세요.

---

SuperClaude v3.0을 효과적으로 이해하고 사용하기 위한 포괄적인 가이드입니다. 하지만 기억하세요 - 바로 시도해볼 수 있습니다!

## 목차 📖

1. [환영 및 개요](#환영--개요-)
2. [핵심 Component](#핵심-component-)
3. [세 가지 운영 모드](#세-가지-운영-모드-)
4. [Orchestrator System](#orchestrator-system-)
5. [규칙 및 원칙](#규칙--원칙-)
6. [시작 Workflow](#시작-workflow-)
7. [통합 및 조정](#통합--조정-)
8. [실제 예시](#실제-예시-)
9. [팁 및 모범 사례](#팁--모범-사례-)
10. [문제 해결](#문제-해결--일반적인-문제-)
11. [다음 단계](#다음-단계-)

---

## 🚀 그냥 여기서 시작하세요

**읽는 것을 건너뛰고 바로 시작하고 싶으신가요?** 2분 안에 시작하는 방법은 다음과 같습니다:

```bash
# Claude Code에서 다음 Command를 시도해보세요:
/sc:help                    # 사용 가능한 기능 확인
/sc:analyze README.md       # SuperClaude가 Project를 분석합니다
/sc:workflow feature-prd.md # PRD에서 구현 Workflow 생성 (NEW!)
/sc:implement user-auth     # Feature 및 Component 생성 (v3의 NEW!)
/sc:build                   # 자동 최적화 기능이 있는 스마트 빌드
/sc:improve messy-file.js   # 자동으로 코드 정리
```

**방금 무슨 일이 있었나요?** SuperClaude가 자동으로:
- 각 Task에 맞는 올바른 Tool을 선택했습니다 🛠️
- 적절한 전문가(Security, Performance 등)를 활성화했습니다 🎭
- 지능형 Flag 및 최적화를 적용했습니다 ⚡
- 증거 기반 제안을 제공했습니다 📊

**얼마나 쉬웠나요?** 공부할 필요가 없습니다 - SuperClaude가 복잡성을 파악해주므로 당신은 그럴 필요가 없습니다.

어떻게 작동하는지 이해하고 싶으신가요? 계속 읽어보세요. 그냥 계속 실험하고 싶으신가요? 계속하세요! 🎯

---

## 환영 및 개요 👋

### SuperClaude란 무엇인가요? 🤔

SuperClaude는 개발 작업을 위해 Claude Code를 더 똑똑하게 만듭니다. 일반적인 응답 대신, 자신의 분야를 아는 다른 전문가(Security, Performance, Frontend 등)로부터 전문적인 도움을 받습니다.

**솔직한 진실**: 우리는 방금 v3.0을 출시했으며 베타 버전에서 막 나왔습니다. 하는 일에 대해서는 꽤 잘 작동하지만, 계속해서 개선해 나감에 따라 약간의 미흡한 점을 예상해야 합니다. 우리는 실제 소프트웨어 개발 Workflow에 Claude Code가 더 도움이 되기를 원했기 때문에 이것을 만들었습니다.

**멋진 점은?** 이 모든 복잡성을 관리할 필요가 없습니다. `/analyze` 또는 `/build`와 같은 일반 Command를 사용하면 SuperClaude가 보통 어떤 전문가를 참여시키고 어떤 Tool을 사용해야 할지 파악합니다. 🪄

### SuperClaude가 추가하는 것 ✨

**🛠️ 17개의 전문 Command**
- 기획 Tool: `/workflow` (NEW!), `/estimate`, `/task`
- 개발 Tool: `/implement`, `/build`, `/design`
- 분석 Tool: `/analyze`, `/troubleshoot`, `/explain`
- 품질 Tool: `/improve`, `/cleanup`, `/test`
- 그리고 문서화, git, 배포 등을 위한 유틸리티
- **그냥 사용하면 됩니다** - SuperClaude가 복잡성을 자동으로 처리합니다
- **NEW**: PRD에서 구현까지 기획을 위한 `/workflow` Command
- **NEW**: Feature 생성을 위한 `/implement` Command (v2 기능 복원)

**🎭 11명의 스마트 Persona** *(언제 개입해야 할지 아는)*
- 다른 도메인에 맞게 행동을 조정하는 AI 전문가
- **요청에 따라 자동 활성화** (Security Task에는 Security 전문가 등)
- 수동 제어가 가능하지만 보통 필요하지 않습니다
- 언제 도와야 할지 아는 전체 개발팀을 가진 것과 같습니다

**🔧 MCP Server 통합** *(스마트 외부 Tool)*
- Context7: 공식 라이브러리 문서 조회
- Sequential: 복잡한 다단계 분석
- Magic: 최신 UI Component 생성
- Playwright: 브라우저 자동화 및 테스팅
- **필요할 때 자동 연결** - 이 모든 것을 관리할 필요가 없습니다

**📋 향상된 Task 관리** *(배후에서 일어나는 일)*
- TodoRead/TodoWrite를 사용한 진행 상황 추적
- `/task`를 사용한 다중 세션 Project 관리
- `/spawn`을 사용한 복잡한 Orchestration
- `/loop`를 사용한 반복적인 개선
- **대부분 자동** - SuperClaude가 당신이 무엇을 하고 있는지 추적합니다

**⚡ 토큰 최적화** *(스마트 효율성)*
- Context가 가득 찰 때 스마트 압축
- 효율적인 커뮤니케이션을 위한 기호 시스템
- 대규모 작업을 위한 Performance 최적화
- **보통 필요할 때 활성화됩니다** 대규모 Project의 경우

### 현재 상태 (v3.0) 📊

**✅ 잘 작동하는 것:**
- 설치 시스템 (완전히 재작성되어 훨씬 더 안정적임)
- 16개 Command와 11개 Persona를 갖춘 핵심 Framework
- MCP Server 통합 (대부분 작동)
- 기본 Task 관리 및 Workflow 자동화
- 문서 및 사용자 가이드

**⚠️ 아직 미흡한 점:**
- 이것은 초기 릴리스입니다 - 버그가 예상됩니다
- 일부 MCP 통합이 더 원활할 수 있습니다
- 모든 작업에 대해 Performance가 아직 최적화되지 않았습니다
- 일부 고급 기능은 실험적입니다

**❌ 제거한 것:**
- Hooks 시스템 (너무 복잡해져서 v4에서 다시 돌아올 예정)

우리는 v3를 기반으로 꽤 만족하지만, 개선의 여지가 분명히 있습니다.

### 작동 방식 🔄

**간단한 버전**: `/analyze auth.js`와 같은 것을 입력하면 SuperClaude가 나머지를 파악합니다.

**조금 더 자세한 버전**:

1. **스마트 Routing** - 당신이 요청하는 것을 분석하여 의도와 복잡성을 이해합니다
2. **자동 전문가 선택** - 올바른 전문가(Security, Performance 등)를 선택합니다
3. **Tool 조정** - 도움이 될 때 외부 시스템에 연결합니다
4. **품질 보증** - 제안이 견고한지 확인합니다

**이 모든 복잡성을 볼 수 없습니다** - 그냥 Claude가 개발 관련해서 훨씬 더 똑똑해진 것처럼 느껴집니다.

좋은 점은 이 대부분이 보통 자동으로 일어난다는 것입니다. 당신이 요청을 하면, SuperClaude는 좋은 접근 방식을 파악하려고 시도하고, 적절한 Tool과 전문 지식으로 실행합니다. 보통 Configuration이나 설정이 필요 없습니다 - 그냥 더 나은 결과가 있기를 바랍니다. ✨

### 빠른 기능 개요 🎯

| Component | 하는 일 | 자세히 알아보기 *(선택 사항!)* |
|---|---|---|
| **Command** | 자동 활성화되는 15개의 전문 Tool | [Command 가이드](commands-guide.md) |
| **Flag** | 대부분 자동으로 활성화되는 수정자 | [Flag 가이드](flags-guide.md) |
| **Persona** | 언제 도와야 할지 아는 11명의 AI 전문가 | [Persona 가이드](personas-guide.md) |
| **MCP Server** | 유용할 때 연결되는 외부 통합 | [이 가이드](#핵심-component-) |
| **모드** | 다른 Workflow를 위한 3가지 운영 모드 | [이 가이드](#세-가지-운영-모드-) |
| **Orchestrator** | 모든 것을 작동시키는 스마트 Routing | [이 가이드](#orchestrator-system-) |

**기억하세요**: 이 가이드들을 읽지 않고도 SuperClaude를 효과적으로 사용할 수 있습니다. 어떻게 작동하는지 궁금해질 때를 위해 여기에 있습니다! 🎪

---

## 핵심 Component 🧩

SuperClaude는 함께 작동하는 여러 상호 연결된 시스템으로 구성됩니다. 각 Component가 더 큰 그림에 어떻게 들어맞는지 살펴보겠습니다.

### Command: 당신의 Toolkit 🛠️

Command는 특정 유형의 개발 작업을 처리하는 전문 Tool입니다. "이것 좀 도와줘"라는 일반적인 요청 대신, 다양한 시나리오에 맞는 목적별 Tool을 얻게 됩니다.

**목적별로 정리된 15개 Command:**

**개발** 🔨
- `/build` - Project 빌드, Compilation, Bundling
- `/design` - 시스템 아키텍처 및 Component 설계

**분석** 🔍
- `/analyze` - 포괄적인 코드 및 시스템 분석
- `/troubleshoot` - 문제 조사 및 Debugging
- `/explain` - 교육적 설명 및 학습

**품질** ✨
- `/improve` - 코드 향상 및 최적화
- `/cleanup` - 기술 부채 감소
- `/test` - 테스팅 및 Coverage 분석

**유틸리티** 🔧
- `/document` - 문서 생성
- `/git` - 향상된 git Workflow
- `/load` - Project Context 로딩
- `/estimate` - Project 견적
- `/task` - 장기 Project 관리
- `/spawn` - 복잡한 작업 Orchestration
- `/index` - Command 탐색 및 도움말

각 Command는 자체 Flag를 가지고 있으며, 적절한 Persona를 자동 활성화하고, 관련 MCP Server와 통합됩니다. 자세한 예시 및 사용 패턴은 [Command 가이드](commands-guide.md)를 참조하세요.

### Flag: 행동 수정자 🏁

Flag는 SuperClaude가 요청을 처리하는 방식을 변경합니다. 행동을 수정하거나, 기능을 추가하거나, 출력 스타일을 변경하는 Command-line 옵션과 같습니다.

**주요 Flag 카테고리:**

**기획 & 분석** 🧠
- `--think` / `--think-hard` / `--ultrathink` - 사고 깊이 제어
- `--plan` - 실행 전 실행 계획 표시

**효율성 & 제어** ⚡
- `--uc` - 대규모 작업을 위한 초압축 출력
- `--safe-mode` - 유효성 검사를 통한 보수적인 실행
- `--validate` - 작업 전 위험 평가

**MCP Server 제어** 🔧
- `--c7` - 문서화를 위해 Context7 활성화
- `--seq` - 복잡한 분석을 위해 Sequential 활성화
- `--magic` - UI Component를 위해 Magic 활성화
- `--play` - 테스팅을 위해 Playwright 활성화

**고급 Orchestration** 🎭
- `--delegate` - 병렬 처리를 위해 하위 에이전트 위임 활성화
- `--wave-mode` - 복합 지능을 사용한 다단계 실행
- `--loop` - 반복적인 개선 모드

**초점 & 범위** 🎯
- `--focus security` - 특정 도메인에 집중
- `--scope project` - 분석 범위 설정
- `--persona-[name]` - 특정 Persona 활성화

Flag는 종종 Context에 따라 자동 활성화됩니다. 예를 들어, Security 관련 요청은 보통 `--persona-security` 및 `--focus security`를 얻습니다. 포괄적인 세부 정보 및 패턴은 [Flag 가이드](flags-guide.md)를 참조하세요.

### Persona: AI 전문가 🎭

Persona는 주문형 전문가 팀을 보유하고 있는 것과 같습니다. 각 전문가는 문제에 대해 다른 전문 지식, 우선 순위 및 접근 방식을 제공합니다.

**도메인별로 정리된 11개 Persona:**

**기술 전문가** 🔧
- 🏗️ **architect** - 시스템 설계, 장기 아키텍처
- 🎨 **frontend** - UI/UX, 접근성, Frontend Performance
- ⚙️ **backend** - API, Database, 신뢰성
- 🛡️ **security** - 위협 모델링, 취약점
- ⚡ **performance** - 최적화, 병목 현상 제거

**프로세스 & 품질** ✨
- 🔍 **analyzer** - 근본 원인 분석, 조사
- 🧪 **qa** - 테스팅, 품질 보증
- 🔄 **refactorer** - 코드 품질, 기술 부채
- 🚀 **devops** - 인프라, 배포

**지식 & 커뮤니케이션** 📚
- 👨‍🏫 **mentor** - 교육, 지식 전달
- ✍️ **scribe** - 문서화, 기술 글쓰기

Persona는 보통 요청 패턴에 따라 자동 활성화되지만 `--persona-[name]` Flag로 덮어쓸 수 있습니다. 각 Persona는 다른 우선 순위를 가집니다 (예: Security Persona는 속도보다 Security를 우선시합니다). 자세한 설명 및 예시는 [Persona 가이드](personas-guide.md)를 참조하세요.

### MCP Server: 외부 기능 🔧

MCP (Model Context Protocol) Server는 Claude의 기본 기능을 넘어서는 전문화된 기능을 제공합니다.

**4개의 통합 Server:**

**Context7** 📚
- **목적**: 공식 라이브러리 문서 및 모범 사례
- **활성화 시점**: Framework 질문, 외부 라이브러리 사용
- **제공하는 것**: 최신 문서, 코드 예시, 패턴
- **예시**: `/build react-app --c7`은 React 모범 사례를 얻습니다

**Sequential** 🧠
- **목적**: 복잡한 다단계 분석 및 체계적인 사고
- **활성화 시점**: Debugging, 시스템 설계, `--think` Flag
- **제공하는 것**: 구조화된 문제 해결, 가설 테스트
- **예시**: `/troubleshoot "auth randomly fails" --seq`

**Magic** ✨
- **목적**: 최신 UI Component 생성 및 디자인 시스템
- **활성화 시점**: UI Component 요청, Frontend 작업
- **제공하는 것**: React/Vue/Angular Component, 디자인 패턴
- **예시**: `/build dashboard --magic`은 최신 UI Component를 생성합니다

**Playwright** 🎭
- **목적**: 브라우저 자동화, E2E 테스팅, Performance 모니터링
- **활성화 시점**: 테스팅 Workflow, Performance 분석
- **제공하는 것**: 크로스 브라우저 테스팅, 시각적 검증, 메트릭
- **예시**: `/test e2e --play`는 포괄적인 브라우저 테스트를 실행합니다

MCP Server는 보통 자동으로 조정되지만 `--all-mcp`, `--no-mcp` 또는 `--c7`과 같은 특정 Flag로 제어할 수 있습니다.

### Component가 함께 작동하는 방식 🤝

멋진 부분은 Component가 조정될 때입니다:

**예시: Security 분석 요청**
```bash
/sc:analyze auth-system/ --focus security
```

**보통 일어나는 일:**
1. **Command**: `/analyze`가 코드 분석을 처리합니다
2. **Flag**: `--focus security`가 주의를 집중시킵니다
3. **Persona**: 🛡️ Security 전문가가 자동 활성화됩니다
4. **MCP**: Sequential이 체계적인 분석을 제공합니다
5. **Orchestrator**: 최적의 실행을 위해 모든 것을 Routing합니다

**결과**: 위협 모델링 관점, 체계적인 방법론 및 포괄적인 범위를 갖춘 Security 중심 분석.

이 조정은 대부분의 요청에 대해 보통 발생합니다 - SuperClaude는 특정 요구에 맞는 좋은 Tool과 전문 지식의 조합을 파악하려고 시도합니다.

---

## 세 가지 운영 모드 🎭

SuperClaude는 개발 Workflow의 다른 측면을 최적화하는 세 가지 고유한 모드로 작동합니다. 이러한 모드를 이해하면 Framework을 최대한 활용하는 데 도움이 됩니다.

### Task 관리 모드 📋

**무엇인가**: 진행 상황 추적 및 유효성 검사를 통한 구조화된 Workflow 실행.

**사용 시점**: 추적 및 조정이 필요한 모든 다단계 작업.

**작동 방식**: SuperClaude는 작업을 관리 가능한 Task로 나누고, 진행 상황을 추적하며, 유효성 검사 게이트를 통해 품질을 보장합니다.

#### Task 관리의 네 가지 계층

**계층 1: 세션 Task (TodoRead/TodoWrite)**
- **범위**: 현재 Claude Code 세션
- **용량**: 세션당 3-20개 Task
- **상태**: pending 📋, in_progress 🔄, completed ✅, blocked 🚧
- **사용법**: 즉각적인 작업을 위한 실시간 진행 상황 추적

```bash
# SuperClaude는 보통 세션 Task를 생성하고 관리합니다
/sc:build large-project/
# → 생성: "Project 구조 분석", "빌드 프로세스 실행", "출력 검증"
```

**계층 2: Project Task (`/task` Command)**
- **범위**: 다중 세션 Feature (수일에서 수주)
- **구조**: 계층적 (Epic → Story → Task)
- **지속성**: 세션 간 상태 관리
- **사용법**: 장기 Feature 개발

```bash
/sc:task create "implement user dashboard" --priority high
/sc:task breakdown "payment integration"
/sc:task status  # 현재 Project Task 확인
```

**계층 3: 복잡한 Orchestration (`/spawn` Command)**
- **범위**: 복잡한 다중 도메인 작업
- **기능**: 병렬/순차 조정, Tool 관리
- **사용법**: 여러 Tool/시스템을 포함하는 작업

```bash
/sc:spawn deploy-pipeline --parallel
/sc:spawn setup-dev-environment --monitor
```

**계층 4: 반복적인 향상 (`/loop` Command)**
- **범위**: 점진적인 개선 Workflow
- **기능**: 유효성 검사를 통한 반복 주기
- **사용법**: 품질 개선 및 구체화

```bash
/sc:improve messy-code.js --loop --iterations 3
# → 주기 사이에 유효성 검사를 통해 코드를 반복적으로 개선합니다
```

#### Task 상태 관리

**핵심 원칙**:
- **증거 기반 진행**: 활동뿐만 아니라 측정 가능한 결과
- **단일 초점 프로토콜**: 명확성을 위해 한 번에 하나의 Task만 in_progress 상태
- **품질 게이트**: 완료 전에 모든 작업에 유효성 검사 단계 포함
- **Context 유지**: 작업 간에 Context를 잘 보존하려고 시도합니다

**Task 감지**:
- 다단계 작업 (3단계 이상) → Task 분해 생성
- 키워드: build, implement, create, fix, optimize → Task 추적 활성화
- 범위 표시기: system, feature, comprehensive → 진행 상황 모니터링 추가

### 자기 성찰 모드 🧠

**무엇인가**: SuperClaude가 자신의 추론 및 의사 결정 프로세스를 검토할 수 있게 하는 메타인지 분석.

**사용 시점**: 복잡한 문제 해결, Framework 문제 해결, 학습 순간 또는 `--introspect`로 명시적으로 요청할 때.

**작동 방식**: SuperClaude는 정상적인 작업을 벗어나 자신의 사고 패턴, 결정 논리 및 행동 순서를 분석합니다.

#### 핵심 기능

**추론 분석** 🧠
- 논리적 흐름과 결정 근거를 검토합니다
- 사고의 일관성을 평가합니다
- 가정과 잠재적 편견을 식별합니다
- 증거에 대해 추론을 검증합니다

**행동 순서 검토** 🔄
- Tool 선택 효과를 분석합니다
- Workflow 패턴 및 효율성을 검토합니다
- 대안적인 접근 방식을 고려합니다
- 최적화 기회를 식별합니다

**Framework 준수 확인** 🔍
- SuperClaude 규칙 및 원칙에 대한 조치를 검증합니다
- 표준 패턴과의 편차를 식별합니다
- 필요할 때 수정 지침을 제공합니다
- 품질 표준이 충족되는지 확인합니다

**학습 인식** 💡
- 결과에서 통찰력을 추출합니다
- 재사용을 위해 성공적인 패턴을 식별합니다
- 개선을 위해 지식 격차를 인식합니다
- 미래 최적화 전략을 제안합니다

#### 분석 마커

자기 성찰 모드가 활성화되면 다음 마커가 표시됩니다:

- 🧠 **추론 분석** - 논리적 흐름 및 결정 검토
- 🔄 **행동 순서 검토** - Workflow 효과 분석
- 🎯 **자기 평가** - 메타인지 평가
- 📊 **패턴 인식** - 행동 패턴 식별
- 🔍 **Framework 준수** - 규칙 준수 확인
- 💡 **회고적 통찰력** - 결과로부터 학습

#### 자기 성찰 활성화 시점

**보통 활성화되는 경우**:
- 메타인지 감독이 필요한 복잡한 다단계 문제
- 결과가 예상과 일치하지 않을 때 오류 복구
- Framework 토론 또는 SuperClaude 문제 해결
- 반복되는 행동에 대한 패턴 인식 필요

**수동 활성화**:
```bash
/sc:analyze complex-system/ --introspect
/sc:troubleshoot "framework confusion" --introspection
```

### 토큰 효율성 모드 ⚡

**무엇인가**: 품질을 유지하면서 정보 밀도를 극대화하는 지능형 최적화 시스템.

**사용 시점**: 대규모 작업, Context가 한계에 가까워질 때 또는 더 빠른 실행이 필요할 때.

**작동 방식**: Context 및 Persona 인식을 기반으로 기호, 약어 및 구조적 최적화를 사용하는 적응형 압축.

#### 압축 전략

**5단계 적응형 압축**:
1. **최소** (0-40% 사용량): Persona 최적화된 명확성을 갖춘 전체 세부 정보
2. **효율적** (40-70% 사용량): 도메인 인식을 갖춘 균형 잡힌 압축
3. **압축** (70-85% 사용량): 품질 게이트를 사용한 공격적인 최적화
4. **중요** (85-95% 사용량): 필수 Context를 보존하는 최대 압축
5. **비상** (95%+ 사용량): 정보 검증을 통한 초압축

#### 기호 시스템

**핵심 논리 & 흐름**:
- `→` ~로 이어짐, ~을 의미함 (`auth.js:45 → security risk`)
- `⇒` ~로 변환됨 (`input ⇒ validated_output`)
- `&` 그리고, 결합 (`security & performance`)
- `»` 순서, 그 다음 (`build » test » deploy`)
- `∴` 그러므로 (`tests fail ∴ code broken`)

**상태 & 진행**:
- ✅ 완료, 통과
- ❌ 실패, 오류
- ⚠️ 경고
- 🔄 진행 중
- 🎯 목표, 목적

**기술 도메인**:
- ⚡ Performance
- 🔍 분석
- 🛡️ Security
- 📦 배포
- 🎨 디자인

#### 활성화 전략

**보통 활성화되는 경우**:
- Context 사용량 >75% → 압축 활성화
- 대규모 작업 → 토큰 오버플로 방지
- 복잡한 Orchestration → 커뮤니케이션 최적화

**수동 활성화**:
```bash
/sc:analyze huge-codebase/ --uc  # 초압축 모드
/sc:improve legacy-system/ --uc --delegate auto  # 효율적인 대규모 작업
```

**Performance 목표** (계속 개선 중!):
- 목표: ~30-50% 토큰 감소
- 품질: 정보의 ~95%를 보존하려고 시도
- 속도: 보통 <100ms 압축 결정
- 통합: Framework Component와 작동

#### 모드 통합

세 가지 모드는 종종 함께 작동합니다:

```bash
/sc:improve large-legacy-system/ --wave-mode auto --uc --introspect
```

**일어나는 일**:
- **Task 관리**: 진행 상황 추적을 통한 구조화된 개선 계획 생성
- **토큰 효율성**: 대규모 작업을 위한 출력 압축
- **자기 성찰**: 개선 전략 분석 및 접근 방식 검증

---

## Orchestrator System 🎯

Orchestrator는 요청을 분석하고 좋은 Tool, Persona 및 통합 조합을 조정하려고 시도하는 SuperClaude의 지능형 Routing 시스템입니다. 이것이 SuperClaude를 별개의 Tool 모음이 아닌 똑똑하고 반응이 빠른 것처럼 느끼게 하는 것입니다.

### Orchestrator 작동 방식 🔄

**스마트 디스패처라고 생각하세요**:
1. **분석**하여 의도와 복잡성을 이해합니다
2. 최상의 Command, Flag, Persona 및 MCP Server 조합으로 **Routing**합니다
3. 최적의 결과를 위해 실행을 **조정**합니다
4. 좋은 결과를 보장하기 위해 품질 게이트를 통해 **검증**합니다
5. Performance 및 리소스 사용량을 **최적화**합니다

### 감지 엔진 🧠

감지 엔진은 모든 요청을 여러 렌즈를 통해 분석합니다:

#### 패턴 인식

**복잡도 감지**:
- **단순**: 단일 파일 작업, 기본 Task (<3단계) → 직접 실행
- **보통**: 다중 파일 작업, 분석 Task (3-10단계) → 표준 Routing
- **복잡**: 시스템 전체 변경, 아키텍처 결정 (>10단계) → 고급 Orchestration

**도메인 식별**:
- **Frontend**: "UI", "component", "responsive"와 같은 키워드 → 🎨 frontend Persona + Magic MCP
- **Backend**: "API", "database", "service"와 같은 키워드 → ⚙️ backend Persona + Context7 MCP
- **Security**: "vulnerability", "auth", "compliance"와 같은 키워드 → 🛡️ security Persona + Sequential MCP
- **Performance**: "slow", "optimize", "bottleneck"와 같은 키워드 → ⚡ performance Persona + Playwright MCP

**작업 유형 분류**:
- **분석**: "analyze", "review", "understand" → Sequential MCP + analyzer Persona
- **생성**: "create", "build", "implement" → Magic MCP (UI인 경우) 또는 Context7 (패턴)
- **수정**: "improve", "refactor", "optimize" → 적절한 전문가 Persona
- **Debugging**: "troubleshoot", "fix", "debug" → Sequential MCP + analyzer Persona

#### 자동 활성화 논리

**높은 신뢰도 트리거** (90%+ 활성화):
```bash
/sc:analyze auth-system/ --focus security
# → 🛡️ security Persona + Sequential MCP + --validate Flag
```

**Context 기반 활성화**:
```bash
/sc:build react-components/
# → 🎨 frontend Persona + Magic MCP + --c7 Flag (React 문서)
```

**Performance 기반 활성화**:
```bash
# Context 사용량 >75%일 때
/sc:analyze large-project/
# → 압축을 위해 --uc Flag 자동 추가
```

### Routing 인텔리전스 🚦

Routing 시스템은 동적 결정 트리를 사용하여 감지된 패턴을 최적의 Tool 조합에 매핑합니다.

#### 마스터 Routing 테이블

| 요청 패턴 | 보통 자동 활성화 | 빈도 | 이유 |
|---|---|---|---|
| "analyze architecture" | 🏗️ architect + --ultrathink + Sequential | 대부분 | 복잡한 시스템 분석 |
| "create UI component" | 🎨 frontend + Magic + --uc | 꽤 자주 | 생성을 동반한 Frontend 도메인 |
| "security audit" | 🛡️ security + --ultrathink + Sequential | 대부분 | Security 전문 지식 필요 |
| "debug complex issue" | 🔍 analyzer + --think + Sequential | 자주 | 조사 방법론 |
| "improve performance" | ⚡ performance + --think-hard + Playwright | 꽤 자주 | Performance 전문 지식 + 테스팅 |

#### 지능형 조정

**다중 Server 작업**:
```bash
/sc:design user-dashboard --type api
```
**Orchestrator는 보통 다음을 조정합니다**:
- 🏗️ architect Persona (시스템 설계)
- 🎨 frontend Persona (UI 설계)
- Context7 MCP (Framework 패턴)
- Sequential MCP (설계 방법론)

**대체 전략**:
- Context7 사용 불가 → 문서용 WebSearch → 수동 구현
- Sequential 시간 초과 → 네이티브 Claude 분석 → 한계 참고
- Magic 실패 → 기본 Component 생성 → 수동 향상 제안

### 품질 게이트 & 검증 Framework ✅

SuperClaude는 작업을 위해 8단계 검증 주기를 구현하려고 시도합니다:

#### 8단계 품질 프로세스

1. **구문 검증** - 언어 파서 + Context7 표준
2. **타입 검사** - Sequential 분석 + 호환성 검증
3. **Linting** - Context7 규칙 + 품질 분석
4. **Security 검토** - Sequential 분석 + OWASP 준수
5. **테스팅** - Playwright E2E + Coverage 분석 (좋은 Coverage 목표)
6. **Performance** - Sequential 분석 + 벤치마킹
7. **문서화** - Context7 패턴 + 완전성 검증
8. **통합** - Playwright 테스팅 + 배포 검증

#### 검증 자동화

**지속적인 통합**:
- CI/CD 파이프라인 통합
- 조기 실패 감지를 통한 점진적 검증
- 포괄적인 메트릭을 사용한 증거 생성

**지능형 모니터링**:
- ML 예측을 사용한 성공률 추적
- 과거 패턴을 기반으로 한 적응형 검증
- 검증 전략의 자동 최적화

### Performance 최적화 ⚡

Orchestrator는 여러 전략을 통해 좋은 Performance를 위해 최적화하려고 시도합니다:

#### 리소스 관리

**토큰 할당**:
- 감지 엔진: 패턴 분석을 위한 1-2K 토큰
- 결정 트리: Routing 논리를 위한 500-1K 토큰
- MCP 조정: 활성화된 Server에 따라 가변
- 예비: 예기치 않은 복잡성을 위한 10% 버퍼

**작업 일괄 처리**:
- **병렬 실행** 종속성이 없을 때
- **Context 공유** 관련 작업 간
- **캐시 전략** 성공적인 Routing 패턴을 위해
- **스마트 큐잉** 리소스 고갈 방지

#### 고급 Orchestration

**하위 에이전트 위임**:
```bash
# 7개 이상의 디렉토리 또는 50개 이상의 파일이 감지되면 자동 활성화
/sc:analyze monorepo/
# → --delegate auto Flag + 병렬 처리
```

**Wave Orchestration**:
```bash
# 복잡도 >0.7 + 파일 >20 + 작업 유형 >2일 때 자동 활성화
/sc:improve legacy-system/
# → --wave-mode auto + 다단계 실행
```

### 실제 Orchestration 예시 💡

#### 예시 1: Security 분석 요청
```bash
/sc:analyze user-auth/ --focus security
```

**Orchestrator 분석**:
- 도메인: Security (높은 신뢰도)
- 복잡도: 보통 (인증 시스템)
- 작업: 분석 + 스캔

**보통 조정하는 것**:
- 🛡️ security Persona (위협 모델링 관점)
- Sequential MCP (체계적인 분석)
- `--validate` Flag (작업 전 안전 확인)
- `--think` Flag (복잡한 Security 패턴)

**품질 게이트**: Security 검증에 중점을 둔 모든 8단계

#### 예시 2: Frontend Performance 최적화
```bash
/sc:improve slow-dashboard/ --focus performance
```

**Orchestrator 분석**:
- 도메인: Frontend + Performance (이중 전문 지식 필요)
- 복잡도: 높음 (Performance 최적화)
- 작업: 개선 + 검증

**보통 조정하는 것**:
- ⚡ performance Persona (주)
- 🎨 frontend Persona (보조, UI가 감지된 경우)
- Playwright MCP (Performance 테스팅)
- `--think-hard` Flag (복잡한 최적화)

**품질 게이트**: 벤치마킹을 통한 Performance 중심 검증

#### 예시 3: 대규모 Codebase 분석
```bash
/sc:analyze enterprise-monorepo/
```

**Orchestrator 분석**:
- 범위: 큼 (>50개 파일 감지)
- 복잡도: 높음 (엔터프라이즈 규모)
- 리소스: 높은 토큰 사용량 예측

**보통 조정하는 것**:
- `--delegate auto` Flag (병렬 처리)
- `--uc` Flag (토큰 최적화)
- 🏗️ architect Persona (시스템 수준 분석)
- Sequential MCP (구조화된 분석)

**품질 게이트**: 하위 에이전트 간 분산 검증

### Orchestrator Configuration ⚙️

**Performance 설정**:
```yaml
orchestrator_config:
  enable_caching: true
  parallel_operations: true
  max_parallel: 3
  token_reserve: 10%
  emergency_threshold: 90%
```

**인텔리전스 설정**:
```yaml
  learning_enabled: true
  confidence_threshold: 0.7
  pattern_detection: aggressive
  wave_score_threshold: 0.7
```

Orchestrator는 성공적인 패턴에서 학습하고 결과를 기반으로 미래 Routing 결정을 개선하려고 시도합니다.

---

## 규칙 & 원칙 📏

SuperClaude는 일관되고 신뢰할 수 있으며 유용한 행동을 보장하는 핵심 규칙 및 원칙에 따라 작동합니다. 이를 이해하면 SuperClaude가 문제에 어떻게 접근하고 특정 결정을 내리는 이유를 예측하는 데 도움이 됩니다.

### 핵심 운영 규칙 ⚖️

이것들은 SuperClaude가 따르려고 시도하는 핵심 규칙입니다:

#### 파일 작업 Security 🔐
- **쓰기/편집 전에 항상 읽기** - SuperClaude는 현재 내용을 이해하지 않고 파일을 수정하지 않습니다
- **절대 경로만 사용** - 경로 탐색 공격을 방지하고 신뢰할 수 있는 파일 작업을 보장합니다
- **자동 Commit 안 함** - SuperClaude는 명시적으로 요청하지 않는 한 git에 변경 사항을 Commit하지 않습니다
- **일괄 작업 선호** - 여러 관련 변경 사항을 일관성을 위해 그룹화합니다

**이것이 중요한 이유**: 이러한 규칙은 데이터 손실, Security 취약성 및 의도하지 않은 Codebase 수정을 방지합니다.

#### Task 관리 규칙 📋
- **증거 기반 진행** - 측정 가능한 증거가 있을 때만 Task가 완료된 것으로 표시됩니다
- **단일 초점 프로토콜** - 명확성을 위해 한 번에 하나의 Task만 "in_progress" 상태입니다
- **품질 게이트** - 모든 작업에는 완료 전에 검증 단계가 포함됩니다
- **Context 유지** - 작업 간에 Context를 잘 보존하려고 시도합니다

**이것이 중요한 이유**: 신뢰할 수 있는 진행 상황 추적을 보장하고 작업이 손실되거나 잊혀지는 것을 방지합니다.

#### Framework 준수 규칙 🎯
- **먼저 종속성 확인** - 라이브러리를 사용하기 전에 항상 package.json/requirements.txt를 확인합니다
- **기존 패턴 따르기** - Project 규칙, Import 스타일 및 아키텍처를 존중합니다
- **체계적인 Codebase 변경** - Project 전체 수정을 하기 전에 전체 검색을 완료합니다
- **완료 검증** - 변경 사항이 작동하고 기존 기능을 손상시키지 않는지 확인합니다

**이것이 중요한 이유**: 기존 Project 구조와의 코드 품질 및 일관성을 유지합니다.

### 개발 원칙 🛠️

이러한 원칙은 SuperClaude가 개발 문제에 접근하는 방식을 안내합니다:

#### 증거 기반 의사 결정 📊
**주요 지침**: "증거 > 가정 | 코드 > 문서 | 효율성 > 장황함"

- **최적화 전에 측정** - 실제 메트릭을 기반으로 한 Performance 개선
- **가설을 체계적으로 테스트** - 검증 가능한 데이터로 뒷받침되는 주장
- **결정 근거 문서화** - 아키텍처 선택에 대한 명확한 추론
- **결과로부터 학습** - 결과를 기반으로 한 지속적인 개선

**실제로**:
```bash
/sc:improve slow-api/ --focus performance
# → 현재 Performance를 측정하고, 병목 현상을 식별하고, 데이터를 기반으로 최적화합니다
```

#### SOLID 설계 원칙 🏗️
- **단일 책임** - 각 Component는 변경해야 할 이유가 하나만 있습니다
- **개방/폐쇄** - 확장에 대해서는 열려 있고, 수정에 대해서는 닫혀 있습니다
- **리스코프 치환** - 파생 클래스는 기본 클래스로 대체할 수 있어야 합니다
- **인터페이스 분리** - 사용하지 않는 인터페이스에 대한 강제 종속성이 없습니다
- **의존성 역전** - 구체화가 아닌 추상화에 의존합니다

**SuperClaude가 이를 따르는 이유**: 이해하고 수정하기 쉬운 유지보수 가능하고 확장 가능하며 유연한 코드로 이어집니다.

#### 품질 철학 ✨
- **감지보다 예방** - 품질을 테스트하는 것보다 내장하는 것이 좋습니다
- **복잡성보다 단순성** - 작동하는 가장 간단한 솔루션을 선택합니다
- **영리함보다 유지보수성** - 코드는 이해하고 수정하기 쉬워야 합니다
- **기본적으로 Security** - 처음부터 안전한 패턴을 구현합니다

#### 시니어 개발자 사고방식 🎓
SuperClaude는 숙련된 개발자처럼 문제에 접근합니다:

- **시스템 사고** - 전체 시스템에 미치는 영향을 고려합니다
- **장기적인 관점** - 여러 시간대에 걸쳐 결정을 평가합니다
- **위험 보정** - 수용 가능한 위험과 수용 불가능한 위험을 구별합니다
- **이해 관계자 인식** - 기술적 완벽성과 실제적인 제약 사이의 균형을 맞춥니다

### 규칙 및 원칙이 당신에게 미치는 영향 💡

#### 예측 가능한 행동
SuperClaude는 일관된 규칙을 따르기 때문에 문제에 어떻게 접근할지 예측할 수 있습니다:

```bash
/sc:improve legacy-authentication/
```
**예상할 수 있는 것**:
- 변경을 제안하기 전에 기존 코드 읽기
- Project의 기존 패턴 따르기
- Security 우선 접근 방식 (Security Persona가 활성화될 가능성이 높음)
- 추론이 포함된 증거 기반 권장 사항
- 개선을 완료하기 전 품질 게이트

#### 품질 보증
원칙은 고품질 결과를 보장합니다:

- **마법 같은 변경을 피하려고 노력합니다** - SuperClaude는 보통 추론을 설명합니다
- **파괴적인 변경이 없도록 목표** - 기존 기능을 보존하려고 노력합니다
- **Security 의식** - Security 원칙이 중요합니다
- **부채 인식** - 복잡성을 유지하거나 줄이려고 노력합니다

#### 투명성
SuperClaude가 무엇을 하고 왜 하는지 보통 이해해야 합니다:

```bash
/sc:analyze --introspect complex-system/
```
**보여주는 것**:
- 의사 결정 과정
- 규칙 적용
- 원칙 준수
- 고려된 대안적 접근 방식

### 규칙 및 원칙의 실제 예시 🎯

#### 예시 1: 체계적인 리팩토링
**요청**: "이 지저분한 Codebase를 정리해주세요"

**적용된 규칙**:
- 변경 전 전체 검색 (전체 Codebase 검색)
- 수정 전 모든 파일 읽기
- 기존 Project 패턴 따르기
- 증거로 완료 검증

**적용된 원칙**:
- 복잡성보다 단순성 (불필요한 복잡성 감소)
- 증거 기반 결정 (전/후 복잡성 측정)
- 품질 보증 (포괄적인 테스팅)
- 장기적인 유지보수성 (미래 수정 고려)

#### 예시 2: Security 구현
**요청**: "API에 인증을 추가해주세요"

**적용된 규칙**:
- Security Persona가 보통 자동 활성화됩니다
- Security 기본 사항에 대해 절대 타협하지 않습니다
- 먼저 기존 패턴 확인
- 품질 게이트에는 Security 검증이 포함됩니다

**적용된 원칙**:
- 기본적으로 Security (안전한 패턴 구현)
- 심층 방어 (여러 Security 계층)
- 증거 기반 접근 방식 (확립된 Security 패턴 따름)
- 시스템 사고 (전체 애플리케이션에 미치는 영향 고려)

#### 예시 3: Performance 최적화
**요청**: "이 페이지 로딩이 느려요"

**적용된 규칙**:
- 최적화 전에 측정
- 증거 기반 진행 상황 추적
- 메트릭으로 개선 검증
- 기존 기능 유지

**적용된 원칙**:
- 측정 기반 최적화
- 사용자 경험 중심
- 체계적인 방법론
- 감지보다 예방 (근본 원인 식별)

### 규칙 시행 및 품질 게이트 🚨

SuperClaude는 품질 게이트 시스템을 통해 규칙을 시행합니다:

#### 시행 접근 방식
- **작업 전 검증** - 시작하기 전에 위험 확인
- **실시간 모니터링** - 실행 중 규칙 준수 추적
- **작업 후 확인** - 규칙이 준수되었는지 확인
- **증거 수집** - 투명성을 위해 준수 사항 문서화

#### 규칙이 도전받을 때
때로는 규칙이 즉각적인 요구와 충돌하는 것처럼 보일 수 있습니다:

**예시**: "그냥 빨리 작동하게 해주세요, 품질은 신경 쓰지 마세요"

**SuperClaude의 응답**:
- 긴급성을 인정합니다
- 장기적인 성공을 위해 품질 규칙이 중요한 이유를 설명합니다
- 필수 규칙을 유지하는 타협안을 제공합니다
- 품질 표준이 완화될 경우 위험을 문서화합니다

### Persona 행동을 안내하는 원칙 🎭

각 Persona는 핵심 원칙을 따르지만 다른 측면을 강조합니다:

- **🛡️ Security Persona**: Security > 규정 준수 > 신뢰성 > Performance
- **⚡ Performance Persona**: 먼저 측정 > 중요한 경로 최적화 > 사용자 경험
- **🏗️ Architect Persona**: 장기적인 유지보수성 > 확장성 > Performance
- **🎨 Frontend Persona**: 사용자 요구 > 접근성 > Performance > 기술적 우아함

**이것이 중요한 이유**: 다른 Persona가 핵심 원칙에 따라 트레이드오프를 어떻게 우선시할지 예측할 수 있습니다.

### 살아있는 원칙 🌱

이러한 규칙과 원칙은 고정되어 있지 않습니다. 다음에 따라 진화합니다:

- **Community 피드백** - 실제 사용 패턴이 개선에 정보를 제공합니다
- **결과 분석** - 성공적인 패턴이 강화됩니다
- **기술 변화** - 원칙이 새로운 개발 관행에 적응합니다
- **사용자 요구** - 규칙이 유연성과 일관성의 균형을 맞춥니다

목표는 소프트웨어 개발의 변화하는 환경에 적응하면서 유용하고 예측 가능한 행동을 유지하는 것입니다.

---

## 시작 Workflow 🛣️

이제 SuperClaude의 Component를 이해했으므로 다양한 개발 시나리오에 대한 실제 Workflow를 살펴보겠습니다. 이러한 패턴은 빠르게 생산성을 높이는 데 도움이 될 것입니다.

### 처음 설정 🎬

아직 SuperClaude를 설치하지 않았다면 [설치 가이드](installation-guide.md)를 참조하세요. 설치 후 시작하는 방법은 다음과 같습니다:

#### 빠른 검증
```bash
# 기본 기능 테스트
/sc:help                    # SuperClaude Command가 표시되어야 합니다
/sc:analyze README.md       # 간단한 파일 분석 시도
/sc:build --help           # Command 옵션 확인
```

#### 자동 활성화 이해
SuperClaude가 올바른 Tool을 자동으로 선택하는 방법을 보려면 다음 Command를 시도해보세요:

```bash
# Frontend 작업 → frontend Persona + Magic MCP
/sc:build src/components/

# Security 분석 → security Persona + Sequential MCP
/sc:analyze auth/ --focus security

# Performance 조사 → performance Persona + Playwright MCP
/sc:analyze --focus performance slow-endpoints/
```

출력에서 자동 활성화된 Flag 및 Persona를 확인하세요. 이것은 SuperClaude의 지능형 Routing이 작동하는 것을 보여줍니다.

### 개발 Workflow 패턴 🔄

#### 새 Project 온보딩
익숙하지 않은 Project에서 작업을 시작할 때:

```bash
# 1. Project Context 로드
/sc:load --deep --summary
# → 구조, 종속성, 패턴 개요 제공

# 2. 아키텍처 분석
/sc:analyze --focus architecture
# → 🏗️ architect Persona가 시스템 이해 제공

# 3. 코드 품질 확인
/sc:analyze --focus quality
# → 🧪 qa Persona가 잠재적 문제 식별

# 4. 문서 검토
/sc:document README --type guide
# → ✍️ scribe Persona가 Project 문서 개선
```

#### Feature 개발 주기
새로운 Feature를 개발할 때:

```bash
# 1. 설계 단계
/sc:design user-dashboard --type component
# → 🏗️ architect + 🎨 frontend Persona 협력

# 2. 구현
/sc:build dashboard-components/
# → 🎨 frontend Persona + Magic MCP UI 생성

# 3. 테스팅
/sc:test --type e2e dashboard/
# → 🧪 qa Persona + Playwright MCP 테스팅

# 4. 문서화
/sc:document dashboard/ --type api
# → ✍️ scribe Persona가 포괄적인 문서 생성
```

#### 버그 조사 및 해결
체계적인 Debugging을 위해:

```bash
# 1. 문제 조사
/sc:troubleshoot "login randomly fails" --think
# → 🔍 analyzer Persona + Sequential MCP 방법론

# 2. 근본 원인 분석
/sc:analyze auth-flow/ --focus debugging
# → 증거 수집을 통한 체계적인 조사

# 3. 수정 구현
/sc:improve auth/ --safe-mode --validate
# → 검증을 통한 안전한 개선

# 4. 검증 테스팅
/sc:test auth-flow/ --coverage
# → 수정이 작동하는지 확인하기 위한 포괄적인 테스팅
```

#### 코드 품질 개선
기존 코드를 개선할 때:

```bash
# 1. 품질 평가
/sc:analyze legacy-code/ --focus quality
# → 🔄 refactorer Persona가 개선 기회 식별

# 2. 안전한 개선
/sc:improve --preview legacy-code/
# → 적용하기 전에 변경될 내용 확인

# 3. 개선 적용
/sc:improve --safe legacy-code/
# → 위험이 낮은 개선만 적용

# 4. 변경 검증
/sc:test --coverage improved-code/
# → 개선이 기존 기능을 손상시키지 않는지 확인
```

### 일반적인 Workflow 조합 🤝

#### Security 우선 개발
```bash
# Security 중심 개발
/sc:analyze --persona-security --focus security
/sc:build --validate --safe-mode
/sc:test --type security
/sc:git --persona-security --validate
```

#### Performance 최적화 Workflow
```bash
# Performance 중심 개발
/sc:analyze --focus performance --persona-performance
/sc:improve --type performance --benchmark
/sc:test --focus performance --play
/sc:test --focus performance --play
```

#### 팀 협업 Workflow
```bash
# 협업 개발 패턴
/sc:analyze team-code/ --persona-qa --focus quality
/sc:document features/ --persona-scribe --type guide
/sc:git --smart-commit --branch-strategy
/sc:task status  # 팀 진행 상황 확인
```

### 고급 Workflow 패턴 🚀

#### 대규모 Codebase 관리
엔터프라이즈 규모 Project에서 작업할 때:

```bash
# 효율적인 대규모 분석
/sc:analyze monorepo/ --delegate auto --uc --focus architecture
# → 병렬 처리 + 압축 + 아키텍처 중심

# 체계적인 개선
/sc:improve legacy-system/ --wave-mode auto --safe-mode
# → 안전 확인을 통한 다단계 개선

# 포괄적인 품질 검토
/sc:analyze enterprise-app/ --delegate folders --focus quality
# → 분산 품질 분석
```

#### 레거시 시스템 현대화
오래된 Codebase를 업데이트할 때:

```bash
# 평가 단계
/sc:analyze legacy/ --persona-architect --ultrathink
# → 깊은 아키텍처 분석

# 기획 단계
/sc:design modernization-strategy --type architecture
# → 포괄적인 현대화 계획

# 구현 단계
/sc:improve legacy/ --wave-mode systematic --safe-mode --loop
# → 검증을 통한 반복적이고 안전한 개선

# 마이그레이션 지원
/sc:migrate --type framework legacy-to-modern/
# → Framework 마이그레이션 지원
```

#### 다중 도메인 Project
여러 기술 도메인에 걸친 Project의 경우:

```bash
# 도메인 간 조정
/sc:analyze fullstack-app/ --all-mcp --delegate auto
# → 모든 MCP Server + 병렬 처리

# 도메인별 개선
/sc:improve frontend/ --persona-frontend --magic
/sc:improve backend/ --persona-backend --c7
/sc:improve infrastructure/ --persona-devops --seq

# 통합 검증
/sc:test --type integration --play
# → 포괄적인 통합 테스팅
```

### Workflow 최적화 팁 💡

#### 작게 시작하여 확장
```bash
# 집중된 범위로 시작
/sc:analyze single-component.js --focus quality

# 필요에 따라 확장
/sc:analyze entire-module/ --focus quality --delegate files

# 전체 시스템으로 확장
/sc:analyze whole-project/ --delegate auto --uc
```

#### 점진적 향상 사용
```bash
# 기본 Command
/sc:build project/

# 인텔리전스 추가
/sc:build project/ --think --c7

# 전체 Orchestration
/sc:build project/ --wave-mode auto --all-mcp --delegate auto
```

#### 보완적인 Persona 결합
```bash
# Security + Performance 분석
/sc:analyze api/ --persona-security
/sc:analyze api/ --persona-performance

# 아키텍처 + 품질 검토
/sc:review system/ --persona-architect --focus architecture
/sc:review system/ --persona-qa --focus quality
```

### Workflow 문제 해결 🚨

#### Command가 예상대로 작동하지 않을 때
```bash
# 자기 성찰로 Debugging
/sc:troubleshoot "command issues" --introspect
# → 무엇이 잘못되었는지에 대한 메타인지 분석

# 다른 접근 방식 시도
/sc:analyze problem/ --persona-analyzer --seq
# → 체계적인 조사 방법론

# Framework 상태 확인
/sc:load framework-status/ --summary
# → 현재 SuperClaude 상태 이해
```

#### Performance가 느릴 때
```bash
# 속도 최적화
/sc:analyze large-project/ --no-mcp --uc --scope module
# → 추가 기능 비활성화, 출력 압축, 범위 제한

# 대규모 Task에 위임 사용
/sc:improve huge-codebase/ --delegate auto --concurrency 5
# → 제어된 동시성을 사용한 병렬 처리
```

#### 결과가 충분히 집중되지 않을 때
```bash
# 특정 초점 Flag 사용
/sc:analyze code/ --focus security --scope file

# 적절한 Persona 수동 활성화
/sc:analyze frontend-code/ --persona-security  # Frontend의 Security 관점

# 여러 접근 방식 결합
/sc:analyze --focus performance --persona-performance --play
```

### 자신만의 Workflow 구축 🛠️

#### 일반적인 패턴 식별
특정 요구에 잘 맞는 조합을 추적하세요:

```bash
# Security 중심 API 개발
alias secure-api="/build api/ --persona-security --validate --c7"

# Performance 최적화된 Frontend 작업
alias perf-frontend="/build ui/ --persona-performance --magic --benchmark"

# 품질 개선 Workflow
alias quality-check="/scan --focus quality && /improve --safe-mode && /test --coverage"
```

#### Flag 조합 실험
가장 잘 맞는 조합을 찾기 위해 다른 조합을 시도해보세요:

```bash
# 학습용: 문서와 함께 상세한 설명
/sc:explain concept --persona-mentor --verbose --c7

# 안전용: 최대 검증 및 확인
/sc:improve critical-code/ --safe-mode --validate --preview

# 효율성용: 병렬 처리를 통한 압축 출력
/sc:analyze big-project/ --uc --delegate auto --concurrency 3
```

기억하세요: SuperClaude는 성공적인 패턴에서 학습하므로 효과적인 조합을 더 많이 사용할수록 요구에 맞는 올바른 접근 방식을 자동 활성화하는 데 더 능숙해집니다.

---

## 통합 & 조정 🤝

SuperClaude의 Component가 어떻게 함께 작동하는지 이해하는 것이 Framework을 효과적으로 사용하는 열쇠입니다. 이 섹션에서는 Command, Flag, Persona 및 MCP Server가 자동으로 어떻게 조정되는지, 그리고 필요할 때 해당 조정을 제어하는 방법을 보여줍니다.

### 자동 조정 예시 🤖

SuperClaude는 Context에 따라 Component를 자동으로 조정합니다. 실제로 어떻게 작동하는지 살펴보겠습니다:

#### Frontend 개발 요청
```bash
/sc:build react-dashboard/
```

**자동 조정**:
- **Command**: `/build`가 Compilation 및 Bundling을 처리합니다
- **Persona**: 🎨 frontend가 자동 활성화됩니다 (React 감지)
- **MCP**: Magic이 최신 UI Component를 제공합니다
- **MCP**: Context7이 React 모범 사례를 제공합니다
- **Flag**: `--c7`이 Framework 문서를 위해 자동 활성화됩니다

**결과**: 최신 Component, 접근성 확인 및 Performance 최적화를 갖춘 React 최적화 빌드.

#### Security 분석 요청
```bash
/sc:scan user-authentication/ --focus security
```

**자동 조정**:
- **Command**: `/scan`이 Security 스캔을 처리합니다
- **Persona**: 🛡️ security가 자동 활성화됩니다 (Security 중심)
- **MCP**: Sequential이 체계적인 분석을 제공합니다
- **Flag**: `--validate`가 자동 활성화됩니다 (고위험 작업)
- **Flag**: `--think`가 자동 활성화됩니다 (복잡한 Security 패턴)

**결과**: 위협 모델링, 취약점 감지 및 규정 준수 확인을 포함한 포괄적인 Security 분석.

#### Performance 조사
```bash
/sc:troubleshoot "API responses are slow"
```

**자동 조정**:
- **Command**: `/troubleshoot`이 조사를 처리합니다
- **Persona**: ⚡ performance가 자동 활성화됩니다 (Performance 키워드)
- **Persona**: 🔍 analyzer가 조사 방법론을 제공합니다
- **MCP**: Sequential이 Debugging 프로세스를 구조화합니다
- **MCP**: Playwright가 Performance 테스팅을 제공합니다
- **Flag**: `--think`가 자동 활성화됩니다 (복잡한 Debugging)

**결과**: 메트릭, 병목 현상 식별 및 최적화 권장 사항을 포함한 체계적인 Performance 조사.

### 수동 조정 제어 🎛️

때로는 특정 요구에 맞게 자동 조정을 덮어쓰고 싶을 때가 있습니다:

#### Persona 선택 덮어쓰기
```bash
# Security 관점에서 Frontend 코드 보기
/sc:analyze react-components/ --persona-security
# → UI Component의 Security 분석 (XSS, 데이터 노출 등)

# 작은 유틸리티에 아키텍처적 사고 적용
/sc:improve utility-function.js --persona-architect
# → 간단한 코드에 대한 디자인 패턴 및 확장성
```

#### MCP Server 사용 제어
```bash
# 속도를 위해 모든 MCP Server 비활성화
/sc:analyze large-codebase/ --no-mcp
# → 40-60% 더 빠른 실행, 네이티브 Tool만 사용

# 포괄적인 분석을 위해 모든 MCP Server 활성화
/sc:analyze complex-system/ --all-mcp
# → 최대 기능, 더 높은 토큰 사용량

# 특정 MCP 조합 사용
/sc:build ui-components/ --magic --c7 --no-seq
# → UI 생성 + 문서, 복잡한 분석 건너뛰기
```

#### 여러 관점 결합
```bash
# 다른 Persona를 사용한 순차적 분석
/sc:analyze payment-system/ --persona-security     # Security 관점
/sc:analyze payment-system/ --persona-performance  # Performance 관점
/sc:analyze payment-system/ --persona-architect    # 아키텍처 관점

# 또는 자동으로 조정
/sc:review payment-system/ --focus quality
# → Security + Performance + 아키텍처 통찰력 자동 조정
```

### Flag 조정 패턴 🏁

Flag는 함께 작동하여 강력한 조합을 만듭니다:

#### 안전 우선 패턴
```bash
# 중요한 코드에 대한 최대 안전성
/sc:improve production-auth/ --safe-mode --validate --preview
# → 보수적인 변경 + 위험 평가 + 적용 전 미리보기

# 대규모 변경의 안전한 탐색
/sc:improve legacy-system/ --wave-mode auto --safe-mode --validate
# → 다단계 개선 + 안전 확인 + 검증 게이트
```

#### Performance 최적화 패턴
```bash
# 대규모 작업을 위한 빠른 실행
/sc:analyze huge-project/ --uc --no-mcp --scope module
# → 압축된 출력 + 네이티브 Tool + 제한된 범위

# 효율적인 병렬 처리
/sc:improve monorepo/ --delegate auto --uc --concurrency 5
# → 병렬 처리 + 압축 + 제어된 리소스 사용량
```

#### 학습 중심 패턴
```bash
# 전체 Context를 갖춘 교육적 설명
/sc:explain complex-concept --persona-mentor --verbose --c7
# → 교육적 접근 + 상세 설명 + 공식 문서

# 투명성을 갖춘 깊은 이해
/sc:analyze mysterious-code/ --persona-analyzer --think-hard --introspect
# → 조사 방법론 + 깊은 분석 + 사고 투명성
```

### MCP Server 조정 🔧

MCP Server는 종종 자동으로 함께 작동합니다:

#### 문서화 + 분석
```bash
/sc:improve old-react-code/
```
**MCP 조정**:
- Context7: 현재 React 모범 사례를 가져옵니다
- Sequential: 최신 패턴에 대해 코드를 분석합니다
- Magic: 최신 Component 패턴을 제안합니다
- 결과: 현재 표준을 사용한 현대화

#### 테스팅 + Performance
```bash
/sc:test dashboard/ --focus performance
```
**MCP 조정**:
- Sequential: 포괄적인 테스트 전략을 계획합니다
- Playwright: Performance 테스팅을 실행합니다
- Context7: 테스팅 모범 사례를 제공합니다
- 결과: 업계 표준을 사용한 Performance 테스팅

#### 복잡한 문제 해결
```bash
/sc:troubleshoot "complex multi-service issue" --ultrathink
```
**MCP 조정**:
- Sequential: 체계적인 조사를 구조화합니다
- Context7: Service 아키텍처 패턴을 제공합니다
- Playwright: Service 상호 작용을 테스트합니다
- 결과: 포괄적인 다중 도메인 Debugging

### Persona 협업 패턴 🎭

Persona는 복잡한 요청에 대해 자동으로 협업합니다:

#### 아키텍처 + Security
```bash
/sc:design payment-api --type secure
```
**Persona 협업**:
- 🏗️ architect: 시스템 설계 및 확장성
- 🛡️ security: 위협 모델링 및 안전한 패턴
- ⚙️ backend: API 구현 패턴
- 결과: 안전하고 확장 가능한 API 설계

#### Frontend + Performance
```bash
/sc:build dashboard --focus performance
```
**Persona 협업**:
- 🎨 frontend: UI/UX 및 접근성
- ⚡ performance: 최적화 및 메트릭
- 🏗️ architect: Component 아키텍처
- 결과: 빠르고 접근 가능하며 잘 구조화된 대시보드

#### 품질 + 리팩토링
```bash
/sc:improve legacy-code/ --focus quality
```
**Persona 협업**:
- 🔄 refactorer: 코드 품질 및 패턴
- 🧪 qa: 테스팅 및 검증
- 🏗️ architect: 구조적 개선
- 결과: 깨끗하고 테스트되었으며 잘 설계된 코드

### 고급 조정 전략 🚀

#### Wave Orchestration
복잡한 다단계 작업을 위해:

```bash
/sc:improve enterprise-system/ --wave-mode systematic
```

**Wave 조정**:
1. **분석 Wave**: 🔍 analyzer + Sequential이 현재 상태를 평가합니다
2. **기획 Wave**: 🏗️ architect + Context7이 개선 사항을 설계합니다
3. **구현 Wave**: 적절한 전문가 + Tool이 변경 사항을 구현합니다
4. **검증 Wave**: 🧪 qa + Playwright가 개선 사항을 확인합니다
5. **최적화 Wave**: ⚡ performance + 메트릭이 결과를 최적화합니다

#### 하위 에이전트 위임
병렬 처리를 위해:

```bash
/sc:analyze large-monorepo/ --delegate folders
```

**위임 조정**:
- **주 에이전트**: 결과를 조정하고 종합합니다
- **하위 에이전트**: 개별 폴더의 전문 분석
- **조정**: 도메인 전문 지식과 결합된 결과
- **MCP 통합**: 모든 에이전트 간 공유

#### 적응형 인텔리전스
SuperClaude는 Context에 따라 조정을 조정합니다:

**개발 단계 감지**:
- 기획 단계 → 🏗️ architect + ✍️ scribe 강조
- 구현 단계 → 도메인 전문가 + Magic/Context7
- 테스팅 단계 → 🧪 qa + Playwright 강조
- 배포 단계 → 🚀 devops + 검증 강조

**복잡도 기반 확장**:
- 단순 Task → 직접 실행
- 보통 복잡도 → Persona + MCP 조정
- 높은 복잡도 → Wave Orchestration + 위임

### 조정 문제 해결 🔧

#### 자동 조정이 잘못될 때
```bash
# 너무 많은 Tool이 활성화됨 (느리거나 비쌈)
/sc:analyze simple-file.js --no-mcp --answer-only
# → 단순 Task를 위한 최소한의 Tool

# 잘못된 Persona 활성화
/sc:analyze backend-api/ --persona-security
# → 명시적 Persona 선택으로 덮어쓰기

# 분석 깊이가 충분하지 않음
/sc:troubleshoot complex-issue --ultrathink --all-mcp
# → 최대 기능 강제
```

#### 조정 최적화
```bash
# 간단하게 시작하여 필요에 따라 복잡성 추가
/sc:analyze code.js                    # 기본 분석
/sc:analyze code.js --think            # 사고 추가
/sc:analyze code.js --think --c7       # 문서 추가
/sc:analyze code.js --think --c7 --seq # 체계적인 분석 추가
```

#### 조정 결정 이해
```bash
# 특정 Tool이 선택된 이유 확인
/sc:analyze complex-system/ --introspect
# → 의사 결정 과정 및 Tool 선택 추론 표시
```

### 통합을 위한 모범 사례 💡

#### 먼저 자동 조정이 작동하도록 두기
- SuperClaude의 자동 Tool 선택을 신뢰하세요
- 특정 관점이 필요할 때만 덮어쓰세요
- 간단한 Command로 시작하여 필요에 따라 Flag를 추가하세요

#### Flag 상호 작용 이해
- 일부 Flag는 다른 Flag를 덮어씁니다 (`--no-mcp`는 `--c7`, `--seq`를 덮어씀)
- 안전 Flag는 최적화 Flag보다 우선합니다
- Persona Flag는 더 구체적인 Persona 요청으로 덮어쓸 수 있습니다

#### 적절한 범위 사용
- 파일 수준: 단일 Persona + 최소 MCP
- 모듈 수준: 도메인 Persona + 관련 MCP
- 시스템 수준: 여러 Persona + 전체 MCP 조정

#### 리소스 사용량 모니터링
- 대규모 작업 → `--uc` 및 `--delegate` 사용
- 단순 Task → `--no-mcp` 및 `--answer-only` 사용
- 중요한 작업 → `--safe-mode` 및 `--validate` 사용

핵심은 SuperClaude의 지능이 단일 기능이 아닌 Component 간의 조정에서 나온다는 것을 이해하는 것입니다. 자동 조정은 대부분의 경우 잘 작동하지만, 제어 방법을 알면 어떤 상황이든 처리할 수 있는 유연성을 얻을 수 있습니다.

---

## 실제 예시 💡

SuperClaude가 실제로 작동하는 실제 시나리오. 이러한 예시는 다양한 Component가 함께 작동하여 일반적인 개발 문제를 해결하는 방법을 보여줍니다.

### 시나리오 1: 새 팀원 온보딩 👋

**상황**: 익숙하지 않은 React/Node.js 전자 상거래 Project에서 작업을 시작합니다.

#### 1단계: Project 이해
```bash
/sc:load --deep --summary
```
**일어나는 일**:
- 🔍 analyzer Persona 활성화 (조사 필요)
- Sequential MCP가 분석을 구조화합니다
- Context7 MCP가 Framework 패턴을 식별합니다
- 포괄적인 Project 개요를 생성합니다

**출력**: Project 구조, 기술 스택, 종속성 및 아키텍처 요약.

#### 2단계: 코드 품질 평가
```bash
/sc:analyze --focus quality
```
**자동 조정**:
- 🧪 qa Persona 활성화 (품질 중심)
- Sequential MCP가 체계적인 분석을 제공합니다
- 코드 품질, Security 및 Performance 문제를 스캔합니다
- 실행 가능한 개선 권장 사항을 생성합니다

**출력**: 특정 문제 및 개선 제안이 포함된 품질 보고서.

#### 3단계: 아키텍처 이해
```bash
/sc:analyze --focus architecture --persona-architect
```
**일어나는 일**:
- 🏗️ architect Persona가 시스템 설계 관점을 제공합니다
- Context7 MCP가 React/Node.js 아키텍처 패턴을 가져옵니다
- Sequential MCP가 아키텍처 분석을 구조화합니다
- 디자인 패턴, 데이터 흐름 및 Component 관계를 식별합니다

**출력**: 디자인 패턴 및 시스템 관계가 포함된 아키텍처 개요.

#### 4단계: 시작 가이드
```bash
/sc:document onboarding --type guide --persona-scribe
```
**일어나는 일**:
- ✍️ scribe Persona가 전문 문서를 생성합니다
- Context7 MCP가 문서 표준을 제공합니다
- 이전 분석을 신규 이민자 친화적인 가이드로 종합합니다
- 설정 지침 및 핵심 개념을 포함합니다

**출력**: 향후 팀원을 위한 포괄적인 온보딩 가이드.

**절약된 시간**: 보통 2-3일의 탐색이 필요한 작업이 약 30분 만에 포괄적인 이해로 압축됩니다.

### 시나리오 2: Security 취약점 조사 🛡️

**상황**: Security 스캐너가 사용자 인증 시스템에서 잠재적인 문제를 발견했습니다.

#### 1단계: Security 중심 분석
```bash
/sc:scan auth-system/ --persona-security --focus security
```
**자동 조정**:
- 🛡️ security Persona 활성화 (Security 전문 지식)
- Sequential MCP가 체계적인 위협 모델링을 제공합니다
- Context7 MCP가 OWASP 및 Security 모범 사례를 가져옵니다
- `--validate` Flag 자동 활성화 (고위험 작업)

**출력**: 위협 평가 및 취약점 우선 순위가 포함된 상세한 Security 분석.

#### 2단계: 근본 원인 조사
```bash
/sc:troubleshoot "JWT token exposure in logs" --think --seq
```
**일어나는 일**:
- 🔍 analyzer Persona가 조사 방법론을 제공합니다
- `--think` Flag가 깊은 분석을 가능하게 합니다
- Sequential MCP가 Debugging 프로세스를 구조화합니다
- 데이터 흐름을 추적하고 노출 지점을 식별합니다

**출력**: 증거 추적 및 영향 평가가 포함된 근본 원인 분석.

#### 3단계: 안전한 구현
```bash
/sc:improve auth-system/ --focus security --safe-mode --validate
```
**자동 조정**:
- 🛡️ security Persona가 Security 초점을 유지합니다
- `--safe-mode`가 보수적인 변경을 보장합니다
- `--validate`가 적용하기 전에 변경 사항을 확인합니다
- Context7 MCP가 안전한 코딩 패턴을 제공합니다

**출력**: 최소한의 위험과 포괄적인 검증을 통한 Security 개선.

#### 4단계: Security 테스팅
```bash
/sc:test auth-system/ --type security --play
```
**일어나는 일**:
- 🧪 qa Persona가 테스팅 전문 지식을 제공합니다
- Playwright MCP가 Security 테스팅 시나리오를 실행합니다
- 인증 흐름, 세션 관리 및 액세스 제어를 테스트합니다
- Security 개선이 작동하는지 확인합니다

**출력**: 개선 효과의 증거가 포함된 포괄적인 Security 테스트 결과.

**위험 감소**: 체계적인 접근 방식은 Security 문제를 놓칠 가능성을 줄이고 포괄적인 범위를 보장합니다.

### 시나리오 3: Performance 최적화 스프린트 ⚡

**상황**: 전자 상거래 대시보드 로딩이 느려 사용자 경험에 영향을 미칩니다.

#### 1단계: Performance 분석
```bash
/sc:analyze dashboard/ --focus performance --persona-performance
```
**자동 조정**:
- ⚡ performance Persona 활성화 (Performance 전문 지식)
- Playwright MCP가 Performance 메트릭 및 테스팅을 제공합니다
- Context7 MCP가 React Performance 모범 사례를 가져옵니다
- `--think-hard` 자동 활성화 (복잡한 Performance 분석)

**출력**: 메트릭 및 우선 순위가 지정된 최적화 기회가 포함된 Performance 병목 현상 식별.

#### 2단계: Frontend Performance 심층 분석
```bash
/sc:analyze frontend/ --persona-frontend --focus performance --play
```
**일어나는 일**:
- 🎨 frontend Persona가 UI/UX 관점을 제공합니다
- ⚡ performance Persona가 조정합니다 (이중 전문 지식)
- Playwright MCP가 Core Web Vitals, 번들 크기, 렌더링 시간을 측정합니다
- Magic MCP가 최신 최적화 패턴을 제안합니다

**출력**: 접근성 및 사용자 경험 고려 사항이 포함된 Frontend별 Performance 분석.

#### 3단계: Backend API Performance
```bash
/sc:analyze api/ --persona-backend --focus performance
```
**자동 조정**:
- ⚙️ backend Persona가 서버 측 전문 지식을 제공합니다
- Sequential MCP가 Database 쿼리 및 API 패턴을 분석합니다
- Context7 MCP가 Node.js/Express 최적화 패턴을 제공합니다
- 느린 쿼리, 비효율적인 Endpoint 및 Caching 기회를 식별합니다

**출력**: Database 및 API 최적화 권장 사항이 포함된 Backend Performance 분석.

#### 4단계: 체계적인 최적화
```bash
/sc:improve dashboard/ --focus performance --loop --iterations 3
```
**일어나는 일**:
- ⚡ performance Persona가 최적화를 주도합니다
- `--loop`가 반복적인 개선을 가능하게 합니다
- 각 반복: 최적화 → 측정 → 검증 → 개선
- 메트릭 검증을 통한 점진적 향상

**출력**: 각 주기 후 측정 가능한 결과가 포함된 반복적인 Performance 개선.

#### 5단계: Performance 테스팅 검증
```bash
/sc:test dashboard/ --focus performance --play --benchmark
```
**일어나는 일**:
- Playwright MCP가 포괄적인 Performance 테스팅을 실행합니다
- 여러 장치, 네트워크 조건 및 브라우저에서 테스트합니다
- Core Web Vitals, 로드 시간 및 사용자 상호 작용 메트릭을 측정합니다
- 개선이 Performance 예산을 충족하는지 확인합니다

**출력**: 최적화 효과를 증명하는 Performance 테스트 결과.

**Performance 향상**: 체계적인 접근 방식은 일반적으로 측정 가능한 검증을 통해 40-70%의 Performance 개선을 달성합니다.

### 시나리오 4: 레거시 코드 현대화 🔄

**상황**: 5년 된 React 애플리케이션을 현재 표준으로 현대화해야 합니다.

#### 1단계: 레거시 평가
```bash
/sc:analyze legacy-app/ --persona-architect --ultrathink
```
**자동 조정**:
- 🏗️ architect Persona가 구조적 분석을 제공합니다
- `--ultrathink`가 최대 분석 깊이를 가능하게 합니다
- Context7 MCP가 현재 React 패턴과 비교합니다
- Sequential MCP가 체계적인 현대화 평가를 제공합니다

**출력**: 현대화 Roadmap 및 위험 평가가 포함된 포괄적인 레거시 분석.

#### 2단계: 현대화 기획
```bash
/sc:design modernization-strategy --type architecture --persona-architect
```
**일어나는 일**:
- 🏗️ architect Persona가 마이그레이션 전략을 설계합니다
- Context7 MCP가 현재 React 생태계 패턴을 제공합니다
- Sequential MCP가 현대화 계획을 구조화합니다
- 마이그레이션 단계, 종속성 및 위험을 식별합니다

**출력**: 단계별 접근 방식 및 위험 완화가 포함된 상세한 현대화 계획.

#### 3단계: 안전한 점진적 개선
```bash
/sc:improve legacy-components/ --safe-mode --wave-mode systematic --loop
```
**자동 조정**:
- 🔄 refactorer Persona가 코드 개선을 주도합니다
- `--safe-mode`가 최소한의 위험을 보장합니다
- `--wave-mode systematic`이 다단계 개선을 가능하게 합니다
- `--loop`가 반복적인 개선을 허용합니다
- 여러 Persona 조정: architect, frontend, qa

**출력**: 안전 확인 및 점진적 향상을 통한 체계적인 현대화.

#### 4단계: 현대화 테스팅
```bash
/sc:test modernized-app/ --type integration --coverage --play
```
**일어나는 일**:
- 🧪 qa Persona가 현대화 전반에 걸쳐 품질을 보장합니다
- Playwright MCP가 포괄적인 테스팅을 제공합니다
- 레거시 호환성 및 새로운 기능을 테스트합니다
- 현대화가 기존 Feature를 손상시키지 않는지 확인합니다

**출력**: 현대화 성공을 증명하는 포괄적인 테스트 결과.

**현대화 성공**: 체계적인 접근 방식은 현대화 위험을 80% 줄이고 호환성을 보장합니다.

### 시나리오 5: 다중 팀 API 설계 🌐

**상황**: 여러 팀이 사용할 새로운 마이크로서비스 API를 설계합니다.

#### 1단계: 요구 사항 분석
```bash
/sc:design user-service-api --type api --persona-backend
```
**자동 조정**:
- ⚙️ backend Persona가 API 설계 전문 지식을 제공합니다
- 🏗️ architect Persona가 시스템 통합을 위해 조정합니다
- Context7 MCP가 API 설계 모범 사례를 제공합니다
- Sequential MCP가 요구 사항 분석을 구조화합니다

**출력**: Endpoint, 데이터 모델 및 통합 패턴이 포함된 포괄적인 API 설계.

#### 2단계: Security 검토
```bash
/sc:review api-design/ --persona-security --focus security
```
**일어나는 일**:
- 🛡️ security Persona가 API Security를 평가합니다
- 인증, 권한 부여 및 데이터 보호를 검토합니다
- Context7 MCP가 OWASP API Security 가이드라인을 제공합니다
- Security 요구 사항 및 위협 벡터를 식별합니다

**출력**: 강화 권장 사항 및 규정 준수 요구 사항이 포함된 Security 평가.

#### 3단계: Performance 고려 사항
```bash
/sc:analyze api-design/ --persona-performance --focus performance
```
**자동 조정**:
- ⚡ performance Persona가 확장성을 평가합니다
- Endpoint Performance, Caching 전략, 속도 제한을 분석합니다
- Context7 MCP가 고성능 API 패턴을 제공합니다
- 부하 상태에서의 Performance를 예측합니다

**출력**: 확장성 권장 사항 및 최적화 전략이 포함된 Performance 분석.

#### 4단계: 여러 팀을 위한 문서화
```bash
/sc:document api/ --type api --persona-scribe --detailed
```
**일어나는 일**:
- ✍️ scribe Persona가 전문 API 문서를 생성합니다
- Context7 MCP가 API 문서 표준을 제공합니다
- 예시, 통합 가이드 및 문제 해결을 생성합니다
- 여러 소비 팀에 맞게 조정됩니다

**출력**: 예시, 통합 가이드 및 모범 사례가 포함된 포괄적인 API 문서.

#### 5단계: 구현 검증
```bash
/sc:build api-implementation/ --validate --test-coverage
```
**자동 조정**:
- ⚙️ backend Persona가 API 패턴을 구현합니다
- 🧪 qa Persona가 품질 및 테스팅을 보장합니다
- Sequential MCP가 설계에 대해 구현을 검증합니다
- 포괄적인 테스팅 및 검증

**출력**: 포괄적인 테스팅 및 검증을 갖춘 Production 준비 API 구현.

**협업 효율성**: 다중 Persona 조정은 설계 반복 주기를 60% 줄이고 교차 팀 조정을 개선합니다.

### 일반적인 패턴 인식 🔍

이러한 예시는 SuperClaude Component가 어떻게 조정되는지에 대한 반복적인 패턴을 보여줍니다:

#### 조사 → 분석 → 구현 → 검증
대부분의 복잡한 Workflow는 각 단계에 적절한 Persona 및 Tool을 사용하여 이 패턴을 따릅니다.

#### 다중 Persona 조정
복잡한 문제는 여러 관점(Security + Performance, 아키텍처 + Frontend 등)에서 이점을 얻습니다.

#### 점진적 향상
간단하게 시작하여 필요에 따라 복잡성을 추가합니다 (`--think` → `--think-hard` → `--ultrathink`).

#### 안전 우선 접근 방식
중요한 작업에는 자동으로 검증 및 안전 확인이 포함됩니다 (`--safe-mode`, `--validate`).

#### Context 인식 Tool 선택
SuperClaude는 감지된 Context에 따라 적절한 MCP Server 및 Flag를 자동으로 선택합니다.

이러한 예시는 SuperClaude의 가치가 단일 기능이 아닌 Component의 지능적인 조정에서 비롯된다는 것을 보여줍니다. Framework은 일관된 품질 및 안전 표준을 유지하면서 요구에 적응합니다.

---

## 팁 & 모범 사례 🎯

실제 사용 패턴 및 성공적인 Workflow를 기반으로 SuperClaude를 최대한 활용하기 위한 실제 팁을 제공합니다.

### 성공적으로 시작하기 🚀

#### 간단한 Command로 시작
```bash
# 여기서 시작 - 기본 기능
/sc:help
/sc:analyze README.md
/sc:build --help

# 여기서 아님 - 복잡한 Orchestration
/sc:improve entire-codebase/ --wave-mode force --all-mcp --delegate auto
```

**이유**: 복잡성을 추가하기 전에 기본 동작을 이해하면 혼란을 방지하고 Framework을 점진적으로 배우는 데 도움이 됩니다.

#### 먼저 자동 활성화 신뢰
```bash
# SuperClaude가 Tool을 선택하도록 둠
/sc:analyze auth-system/
# → 자동 활성화되는 것 확인 (아마도 Security Persona + 검증)

# 그런 다음 수동 제어 실험
/sc:analyze auth-system/ --persona-performance
# → 동일한 코드에 대한 다른 관점 보기
```

**이유**: 자동 활성화는 보통 올바르게 작동하며 다양한 시나리오에 대한 최적의 Tool 조합을 보여줍니다.

#### 미리보기 및 안전 모드 사용
```bash
# 먼저 무슨 일이 일어날지 확인
/sc:improve messy-code.js --preview

# 안전하게 변경 사항 적용
/sc:improve messy-code.js --safe-mode

# 중요한 코드의 경우 둘 다 사용
/sc:improve production-auth/ --preview --safe-mode --validate
```

**이유**: 의도하지 않은 변경을 방지하고 SuperClaude가 무엇을 할지 하기 전에 이해하는 데 도움이 됩니다.

### Flag 사용 패턴 🏁

#### 간단하게 시작하여 복잡성 추가
```bash
# 기본 Command
/sc:analyze complex-system/

# 필요한 경우 사고 추가
/sc:analyze complex-system/ --think

# 외부 라이브러리가 관련된 경우 문서 추가
/sc:analyze complex-system/ --think --c7

# 중요한 시스템에 대한 전체 분석
/sc:analyze complex-system/ --think-hard --c7 --seq --validate
```

**이유**: 점진적인 복잡성은 각 Flag가 무엇을 추가하는지 이해하는 데 도움이 되며 간단한 문제를 과도하게 엔지니어링하는 것을 방지합니다.

#### 잘 작동하는 일반적인 Flag 조합
```bash
# 안전한 개선 Workflow
/sc:improve --preview → /improve --safe-mode → /test --coverage

# 깊은 조사 Workflow
/sc:troubleshoot issue --think --seq → /analyze affected-code/ --focus quality

# 학습 및 문서화 Workflow
/sc:explain concept --persona-mentor --verbose --c7

# Performance 최적화 Workflow
/sc:analyze --focus performance --persona-performance --play
```

**이유**: 이러한 조합은 함께 잘 작동하고 충돌하지 않는 입증된 패턴입니다.

#### Flag 충돌 방지
```bash
# ❌ 충돌하는 Flag
/sc:analyze code/ --no-mcp --c7  # --no-mcp가 --c7을 덮어씀

# ❌ 비생산적인 조합
/sc:analyze small-file.js --ultrathink --all-mcp  # 단순 Task에 과도함

# ✅ 합리적인 조합
/sc:analyze large-system/ --think --delegate auto  # 복잡성에 적합
/sc:analyze simple-utility.js --answer-only       # 단순성에 적합
```

**이유**: Flag 우선 순위 및 상호 작용을 이해하면 예기치 않은 동작과 낭비되는 리소스를 방지할 수 있습니다.

### Persona 최적화 🎭

#### 도메인 자동 활성화가 작동하도록 두기
```bash
# 이것들은 자동으로 올바른 Persona를 얻습니다
/sc:build react-components/     # → frontend Persona
/sc:scan auth/ --focus security # → security Persona
/sc:troubleshoot slow-api/      # → performance + analyzer Persona
```

**이유**: 자동 활성화는 입증된 패턴을 기반으로 하며 보통 가장 적절한 전문 지식을 선택합니다.

#### 다른 관점을 위한 수동 덮어쓰기
```bash
# 동일한 코드에 대한 다른 관점 얻기
/sc:analyze payment-flow/ --persona-security    # Security 관점
/sc:analyze payment-flow/ --persona-performance # Performance 관점
/sc:analyze payment-flow/ --persona-architect   # 아키텍처 관점
```
