# 풀스택 개발자를 위한 MCP 서버 추천 가이드

## 🚀 풀스택 개발자를 위한 추천 우선순위

### 1단계 (필수 설치)

1. **GitHub MCP Server** - 코드 관리의 핵심
2. **Filesystem MCP Server** - 파일 시스템 조작
3. **Git MCP Server** - 버전 관리
4. **PostgreSQL MCP Server** - 데이터베이스 관리
5. **Fetch MCP Server** - API 개발과 테스트
6. **Playwright MCP Server** - 모던 웹 테스트 자동화

### 2단계 (고급 개발)

7. **Supabase MCP Server** - 모던 백엔드 서비스
8. **Brave Search MCP Server** - 기술 리서치
9. **Memory MCP Server** - 프로젝트 상태 관리
10. **Docker MCP Server** - 컨테이너 관리
11. **Kubernetes MCP Server** - 클러스터 관리
12. **Context7 MCP Server** - 고급 컨텍스트 관리
13. **Task-Master-AI MCP Server** - AI 기반 작업 관리

### 3단계 (특화 기능)

14. **Figma Context MCP Server** - 디자인 연동
15. **Terraform MCP Server** - 인프라 관리
16. **Slack MCP Server** - 팀 협업
17. **Pandoc MCP Server** - 문서 자동화
18. **Tavily MCP Server** - AI 검색
19. **Sequential-Thinking MCP Server** - 논리적 문제 해결

---

## 🚀 필수 MCP 서버 (우선순위 높음)

### 1. GitHub MCP Server

- **용도**: Git 저장소 관리, 이슈 트래킹, PR 관리
- **설치**: `npx -y @modelcontextprotocol/server-github`
- **환경변수**: `GITHUB_TOKEN`
- **추천 이유**: 20년 경험의 풀스택 개발자에게 필수적인 버전 관리 도구

### 2. Filesystem MCP Server

- **용도**: 로컬 파일 시스템 조작, 파일 검색, 메타데이터 분석
- **설치**: `npx -y @mcp/filesystem` 또는 `npx -y @modelcontextprotocol/server-filesystem`
- **추천 이유**: 모든 개발 작업의 기초가 되는 파일 관리

### 3. Git MCP Server

- **용도**: Git 명령어 실행, 브랜치 관리, 커밋 히스토리 조회
- **설치**: `npx -y @modelcontextprotocol/server-git`
- **추천 이유**: 버전 관리와 협업을 위한 핵심 도구

## 🗄️ 데이터베이스 연동 (풀스택 개발 필수)

### 4. PostgreSQL MCP Server

- **용도**: 데이터베이스 쿼리, 스키마 관리, 데이터 분석
- **설치**: `npx -y @modelcontextprotocol/server-postgres`
- **환경변수**: 데이터베이스 연결 정보
- **추천 이유**: 엔터프라이즈급 데이터베이스 작업

### 5. SQLite MCP Server

- **용도**: 경량 데이터베이스 쿼리 및 관리
- **설치**: `npx -y @modelcontextprotocol/server-sqlite`
- **추천 이유**: 프로토타이핑과 개발 환경에서 유용

### 6. MySQL MCP Server

- **용도**: MySQL 데이터베이스 작업
- **설치**: `npx -y mcp-server-mysql`
- **추천 이유**: 레거시 시스템 연동 시 필요

## 🌐 웹 개발 특화 MCP 서버

### 7. Fetch MCP Server

- **용도**: HTTP 요청, REST API 테스트 및 디버깅
- **설치**: `npx -y @modelcontextprotocol/server-fetch`
- **추천 이유**: API 개발과 테스트에 필수

### 8. Puppeteer/Playwright MCP Server

- **용도**: 웹 스크래핑, E2E 테스트, 브라우저 자동화
- **설치**: `npx -y @modelcontextprotocol/server-puppeteer` 또는 `npx -y mcp-server-playwright`
- **추천 이유**: 웹 애플리케이션 테스트 자동화

### 9. Firecrawl MCP Server

