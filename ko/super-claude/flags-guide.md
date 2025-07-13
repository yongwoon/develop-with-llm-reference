# SuperClaude Flags 사용자 가이드 🏁

## 🤖 대부분의 Flag는 자동으로 활성화됩니다 - 스트레스 받지 마세요!

**솔직한 진실**: 이 Flag들을 외울 필요가 없습니다. SuperClaude는 보통 당신이 하고 있는 일에 따라 유용한 Flag들을 추가하려고 시도합니다!

**실제로 일어나는 일:**
- 당신이 `/analyze auth.js`를 입력합니다
- SuperClaude는 그것이 Security 관련 코드임을 감지합니다
- **보통 `--persona-security`, `--focus security`, `--validate`를 추가합니다**
- 당신은 종종 Flag를 관리하지 않고도 전문적인 Security 분석을 받게 됩니다

**언제 수동으로 Flag를 사용할 수 있나요?**
- SuperClaude가 선택한 것을 **덮어쓰고** 싶을 때 (드묾)
- 특정 측면에 대해 **궁금할** 때 (`--focus performance`)
- 다른 접근 방식을 **실험해보고** 싶을 때

**결론**: 그냥 기본 Command를 사용하고 자동 활성화가 작동하도록 두세요. 이 Flag들은 당신이 필요할 때를 위해 있는 것이지, 당신이 필요하기 때문에 있는 것이 아닙니다. 🎯

---

## 🚀 그냥 이것들을 시도해보세요 (Flag 지식 필요 없음)

```bash
# 이것들은 Flag 지식 없이도 잘 작동합니다:
/sc:analyze src/                    # 올바른 분석 Flag를 자동 선택
/sc:build                          # Project에 따라 자동 최적화
/sc:improve messy-code.js          # 품질 및 안전 Flag를 자동 활성화
/sc:troubleshoot "weird error"     # Debugging 및 분석 Flag를 자동 활성화
```

**보셨죠? Flag가 필요 없습니다.** 아래의 모든 내용은 당신이 배후에서 무슨 일이 일어나고 있는지 궁금해질 때를 위한 것입니다.

---

SuperClaude의 Flag 시스템에 대한 실용적인 가이드입니다. Flag는 SuperClaude의 동작을 변경하는 Command-line 옵션과 같습니다 - Command에 대한 초능력이라고 생각하세요.

## Flag란 무엇인가요? 🤔

**Flag는 수정자**로, SuperClaude가 요청을 처리하는 방식을 변경합니다. Command 뒤에 오며 `--`로 시작합니다.

**기본 구문** (하지만 보통 이것을 알 필요는 없습니다):
```bash
/sc:command --flag-name
/sc:command --flag-name value
/sc:analyze src/ --focus security --depth deep
```

**실제로 Flag가 작동하는 방식**:
1. **자동 활성화** - SuperClaude가 Context에 따라 추가합니다 (이것이 주요 방식입니다! 🎯)
2. **수동 덮어쓰기** - 다른 동작을 원할 경우 명시적으로 추가할 수 있습니다

**Flag가 존재하는 이유** (주로 자동적인 이점):
- 더 좋고 집중된 결과를 얻습니다
- 올바른 사고 깊이를 자동 활성화합니다
- 유용할 때 특별한 기능에 연결합니다
- Task에 따라 속도나 세부 사항을 최적화합니다
- 실제로 작업하고 있는 것에 주의를 집중시킵니다

**핵심**: SuperClaude는 당신이 생각할 필요가 없도록 Flag 선택을 지능적으로 처리합니다! 🧠

## Flag 카테고리 📂

### 기획 & 분석 Flag 🧠

이들은 SuperClaude가 요청에 대해 얼마나 깊이 생각하는지를 제어합니다.

#### `--plan`
**기능**: 무언가를 하기 전에 실행 계획을 보여줍니다
**사용 시점**: SuperClaude가 먼저 무엇을 할지 보고 싶을 때
**예시**: `/build --plan` - 실행하기 전에 빌드 단계를 봅니다

