# VisionCoder

**One API key for Claude, GPT, and Gemini. An LLM gateway for developers — transparent per-call billing, no opaque multipliers.**

一个 API Key 直连 Claude、GPT、Gemini。面向开发者的大模型网关，按次透明扣费，不做模糊倍率。

[官网](https://visioncoder.cn) · [模型价格](https://visioncoder.cn/model_pricing) · [计费规则](https://visioncoder.cn/billing) · [服务状态](https://status.visioncoder.cn/status/coder)

---

## 支持的工具

在国内环境直接跑通这些 AI 编程工具，无需额外配置：

| 工具 | 配置教程 |
| --- | --- |
| Claude Code | [完整配置](https://visioncoder.cn/docx/claude-code) · [5 分钟快速安装](https://visioncoder.cn/docx/claude-code-quickstart) |
| OpenAI Codex CLI | [config.toml 完整示例](https://visioncoder.cn/docx/codex) |
| Gemini CLI | [接入 Gemini 模型](https://visioncoder.cn/docx/gemini) |
| OpenCode | [多模型编程助手接入](https://visioncoder.cn/docx/opencode) |
| OpenClaw | [安装与模型接入](https://visioncoder.cn/docx/openclaw) |
| Hermes Agent | [个人智能体接入](https://visioncoder.cn/docx/hermes) |

## 快速开始

一条命令装好 Node.js、Claude Code 和 Codex CLI（macOS / Linux / Windows WSL）：

```bash
curl -fsSL https://visioncoder.cn/install.sh | bash
```

Windows 用户用 [install.bat](https://visioncoder.cn/install.bat)。装完到 [控制台](https://visioncoder.cn/start) 领 API Key。

## 计费

- 按 API 调用次数扣积分，[每个模型的实际消耗](https://visioncoder.cn/model_pricing)在价格页逐条列出
- 文本模型异常失败时预扣积分自动退回
- 一次对话可能产生多次调用（Agent、工具调用、重试各算一次），[计费规则](https://visioncoder.cn/billing)有完整说明
- 想先估算成本可以用[价格计算器](https://visioncoder.cn/calculator)

## 常见问题

- [报错怎么解决](https://visioncoder.cn/docx/troubleshooting) —— 403 积分不足、429 限流、503 无可用节点、401 Key 无效等逐条对照
- [模型怎么选](https://visioncoder.cn/docx/model-comparison) —— 基于平台真实调用记录的响应耗时与积分消耗对比

---

<sub>关键词：Claude Code 国内配置 · Codex CLI 接入 · Gemini CLI 教程 · 多模型 API 网关 · AI 编程工具</sub>
