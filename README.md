# Priority Tasks

> A React + TypeScript task manager with priority levels, filters, and note-taking. Built entirely using **Cline** (VS Code AI coding agent) connected to **Qwen 2.5 Coder 14B** running on a rented RTX 3090 GPU via SSH tunnel. No OpenAI. No Anthropic.

---

## What This Demonstrates

This app was created as a real-world test of the cloud GPU LLM setup documented at [cloud-gpu-llm-setup](../cloud-gpu-llm-setup). The goal: can a 14B open-source model, running on rented cloud hardware, generate production-quality React code via an AI coding agent?

**The answer: yes, for single-component tasks.**

---

## Features

- Add tasks with priority levels (Low / Medium / High)
- Filter by All / Active / Completed
- Toggle individual tasks or check/uncheck all
- Clear completed tasks
- TypeScript throughout
- Tailwind CSS styling

---

## Stack

| Layer | Choice |
|-------|--------|
| Framework | React 18 + TypeScript |
| Styling | Tailwind CSS |
| AI Agent | Cline (VS Code extension) |
| Model | Qwen 2.5 Coder 14B Q4_K_M |
| Inference | Ollama on RTX 3090 (Vast.ai) |
| Connection | SSH tunnel → localhost:11434 |

---

## How It Was Built

```
1. SSH tunnel opened → localhost:11434 forwards to remote GPU
2. Cline configured → Ollama provider, http://localhost:11434, qwen2.5-coder:14b
3. Cline prompted → "create a React todo app with priority levels and filters"
4. Model generated → components, types, state management, styling
5. Cline wrote files → showed diffs, asked for approval per change
```

---

## Run It

```bash
npm install
npm start
# Opens http://localhost:3000
```

---

## Related

- [Cloud GPU Setup Guide](https://github.com/shubhamkokul/cloud-gpu-llm-setup) — full setup walkthrough
