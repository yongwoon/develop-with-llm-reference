# SuperClaude 설치 가이드 📦

## 🎯 보기보다 쉽습니다!

**솔직한 진실**: 이 가이드는 모든 세부 사항을 다루고 싶어서 길어 보이지만, 실제 설치는 매우 간단합니다. 대부분의 사람들은 하나의 Command로 2분 안에 끝냅니다!

### 1단계: Package 설치

**옵션 A: PyPI에서 (권장)**
```bash
uv add SuperClaude
```

**옵션 B: Source에서**
```bash
git clone https://github.com/NomenAK/SuperClaude.git
cd SuperClaude
uv sync
```
### 🔧 UV / UVX 설정 가이드

SuperClaude v3는 [`uv`](https://github.com/astral-sh/uv) (더 빠르고 현대적인 Python package manager) 또는 크로스플랫폼 사용을 위한 `uvx`를 통한 설치도 지원합니다.

### 🌀 `uv`로 설치

`uv`가 설치되어 있는지 확인하세요:

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> 또는 [https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)의 지침을 따르세요.

`uv`가 사용 가능하면 다음과 같이 SuperClaude를 설치할 수 있습니다:

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ `uvx`로 설치 (크로스플랫폼 CLI)

`uvx`를 사용하는 경우 다음을 실행하세요:

```bash
uvx pip install SuperClaude
```
## 🔧 UV / UVX 설정 가이드

SuperClaude v3는 [`uv`](https://github.com/astral-sh/uv) (더 빠르고 현대적인 Python package manager) 또는 크로스플랫폼 사용을 위한 `uvx`를 통한 설치도 지원합니다.

### 🌀 `uv`로 설치

`uv`가 설치되어 있는지 확인하세요:

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> 또는 [https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)의 지침을 따르세요.

`uv`가 사용 가능하면 다음과 같이 SuperClaude를 설치할 수 있습니다:

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ `uvx`로 설치 (크로스플랫폼 CLI)

`uvx`를 사용하는 경우 다음을 실행하세요:

```bash
uvx pip install SuperClaude
```

### ✅ 설치 완료

설치 후 일반적인 설치 단계를 계속 진행하세요:

```bash
python3 -m SuperClaude install
```

또는 bash 스타일 CLI 사용:

```bash
SuperClaude install
```

### 🧠 참고:

* `uv`는 더 나은 Caching과 Performance를 제공합니다.
* Python 3.8+와 호환되며 SuperClaude와 원활하게 작동합니다.

---

### ⚠️ 중요 참고
**SuperClaude 설치 후.**
**`SuperClaude commands`, `python3 -m SuperClaude commands` 또는 `python3 SuperClaude commands`를 사용할 수 있습니다.**

**방금 무슨 일이 있었나요?** SuperClaude가 필요한 모든 것을 설정하려고 시도했습니다. 보통 복잡한 Configuration, 종속성 찾기 또는 설정 골칫거리가 없습니다! 🎉

---

SuperClaude v3 설치에 대한 포괄적인 가이드입니다. 하지만 기억하세요 - 대부분의 사람들은 위의 빠른 시작 부분을 읽을 필요가 없습니다! 😊

## 시작하기 전에 🔍

### 필요한 것 💻

SuperClaude는 **Windows**, **macOS**, **Linux**에서 작동합니다. 필요한 것은 다음과 같습니다:

**필수:**
- **Python 3.8 이상** - Framework이 Python으로 작성되었습니다.
- **Claude CLI** - SuperClaude는 Claude Code를 향상시키므로 먼저 설치해야 합니다.

**선택 사항 (권장):**
- **Node.js 16+** - MCP Server 통합을 원하는 경우에만 필요합니다.
- **Git** - 개발 Workflow에 유용합니다.

### 빠른 확인 🔍

설치하기 전에 기본 사항이 있는지 확인해 보겠습니다:

```bash
# Python 버전 확인 (3.8+ 여야 함)
python3 --version

# Claude CLI 설치 여부 확인
claude --version

# Node.js 확인 (선택 사항, MCP Server용)
node --version
```

이 중 하나라도 실패하면 아래의 [사전 요구 사항 설정](#사전-요구-사항-설정-️) 섹션을 참조하세요.

## 빠른 시작 🚀

**🏆 "그냥 작동하게 만들기" 접근 방식 (사용자의 90%에게 권장)**
**옵션 A: PyPI에서 (권장)**
```bash
pip install SuperClaude

# 권장 설정으로 설치
SuperClaude install --quick

# 끝입니다! 🎉
```
**옵션 B: Source에서**
```bash
# repo 복제
git clone <repository-url>
cd SuperClaude
pip install .

# 권장 설정으로 설치
SuperClaude install --quick

# 끝입니다! 🎉
```
**⚠️ 중요 참고**
**SuperClaude 설치 후.**
**`SuperClaude commands`, `python3 -m SuperClaude commands` 또는 `python3 SuperClaude commands`를 사용할 수 있습니다.**

**방금 얻은 것:**
- ✅ 전문가를 자동 활성화하는 16개의 스마트 Command
- ✅ 언제 도와야 할지 아는 11명의 전문가 Persona
- ✅ 복잡성을 파악하는 지능형 Routing
- ✅ 약 2분의 시간과 ~50MB의 디스크 공간

**정말입니다, 끝났습니다.** Claude Code를 열고 `/help`를 입력하여 SuperClaude가 마법을 부리는 것을 지켜보세요.

**무슨 일을 할지 불안하신가요?** 먼저 다음으로 확인하세요:
```bash
SuperClaude install --quick --dry-run
```

## 설치 옵션 🎯

세 가지 설치 프로필 중에서 선택할 수 있습니다:

### 🎯 최소 설치
```bash
SuperClaude install --minimal
```
- **내용**: 핵심 Framework 파일만
- **시간**: ~1분
- **공간**: ~20MB
- **적합 대상**: 테스트, 기본 향상, 최소 설정
- **포함 내용**: Claude를 안내하는 핵심 동작 문서

### 🚀 빠른 설치 (권장)
```bash
SuperClaude install --quick
```
- **내용**: 핵심 Framework + 16개 슬래시 Command
- **시간**: ~2분
- **공간**: ~50MB
- **적합 대상**: 대부분의 사용자, 일반 개발
- **포함 내용**: 최소 설치의 모든 것 + `/analyze`, `/build`, `/improve`와 같은 전문 Command

### 🔧 개발자 설치
```bash
SuperClaude install --profile developer
```
- **내용**: MCP Server 통합을 포함한 모든 것
- **시간**: ~5분
- **공간**: ~100MB
- **적합 대상**: 파워 유저, 기여자, 고급 Workflow
- **포함 내용**: 모든 것 + Context7, Sequential, Magic, Playwright Server

### 🎛️ 대화형 설치
```bash
SuperClaude install
```
- Component를 선택할 수 있습니다.
- 각 Component가 수행하는 작업에 대한 자세한 설명을 보여줍니다.
- 설치되는 항목을 제어하고 싶을 때 좋습니다.

## 단계별 설치 📋

### 사전 요구 사항 설정 🛠️

**Python이 없나요?**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install python3 python3-pip

# macOS
brew install python3

# Windows
# https://python.org/downloads/ 에서 다운로드
# 또는 command prompt 또는 powershell 열기
winget install python
```

**Claude CLI가 없나요?**
- 설치 지침은 https://claude.ai/code 를 방문하세요.
- SuperClaude는 Claude Code를 향상시키므로 먼저 필요합니다.

**Node.js가 없나요? (선택 사항)**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install nodejs npm

# macOS
brew install node

# Windows
# https://nodejs.org/ 에서 다운로드
# 또는 command prompt 또는 powershell 열기
winget install nodejs
```

### SuperClaude 받기 📥

**옵션 1: PyPI에서 (권장)**
```bash
pip install SuperClaude
```

**옵션 2: 최신 릴리스 다운로드**
```bash
# 최신 릴리스 다운로드 및 압축 해제
# (URL을 실제 릴리스 URL로 교체)
curl -L <release-url> -o superclaude-v3.zip
unzip superclaude-v3.zip
cd superclaude-v3
pip install .
```

**옵션 3: Git에서 복제**
```bash
git clone <repository-url>
cd SuperClaude
pip install .
```

### 설치 프로그램 실행 🎬

설치 프로그램은 매우 스마트하며 프로세스를 안내합니다:

```bash
# 사용 가능한 모든 옵션 보기
SuperClaude install --help

# 빠른 설치 (권장)
SuperClaude install --quick

# 먼저 무슨 일이 일어날지 보고 싶으신가요?
SuperClaude install --quick --dry-run

# 모든 것 설치
SuperClaude install --profile developer

# 조용한 설치 (최소 출력)
SuperClaude install --quick --quiet

# 강제 설치 (확인 건너뛰기)
python3 SuperClaude.py install --quick --force
```

### 설치 중 📱

설치 시 발생하는 일은 다음과 같습니다:

1. **System 확인** - 필요한 종속성이 있는지 확인합니다.
2. **Directory 설정** - `~/.claude/` 디렉토리 구조를 생성합니다.
3. **핵심 파일** - Framework 문서 파일을 복사합니다.
4. **Command** - 슬래시 Command 정의를 설치합니다 (선택한 경우).
5. **MCP Server** - MCP Server를 다운로드하고 구성합니다 (선택한 경우).
6. **Configuration** - `settings.json`을 기본 설정으로 설정합니다.
7. **Validation** - 모든 것이 작동하는지 테스트합니다.

설치 프로그램은 진행 상황을 보여주고 문제가 발생하면 알려줍니다.

## 설치 후 ✅

### 빠른 테스트 🧪

모든 것이 작동했는지 확인해 보겠습니다:

```bash
# 파일이 설치되었는지 확인
ls ~/.claude/

# CLAUDE.md, COMMANDS.md, settings.json 등이 표시되어야 합니다.
```

**Claude Code로 테스트:**
1. Claude Code 열기
2. `/help`를 입력해 보세요 - SuperClaude Command가 표시되어야 합니다.
3. `/analyze --help`를 시도해 보세요 - Command 옵션이 표시되어야 합니다.

### 설치된 것 📂

SuperClaude는 기본적으로 `~/.claude/`에 설치됩니다. 찾을 수 있는 내용은 다음과 같습니다:

```
~/.claude/
├── CLAUDE.md              # 주 Framework 진입점
├── COMMANDS.md             # 사용 가능한 슬래시 Command
├── FLAGS.md                # Command Flag 및 옵션
├── PERSONAS.md             # 스마트 Persona 시스템
├── PRINCIPLES.md           # 개발 원칙
├── RULES.md                # 운영 규칙
├── MCP.md                  # MCP Server 통합
├── MODES.md                # 운영 모드
├── ORCHESTRATOR.md         # 지능형 Routing
├── settings.json           # Configuration 파일
└── commands/               # 개별 Command 정의
    ├── analyze.md
    ├── build.md
    ├── improve.md
    └── ... (13개 더)
```

**각 파일의 역할:**
- **CLAUDE.md** - Claude Code에 SuperClaude에 대해 알리고 다른 파일을 로드합니다.
- **settings.json** - Configuration (MCP Server, hook 등)
- **commands/** - 각 슬래시 Command에 대한 자세한 정의

### 첫 단계 🎯

시작하려면 다음 Command를 시도해 보세요:

```bash
# Claude Code에서 다음을 시도해 보세요:
/sc:help                    # 사용 가능한 Command 보기
/sc:analyze README.md       # 파일 분석
/sc:build --help           # 빌드 옵션 보기
/sc:improve --help         # 개선 옵션 보기
```

**너무 부담스럽게 느껴져도 걱정하지 마세요** - SuperClaude는 Claude Code를 점진적으로 향상시킵니다. 원하는 만큼 많이 또는 적게 사용할 수 있습니다.

## 설치 관리 🛠️

### 업데이트 📅

SuperClaude를 최신 상태로 유지하세요:

```bash
# 업데이트 확인
SuperClaude update

# 강제 업데이트 (로컬 변경 사항 덮어쓰기)
SuperClaude update --force

# 특정 Component만 업데이트
SuperClaude update --components core,commands

# 업데이트될 내용 보기
SuperClaude update --dry-run
```

**업데이트 시기:**
- 새로운 SuperClaude 버전이 출시될 때
- 문제가 있는 경우 (업데이트에는 종종 수정 사항이 포함됨)
- 새로운 MCP Server가 사용 가능해질 때

### 백업 💾

주요 변경 전에 백업을 만드세요:

```bash
# 백업 생성
SuperClaude backup --create

# 기존 백업 목록
SuperClaude backup --list

# 백업에서 복원
SuperClaude backup --restore

# 사용자 지정 이름으로 백업 생성
SuperClaude backup --create --name "before-update"
```

**백업 시기:**
- SuperClaude 업데이트 전
- 설정 실험 전
- 제거 전
- 많이 사용자화한 경우 주기적으로

### 제거 🗑️

SuperClaude를 제거해야 하는 경우:

```bash
# SuperClaude 제거 (백업 유지)
SuperClaude uninstall

# 완전 제거 (모든 것 제거)
SuperClaude uninstall --complete

# 제거될 내용 보기
SuperClaude uninstall --dry-run
```

**제거되는 것:**
- `~/.claude/`의 모든 파일
- MCP Server Configuration
- Claude Code의 SuperClaude 설정

**남는 것:**
- 백업 (`--complete`를 사용하지 않는 한)
- Claude Code 자체 (SuperClaude는 건드리지 않음)
- Project 및 기타 파일

## 문제 해결 🔧

### 일반적인 문제 🚨

**"Python not found"**
```bash
# python3 대신 python 시도
python --version

# 또는 설치되었지만 PATH에 없는지 확인
which python3
```

**"Claude CLI not found"**
- 먼저 Claude Code가 설치되어 있는지 확인하세요.
- `claude --version`으로 확인해 보세요.
- 설치 도움말은 https://claude.ai/code 를 방문하세요.

**"Permission denied"**
```bash
# 명시적 Python 경로로 시도
/usr/bin/python3 SuperClaude.py install --quick

# 또는 다른 권한이 필요한지 확인
ls -la ~/.claude/
```

**"MCP servers won't install"**
- Node.js가 설치되어 있는지 확인: `node --version`
- npm이 사용 가능한지 확인: `npm --version`
- 먼저 MCP 없이 설치 시도: `--minimal` 또는 `--quick`

**"Installation fails partway through"**
```bash
# 상세 출력으로 무슨 일이 일어나고 있는지 확인
SuperClaude install --quick --verbose

# 또는 먼저 dry run 시도
SuperClaude install --quick --dry-run
```

### 플랫폼별 문제 🖥️

**Windows:**
- "command not found"가 표시되면 `python3` 대신 `python`을 사용하세요.
- 권한 오류가 발생하면 Command Prompt를 관리자 권한으로 실행하세요.
- Python이 PATH에 있는지 확인하세요.

**macOS:**
- Security & Privacy 설정에서 SuperClaude를 승인해야 할 수 있습니다.
- Python 3.8+가 없는 경우 `brew install python3`를 사용하세요.
- `python` 대신 `python3`를 명시적으로 사용해 보세요.

**Linux:**
- `python3-pip`가 설치되어 있는지 확인하세요.
- 일부 package 설치에는 `sudo`가 필요할 수 있습니다.
- `~/.local/bin`이 PATH에 있는지 확인하세요.

### 아직도 문제가 있나요? 🤔

**문제 해결 리소스를 확인하세요:**
- GitHub Issues: https://github.com/NomenAK/SuperClaude/issues
- 당신과 유사한 기존 문제를 찾아보세요.
- 해결책을 찾을 수 없으면 새 issue를 만드세요.

**버그를 보고할 때 다음을 포함해 주세요:**
- 운영 체제 및 버전
- Python 버전 (`python3 --version`)
- Claude CLI 버전 (`claude --version`)
- 실행한 정확한 Command
- 전체 오류 메시지
- 예상했던 결과

**도움 받기:**
- 일반적인 질문은 GitHub Discussions
- 최신 업데이트는 README.md 확인
- 문제가 알려져 있는지 ROADMAP.md 확인

## 고급 옵션 ⚙️

### 사용자 지정 설치 디렉토리

```bash
# 사용자 지정 위치에 설치
SuperClaude install --quick --install-dir /custom/path

# 환경 변수 사용
export SUPERCLAUDE_DIR=/custom/path
SuperClaude install --quick
```

### Component 선택

```bash
# 사용 가능한 Component 보기
SuperClaude install --list-components

# 특정 Component만 설치
SuperClaude install --components core,commands

# 특정 Component 건너뛰기
SuperClaude install --quick --skip mcp
```

### 개발 설정

SuperClaude에 기여하거나 수정할 계획인 경우:

```bash
# 모든 Component가 포함된 개발자 설치
SuperClaude install --profile developer

# 개발 모드로 설치 (복사 대신 심볼릭 링크)
SuperClaude install --profile developer --dev-mode

# 개발용 git hook과 함께 설치
SuperClaude install --profile developer --dev-hooks
```

## 다음은 무엇인가요? 🚀

**이제 SuperClaude가 설치되었습니다 (쉬웠죠?):**

1. **그냥 사용 시작** - `/analyze some-file.js` 또는 `/build`를 시도하고 무슨 일이 일어나는지 보세요 ✨
2. **학습에 스트레스 받지 마세요** - SuperClaude는 보통 당신에게 필요한 것을 파악합니다.
3. **자유롭게 실험하세요** - `/improve` 및 `/troubleshoot`과 같은 Command는 꽤 관대합니다.
4. **궁금하면 가이드 읽기** - 방금 무슨 일이 일어났는지 이해하고 싶을 때 `Docs/`를 확인하세요.
5. **피드백 제공** - 무엇이 효과가 있고 무엇이 없는지 알려주세요.

**진짜 비밀**: SuperClaude는 새로운 것을 많이 배울 필요 없이 기존 Workflow를 향상시키도록 설계되었습니다. 일반 Claude Code를 사용하듯이 사용하되, 얼마나 더 똑똑해지는지 주목하세요! 🎯

**아직도 불확실한가요?** `/help`와 `/analyze README.md`로 시작해 보세요 - 실제로 얼마나 위협적이지 않은지 알게 될 것입니다.

---

## 최종 참고 사항 📝

- **설치는 선택에 따라 1-5분 소요됩니다.**
- **필요한 디스크 공간: 20-100MB** (많지 않음!)
- **기존 Tool과 함께 작동** - 설정에 방해되지 않습니다.
- **마음이 바뀌면 쉽게 제거할 수 있습니다.**
- **Community 지원** - 우리는 실제로 issue를 읽고 응답합니다.
- ### ⚠️ 중요 참고
**SuperClaude 설치 후.**
**`SuperClaude commands`, `python3 -m SuperClaude commands` 또는 `python3 SuperClaude commands`를 사용할 수 있습니다.**

SuperClaude를 사용해 주셔서 감사합니다! 개발 Workflow가 조금 더 원활해지기를 바랍니다. 🙂

---

*마지막 업데이트: 2024년 7월 - 이 가이드에 잘못되었거나 혼란스러운 내용이 있으면 알려주세요!*