- **용도**: 웹 스크래핑, 경쟁사 리서치, 데이터 추출
- **설치**: `npx -y @firecrawl/mcp-server`
- **환경변수**: `FIRECRAWL_API_KEY`
- **추천 이유**: 고급 웹 스크래핑 기능

### 10. Browserbase MCP Server

- **용도**: 브라우저 자동화, 웹 애플리케이션 테스트, 스크린샷 캡처
- **환경변수**: `BROWSERBASE_API_KEY`, `BROWSERBASE_PROJECT_ID`
- **추천 이유**: 클라우드 기반 브라우저 자동화

## 🎨 디자인 & 협업 도구

### 11. Figma Context MCP Server

- **용도**: Figma 디자인 통합, 디자인 사양 확인, 컴포넌트 관계 파악
- **설치**: `npx -y figma-context-mcp`
- **환경변수**: `FIGMA_ACCESS_TOKEN`
- **추천 이유**: 디자인과 개발 간의 원활한 연결

### 12. Slack MCP Server

- **용도**: Slack 워크스페이스 연동, 팀 협업
- **설치**: `npx -y mcp-server-slack`
- **추천 이유**: 팀 커뮤니케이션 자동화

## 📊 데이터 처리 & 문서화

### 13. Excel MCP Server

- **용도**: Excel 스프레드시트 처리, 데이터 분석, 리포트 생성
- **설치**: `npx -y excel-mcp-server`
- **추천 이유**: 비즈니스 데이터 처리

### 14. Pandoc MCP Server

- **용도**: 문서 포맷 변환 (마크다운, PDF, HTML, DOCX)
- **설치**: `npx -y mcp-pandoc`
- **전제조건**: Pandoc 시스템 설치 필요
- **추천 이유**: 문서 자동화

### 15. Google Drive MCP Server

- **용도**: 클라우드 스토리지 통합, 팀 협업, 문서 관리
- **설치**: `npx -y @mcp/gdrive`
- **환경변수**: Google OAuth 인증 정보
- **추천 이유**: 클라우드 기반 문서 관리

### 16. Pandas MCP Server

- **용도**: 데이터 분석 및 처리
- **설치**: `npx -y mcp-server-pandas`
- **추천 이유**: 데이터 과학 작업

## 🔍 리서치 & 검색

### 17. Brave Search MCP Server

- **용도**: 프라이버시 중심 웹 검색, 기술 리서치
- **설치**: `npx -y @mcp/brave-search`
- **환경변수**: `BRAVE_API_KEY`
- **추천 이유**: 실시간 기술 문서 검색

### 18. Tavily MCP Server

- **용도**: AI 기반 검색, 맥락적 검색 결과
- **설치**: `npx -y mcp-server-tavily`
- **환경변수**: `TAVILY_API_KEY`
- **추천 이유**: 고급 AI 검색 기능

## 🏗️ 인프라 & DevOps (Infrastructure as Code)

### 19. AWS Terraform MCP Server (공식)

- **용도**: AWS 베스트 프랙티스, IaC 패턴, Checkov 보안 컴플라이언스
- **제공**: AWS Labs 공식 지원
- **기능**: CDK, Terraform 등 AWS 워크플로우 자동화
- **저장소**: awslabs/mcp

### 20. HashiCorp Terraform MCP Server (공식)

- **용도**: Terraform Registry API 통합, IaC 개발 자동화
- **기능**: Terraform 레지스트리 데이터를 활용한 설정 작성 지원
- **저장소**: hashicorp/terraform-mcp-server

### 21. Terraform Cloud MCP Server

- **용도**: Terraform Cloud API 통합, 워크스페이스 및 실행 관리
- **기능**: 자연어로 인프라 관리, 계획 및 적용
- **저장소**: severity1/terraform-cloud-mcp

### 22. Kubernetes MCP Server

- **용도**: Kubernetes 클러스터 연결 및 관리
- **기능**: kubeconfig 자동 감지, 모든 K8s/OpenShift 리소스 관리
- **저장소**: Flux159/mcp-server-kubernetes 또는 manusa/kubernetes-mcp-server

### 23. Docker MCP Server

