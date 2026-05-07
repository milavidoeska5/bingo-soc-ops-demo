# Copilot Workspace Instructions

## Development Checklist

Before committing, run in order:
- [ ] `uv run ruff check .` — lint, must pass clean
- [ ] `uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000` — confirm server starts
- [ ] `uv run pytest` — all tests pass
- [ ] Python conventions: snake_case, type hints on all functions

## Project

**Soc Ops** — Social Bingo (FastAPI + Jinja2 + HTMX). Players mark squares by finding people matching questions; first to 5-in-a-row wins.

Key files: `app/main.py` (routes), `app/game_service.py` (session state), `app/game_logic.py` (pure logic), `app/data.py` (edit questions here), `app/models.py` (Pydantic models).

## Conventions

- **HTMX**: Routes return HTML fragments (`components/*.html`), not JSON.
- **State**: Server-side via `GameSession` + signed cookies (`SessionMiddleware`).
- **Styling**: Custom utility classes in `app/static/css/app.css` — see [css-utilities](.github/instructions/css-utilities.instructions.md). No Tailwind, no npm.
- **Browser**: Never use Simple Browser — HTMX needs a real browser at http://localhost:8000.

## Agents & Resources

| Agent | Purpose |
|-------|---------|
| **Quiz Master** | Themed questions for `app/data.py` |
| **TDD Supervisor** | Full Red→Green→Refactor cycle |
| **Pixel Jam** | Iterative UI design with Playwright |
| **UI Review** | Playwright-based UX audit |

See also: [frontend-design](.github/instructions/frontend-design.instructions.md) · [setup](.github/prompts/setup.prompt.md) · [workshop guide](workshop/GUIDE.md)
