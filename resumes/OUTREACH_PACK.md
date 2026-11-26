# Outreach & Offer Conversion Pack (EN + RU)

---

## 1. US / EU Remote — Cold DM / Application (LinkedIn / Wellfound / YC / Email)

**Subject:** Staff Rust / AI Infra Engineer — Built Sub-ms LLM Cost & Security Gateway (`aegis-llm-gateway`) + Mozilla/Tabularis OSS PRs

Hi [Name],

I'm Konstantin, a Systems & AI Infrastructure Engineer specializing in `#![forbid(unsafe_code)]` Rust, Go, and high-throughput backends.

A few concrete things I've shipped recently that map directly to [Company]'s stack:
- **Aegis AI Gateway** (`github.com/markankamaransheogarat-sys/aegis-llm-gateway`, `v0.2.0`): Drop-in Rust reverse proxy for OpenAI/Anthropic/vLLM cutting token spend 40–70% via L1 SHA-256 + L2 SimHash-64 semantic caching, outbound secret scrubbing (`sk-`, `AKIA`, `ghp_`, JWT), prompt-injection WAF, per-key RPM + USD budget caps, live `/admin` UI, and Stripe/YooKassa/CryptoBot billing webhooks.
- **MCP Guard & Dep-Xray**: Rust security firewall for MCP servers (`stdio`/SSE/HTTP) and `tree-sitter` AST supply-chain diff analyzer (`SARIF 2.1.0`).
- **30+ Open-Source PRs**: Merged contributions to **Mozilla `neqo`** (QUIC/HTTP3 in Rust), **TabularisDB** (8+ features), **Linux Foundation Hiero SDK**, plus active PRs in **MoonshotAI/kimi-code**, **OpenAI codex-security**, and **Leonida**.

My 1-page resume (PDF) is attached (`RESUME_EN.pdf`). Happy to jump on a 15-min technical chat this week.

Best,  
Konstantin  
GitHub: https://github.com/markankamaransheogarat-sys  
Telegram: https://t.me/amadeus1827 · Email: markankamaransheogarat@gmail.com

---

## 2. РФ / СНГ — Отклик рекрутеру / CTO / Тимлиду (HH / Telegram / Хабр Карьера)

Привет, [Имя]!

Ищу позицию **Staff / Senior Backend или Systems Engineer (Rust / Go / Python / High-Load / AI Infra)**.

Коротко о том, что делал на практике (всё открыто с кодом, тестами и бенчмарками на GitHub):
- **High-Load и БД**: транзакционный outbox-диспетчер на Go (`pgx` `FOR UPDATE SKIP LOCKED`, circuit breaker, Prometheus), zero-alloc SSE-прокси (`go-sse-gateway`), движок колоночной аналитики на raw `asyncpg` + ClickHouse (`1.56M ord/s`), чат-брокер с CRDT (`145k msg/s`, `6.88 µs`).
- **AI-инфраструктура и AppSec**: `aegis-llm-gateway` `v0.2.0` на Rust (`#![forbid(unsafe_code)]`) — кэширующий шлюз перед OpenAI/Anthropic/GigaChat (экономия 40–70% токен-бюджета, редакция утечек ключей, WAF от prompt-injection, RPM/USD-лимиты, `/admin` UI, вебхуки ЮKassa/Stripe/CryptoBot); `llm-cache-edge` `v0.1.0`, `mcp-guard` `v0.2.0` и AST-анализатор зависимостей `dep-xray` `v0.2.0`.
- **Open-Source**: 30+ PR в крупные проекты (**Mozilla `neqo`**, **TabularisDB** — 8+ фич, **Linux Foundation Hiero SDK**, **MoonshotAI/kimi-code**, **OpenAI codex-security**).

Резюме (PDF) прикрепил (`RESUME_RU.pdf`). Готов пройти техсобес или разобрать архитектуру ваших сервисов на созвоне.

Константин  
Telegram: @amadeus1827 · GitHub: https://github.com/markankamaransheogarat-sys

---

## 3. B2B Pitch — Продажа `aegis-llm-gateway` компаниям и AI-стартапам

**Subject:** Cut your OpenAI / Anthropic bill by 40–60% in 5 minutes (self-hosted Rust gateway)

Hi [Founder / CTO Name],

Noticed [Company] runs heavy LLM workflows in production. Most teams I talk to burn 40–65% of their OpenAI/Anthropic bill on repeated system prompts, near-identical agent loops, and unguarded retries — plus risk leaking internal API keys/PII in prompts.

I built **Aegis AI Gateway** (`https://markankamaransheogarat-sys.github.io/aegis-llm-gateway/`):
- **1-command deploy** (`docker compose up -d`, single 12 MB Rust binary, zero Python/vector-DB bloat).
- **Sub-ms L1/L2 semantic cache** + **automatic secret redaction** (`sk-`, `AKIA`, `ghp_`, JWT) + **per-key daily USD caps**.
- Free Community Edition, or **$49/mo Pro / $299/mo Enterprise** (Global via Stripe/CryptoBot, or **4 900 ₽ / 29 900 ₽/мес** in RU/CIS via YooKassa & 152-FZ on-prem) with custom PII rules & SLA.

Happy to set up a 10-minute benchmark on your traffic to show exact $/month savings. Want me to send a Pro trial key?

Best,  
Konstantin (`@amadeus1827`)