#### `--think`
**기능**: 다중 파일 분석 (~4K 토큰)
**사용 시점**: 여러 파일과 관련된 복잡한 문제
**자동 활성화**: 5개 이상의 파일 Import 체인, 10개 이상의 참조가 있는 모듈 간 호출
**예시**: `/analyze complex-system/ --think`

#### `--think-hard`
**기능**: 깊은 아키텍처 분석 (~10K 토큰)
**사용 시점**: 시스템 전반의 문제, 아키텍처 결정
**자동 활성화**: 시스템 리팩토링, 3개 이상의 모듈에 걸친 병목 현상
**예시**: `/improve legacy-system/ --think-hard`

#### `--ultrathink`
**기능**: 최대 깊이 분석 (~32K 토큰)
**사용 시점**: 중요한 시스템 재설계, 복잡한 Debugging
**자동 활성화**: 레거시 현대화, 중요한 취약점
**예시**: `/troubleshoot "entire auth system broken" --ultrathink`

**💡 팁**: `--think`로 시작하고, 필요할 때만 더 깊이 들어가세요. 더 많이 생각할수록 느리지만 더 철저합니다.

---

### 효율성 & 제어 Flag ⚡

출력 스타일, 안전성 및 Performance를 제어합니다.

#### `--uc` / `--ultracompressed`
**기능**: 기호를 사용하여 60-80% 토큰 감소
**사용 시점**: 대규모 작업, Context가 가득 찰 때
**자동 활성화**: Context 사용량 >75%, 대규모 작업
**예시**: `/analyze huge-codebase/ --uc`

#### `--safe-mode`
**기능**: 최대 유효성 검사, 보수적인 실행
**사용 시점**: Production 환경, 위험한 작업
**자동 활성화**: 리소스 사용량 >85%, Production 환경
**예시**: `/improve production-code/ --safe-mode`

#### `--validate`
**기능**: 작업 전 유효성 검사 및 위험 평가
**사용 시점**: 변경하기 전에 확인하고 싶을 때
**자동 활성화**: 위험 점수 >0.7
**예시**: `/cleanup legacy/ --validate`

#### `--verbose`
**기능**: 최대 세부 정보 및 설명
**사용 시점**: 학습, Debugging, 전체 Context가 필요할 때
**예시**: `/build --verbose` - 모든 빌드 단계를 봅니다

#### `--answer-only`
**기능**: Task 생성 없이 직접적인 응답
**사용 시점**: 빠른 질문, Workflow 자동화를 원하지 않을 때
**예시**: `/explain React hooks --answer-only`

**💡 팁**: `--uc`는 큰 작업에 좋습니다. `--safe-mode`는 중요한 모든 것에 사용하세요. `--verbose`는 학습할 때 사용하세요.

---

### MCP Server Flag 🔧

MCP Server를 통해 전문화된 기능을 활성화합니다.

#### `--c7` / `--context7`
**기능**: 공식 라이브러리 문서를 위해 Context7을 활성화합니다
**사용 시점**: Framework으로 작업할 때, 공식 문서가 필요할 때
**자동 활성화**: 외부 라이브러리 Import, Framework 질문
**예시**: `/build react-app/ --c7` - React 모범 사례를 얻습니다

#### `--seq` / `--sequential`
**기능**: 복잡한 다단계 분석을 위해 Sequential을 활성화합니다
**사용 시점**: 복잡한 Debugging, 시스템 설계
**자동 활성화**: 복잡한 Debugging, `--think` Flag
**예시**: `/troubleshoot "auth flow broken" --seq`

#### `--magic`
**기능**: UI Component 생성을 위해 Magic을 활성화합니다
**사용 시점**: UI Component, 디자인 시스템 생성
**자동 활성화**: UI Component 요청, Frontend Persona
**예시**: `/build dashboard --magic` - 최신 UI Component를 얻습니다

