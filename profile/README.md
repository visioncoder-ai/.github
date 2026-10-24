# VisionCoder

**One API key for OpenAI, Anthropic, and Gemini protocols. An LLM gateway for developers — one balance for every model, just change the Base URL.**

一个 API Key 同时兼容 OpenAI、Anthropic、Gemini 三套协议，背后接入多家模型厂商，所有模型共用同一份额度。已有的 SDK 和工具只改 Base URL 和 Key，不用改代码。

## 选择版本

海外版和国内版是两个独立站点，账号、套餐、价格、文档各自分开，按你所在地区选一个：

|  | 海外版 Global | 国内版 China |
| --- | --- | --- |
| 官网 | [visioncoder.ai](https://visioncoder.ai) | [visioncoder.cn](https://visioncoder.cn) |
| 文档 | [docs.visioncoder.ai](https://docs.visioncoder.ai) | [docs.visioncoder.cn](https://docs.visioncoder.cn) |
| 模型列表 | [models](https://visioncoder.ai/models) | [models](https://visioncoder.cn/models) |
| 套餐价格 | [pricing](https://visioncoder.ai/pricing) | [pricing](https://visioncoder.cn/pricing) |
| 计费规则 | [billing](https://visioncoder.ai/billing) | [billing](https://visioncoder.cn/billing) |
| API Key | [me/keys](https://visioncoder.ai/me/keys) | [me/keys](https://visioncoder.cn/me/keys) |
| OpenAI Base URL | `https://visioncoder.ai/v1` | `https://visioncoder.cn/v1` |
| Anthropic Base URL | `https://visioncoder.ai` | `https://visioncoder.cn` |
| Gemini Base URL | `https://visioncoder.ai/v1beta` | `https://visioncoder.cn/v1beta` |

> OpenAI 协议的 Base URL 要带 `/v1`，Anthropic 协议的不带（客户端会自己拼 `/v1/messages`），填错会得到 404。

下文示例用海外版地址，国内版把 `visioncoder.ai` 换成 `visioncoder.cn` 即可。

---

## 快速开始

1. 在所选版本的官网购买套餐或使用兑换码获得额度
2. 在 API Key 管理页创建 Key（只完整显示一次，创建后立即保存）
3. 发出第一个请求：

```bash
curl https://visioncoder.ai/v1/chat/completions \
  -H "Authorization: Bearer $VISIONCODER_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model":"gpt-5.5","messages":[{"role":"user","content":"Hello"}]}'
```

可用模型因 Key 而异，用 `GET /v1/models` 查询，不要把模型 ID 写死。

## 一键安装 Claude Code 和 Codex CLI

macOS / Linux / WSL：

```bash
curl -fsSL https://visioncoder.ai/install.sh | bash   # 安装
curl -fsSL https://visioncoder.ai/config.sh | bash    # 写入 API Key
```

Windows 用同域名下的 `install.bat` 和 `config.bat`，完整步骤见文档的「一键安装」：[海外版](https://docs.visioncoder.ai/install/) · [国内版](https://docs.visioncoder.cn/install/)。

## 工具接入

只要工具支持自定义 Base URL 和 API Key 就能接入，以下 14 个工具有逐步配置说明：

| 工具 | 海外版 | 国内版 |
| --- | --- | --- |
| Claude Code | [文档](https://docs.visioncoder.ai/ai-tools/claude-code/) | [文档](https://docs.visioncoder.cn/ai-tools/claude-code/) |
| Codex CLI | [文档](https://docs.visioncoder.ai/ai-tools/codex/) | [文档](https://docs.visioncoder.cn/ai-tools/codex/) |
| Gemini CLI | [文档](https://docs.visioncoder.ai/ai-tools/gemini/) | [文档](https://docs.visioncoder.cn/ai-tools/gemini/) |
| Aider | [文档](https://docs.visioncoder.ai/ai-tools/aider/) | [文档](https://docs.visioncoder.cn/ai-tools/aider/) |
| CC Switch | [文档](https://docs.visioncoder.ai/ai-tools/cc-switch/) | [文档](https://docs.visioncoder.cn/ai-tools/cc-switch/) |
| OpenClaw | [文档](https://docs.visioncoder.ai/ai-tools/openclaw/) | [文档](https://docs.visioncoder.cn/ai-tools/openclaw/) |
| Hermes | [文档](https://docs.visioncoder.ai/ai-tools/hermes/) | [文档](https://docs.visioncoder.cn/ai-tools/hermes/) |
| Cursor | [文档](https://docs.visioncoder.ai/ai-tools/cursor/) | [文档](https://docs.visioncoder.cn/ai-tools/cursor/) |
| Cline | [文档](https://docs.visioncoder.ai/ai-tools/cline/) | [文档](https://docs.visioncoder.cn/ai-tools/cline/) |
| Roo Code | [文档](https://docs.visioncoder.ai/ai-tools/roo-code/) | [文档](https://docs.visioncoder.cn/ai-tools/roo-code/) |
| Kilo Code | [文档](https://docs.visioncoder.ai/ai-tools/kilo-code/) | [文档](https://docs.visioncoder.cn/ai-tools/kilo-code/) |
| OpenCode | [文档](https://docs.visioncoder.ai/ai-tools/opencode/) | [文档](https://docs.visioncoder.cn/ai-tools/opencode/) |
| Zed | [文档](https://docs.visioncoder.ai/ai-tools/zed/) | [文档](https://docs.visioncoder.cn/ai-tools/zed/) |
| Continue | [文档](https://docs.visioncoder.ai/ai-tools/continue/) | [文档](https://docs.visioncoder.cn/ai-tools/continue/) |

DeepSeek、GLM、Qwen、Kimi、MiniMax 也支持 Anthropic 协议，可以直接在 Claude Code 里用：[海外版](https://docs.visioncoder.ai/domestic-models/) · [国内版](https://docs.visioncoder.cn/domestic-models/)。

## 计费

- 按输入、输出、缓存命中、缓存写入分项计价，失败请求不收费
- 额度以积分显示，来自订阅套餐、加油包或兑换码
- 两个版本的价格和套餐不同，以所选版本官网的模型列表、套餐价格、计费规则页为准

## 更多文档

- API 文档 —— 鉴权、端点、错误处理：[海外版](https://docs.visioncoder.ai/api-reference/introduction/) · [国内版](https://docs.visioncoder.cn/api-reference/introduction/)
- 使用手册 —— 开通、套餐、Key、用量：[海外版](https://docs.visioncoder.ai/manual/personal/) · [国内版](https://docs.visioncoder.cn/manual/personal/)
- 遇到问题联系客服时，请带上响应头里的 `X-Request-Id`

---

<sub>Keywords: LLM API gateway · OpenAI compatible API · Anthropic API · Claude Code · Codex CLI · Gemini CLI · Cursor · DeepSeek · AI coding tools · 多模型 API 网关</sub>
