🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# 🎯 Soc Ops — Social Bingo for Real-World Mixers

Turn awkward intros into a fast, fun social game.  
Players race to match people to prompts and complete 5 in a row on a bingo board.

[Start the lab →](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) · [Read workshop docs →](workshop/)

---

## Why Soc Ops?

- ✅ **Instant engagement** for team events, workshops, and meetups
- ✅ **Simple rules** that take less than a minute to explain
- ✅ **Interactive web UI** powered by FastAPI + Jinja2 + HTMX
- ✅ **Easy customization** of prompts in one place (`app/data.py`)

---

## How the game works

1. Start a session and share the board.
2. Players find people who match each square’s prompt.
3. Mark confirmed matches.
4. First player to complete 5 in a row wins.

---

## 🚀 Quick Start

```bash
uv sync
uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

Then open: **http://localhost:8000**

## ✅ Development Checklist

Before committing changes:

```bash
uv run ruff check .
uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
uv run pytest
```

---

## 🧱 Tech Stack

- **Backend:** FastAPI
- **Templates:** Jinja2
- **Interaction:** HTMX
- **State:** Server-side game sessions + signed cookies
- **Testing/Linting:** Pytest + Ruff

---

## 📚 Workshop / Lab Guide

| Part | Topic |
|------|-------|
| [**00**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=00-overview) | Overview & Checklist |
| [**01**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=01-setup) | Setup & Context Engineering |
| [**02**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=02-design) | Design-First Frontend |
| [**03**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=03-quiz-master) | Custom Quiz Master |
| [**04**](https://copilot-dev-days.github.io/agent-lab-python/docs/step.html?step=04-multi-agent) | Multi-Agent Development |

> 📝 Prefer offline docs? Use the [`workshop/`](workshop/) folder.