- **용도**: Docker 컨테이너 및 Compose 스택 관리
- **기능**: Claude AI를 통한 컨테이너 작업 자동화
- **저장소**: QuantGeekDev/docker-mcp 또는 ckreiling/mcp-server-docker

## 🛠️ 추가 개발 도구

### 24. Memory MCP Server

- **용도**: 세션 간 컨텍스트 유지, 프로젝트 상태 저장, 메모리 상태 모니터링
- **추천 이유**: 장기 프로젝트 관리에 유용

### 25. Time MCP Server

- **용도**: 시간 관련 작업 및 스케줄링
- **추천 이유**: 작업 스케줄링과 시간 관리

### 26. Magic MCP Server

- **용도**: AI 기반 이미지 생성, 텍스트 변환, 코드 생성
- **설치**: `npx -y @21st/magic-mcp`
- **환경변수**: `OPENAI_API_KEY`
- **추천 이유**: AI 기반 콘텐츠 생성

### 27. Mindmap MCP Server

- **용도**: 아이디어 시각화, 프로젝트 아키텍처 계획
- **설치**: `npx -y mindmap-mcp-server`
- **추천 이유**: 프로젝트 설계와 아이디어 정리

### 28. Context7 MCP Server

- **용도**: 고급 컨텍스트 관리, 프로젝트 상태 추적
- **추천 이유**: 복잡한 프로젝트의 컨텍스트 유지

### 29. Sequential-Thinking MCP Server

- **용도**: 순차적 사고 프로세스, 논리적 문제 해결
- **추천 이유**: 복잡한 개발 문제의 체계적 접근

### 30. Playwright MCP Server

- **용도**: 웹 스크래핑, E2E 테스트, 브라우저 자동화
- **설치**: `npx -y mcp-server-playwright`
- **추천 이유**: 모던 웹 테스트 자동화 (Puppeteer의 진화형)

### 31. Task-Master-AI MCP Server

- **용도**: AI 기반 작업 관리, 프로젝트 계획 자동화
- **추천 이유**: 개발 작업의 지능적 관리

### 32. Supabase MCP Server

- **용도**: Supabase 백엔드 서비스 연동, 실시간 데이터베이스 관리
- **추천 이유**: 모던 백엔드 서비스 통합

## 📊 MCP 서버 전체 목록 (표 형태)

