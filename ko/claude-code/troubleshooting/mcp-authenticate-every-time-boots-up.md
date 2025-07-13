## Outline

Claude Code를 실행할 때마다 Atlassian MCP, Notion MCP 인증을 요청받는 문제

## Cause

`~/.mcp-auth/mcp-remote-xxxx/` 에 오래된 잠금 파일(`xxxxxxxxx_lock.json`)이 남아 있어, 이미 종료된 프로세스의 정보가 포함되어 있었기 때문에 인증 정보가 영구적으로 저장되지 않았습니다.

## How to fix

먼저, 모든 Claude Code 프로세스를 종료한 후, 아래 명령어를 실행하여 잠금 파일을 삭제합니다.

```bash
rm ~/.mcp-auth/mcp-remote-*/*_lock.json
```
