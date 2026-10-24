# VisionCoder

**One API key for every frontier model.** OpenAI, Anthropic, and Gemini compatible — keep your SDKs and tools, just change the Base URL.

[Website](https://visioncoder.ai) · [Docs](https://docs.visioncoder.ai) · [Models](https://visioncoder.ai/models) · [Pricing](https://visioncoder.ai/pricing)

## Quick start

Create an API key at [visioncoder.ai/me/keys](https://visioncoder.ai/me/keys), then point your client at:

| Protocol | Base URL |
| --- | --- |
| OpenAI | `https://visioncoder.ai/v1` |
| Anthropic | `https://visioncoder.ai` |
| Gemini | `https://visioncoder.ai/v1beta` |

```bash
curl https://visioncoder.ai/v1/chat/completions \
  -H "Authorization: Bearer $VISIONCODER_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"gpt-5.5","messages":[{"role":"user","content":"Hello"}]}'
```

## Claude Code & Codex CLI in one command

```bash
curl -fsSL https://visioncoder.ai/install.sh | bash   # install
curl -fsSL https://visioncoder.ai/config.sh | bash    # set your API key
```

Windows: see the [install guide](https://docs.visioncoder.ai/install/).

## Works with

[Claude Code](https://docs.visioncoder.ai/ai-tools/claude-code/) · [Codex CLI](https://docs.visioncoder.ai/ai-tools/codex/) · [Gemini CLI](https://docs.visioncoder.ai/ai-tools/gemini/) · [Cursor](https://docs.visioncoder.ai/ai-tools/cursor/) · [Cline](https://docs.visioncoder.ai/ai-tools/cline/) · [Roo Code](https://docs.visioncoder.ai/ai-tools/roo-code/) · [Kilo Code](https://docs.visioncoder.ai/ai-tools/kilo-code/) · [Aider](https://docs.visioncoder.ai/ai-tools/aider/) · [OpenCode](https://docs.visioncoder.ai/ai-tools/opencode/) · [Zed](https://docs.visioncoder.ai/ai-tools/zed/) · [Continue](https://docs.visioncoder.ai/ai-tools/continue/) · [CC Switch](https://docs.visioncoder.ai/ai-tools/cc-switch/) · [OpenClaw](https://docs.visioncoder.ai/ai-tools/openclaw/) · [Hermes](https://docs.visioncoder.ai/ai-tools/hermes/)

Any tool that accepts a custom Base URL and API key works. [API reference →](https://docs.visioncoder.ai/api-reference/introduction/)

---

<sub>Users in mainland China: [visioncoder.cn](https://visioncoder.cn) · Keywords: LLM API gateway · OpenAI compatible API · Anthropic API · Gemini API · Claude Code · Codex CLI · Cursor · AI coding tools</sub>