#### `--play` / `--playwright`
**기능**: 브라우저 자동화 및 테스팅을 위해 Playwright를 활성화합니다
**사용 시점**: E2E 테스팅, Performance 모니터링
**자동 활성화**: Test Workflow, QA Persona
**예시**: `/test e2e --play`

#### `--all-mcp`
**기능**: 모든 MCP Server를 동시에 활성화합니다
**사용 시점**: 복잡한 다중 도메인 문제
**자동 활성화**: 문제 복잡도 >0.8, 다중 도메인 지표
**예시**: `/analyze entire-app/ --all-mcp`

#### `--no-mcp`
**기능**: 모든 MCP Server를 비활성화하고, 네이티브 Tool만 사용합니다
**사용 시점**: 더 빠른 실행, 전문화된 기능이 필요 없을 때
**예시**: `/analyze simple-script.js --no-mcp`

**💡 팁**: MCP Server는 기능을 추가하지만 더 많은 토큰을 사용합니다. 문서에는 `--c7`, 생각에는 `--seq`, UI에는 `--magic`을 사용하세요.

---

### 고급 Orchestration Flag 🎭

복잡한 작업 및 Workflow를 위한 것입니다.

#### `--delegate [files|folders|auto]`
**기능**: 병렬 처리를 위해 하위 에이전트 위임을 활성화합니다
**사용 시점**: 대규모 Codebase, 복잡한 분석
**자동 활성화**: 7개 이상의 디렉토리 또는 50개 이상의 파일
**옵션**:
- `files` - 개별 파일 분석 위임
- `folders` - 디렉토리 수준 분석 위임
- `auto` - 스마트 위임 전략

**예시**: `/analyze monorepo/ --delegate auto`

#### `--wave-mode [auto|force|off]`
**기능**: 복합 지능을 사용한 다단계 실행
**사용 시점**: 복잡한 개선, 체계적인 분석
**자동 활성화**: 복잡도 >0.8 AND 파일 >20 AND 작업 유형 >2
**예시**: `/improve legacy-system/ --wave-mode force`

#### `--loop`
**기능**: 반복적인 개선 모드
**사용 시점**: 품질 개선, 구체화 작업
**자동 활성화**: polish, refine, enhance 키워드
**예시**: `/improve messy-code.js --loop`

#### `--concurrency [n]`
**기능**: 최대 동시 하위 에이전트 수 제어 (1-15)
**사용 시점**: 리소스 사용량 제어
**예시**: `/analyze --delegate auto --concurrency 3`

**💡 팁**: 이것들은 강력하지만 복잡합니다. 큰 Project에는 `--delegate auto`로, 개선에는 `--loop`로 시작하세요.

---

### 초점 & 범위 Flag 🎯

SuperClaude의 주의를 특정 영역으로 향하게 합니다.

#### `--scope [level]`
**옵션**: file, module, project, system
**기능**: 분석 범위 설정
**예시**: `/analyze --scope module auth/`

#### `--focus [domain]`
**옵션**: performance, security, quality, architecture, accessibility, testing
**기능**: 특정 도메인에 분석 초점
**예시**: `/analyze --focus security --scope project`

#### Persona Flag
**사용 가능한 Persona**: architect, frontend, backend, analyzer, security, mentor, refactorer, performance, qa, devops, scribe
**기능**: 전문가 행동 패턴 활성화
**예시**: `/analyze --persona-security` - Security 중심 분석

**💡 팁**: `--focus`는 대상 분석에 좋습니다. Persona는 자동 활성화되지만 수동 제어가 도움이 됩니다.

---

## 일반적인 Flag 패턴 🔄

### 빠른 분석
```bash
/sc:analyze src/ --focus quality          # 빠른 품질 확인
/sc:analyze --uc --focus security         # 빠른 Security 스캔
```

