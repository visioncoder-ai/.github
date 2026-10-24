# VisionCoder

**One API key for OpenAI, Anthropic, and Gemini protocols. An LLM gateway for developers — one balance for every model, just change the Base URL.**

一个 API Key 同时兼容 OpenAI、Anthropic、Gemini 三套协议，背后接入多家模型厂商，所有模型共用同一份额度。已有的 SDK 和工具只改 Base URL 和 Key，不用改代码。

[官网](https://visioncoder.cn) · [文档](https://docs.visioncoder.cn) · [模型列表](https://visioncoder.cn/models) · [套餐价格](https://visioncoder.cn/pricing) · [计费规则](https://visioncoder.cn/billing)

---

## 服务地址

| 协议 | Base URL | 适用 |
| --- | --- | --- |
| OpenAI | `https://visioncoder.cn/v1` | OpenAI SDK、Codex CLI、Cursor、Cline |
| Anthropic | `https://visioncoder.cn` | Anthropic SDK、Claude Code |
| Gemini | `https://visioncoder.cn/v1beta` | Gemini CLI、Google 官方 SDK |

> OpenAI 协议的 Base URL 要带 `/v1`，Anthropic 协议的不带（客户端会自己拼 `/v1/messages`），填错会得到 404。

## 快速开始

1. 获得额度：[购买套餐](https://visioncoder.cn/pricing)或[兑换码](https://visioncoder.cn/me/redeem)
2. 在 [API Key 管理](https://visioncoder.cn/me/keys)创建 Key（只完整显示一次，创建后立即保存）
3. 发出第一个请求：

```bash
curl https://visioncoder.cn/v1/chat/completions \
  -H "Authorization: Bearer $VISIONCODER_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"gpt-5.5","messages":[{"role":"user","content":"Hello"}]}'
```

可用模型因 Key 而异，用 [`GET /v1/models`](https://docs.visioncoder.cn/api-reference/endpoint/models/) 查询，不要把模型 ID 写死。

## 一键安装 Claude Code 和 Codex CLI

macOS / Linux / WSL：

```bash
curl -fsSL https://visioncoder.cn/install.sh | bash   # 安装
curl -fsSL https://visioncoder.cn/config.sh | bash    # 写入 API Key
```

Windows 用 [install.bat](https://visioncoder.cn/install.bat) 和 [config.bat](https://visioncoder.cn/config.bat)，完整步骤见[一键安装](https://docs.visioncoder.cn/install/)。

## 工具接入

只要工具支持自定义 Base URL 和 API Key 就能接入，以下 14 个工具有逐步配置说明：

| 类型 | 工具 |
| --- | --- |
| CLI | [Claude Code](https://docs.visioncoder.cn/ai-tools/claude-code/) · [Codex CLI](https://docs.visioncoder.cn/ai-tools/codex/) · [Gemini CLI](https://docs.visioncoder.cn/ai-tools/gemini/) · [Aider](https://docs.visioncoder.cn/ai-tools/aider/) · [CC Switch](https://docs.visioncoder.cn/ai-tools/cc-switch/) · [OpenClaw](https://docs.visioncoder.cn/ai-tools/openclaw/) · [Hermes](https://docs.visioncoder.cn/ai-tools/hermes/) |
| 编辑器与插件 | [Cursor](https://docs.visioncoder.cn/ai-tools/cursor/) · [Cline](https://docs.visioncoder.cn/ai-tools/cline/) · [Roo Code](https://docs.visioncoder.cn/ai-tools/roo-code/) · [Kilo Code](https://docs.visioncoder.cn/ai-tools/kilo-code/) · [OpenCode](https://docs.visioncoder.cn/ai-tools/opencode/) · [Zed](https://docs.visioncoder.cn/ai-tools/zed/) · [Continue](https://docs.visioncoder.cn/ai-tools/continue/) |

DeepSeek、GLM、Qwen、Kimi、MiniMax 也支持 Anthropic 协议，可以直接在 Claude Code 里用，见[国产模型](https://docs.visioncoder.cn/domestic-models/)。

## 计费

- 按输入、输出、缓存命中、缓存写入分项计价，失败请求不收费，详见[计费规则](https://visioncoder.cn/billing)
- 额度以积分显示，来自订阅套餐、加油包或兑换码，见[套餐价格](https://visioncoder.cn/pricing)
- 每个模型的价格见[模型列表](https://visioncoder.cn/models)

## 更多文档

- [API 文档](https://docs.visioncoder.cn/api-reference/introduction/) —— 鉴权、端点、[错误处理](https://docs.visioncoder.cn/api-reference/errors/)
- [使用手册](https://docs.visioncoder.cn/manual/personal/) —— 开通、套餐、Key、用量
- 遇到问题联系客服时，请带上响应头里的 `X-Request-Id`

---

<sub>Keywords: LLM API gateway · OpenAI compatible API · Anthropic API · Claude Code · Codex CLI · Gemini CLI · Cursor · DeepSeek · AI coding tools · 多模型 API 网关</sub>