| 순위 | MCP Server 이름                | 용도                                  | 전제 조건            | 추천 이유             | 설치 방법                                       | 주요 기능                                 | 환경 설정             | 카테고리     |
| ---- | ------------------------------ | ------------------------------------- | -------------------- | --------------------- | ----------------------------------------------- | ----------------------------------------- | --------------------- | ------------ |
| 1    | GitHub MCP Server              | Git 저장소 관리, 이슈 트래킹, PR 관리 | GitHub 계정          | 버전 관리 필수 도구   | `npx -y @modelcontextprotocol/server-github`    | 이슈 관리, PR 생성/리뷰, 레포지토리 관리  | `GITHUB_TOKEN`        | 필수         |
| 2    | Filesystem MCP Server          | 로컬 파일 시스템 조작, 파일 검색      | 없음                 | 모든 개발 작업의 기초 | `npx -y @mcp/filesystem`                        | 파일 CRUD, 디렉토리 탐색, 메타데이터 분석 | 프로젝트 경로 설정    | 필수         |
| 3    | Git MCP Server                 | Git 명령어 실행, 브랜치 관리          | Git 설치             | 버전 관리 핵심        | `npx -y @modelcontextprotocol/server-git`       | 커밋, 브랜치, 머지, 히스토리 조회         | 레포지토리 경로       | 필수         |
| 4    | PostgreSQL MCP Server          | 데이터베이스 쿼리, 스키마 관리        | PostgreSQL 설치      | 엔터프라이즈급 DB     | `npx -y @modelcontextprotocol/server-postgres`  | 쿼리 실행, 스키마 관리, 데이터 분석       | DB 연결 정보          | 필수         |
| 5    | Fetch MCP Server               | HTTP 요청, REST API 테스트            | 없음                 | API 개발 필수         | `npx -y @modelcontextprotocol/server-fetch`     | HTTP 요청, 응답 처리, API 테스트          | 없음                  | 필수         |
| 6    | Playwright MCP Server          | 웹 테스트, 브라우저 자동화            | Playwright 설치      | 모던 웹 테스트 도구   | `npx -y mcp-server-playwright`                  | E2E 테스트, 스크래핑, 스크린샷            | 브라우저 설정         | 필수         |
| 7    | Supabase MCP Server            | Supabase 백엔드 서비스 연동           | Supabase 프로젝트    | 모던 백엔드 서비스    | 설치 방법 확인 필요                             | 실시간 DB, 인증, 스토리지 관리            | Supabase API 키       | 고급         |
| 8    | Brave Search MCP Server        | 프라이버시 중심 웹 검색               | Brave API 키         | 기술 리서치 필수      | `npx -y @mcp/brave-search`                      | 웹 검색, 기술 문서 검색                   | `BRAVE_API_KEY`       | 고급         |
| 9    | Memory MCP Server              | 세션 간 컨텍스트 유지                 | 없음                 | 장기 프로젝트 관리    | 설치 방법 확인 필요                             | 상태 저장, 컨텍스트 관리                  | 없음                  | 고급         |
| 10   | Docker MCP Server              | 컨테이너 관리                         | Docker 설치          | 컨테이너 기반 개발    | `npx -y mcp-server-docker`                      | 컨테이너 CRUD, Compose 관리               | Docker 소켓 접근      | 고급         |
| 11   | Kubernetes MCP Server          | 클러스터 관리                         | kubectl 설치         | 클러스터 관리         | `npx -y mcp-server-kubernetes`                  | 리소스 관리, 배포, 모니터링               | kubeconfig            | 고급         |
| 12   | Context7 MCP Server            | 고급 컨텍스트 관리                    | 없음                 | 복잡한 프로젝트 관리  | 설치 방법 확인 필요                             | 컨텍스트 추적, 상태 관리                  | 없음                  | 고급         |
| 13   | Task-Master-AI MCP Server      | AI 기반 작업 관리                     | OpenAI API 키        | 지능적 작업 관리      | 설치 방법 확인 필요                             | 작업 계획, 우선순위 관리                  | AI API 키             | 고급         |
| 14   | Figma Context MCP Server       | Figma 디자인 통합                     | Figma 계정           | 디자인-개발 연결      | `npx -y figma-context-mcp`                      | 디자인 사양, 컴포넌트 분석                | `FIGMA_ACCESS_TOKEN`  | 특화         |
| 15   | AWS Terraform MCP Server       | AWS 인프라 관리                       | AWS 계정, Terraform  | 클라우드 인프라       | awslabs/mcp 저장소                              | IaC, 보안 컴플라이언스                    | AWS 자격증명          | 특화         |
| 16   | Slack MCP Server               | 팀 협업 도구                          | Slack 워크스페이스   | 팀 커뮤니케이션       | `npx -y mcp-server-slack`                       | 메시지 전송, 채널 관리                    | Slack API 토큰        | 특화         |
| 17   | Pandoc MCP Server              | 문서 포맷 변환                        | Pandoc 설치          | 문서 자동화           | `npx -y mcp-pandoc`                             | 마크다운, PDF, HTML 변환                  | 없음                  | 특화         |
| 18   | Tavily MCP Server              | AI 기반 검색                          | Tavily API 키        | 고급 검색 기능        | `npx -y mcp-server-tavily`                      | 맥락적 검색, AI 분석                      | `TAVILY_API_KEY`      | 특화         |
| 19   | Sequential-Thinking MCP Server | 순차적 사고 프로세스                  | 없음                 | 논리적 문제 해결      | 설치 방법 확인 필요                             | 단계별 분석, 논리적 추론                  | 없음                  | 특화         |
| 20   | SQLite MCP Server              | 경량 데이터베이스 관리                | SQLite               | 프로토타이핑          | `npx -y @modelcontextprotocol/server-sqlite`    | 쿼리 실행, 스키마 관리                    | DB 파일 경로          | 데이터베이스 |
| 21   | MySQL MCP Server               | MySQL 데이터베이스 작업               | MySQL 설치           | 레거시 시스템 연동    | `npx -y mcp-server-mysql`                       | 쿼리 실행, 데이터 관리                    | MySQL 연결 정보       | 데이터베이스 |
| 22   | Firecrawl MCP Server           | 웹 스크래핑                           | Firecrawl API 키     | 고급 스크래핑         | `npx -y @firecrawl/mcp-server`                  | 웹 데이터 추출, 경쟁사 분석               | `FIRECRAWL_API_KEY`   | 웹개발       |
| 23   | Browserbase MCP Server         | 브라우저 자동화                       | Browserbase 계정     | 클라우드 브라우저     | API 키 필요                                     | 스크린샷, 웹 테스트                       | `BROWSERBASE_API_KEY` | 웹개발       |
| 24   | Excel MCP Server               | 스프레드시트 처리                     | 없음                 | 비즈니스 데이터 처리  | `npx -y excel-mcp-server`                       | Excel 파일 처리, 데이터 분석              | 없음                  | 데이터처리   |
| 25   | Google Drive MCP Server        | 클라우드 스토리지 통합                | Google 계정          | 클라우드 문서 관리    | `npx -y @mcp/gdrive`                            | 파일 업로드/다운로드, 공유                | Google OAuth          | 협업         |
| 26   | Pandas MCP Server              | 데이터 분석                           | Python, Pandas       | 데이터 과학 작업      | `npx -y mcp-server-pandas`                      | 데이터 분석, 시각화                       | Python 환경           | 데이터처리   |
| 27   | Time MCP Server                | 시간 관련 작업                        | 없음                 | 작업 스케줄링         | 설치 방법 확인 필요                             | 스케줄링, 시간 관리                       | 없음                  | 유틸리티     |
| 28   | Magic MCP Server               | AI 기반 콘텐츠 생성                   | OpenAI API 키        | AI 콘텐츠 생성        | `npx -y @21st/magic-mcp`                        | 이미지 생성, 텍스트 변환                  | `OPENAI_API_KEY`      | AI도구       |
| 29   | Mindmap MCP Server             | 아이디어 시각화                       | 없음                 | 프로젝트 설계         | `npx -y mindmap-mcp-server`                     | 마인드맵 생성, 아키텍처 계획              | 없음                  | 시각화       |
| 30   | HashiCorp Terraform MCP Server | Terraform 통합                        | Terraform 설치       | IaC 개발              | hashicorp/terraform-mcp-server                  | Terraform 레지스트리 연동                 | Terraform 설정        | 인프라       |
| 31   | Terraform Cloud MCP Server     | Terraform Cloud 연동                  | Terraform Cloud 계정 | 클라우드 인프라 관리  | severity1/terraform-cloud-mcp                   | 워크스페이스 관리, 계획 실행              | Terraform Cloud API   | 인프라       |
| 32   | Puppeteer MCP Server           | 브라우저 자동화                       | Puppeteer 설치       | 웹 스크래핑           | `npx -y @modelcontextprotocol/server-puppeteer` | 스크래핑, 테스트 자동화                   | 브라우저 설정         | 웹개발       |

## 📝 설치 및 설정 예시

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/path/to/your/project"
      ]
    },
    "git": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-git",
        "--repository",
        "/path/to/repo"
      ]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_TOKEN": "your-github-token"
      }
    },
    "postgres": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-postgres"],
      "env": {
        "POSTGRES_CONNECTION_STRING": "postgresql://user:password@localhost:5432/database"
      }
    },
    "fetch": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-fetch"]
    }
  }
}
```

## 📚 추가 리소스

- **Anthropic MCP 공식 문서**: https://docs.anthropic.com
- **Claude Code 지원**: https://support.anthropic.com
- **커뮤니티 MCP 서버**: GitHub에서 "mcp-server" 검색

20년 경험의 풀스택 개발자라면 위의 MCP 서버들을 단계별로 도입하여 Claude Code와 함께 생산성을 극대화할 수 있습니다. 특히 1단계 필수 서버들부터 시작하여 프로젝트 요구사항에 맞춰 확장해나가시기 바랍니다.