### 심층 조사
```bash
/sc:troubleshoot "bug" --think --seq      # 체계적인 Debugging
/sc:analyze --think-hard --focus architecture  # 아키텍처 분석
```

### 대규모 Project 작업
```bash
/sc:analyze monorepo/ --delegate auto --uc     # 효율적인 대규모 분석
/sc:improve legacy/ --wave-mode auto --safe-mode  # 안전한 체계적 개선
```

### 학습 & 문서화
```bash
/sc:explain React hooks --c7 --verbose    # 문서와 함께 상세한 설명
/sc:document api/ --persona-scribe        # 전문적인 문서화
```

### Performance 중심
```bash
/sc:analyze --focus performance --play     # 테스팅을 통한 Performance 분석
/sc:build --uc --no-mcp                   # 추가 기능 없는 빠른 빌드
```

### Security 중심
```bash
/sc:analyze --focus security --think --validate  # 철저한 Security 분석
/sc:scan --persona-security --safe-mode         # 보수적인 Security 스캔
```

## 실제 예시 💡

### 전/후: 기본 분석
**전** (기본):
```bash
/sc:analyze auth.js
# → 간단한 파일 분석
```

**후** (Flag 사용):
```bash
/sc:analyze auth.js --focus security --think --c7
# → Security 중심 분석, 깊은 사고 및 공식 문서 포함
# → 훨씬 더 철저하고, Security 패턴을 찾고, 모범 사례와 비교 확인
```

### 전/후: 대규모 Project
**전** (느림):
```bash
/sc:analyze huge-monorepo/
# → 모든 것을 한 번에 분석하려고 시도하여 시간 초과 또는 너무 많은 토큰 사용 가능
```

**후** (효율적):
```bash
/sc:analyze huge-monorepo/ --delegate auto --uc --focus architecture
# → 하위 에이전트에게 작업 위임, 출력 압축, 아키텍처에 집중
# → 더 빠르고, 더 집중되고, 더 나은 결과
```

### 전/후: 개선 작업
**전** (위험):
```bash
/sc:improve legacy-system/
# → 너무 많은 변경을 하여 시스템을 망가뜨릴 수 있음
```

**후** (안전):
```bash
/sc:improve legacy-system/ --safe-mode --loop --validate --preview
# → 안전한 변경만, 반복적인 접근, 먼저 유효성 검사, 미리보기 표시
# → 훨씬 더 안전하고 점진적인 개선
```

## 자동 활성화 예시 🤖

SuperClaude는 보통 Context에 따라 Flag를 추가합니다. 시도하는 경우는 다음과 같습니다:

### 복잡도 기반
```bash
/sc:analyze huge-codebase/
# 자동 추가: --delegate auto --uc
# 이유: 50개 이상의 파일 감지, Context 관리 필요

/sc:troubleshoot "complex system issue"
# 자동 추가: --think --seq
# 이유: 다중 Component 문제 감지
```

### 도메인 기반
```bash
/sc:build react-app/
# 자동 추가: --c7 --persona-frontend
# 이유: Frontend Framework 감지

/sc:analyze --focus security
# 자동 추가: --persona-security --validate
# 이유: Security 초점이 Security 전문가를 트리거
```

### Performance 기반
```bash
# Context 사용량 >75%일 때
/sc:analyze large-project/
# 자동 추가: --uc
# 이유: 토큰 최적화 필요

# 위험 점수 >0.7일 때
/sc:improve production-code/
# 자동 추가: --safe-mode --validate
# 이유: 고위험 작업 감지
```

## 고급 사용법 🚀

### 복잡한 Flag 조합

**포괄적인 코드 리뷰**:
```bash
/sc:review codebase/ --persona-qa --think-hard --focus quality --validate --c7
# → QA 전문가 + 깊은 사고 + 품질 초점 + 유효성 검사 + 문서
```

**레거시 시스템 현대화**:
```bash
/sc:improve legacy/ --wave-mode force --persona-architect --safe-mode --loop --c7
# → Wave Orchestration + 아키텍트 관점 + 안전성 + 반복 + 문서
```

