# portfolio — Project Context for Claude Code

> Personal identity + background live in `~/.claude/CLAUDE.md` (global). This covers THIS repo.

## What this is
Sanjay's personal portfolio site. Static site deployed via GitHub Pages.
- Live: https://sanjayprakash-git.github.io/portfolio/
- Repo: github.com/sanjayprakash-git (GitHub Pages, `.nojekyll` present)
- Deploy: push to main → GitHub Actions workflow in `.github/workflows/`

## Files
- `index.html` — main page (current). `index_original.html` / `style_original.css` — pre-redesign backups.
- `style.css` — current styles.
- `resume.html` — web resume. `bennova-case-study.html` — Bennova case study page.

## Connected services (hosted elsewhere, not in this repo)
- Chatbot: Groq `llama-3.3-70b-versatile` via proxy — answers visitor questions about Sanjay.
- Proxy (serverless): https://portfolio-proxy-two.vercel.app — handles chat + Telegram
  visitor notifications + BA toolkit backend.
- Visitor tracking: Telegram notify on page open + scroll %/clicks/time on exit.
- BA Toolkit (separate repo ~/ba-toolkit): https://sanjayprakash-git.github.io/BA-Analysis_toolkit/

## Conventions
- Keep it static, no build step. Accessibility-compliant markup.
- Portfolio should TEASE, not explain everything — save depth for interviews.
- PDF (if generating resume): Chrome headless only, both flags
  `--print-to-pdf-no-header --no-pdf-header-footer`. Never weasyprint/wkhtmltopdf.
- Do NOT commit any API keys — chatbot/notification secrets live in the Vercel proxy, not here.
