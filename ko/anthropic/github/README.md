# github review with claude

`.github/workflows/claude.yml` 파일은 GitHub Actions 워크플로우로, **Claude AI가 GitHub 이슈와 PR에서 코드 리뷰를 자동으로 수행**하도록 설정하는 역할을 합니다.

## 주요 기능

### 1. **트리거 조건**

다음 상황에서 Claude가 자동으로 실행됩니다:

- 이슈 코멘트에 `@claude`가 포함된 경우
- PR 리뷰 코멘트에 `@claude`가 포함된 경우
- PR 리뷰 본문에 `@claude`가 포함된 경우
- 이슈 제목이나 본문에 `@claude`가 포함된 경우

### 2. **실행 환경**

- Ubuntu 최신 버전에서 실행
- 필요한 권한: 코드 읽기, PR 읽기, 이슈 읽기, ID 토큰 쓰기

### 3. **Claude Code Action 사용**

```yaml
- name: Run Claude Code
  uses: anthropics/claude-code-action@beta
  with:
    anthropic_api_key: ${{ secrets.ANTHROPIC_API_KEY }}
```

## 사용 방법

### 이슈에서 사용

```
@claude 이 코드를 리뷰해주세요
```

### PR 코멘트에서 사용

```
@claude 이 변경사항이 적절한가요?
```

### PR 리뷰에서 사용

리뷰 본문에 `@claude`를 포함하면 자동으로 코드 분석을 수행합니다.

## 장점

1. **자동화된 코드 리뷰**: 개발자가 `@claude`만 언급하면 자동으로 AI 리뷰
2. **일관된 품질**: 모든 코드 변경사항에 대해 일관된 기준으로 검토
3. **시간 절약**: 수동 리뷰 시간을 줄이고 개발 속도 향상
4. **24/7 가용성**: 언제든지 AI 리뷰 요청 가능

이 워크플로우는 팀의 코드 품질을 향상시키고 리뷰 프로세스를 자동화하는 데 도움이 됩니다.

## GitHub Secrets 등록방법

GitHub Secrets는 **GitHub 저장소 설정**에서 등록할 수 있습니다. 다음 단계를 따라하세요:

### 1. GitHub 저장소 접속

1. GitHub에서 해당 저장소로 이동
2. 저장소 메인 페이지에서 **Settings** 탭 클릭

### 2. Secrets & variables 메뉴 접속

1. 왼쪽 사이드바에서 **Secrets and variables** 클릭
2. **Actions** 선택

### 3. New repository secret 추가

1. **New repository secret** 버튼 클릭
2. 다음 정보 입력:
   - **Name**: `ANTHROPIC_API_KEY`
   - **Value**: Anthropic에서 발급받은 API 키

### 4. API 키 발급 방법 (Anthropic)

1. [Anthropic Console](https://console.anthropic.com/) 접속
2. 로그인 또는 회원가입
3. **API Keys** 섹션에서 **Create Key** 클릭
4. API 키 생성 후 복사

### 5. 보안 주의사항

- ✅ **Secret으로 등록**: API 키는 반드시 GitHub Secrets로 등록
- ❌ **코드에 직접 입력 금지**: `.env` 파일이나 코드에 직접 입력하지 마세요
- 🔒 **권한 관리**: API 키는 안전하게 보관하고 필요시 재발급

### 6. 확인 방법

워크플로우가 실행될 때 `${{ secrets.ANTHROPIC_API_KEY }}`로 안전하게 API 키에 접근할 수 있습니다.

이렇게 설정하면 GitHub Actions에서 Claude API를 안전하게 사용할 수 있습니다!