**Security 감사**:
```bash
/sc:scan --persona-security --ultrathink --focus security --validate --seq
# → Security 전문가 + 최대 사고 + Security 초점 + 유효성 검사 + 체계적인 분석
```

### Performance 최적화

**속도를 위해**:
```bash
/sc:analyze --no-mcp --uc --scope file
# → 추가 기능 비활성화, 출력 압축, 범위 제한
```

**철저함을 위해**:
```bash
/sc:analyze --all-mcp --think-hard --delegate auto
# → 모든 기능, 깊은 사고, 병렬 처리
```

### 맞춤형 Workflow

**버그 조사 Workflow**:
```bash
/sc:troubleshoot "specific error" --seq --think --validate
/sc:analyze affected-files/ --focus quality --persona-analyzer
/sc:test --play --coverage
```

**Feature 개발 Workflow**:
```bash
/sc:design new-feature --persona-architect --c7
/sc:build --magic --persona-frontend --validate
/sc:test --play --coverage
/sc:document --persona-scribe --c7
```

## 빠른 참조 📋

### 가장 유용한 Flag
| Flag | 목적 | 사용 시점 |
|---|---|---|
| `--think` | 더 깊은 분석 | 복잡한 문제 |
| `--uc` | 출력 압축 | 대규모 작업 |
| `--safe-mode` | 보수적인 실행 | 중요한 코드 |
| `--c7` | 공식 문서 | Framework 작업 |
| `--seq` | 체계적인 분석 | Debugging |
| `--focus security` | Security 초점 | Security 문제 |
| `--delegate auto` | 병렬 처리 | 대규모 Codebase |
| `--validate` | 실행 전 확인 | 위험한 작업 |

### 잘 작동하는 Flag 조합
```bash
# 안전한 개선
--safe-mode --validate --preview

# 심층 분석
--think --seq --c7

# 대규모 Project
--delegate auto --uc --focus

# 학습
--verbose --c7 --persona-mentor

# Security 작업
--persona-security --focus security --validate

# Performance 작업
--persona-performance --focus performance --play
```

### 자동 활성화 트리거
- **--think**: 복잡한 Import, 모듈 간 호출
- **--uc**: Context >75%, 대규모 작업
- **--safe-mode**: 리소스 사용량 >85%, Production
- **--delegate**: 7개 이상의 디렉토리 또는 50개 이상의 파일
- **--c7**: Framework Import, 문서화 요청
- **--seq**: Debugging 키워드, --think Flag
- **Persona**: 도메인별 키워드 및 패턴

## Flag 문제 해결 🚨

### 일반적인 문제

**"Flag가 작동하지 않는 것 같아요"**
- 철자 확인 (일반적인 오타: `--ultracompresed`, `--persona-fronted`)
- 일부 Flag는 값이 필요합니다: `--scope project`, `--focus security`
- Flag 충돌: `--no-mcp`는 `--c7`, `--seq` 등을 덮어씁니다.

**"작업이 너무 느려요"**
- 압축을 위해 `--uc`를 시도해보세요
- 추가 기능을 비활성화하려면 `--no-mcp`를 사용하세요
- 범위 제한: `--scope project` 대신 `--scope file`

**"출력이 너무 많아요"**
- 압축을 위해 `--uc`를 추가하세요
- `--verbose`가 있다면 제거하세요
- 간단한 질문에는 `--answer-only`를 사용하세요

**"충분히 철저하지 않아요"**
- `--think` 또는 `--think-hard`를 추가하세요
- 관련 MCP Server 활성화: `--seq`, `--c7`
- 적절한 Persona 사용: `--persona-analyzer`

**"변경이 너무 위험해요"**
- 중요한 코드에는 항상 `--safe-mode`를 사용하세요
- 먼저 확인하려면 `--validate`를 추가하세요
- 적용하기 전에 변경 사항을 보려면 `--preview`를 사용하세요

