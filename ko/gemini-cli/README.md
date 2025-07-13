# GETTING START

Gemini CLI를 실행하는 방법을 알려드리겠습니다.

## 설치 방법

**Node.js 환경에서:**

```bash
npm install -g @google/generative-ai-cli
```

**또는 직접 다운로드:**
Google AI Studio에서 API 키를 발급받은 후, 공식 CLI 도구를 다운로드할 수 있습니다.

## 기본 실행 방법

**1. API 키 설정:**

```bash
export GEMINI_API_KEY="your-api-key-here"
```

**2. 기본 실행:**

```bash
gemini "안녕하세요"
```

**3. 파일과 함께 실행:**

```bash
gemini "이 이미지를 설명해주세요" --image image.jpg
```

**4. 대화형 모드:**

```bash
gemini --interactive
```

## 주요 옵션들

- `--model`: 사용할 모델 지정 (gemini-pro, gemini-pro-vision 등)
- `--temperature`: 창의성 수준 조절 (0.0-1.0)
- `--max-tokens`: 최대 토큰 수 제한
- `--image`: 이미지 파일 첨부
- `--file`: 텍스트 파일 첨부

혹시 특정 설치나 사용 과정에서 문제가 있으시면 더 구체적으로 알려주세요!
