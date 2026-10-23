# Awesome LLM Models [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> The complete index of Large Language Models — open-weight and proprietary. Ranked by capability, sized by parameters, costed by token, filtered by license and availability.

**Last Updated: 2026-10-04**  
*Intelligence Index from Artificial Analysis v4.3.2. Pricing from official providers. Rankings shift weekly — verify before committing.*

[![Models](https://img.shields.io/badge/Models%20Tracked-80%2B-blue?style=for-the-badge)](#-the-master-ranking)
[![Open](https://img.shields.io/badge/Open%20Weight-60%2B-green?style=for-the-badge)](#-open-weight-models)
[![Proprietary](https://img.shields.io/badge/Proprietary-20%2B-red?style=for-the-badge)](#-proprietary-models)
[![Updated](https://img.shields.io/badge/Updated-2026--10--04-orange?style=for-the-badge)](#)

---

## Table of Contents

1. [The Master Ranking (All Models)](#1-the-master-ranking-all-models)
2. [Open-Weight Models](#2-open-weight-models)
3. [Proprietary Models](#3-proprietary-models)
4. [By Size Class](#4-by-size-class)
5. [By Capability](#5-by-capability)
6. [By Cost (per 1M tokens)](#6-by-cost-per-1m-tokens)
7. [By License](#7-by-license)
8. [By Provider](#8-by-provider)
9. [Hardware Requirements](#9-hardware-requirements)
10. [Maintenance Strategy](#10-maintenance-strategy)
11. [Contributing](#-contributing)

---

## 1. The Master Ranking (All Models)

Every notable model — open and closed — ranked by Intelligence Index. This is the single source of truth.

| Rank | Model | Provider | Type | Params | Context | Index | Input $/1M | Output $/1M |
|:---:|---|---|---|---|---|---|---|---|
| 1 | **Claude Opus 5.5** | Anthropic | 🔒 Proprietary | — | 1M | **57.6** | $15.00 | $75.00 |
| 2 | **Gemini 3.0 Ultra** | Google | 🔒 Proprietary | — | 2M | **56.4** | $7.00 | $21.00 |
| 3 | **GPT-5.5** | OpenAI | 🔒 Proprietary | — | 400K | **55.8** | $10.00 | $30.00 |
| 4 | **Claude Sonnet 5** | Anthropic | 🔒 Proprietary | — | 1M | **54.2** | $3.00 | $15.00 |
| 5 | **Grok 5** | xAI | 🔒 Proprietary | — | 256K | **52.8** | $5.00 | $15.00 |
| 6 | **GPT-5.2** | OpenAI | 🔒 Proprietary | — | 400K | **51.4** | $5.00 | $15.00 |
| 7 | **Gemini 3.0 Pro** | Google | 🔒 Proprietary | — | 2M | **50.9** | $2.50 | $10.00 |
| 8 | **Claude Haiku 5** | Anthropic | 🔒 Proprietary | — | 500K | **48.7** | $0.80 | $4.00 |
| 9 | **o4** | OpenAI | 🔒 Proprietary | — | 200K | **47.5** | $3.00 | $12.00 |
| 10 | **MiMo-V2.6-Pro** | Xiaomi | 🟢 Open | 1.02T/42B | 1M | **46.3** | $0.44 | $0.87 |
| 11 | **GLM-5.3** | Zhipu AI | 🟢 Open | 744B/40B | 1,048K | **44.8** | $1.40 | $4.40 |
| 12 | **Kimi K3** | Moonshot | 🟢 Open | 2.8T/104B | 1M | **43.6** | $3.00 | $15.00 |
| 13 | **Qwen3.5-397B** | Alibaba | 🟢 Open | 397B/17B | 262K | **42.0** | $0.50 | $3.30 |
| 14 | **DeepSeek V4 Pro** | DeepSeek | 🟢 Open | 1.6T/49B | 1M | **41.0** | $1.32 | $3.96 |
| 15 | **Gemini 3.0 Flash** | Google | 🔒 Proprietary | — | 1M | **40.8** | $0.15 | $0.60 |
| 16 | **MiMo-V2.6-Flash** | Xiaomi | 🟢 Open | 309B/15B | 1M | **40.0** | — | — |
| 17 | **DeepSeek V4 Flash** | DeepSeek | 🟢 Open | 284B/13B | 1M | **39.5** | $0.14 | $0.28 |
| 18 | **Gemma 4 31B** | Google | 🟢 Open | 31B | 128K | **39.0** | — | — |
| 19 | **Command A** | Cohere | 🟢 Open | 111B | 256K | **38.5** | $2.50 | $10.00 |
| 20 | **Mistral Large 3** | Mistral | 🟢 Open | 123B | 128K | **37.2** | $2.00 | $6.00 |
| 21 | **Llama 4 Maverick** | Meta | 🟢 Open | 400B/17B | 1M | **36.8** | $0.27 | $0.85 |
| 22 | **GPT-4o** | OpenAI | 🔒 Proprietary | — | 128K | **36.5** | $2.50 | $10.00 |
| 23 | **Qwen3.8-27B** | Alibaba | 🟢 Open | 27B | 262K | **34.0** | $0.44 | $3.30 |
| 24 | **Llama 4 Scout** | Meta | 🟢 Open | 109B/17B | 10M | **33.4** | $0.11 | $0.34 |
| 25 | **Claude Haiku 4.5** | Anthropic | 🔒 Proprietary | — | 200K | **32.8** | $1.00 | $5.00 |
| 26 | **Mistral Medium 3** | Mistral | 🔒 Proprietary | — | 128K | **32.5** | $0.40 | $2.00 |
| 27 | **Phi-4** | Microsoft | 🟢 Open | 14B | 16K | **31.2** | — | — |
| 28 | **Nova Pro** | Amazon | 🔒 Proprietary | — | 300K | **30.8** | $0.80 | $3.20 |
| 29 | **Qwen3.5 9B** | Alibaba | 🟢 Open | 9B | 262K | **29.5** | $0.17 | $0.25 |
| 30 | **Gemini 3.0 Flash-Lite** | Google | 🔒 Proprietary | — | 1M | **28.6** | $0.075 | $0.30 |

*Index = Artificial Analysis Intelligence Index v4.3.2 (composite of reasoning, coding, knowledge, agentic). Proprietary scores are from public benchmarks as of Oct 2026.*

---

## 2. Open-Weight Models

Models whose weights are publicly downloadable. Ranked by capability.

### 2.1 Trillion-Class (>1T total params)

| Model | Total / Active | Context | License | Released | Notes |
|---|---|---|---|---|---|
| **Kimi K3** | 2.8T / 104B | 1M | Modified MIT | Jul 2026 | Largest open model; native vision; 1,561 GB on HF |
| **DeepSeek V4 Pro** | 1.6T / 49B | 1M | MIT | Apr 2026 | Largest open MoE; 49B active per token |
| **MiMo-V2.6-Pro** | 1.02T / 42B | 1M | Apache 2.0 | Sep 2026 | Xiaomi frontier; #5 open on Agent Arena |
| **LongCat 2.0** | 1.6T / 48B | 1M | Open | 2026 | Long-context specialist |
| **Qwen3.8 2.4T A95B** | 2.4T / 95B | 1M | Apache 2.0 | 2026 | Alibaba's largest; 4.9 TB BF16 |
| **Kimi K2 Thinking** | 1T / 32B | 256K | Modified MIT | 2026 | Reasoning-focused K2 variant |

### 2.2 Large-Class (200B–1T params)

| Model | Total / Active | Context | License | Notes |
|---|---|---|---|---|
| **GLM-5.3** | 744B / 40B | 1,048K | MIT | Best open reasoning; near-frontier coding |
| **Qwen3.5-397B** | 397B / 17B | 262K | Apache 2.0 | Best efficiency; GPQA 86% |
| **MiMo-V2.6-Flash** | 309B / 15B | 1M | Apache 2.0 | Agent-optimized mid-size |
| **DeepSeek V4 Flash** | 284B / 13B | 1M | MIT | Best price/performance; 217 t/s |
| **Qwen3-235B** | 235B / 22B | 262K | Apache 2.0 | Workhorse from previous gen |
| **MiniMax M2.5** | 230B / 10B | 205K | Open | Strong agentic; 8/8 tool-use |
| **Llama 4 Maverick** | 400B / 17B | 1M | Llama Community | Meta's mid-tier |
| **Ling 3.1 Flash** | 560B / 25B | 1M | Open | 203 t/s |
| **GLM-5.1** | 754B / 40B | 200K | MIT | Previous flagship |

### 2.3 Mid-Class (30B–200B params)

| Model | Params | Context | License | Notes |
|---|---|---|---|---|
| **GPT-OSS 120B** | 120B | 131K | Apache 2.0 | OpenAI's open-weight release |
| **Llama 4 Scout** | 109B / 17B | 10M | Llama Community | 10M-token context |
| **Ling 3.0 Flash** | 124B / 5.1B | 262K | Open | Extremely efficient MoE |
| **Mistral Small 3.1** | 24B | 128K | Apache 2.0 | Enterprise-safe; multimodal |
| **Qwen3.8-27B** | 27B | 262K | Apache 2.0 | Most popular on HF (Sept 2026) |
| **Gemma 4 31B** | 31B | 128K | Gemma Terms | Best sub-32B reasoning |
| **Ornith-1.0-35B** | 35B MoE | 256K | MIT | Agentic coding specialist |
| **Command A** | 111B | 256K | CC-BY-NC | Cohere enterprise |
| **Step 3.7 Flash** | 198B / 11B | 262K | Open | Cost-effective mid-size |
| **Yi-Large 2** | 200B | 200K | Open | 01.AI |
| **Falcon 3 180B** | 180B | 128K | TII Falcon | TII Abu Dhabi |

### 2.4 Small-Class (<30B params)

| Model | Params | Context | License | Notes |
|---|---|---|---|---|
| **Qwen3.5 9B** | 9B | 262K | Apache 2.0 | Cheapest serious model |
| **Phi-4** | 14B | 16K | MIT | Microsoft |
| **Phi-4-mini** | 3.8B | 128K | MIT | Runs on modest machines |
| **Llama 4 7B** | 7B | — | Llama Community | Smallest Llama 4 |
| **Gemma 3 12B** | 12B | 128K | Gemma Terms | Multimodal |
| **Ornith-1.0-9B** | 9B | 128K | MIT | SWE-bench 69.4% |
| **MiniCPM5-2B** | 2B | — | Open | Best open under 4B |
| **SmolLM3-3B** | 3B | 128K | Apache 2.0 | HuggingFace |
| **Qwen3.5 4B** | 4B | 262K | Apache 2.0 | Laptop-friendly |
| **TinyLlama 1.1B** | 1.1B | 2K | Apache 2.0 | Ultra-small |
| **OLMo 2 13B** | 13B | 4K | Apache 2.0 | Fully open (data + code) |

---

## 3. Proprietary Models

Closed-source models accessed via API. Ranked by capability.

### 3.1 Frontier Tier

| Model | Provider | Context | Index | Input $/1M | Output $/1M | Notes |
|---|---|---|---|---|---|---|
| **Claude Opus 5.5** | Anthropic | 1M | 57.6 | $15.00 | $75.00 | Current best overall |
| **Gemini 3.0 Ultra** | Google | 2M | 56.4 | $7.00 | $21.00 | Largest context, best multimodal |
| **GPT-5.5** | OpenAI | 400K | 55.8 | $10.00 | $30.00 | Best agentic + reasoning |
| **Claude Sonnet 5** | Anthropic | 1M | 54.2 | $3.00 | $15.00 | Best value frontier |
| **Grok 5** | xAI | 256K | 52.8 | $5.00 | $15.00 | Real-time knowledge |
| **GPT-5.2** | OpenAI | 400K | 51.4 | $5.00 | $15.00 | Previous flagship |
| **Gemini 3.0 Pro** | Google | 2M | 50.9 | $2.50 | $10.00 | Best mid-frontier |

### 3.2 Reasoning & Math Tier

| Model | Provider | Context | Index | Input $/1M | Output $/1M | Notes |
|---|---|---|---|---|---|---|
| **o4** | OpenAI | 200K | 47.5 | $3.00 | $12.00 | Math + science specialist |
| **o4-mini** | OpenAI | 200K | 44.2 | $1.10 | $4.40 | Cheapest reasoner |
| **Claude Haiku 5** | Anthropic | 500K | 48.7 | $0.80 | $4.00 | Fast + cheap reasoning |
| **Gemini 3.0 Deep Think** | Google | 1M | 49.8 | $5.00 | $20.00 | Extended thinking mode |

### 3.3 Fast & Cheap Tier

| Model | Provider | Context | Index | Input $/1M | Output $/1M | Notes |
|---|---|---|---|---|---|---|
| **Gemini 3.0 Flash** | Google | 1M | 40.8 | $0.15 | $0.60 | Best cheap proprietary |
| **Gemini 3.0 Flash-Lite** | Google | 1M | 28.6 | $0.075 | $0.30 | Cheapest overall |
| **GPT-5.2-mini** | OpenAI | 200K | 38.4 | $0.60 | $2.40 | Budget OpenAI |
| **Claude Haiku 4.5** | Anthropic | 200K | 32.8 | $1.00 | $5.00 | Previous gen |
| **Mistral Medium 3** | Mistral | 128K | 32.5 | $0.40 | $2.00 | EU-based |
| **Nova Pro** | Amazon | 300K | 30.8 | $0.80 | $3.20 | AWS-native |

### 3.4 Legacy & Still-Used

| Model | Provider | Context | Index | Input $/1M | Output $/1M | Notes |
|---|---|---|---|---|---|---|
| **GPT-4o** | OpenAI | 128K | 36.5 | $2.50 | $10.00 | Still widely deployed |
| **GPT-4o-mini** | OpenAI | 128K | 31.0 | $0.15 | $0.60 | Budget workhorse |
| **Claude Sonnet 4.5** | Anthropic | 200K | 42.1 | $3.00 | $15.00 | Previous flagship |
| **Gemini 2.5 Pro** | Google | 1M | 40.2 | $1.25 | $10.00 | Previous flagship |
| **Grok 4** | xAI | 256K | 44.0 | $3.00 | $15.00 | Previous flagship |

### 3.5 Specialized

| Model | Provider | Use Case | Notes |
|---|---|---|---|
| **o3-deep-research** | OpenAI | Deep research | Web-browsing agent |
| **Claude Code** | Anthropic | Agentic coding | Optimized for terminal |
| **Gemini Code Assist** | Google | IDE coding | Deep IDE integration |
| **GitHub Copilot** | Microsoft | IDE coding | OpenAI + Anthropic backend |
| **Cursor Composer** | Cursor | Agentic coding | Custom fine-tuned model |
| **Nova Sonic** | Amazon | Speech | Realtime voice |
| **Nova Canvas** | Amazon | Image generation | Multimodal |
| **GPT-4o Realtime** | OpenAI | Voice | Realtime audio |

---

## 4. By Size Class

### 4.1 Size vs. Deployment Reality

| Size Class | Params | Typical Hardware | Open Models | Proprietary Equivalent |
|---|---|---|---|---|
| **Nano** | <2B | Phone, edge | TinyLlama, SmolLM3 | Gemini Flash-Lite, GPT-4o-mini |
| **Small** | 2–10B | Consumer GPU, MacBook | Qwen3.5 9B, Phi-4-mini | GPT-5.2-mini, Claude Haiku |
| **Medium** | 10–30B | RTX 4090, M2 Max | Gemma 4 31B, Qwen3.8-27B | Mistral Medium 3, Nova Pro |
| **Large** | 30–200B | 4× A100 | Llama 4 Scout, Command A | Gemini 3.0 Pro |
| **Very Large** | 200B–1T | 8× H100 | GLM-5.3, Qwen3.5-397B | GPT-5.5, Claude Sonnet 5 |
| **Trillion** | >1T | 16× H100+ | Kimi K3, DeepSeek V4 Pro | Claude Opus 5.5, Gemini 3.0 Ultra |

### 4.2 MoE vs. Dense

| Type | Example | Active Params | Pros | Cons |
|---|---|---|---|---|
| **Dense** | Phi-4 14B | 14B | Predictable latency | Higher cost per token |
| **MoE** | MiMo-V2.6-Pro | 42B of 1.02T | Fast + cheap | Complex infrastructure |
| **Hybrid** | Llama 4 Scout | 17B of 109B | Balance | Requires careful batching |

---

## 5. By Capability

### 5.1 Coding & Software Engineering

| Model | Type | SWE-bench Verified | Notes |
|---|---|---|---|
| **Claude Sonnet 5** | 🔒 | **77.2%** | Best proprietary coder |
| **Ornith-1.0-35B** | 🟢 | 75.6% | Best open agentic coder |
| **GPT-5.5** | 🔒 | 74.9% | Strong multi-file |
| **Ornith-1.0-9B** | 🟢 | 69.4% | Best small coder |
| **GLM-5.3** | 🟢 | ~62% | Complex refactors |
| **Qwen3-Coder-480B** | 🟢 | 91.9% (HumanEval) | Best open by accuracy |
| **Gemini 3.0 Pro** | 🔒 | 71.0% | Best for Google Cloud |
| **DeepSeek V4 Pro** | 🟢 | — | 1M context agentic |

### 5.2 Reasoning & Math

| Model | Type | Index | GPQA | Notes |
|---|---|---|---|---|
| **Claude Opus 5.5** | 🔒 | 57.6 | — | Best overall |
| **Gemini 3.0 Ultra** | 🔒 | 56.4 | — | Best multimodal reasoning |
| **o4** | 🔒 | 47.5 | 92% | Math specialist |
| **MiMo-V2.6-Pro** | 🟢 | 46.3 | — | Best open reasoner |
| **GLM-5.3** | 🟢 | 44.8 | — | Near-frontier open |
| **Qwen3.5-397B** | 🟢 | 42.0 | 86% | Best sub-400B |

### 5.3 Multimodal (Vision + Text)

| Model | Type | MMMU-Pro | Notes |
|---|---|---|---|
| **Gemini 3.0 Ultra** | 🔒 | **82%** | Best overall vision |
| **Claude Opus 5.5** | 🔒 | 80% | Strong document parsing |
| **GPT-5.5** | 🔒 | 79% | Strong chart/graph |
| **Qwen3.5-397B** | 🟢 | 75% | Best open vision |
| **Gemma 4 31B** | 🟢 | 73% | Best sub-32B vision |
| **Kimi K3** | 🟢 | — | Native at trillion scale |

### 5.4 Agentic & Tool Use

| Model | Type | Agentic Index | TerminalBench | Notes |
|---|---|---|---|---|
| **Claude Sonnet 5** | 🔒 | **58** | **62%** | Best agentic model |
| **Qwen3.5-397B** | 🟢 | 55 | — | Best open agentic |
| **GPT-5.5** | 🔒 | 57 | 60% | Strong tool use |
| **Gemini 3.0 Ultra** | 🔒 | 55 | 58% | Deep Research |
| **MiMo-V2.6-Pro** | 🟢 | — | 34.8% | Open terminal agent |
| **Gemma 4 31B** | 🟢 | — | 36% | Small open agent |

### 5.5 Long Context

| Model | Type | Context | Notes |
|---|---|---|---|
| **Llama 4 Scout** | 🟢 | **10M** | Largest open |
| **Gemini 3.0 Ultra** | 🔒 | 2M | Largest proprietary |
| **Gemini 3.0 Pro** | 🔒 | 2M | Same window, cheaper |
| **Claude Opus 5.5** | 🔒 | 1M | Best long-doc |
| **Kimi K3** | 🟢 | 1M | Open + vision |
| **DeepSeek V4 Pro** | 🟢 | 1M | Open MoE |
| **GLM-5.3** | 🟢 | 1,048K | Max open context |

### 5.6 Voice & Audio

| Model | Type | Notes |
|---|---|---|
| **GPT-4o Realtime** | 🔒 | Native speech-to-speech |
| **Gemini 3.0 Live** | 🔒 | Multimodal voice |
| **Nova Sonic** | 🔒 | Amazon realtime |
| **Whisper Large v3** | 🟢 | Best open STT |
| **Kokoro TTS** | 🟢 | Best open TTS |

---

## 6. By Cost (per 1M tokens)

### 6.1 Ultra-Budget (<$0.10 input)

| Model | Type | Input | Output | Notes |
|---|---|---|---|---|
| **Gemini 3.0 Flash-Lite** | 🔒 | $0.075 | $0.30 | Cheapest proprietary |
| **Llama 4 Scout** | 🟢 | $0.11 | $0.34 | Cheapest large open |
| **DeepSeek V4 Flash** | 🟢 | $0.14 | $0.28 | Best budget frontier-adjacent |
| **GPT-OSS 120B** | 🟢 | $0.15 | $0.60 | Apache 2.0 |
| **Gemini 3.0 Flash** | 🔒 | $0.15 | $0.60 | Google's budget |
| **GPT-4o-mini** | 🔒 | $0.15 | $0.60 | OpenAI budget |

### 6.2 Budget ($0.10–$1.00 input)

| Model | Type | Input | Output | Notes |
|---|---|---|---|---|
| **Qwen3.5 9B** | 🟢 | $0.17 | $0.25 | Best tiny |
| **MiMo-V2.6-Pro** | 🟢 | $0.44 | $0.87 | Best overall open at budget |
| **Qwen3.8-27B** | 🟢 | $0.44 | $3.30 | Popular HF model |
| **Qwen3.5-397B** | 🟢 | $0.50 | $3.30 | Frontier at mid-price |
| **GPT-5.2-mini** | 🔒 | $0.60 | $2.40 | OpenAI mid |
| **Claude Haiku 5** | 🔒 | $0.80 | $4.00 | Anthropic budget |
| **Nova Pro** | 🔒 | $0.80 | $3.20 | AWS budget |

### 6.3 Mid Tier ($1.00–$5.00 input)

| Model | Type | Input | Output | Notes |
|---|---|---|---|---|
| **Claude Haiku 4.5** | 🔒 | $1.00 | $5.00 | Previous gen |
| **DeepSeek V4 Pro** | 🟢 | $1.32 | $3.96 | 1.6T open |
| **GLM-5.3** | 🟢 | $1.40 | $4.40 | Best open reasoning |
| **Mistral Large 3** | 🟢 | $2.00 | $6.00 | EU enterprise |
| **Gemini 3.0 Pro** | 🔒 | $2.50 | $10.00 | Google mid |
| **GPT-4o** | 🔒 | $2.50 | $10.00 | Previous flagship |
| **Claude Sonnet 5** | 🔒 | $3.00 | $15.00 | Best value frontier |

### 6.4 Premium (>$5.00 input)

| Model | Type | Input | Output | Notes |
|---|---|---|---|---|
| **Grok 5** | 🔒 | $5.00 | $15.00 | Real-time knowledge |
| **GPT-5.2** | 🔒 | $5.00 | $15.00 | Previous flagship |
| **Gemini 3.0 Ultra** | 🔒 | $7.00 | $21.00 | Best multimodal |
| **GPT-5.5** | 🔒 | $10.00 | $30.00 | Best agentic |
| **Claude Opus 5.5** | 🔒 | $15.00 | $75.00 | Best overall |

### 6.5 Open vs. Proprietary Cost Gap

| Capability Level | Open Price | Proprietary Price | Savings |
|---|---|---|---|
| **Frontier (Index 40+)** | $0.44–$3.00 | $3.00–$15.00 | **70–85%** |
| **Mid (Index 30–40)** | $0.14–$0.50 | $0.80–$5.00 | **75–90%** |
| **Budget (Index <30)** | $0.17–$0.44 | $0.075–$1.00 | **0–80%** |

**Market context:** The Silicon Data LLM Token Expenditure Index hit $0.97 per million tokens in September 2026 — first time below $1. Open weights average $0.83/M, proprietary $6.03/M — a **7.3x gap**.

---

## 7. By License

### 7.1 Open-Weight Licenses

| License | Commercial Use | Models | Key Terms |
|---|---|---|---|
| **Apache 2.0** | ✅ Unrestricted | Qwen3.5, MiMo-V2.6, Mistral Small, Gemma 4, GPT-OSS, OLMo | Patent grant; attribution |
| **MIT** | ✅ Unrestricted | DeepSeek V4, GLM-5.3, Phi-4, Ornith | Barely-there attribution |
| **Modified MIT** | ⚠️ Revenue-gated | Kimi K3 | Above $20M/$50M API revenue |
| **Llama 4 Community** | ⚠️ >700M MAU restricted | Llama 4 Scout, Maverick | AUP; "Built with Llama" |
| **Gemma Terms** | ⚠️ Use restrictions | Gemma 3, Gemma 4 | Prohibited Use Policy |
| **CC-BY-NC** | ❌ Non-commercial | Command A | Research only |
| **TII Falcon** | ⚠️ Royalty-free with conditions | Falcon 3 | Acceptable Use Policy |

### 7.2 Proprietary Access

| Provider | Access Model | Enterprise Options |
|---|---|---|
| **Anthropic** | API + Claude.ai | Bedrock, Vertex, direct |
| **OpenAI** | API + ChatGPT | Azure OpenAI, direct |
| **Google** | API + Gemini | Vertex AI, Workspace |
| **xAI** | API + X Premium | Direct |
| **Amazon** | API | Bedrock |
| **Cohere** | API | Private deployment |
| **Mistral** | API + weights | On-prem + cloud |

### 7.3 Safest for Commercial Products

- **Apache 2.0 / MIT**: Qwen, DeepSeek, GLM, MiMo, GPT-OSS, Mistral, Phi
- **Avoid for products**: CC-BY-NC models (Command A)
- **Check per-version**: Llama and Gemma terms change between releases

---

## 8. By Provider

### 8.1 Open-Weight Providers

| Provider | Flagship | Strengths | Country |
|---|---|---|---|
| **Alibaba (Qwen)** | Qwen3.8 2.4T | Size variety, Apache 2.0 | 🇨🇳 |
| **DeepSeek** | V4 Pro | MoE efficiency, MIT | 🇨🇳 |
| **Zhipu AI (GLM)** | GLM-5.3 | Reasoning, MIT | 🇨🇳 |
| **Xiaomi (MiMo)** | V2.6-Pro | Frontier + agentic | 🇨🇳 |
| **Moonshot (Kimi)** | K3 | Largest open | 🇨🇳 |
| **Meta (Llama)** | Llama 4 Maverick | Ecosystem, tooling | 🇺🇸 |
| **Google (Gemma)** | Gemma 4 31B | Efficiency, small | 🇺🇸 |
| **Mistral** | Mistral Large 3 | EU, enterprise | 🇫🇷 |
| **Microsoft (Phi)** | Phi-4 | Small, capable | 🇺🇸 |
| **Cohere** | Command A | Enterprise RAG | 🇨🇦 |
| **TII** | Falcon 3 | Arabic, multilingual | 🇦🇪 |
| **AI2** | OLMo 2 | Fully open (data + code) | 🇺🇸 |

### 8.2 Proprietary Providers

| Provider | Flagship | Strengths | Country |
|---|---|---|---|
| **Anthropic** | Claude Opus 5.5 | Best coding, agentic | 🇺🇸 |
| **OpenAI** | GPT-5.5 | Reasoning, ecosystem | 🇺🇸 |
| **Google** | Gemini 3.0 Ultra | Multimodal, context | 🇺🇸 |
| **xAI** | Grok 5 | Real-time, X data | 🇺🇸 |
| **Amazon** | Nova Pro | AWS integration | 🇺🇸 |
| **Microsoft** | Copilot | IDE + Office | 🇺🇸 |
| **Cohere** | Command R+ | Enterprise RAG | 🇨🇦 |
| **AI21** | Jamba 1.6 | Long context | 🇮🇱 |

---

## 9. Hardware Requirements

### 9.1 VRAM Estimates (4-bit Quantization)

| Size | 4-bit VRAM | Runs On | Example Models |
|---|---|---|---|
| <10B | 4–8 GB | Consumer GPU, MacBook | Qwen3.5 9B, Phi-4-mini |
| 10–30B | 8–18 GB | RTX 4090, M2 Max | Gemma 4 31B, Qwen3.8-27B |
| 30–70B | 18–40 GB | 2× RTX 4090, A6000 | Ornith-1.0-35B, Command A |
| 70–200B | 40–100 GB | H100 80GB, 2× A6000 | Llama 4 Scout |
| 200B–1T | 100–500 GB | 8× H100, 4× H200 | GLM-5.3, Qwen3.5-397B |
| >1T | 500 GB–4 TB | 16× H100+ | Kimi K3, DeepSeek V4 Pro |

### 9.2 Practical Deployment Notes

- **Qwen3.8-27B:** 16.5 GB in 4-bit — fits a single 24 GB GPU
- **Gemma 4 31B / Qwen3.5 27B:** Fit a single H100 80GB in BF16; local Mac with quant
- **MiMo-V2.6-Pro:** 1.02T — 8× H100 minimum or heavy quant
- **Kimi K3:** 2.8T — 1,561 GB on HF; serious infrastructure only
- **Proprietary:** No local option — API only, or Bedrock/Vertex/Azure

---

## 10. Maintenance Strategy

This list changes weekly. Here's how to keep it current without burning out.

### 10.1 Pin the Volatile Data

Put rankings, pricing, and capability scores in a YAML file (`data/models.yaml`) and render the markdown from it.

```yaml
models:
  - name: "Claude Opus 5.5"
    provider: "Anthropic"
    type: "proprietary"
    params: null
    context: "1M"
    intelligence: 57.6
    input_cost: 15.00
    output_cost: 75.00
    license: "Proprietary"
    updated: "2026-10-04"

  - name: "MiMo-V2.6-Pro"
    provider: "Xiaomi"
    type: "open"
    params: "1.02T/42B"
    context: "1M"
    intelligence: 46.3
    input_cost: 0.44
    output_cost: 0.87
    license: "Apache 2.0"
    updated: "2026-10-04"
```

Then a Python/Node script regenerates the tables. Update YAML → run script → commit. **Biggest time-saver.**

### 10.2 Automate the Delta

- **Artificial Analysis** — Intelligence Index updates weekly
- **Hugging Face** — trending models API
- **Provider pricing pages** — Together, NEAR, OpenAI, Anthropic, Google
- **GitHub Action** — weekly fetch + PR with diff

### 10.3 Update Cadence

| Section | Frequency | How |
|---|---|---|
| Master ranking | Weekly | YAML + script |
| Cost tables | Weekly | YAML + script |
| Capability summaries | Monthly | Manual |
| Size class descriptions | Monthly | Manual |
| License table | Quarterly | Manual |
| Provider table | Quarterly | Manual |
| Maintenance guide | Never | Static |

### 10.4 Archive, Don't Delete

Move fallen-out-of-top-10 models to `archive/`. History of what was frontier is valuable data.

---

## 🤝 Contributing


## 📜 License

[![CC0](https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge)](LICENSE)

To the extent possible under law, all contributors have waived all copyright and related or neighboring rights to this work.
