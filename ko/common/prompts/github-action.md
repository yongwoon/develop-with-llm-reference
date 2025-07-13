# Prompt - github action

- Lint, basic set up

```
CI 를설정하고 싶다. github actions 을 이용할탠데, pull request 할 때, ruff, mypy 를 실행시킬 수 있게 했으면 좋겠다.
CI 작성시 아래와 같은 조건을 만족해야한다.

- parallel 처리를 해서 실행 속도를 빠르게 하기위해 개선해줘
- 실행 속도가 빠르도록 cache 를 적극적으로 이용한다.
- CI 가 실행 중에, 새로은 commit 이 push 되면 기존의 CI 실행을 멈추고, 새롭게 push 된 commit 에 대한 CI 를 싱행시킨다.
- dependabot.yml 을 추가해줘
- CI 실행조건
    1. /**/*.md 만 갱신되면 backend, frontend CI 는 실행 안하기
    2. backend 폴더만 갱신되면, Frontend CI 는 SKIP (backend 폴더안의 markdown file 만 갱신될경우에도 SKIP)
    3. frontend 폴더만 갱신되면, backend CI 는 SKIP (frontend 폴더안의 markdown file 만 갱신될경우에도 SKIP)
```

- CI 개선

```
 CI 설정에 개선할 점이 있는지 검토해줘
```
