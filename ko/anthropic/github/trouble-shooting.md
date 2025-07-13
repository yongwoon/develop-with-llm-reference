# Trouble shooting

[github action failed(claude code)](./imgs/claude-code-failed.png)

```txt
Error: Failed to setup GitHub token: Error: Claude Code is not installed on this repository. Please install the Claude Code GitHub App at https://github.com/apps/claude.
If you instead wish to use this action with a custom GitHub token or custom GitHub app, provide a `github_token` in the `uses` section of the app in your workflow yml file.
Attempt 3 failed: Claude Code is not installed on this repository. Please install the Claude Code GitHub App at https://github.com/apps/claude
Operation failed after 3 attempts
Error: Process completed with exit code 1.
Run curl -L \
```

오류 메시지가 명확하게 문제를 알려주고 있네요. **Claude Code GitHub App**이 저장소에 설치되지 않아서 발생하는 문제입니다.

## **해결방법 1: Claude Code GitHub App 설치**

### **1단계: GitHub App 설치**

1. https://github.com/apps/claude 로 이동
2. **"Install"** 또는 **"Configure"** 버튼 클릭
3. 설치할 계정/조직 선택
4. 저장소 접근 권한 설정:
   - **All repositories** 또는
   - **Selected repositories** (해당 저장소 선택)

### **2단계: 권한 확인**

설치 후 다음 권한이 부여되는지 확인:

- Issues (read & write)
- Pull requests (read & write)
- Contents (read)
- Metadata (read)

## **해결방법 2: Custom GitHub Token 사용**

GitHub App 설치 없이 Personal Access Token을 사용하는 방법입니다.

### **1단계: GitHub Token 생성**

1. GitHub **Settings** > **Developer settings** > **Personal access tokens** > **Tokens (classic)**
2. **"Generate new token (classic)"** 클릭
3. 필요한 스코프 선택:
   - `repo` (private 저장소의 경우)
   - `public_repo` (public 저장소의 경우)
   - `issues`
   - `pull_requests`

### **2단계: 워크플로우 파일 수정**

```yaml
- name: Run Claude Code
  id: claude
  uses: anthropics/claude-code-action@beta
  with:
    anthropic_api_key: ${{ secrets.ANTHROPIC_API_KEY }}
    github_token: ${{ secrets.GITHUB_TOKEN }} # 추가
```

또는 custom token 사용:

```yaml
- name: Run Claude Code
  id: claude
  uses: anthropics/claude-code-action@beta
  with:
    anthropic_api_key: ${{ secrets.ANTHROPIC_API_KEY }}
    github_token: ${{ secrets.CLAUDE_GITHUB_TOKEN }} # custom token
```

### **3단계: Secret 등록**

저장소 **Settings** > **Secrets and variables** > **Actions**에서:

- `CLAUDE_GITHUB_TOKEN`: 생성한 Personal Access Token

## **해결방법 3: 직접 API 호출 (권장)**

GitHub App 의존성을 제거하고 직접 구현하는 방법:

```yaml
name: Claude Code Review

on:
  issue_comment:
    types: [created]
  pull_request_review_comment:
    types: [created]

jobs:
  claude-review:
    if: contains(github.event.comment.body, '@claude')
    runs-on: ubuntu-latest
    permissions:
      contents: read
      issues: write
      pull-requests: write

    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Get PR Files
        id: pr-files
        if: github.event.pull_request
        run: |
          files=$(gh api repos/${{ github.repository }}/pulls/${{ github.event.pull_request.number }}/files --jq '.[].filename' | head -10)
          echo "files<<EOF" >> $GITHUB_OUTPUT
          echo "$files" >> $GITHUB_OUTPUT
          echo "EOF" >> $GITHUB_OUTPUT
        env:
          GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      - name: Call Claude API
        id: claude
        run: |
          response=$(curl -X POST https://api.anthropic.com/v1/messages \
            -H "Content-Type: application/json" \
            -H "x-api-key: ${{ secrets.ANTHROPIC_API_KEY }}" \
            -H "anthropic-version: 2023-06-01" \
            -d '{
              "model": "claude-3-sonnet-20240229",
              "max_tokens": 2000,
              "messages": [
                {
                  "role": "user",
                  "content": "다음 코드를 리뷰해주세요:\n\n${{ github.event.comment.body }}"
                }
              ]
            }' | jq -r '.content[0].text')

          echo "response<<EOF" >> $GITHUB_OUTPUT
          echo "$response" >> $GITHUB_OUTPUT
          echo "EOF" >> $GITHUB_OUTPUT

      - name: Comment on Issue/PR
        uses: actions/github-script@v7
        with:
          script: |
            const response = `${{ steps.claude.outputs.response }}`;

            if (context.eventName === 'issue_comment') {
              await github.rest.issues.createComment({
                owner: context.repo.owner,
                repo: context.repo.repo,
                issue_number: context.issue.number,
                body: `🤖 **Claude Code Review**\n\n${response}`
              });
            }
```

## **권장사항**

**가장 간단한 해결책**: https://github.com/apps/claude 에서 GitHub App을 설치하는 것이 가장 쉽고 안정적입니다.

**장기적 해결책**: 해결방법 3처럼 직접 API를 호출하면 외부 의존성 없이 더 안정적으로 작동합니다.

어떤 방법을 선택하시겠나요?