### Flag 충돌

**이것들은 다른 것을 덮어씁니다**:
- `--no-mcp`는 모든 MCP Flag (`--c7`, `--seq` 등)를 덮어씁니다.
- `--safe-mode`는 최적화 Flag를 덮어씁니다.
- 마지막 Persona Flag가 이깁니다: `--persona-frontend --persona-backend` → backend

**우선순위**:
1. 안전 Flag (`--safe-mode`)가 최적화보다 우선합니다
2. 명시적 Flag가 자동 활성화보다 우선합니다
3. 사고 깊이: `--ultrathink` > `--think-hard` > `--think`
4. 범위: system > project > module > file

## 효과적인 Flag 사용 팁 💡

### 시작하기 (솔직한 진실)
1. **처음에는 Flag를 무시하세요** - 자동 활성화가 대부분의 경우를 꽤 잘 처리합니다
2. **자동 활성화되는 것을 지켜보세요** - SuperClaude가 선택하는 것을 보면서 배우게 될 것입니다
3. **궁금할 때 `--help`를 사용하세요** - 많은 Command가 사용 가능한 Flag를 보여줍니다
4. **자동화를 신뢰하세요** - SuperClaude는 보통 합리적인 기본값을 선택합니다

### 고급화하기 (원한다면)
1. **덮어쓰기를 실험해보세요** - Security 코드가 아닌 곳에 `--persona-security`를 시도하여 다른 관점을 얻어보세요
2. **유용한 조합을 배우세요** - 중요한 것에는 `--safe-mode --validate`
3. **Performance 트레이드오프를 이해하세요** - 빠른 (`--uc --no-mcp`) vs 철저한 (`--think-hard --all-mcp`)
4. **학습을 위해 Flag를 사용하세요** - 무슨 일이 일어나고 있는지 이해하고 싶을 때 `--verbose`

### Performance 팁 (파워 유저용)
- **속도를 위해**: `--uc --no-mcp --scope file`
- **철저함을 위해**: `--think-hard --all-mcp --delegate auto`
- **안전성을 위해**: `--safe-mode --validate --preview`
- **학습을 위해**: `--verbose --c7 --persona-mentor`

---

## 최종 참고 사항 📝

**Flag에 대한 진짜 진실** 💯:
- **자동 활성화는 수동 Flag 선택보다 보통 꽤 잘 작동합니다**
- **이 가이드의 대부분을 무시하고** 기본 Command만 사용해도 됩니다
- **Flag는 당신이 원할 때를 위해 있습니다** - 당신이 필요하기 때문이 아닙니다
- **학습은 가이드를 공부하는 것이 아니라** 사용을 통해 자연스럽게 일어납니다 😊

**압도당하지 마세요** 🧘‍♂️:
- SuperClaude는 Flag 지식 없이도 잘 작동하도록 노력합니다
- 위의 상세 정보는 필요성이 아니라 호기심을 위한 것입니다
- 자동 활성화는 사용 패턴에 따라 계속해서 더 똑똑해집니다
- Flag를 외우지 않는다고 해서 놓치는 것은 없습니다

**실제로 Flag가 필요할 때**:
- 자동 활성화 덮어쓰기 (드묾)
- 다른 접근 방식 실험 (재미)
- 특정 Performance 요구에 맞게 최적화 (고급)
- 무슨 일이 일어났는지 학습 (교육적)

**간단하게 시작하고, 간단하게 유지하세요** 🎯:
- 기본 Command 사용: `/analyze`, `/build`, `/improve`
- 복잡성은 자동 활성화에 맡기세요
- 실험하고 싶을 때만 수동 Flag를 추가하세요
- SuperClaude가 무엇을 하고 있는지 신뢰하세요

---

*기억하세요: 이 모든 명백한 복잡성 뒤에는, SuperClaude는 실제로 사용하기 간단합니다. 그냥 Command를 입력하기 시작하세요! 🚀*
