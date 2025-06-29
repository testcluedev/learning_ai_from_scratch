# AI Assistant: Learning Plan & Local Model Setup Guide

## 🎯 Goal
Design and implement a hybrid AI assistant that:
- Combines local private LLM (for memory and reasoning) with cloud APIs (OpenAI, Codex)
- Supports memory persistence (via vector DB + relational DB)
- Handles multi-modal I/O (text, voice)
- Integrates cost tracking, VAT logic, billing/invoicing

---

## 📚 Learning Plan (Flexible Milestones)

### 📌 Phase 1: Foundations of LLMs + Prompting
- [AI For Everyone](https://www.coursera.org/learn/ai-for-everyone) (Coursera, Andrew Ng)
- [Natural Language Processing Specialization](https://www.coursera.org/specializations/natural-language-processing) (Coursera)

- [ChatGPT Prompt Engineering for Developers](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) (DeepLearning.AI short course)
- [Building Systems with the ChatGPT API](https://www.deeplearning.ai/short-courses/building-systems-with-chatgpt/) (DeepLearning.AI short course)

---

### 📌 Phase 2: LLM Application Development
- [LangChain official docs](https://python.langchain.com)
- [LlamaIndex official docs](https://gpt-index.readthedocs.io)
- Explore YouTube tutorials / OSS demos for LangChain + LlamaIndex

---

### 📌 Phase 3: Local LLM Deployment + Multi-modal Interaction
- [llama.cpp GitHub](https://github.com/ggerganov/llama.cpp) (Run LLaMA, Mistral, Mixtral locally)
- [Ollama](https://ollama.com) (Easiest way to serve LLaMA, Mistral, Phi-3 locally)
- [Mistral AI](https://mistral.ai)
- [Phi-3](https://www.microsoft.com/en-us/research/project/phi/)
- [Gemma](https://ai.google.dev/gemma)

---

## 💡 Local Model Options

| Model | Recommended When | Notes |
|--------|----------------|-------|
| **LLaMA 3 (7B/13B/70B)** | You want a mainstream OSS model with big community | Good general-purpose model, large footprint at high scale |
| **Mistral 7B / Mixtral 8x7B** | You want fast, smart models with smaller resource needs | Highly competitive OSS models |
| **Phi-3** | You want small model with strong reasoning (esp. code + logic) | Excellent small-scale model for local/private use |
| **Gemma** | You want a Google-backed OSS model | Decent performance, open weights |

---

## 🛠 Local Model Setup Guidance

### ✅ Easiest Way: Ollama
1️⃣ Install Ollama  
```bash
curl -fsSL https://ollama.com/install.sh | sh