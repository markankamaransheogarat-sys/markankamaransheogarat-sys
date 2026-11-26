# Senior / Staff Job Hunt & Outreach Playbook (Global Remote + РФ/СНГ)
*Дата актуализации: 2026-11-26 · Все ссылки проверены напрямую через API Ashby, Greenhouse и Хабр Карьеры*

Прикрепляемые резюме:
- **Global (EN):** `RESUME_EN.pdf` (`markankamaransheogarat-sys/resumes/RESUME_EN.pdf`)
- **РФ / СНГ (RU):** `RESUME_RU.pdf` (`markankamaransheogarat-sys/resumes/RESUME_RU.pdf`)
- **GitHub / Витрина:** `https://github.com/markankamaransheogarat-sys` · `https://markankamaransheogarat-sys.github.io/aegis-llm-gateway/`

---

## 1. TOP PRIORITY — Global Remote / EMEA (Ashby & Greenhouse)

| # | Компания | Позиция | Локация / Формат | Стек и фокус | Чем бьём точно в цель (твои проекты/PR) | Ссылка на отклик |
|---|---|---|---|---|---|---|
| 1 | **Supabase** | **Software Engineer - AI Tooling Infrastructure** | `Remote, Global` | Backend-сервисы под AI-продукты и production **Supabase MCP server**, agent skills | **`mcp-guard v0.2.0`** (MCP proxy/WAF, `tools/list` filter, path-jail, SSRF), **`aegis-llm-gateway v0.2.0`**, **`llm-cache-edge v0.1.0`**, `TabularisDB` MCP PRs | [Податься (Ashby)](https://jobs.ashbyhq.com/supabase/fb0b563a-e541-43fd-8555-9eb6473aaa11) |
| 2 | **Supabase** | **AI Platform Engineer** | `Remote, Global` | Execution layer для внутренних AI-систем и надёжная оркестрация | **`aegis-llm-gateway v0.2.0`**, **`go-outbox-dispatcher`** (`FOR UPDATE SKIP LOCKED`), **`go-sse-gateway`**, `OpenSandbox` PR | [Податься (Ashby)](https://jobs.ashbyhq.com/supabase/3b5d54ca-741b-45ac-bd3f-31605a0d3541) |
| 3 | **Supabase** | **Product Security Engineer** | `Remote, Global` | Product/AppSec, shift-left security, безопасная инфраструктура | **`mcp-guard v0.2.0`**, **`dep-xray v0.2.0`** (AST supply-chain SARIF), **`OpenAI codex-security`** PRs, `OpenSandbox` symlink-escape PR | [Податься (Ashby)](https://jobs.ashbyhq.com/supabase/62ad3b86-3a18-435a-ab29-dc62b77154e5) |
| 4 | **Inferact** *(создатели vLLM)* | **Member of Technical Staff, Exceptional Generalist** | `Remote` (Worldwide) | Весь стек **vLLM** от распределённых систем до низкоуровневого inference | **`tensor-gateway-rs`** (PagedAttention, CoW, Radix prefix cache, Orca batching), **`llm-cache-edge v0.1.0`**, `Leonida` SPIR-V/GPU PRs | [Податься (Ashby)](https://jobs.ashbyhq.com/inferact/f0d2619d-28e0-4b25-8d30-3ac555071abb) |
| 5 | **Poolside** | **Member of Engineering (Inference Infrastructure)** | `Remote (EMEA)` | Масштабирование inference-инфраструктуры (Go, K8s, distributed systems) | **`tensor-gateway-rs`**, **`aegis-llm-gateway v0.2.0`**, **`go-sse-gateway`**, **`go-outbox-dispatcher`** | [Податься (Ashby)](https://jobs.ashbyhq.com/poolside/1f2a733a-a3fe-48fe-bf61-1425eddb30f6) |
| 6 | **Poolside** | **Member of Engineering (Infrastructure)** | `Remote (EMEA)` | Облачная и распределённая инфраструктура | **`go-outbox-dispatcher`**, **`go-sse-gateway`**, `Mozilla neqo` PRs, **`aegis-llm-gateway v0.2.0`** | [Податься (Ashby)](https://jobs.ashbyhq.com/poolside/ade02c95-890f-4f1d-9ca6-05076b6fe687) |
| 7 | **Blockstream** | **Rust-Simplicity Maintainer** | `Remote` | Rust, Simplicity, Bitcoin/Liquid core & tooling | Местная специализация в Rust (`#![forbid(unsafe_code)]`), `dep-xray`, `neqo` + готовый черновик письма в scratch | [Податься (Ashby)](https://jobs.ashbyhq.com/blockstream/6d5c33ed-e473-4e1f-a19e-cde337d66eaa) |
| 8 | **Blockstream** | **Security Architect** | `Remote` | Архитектура безопасности, threat modeling, Rust/systems | **`mcp-guard v0.2.0`**, **`dep-xray v0.2.0`**, **`aegis-llm-gateway v0.2.0`**, `OpenSandbox` & `codex-security` PRs | [Податься (Ashby)](https://jobs.ashbyhq.com/blockstream/5944eb5a-4d26-459d-9de9-d8ba5f12cd62) |
| 9 | **Nebius** | **Senior SRE — Token Factory (Inference Platform)** | `Remote - Europe` / EU | Token Factory, high-load inference platform | **`aegis-llm-gateway v0.2.0`**, **`tensor-gateway-rs`**, **`llm-cache-edge v0.1.0`**, Prometheus/Grafana observability | [Податься (GH)](https://careers.nebius.com/?gh_jid=4600919101) |
| 10 | **Nebius** | **Senior Infrastructure (Cloud) Security Engineer** | `Remote - Europe` | Облачная и инфраструктурная безопасность | **`mcp-guard v0.2.0`**, **`dep-xray v0.2.0`**, **`aegis-llm-gateway v0.2.0`**, `OpenSandbox` symlink fix | [Податься (GH)](https://careers.nebius.com/?gh_jid=5048246101) |
| 11 | **Lightning AI** | **Senior Infrastructure Software Engineer** | `Remote` | Облачная/GPU инфраструктура, Python/Go/Rust | **`tensor-gateway-rs`**, **`llm-cache-edge v0.1.0`**, **`go-outbox-dispatcher`**, Colab T4 GPU harness в `Leonida` | [Податься (GH)](https://job-boards.greenhouse.io/lightningai/jobs/7980765003) |
| 12 | **Together AI** | **AI Infrastructure Systems Engineer** | `Amsterdam` *(релокация/EU)* | Системный инжиниринг inference & fleet (Python, Go, Rust, K8s) | **`tensor-gateway-rs`**, **`llm-cache-edge v0.1.0`**, **`aegis-llm-gateway v0.2.0`** | [Податься (GH)](https://job-boards.greenhouse.io/togetherai/jobs/4555544007) |

---

## 2. TOP PRIORITY — РФ / СНГ & EU Remote (Хабр Карьера + Прямые фильтры)

| # | Компания | Позиция | Формат и вилка | Стек | Чем бьём | Ссылка |
|---|---|---|---|---|---|---|
| 1 | **Vital Partners** | **Go Architect / Solution Architect** | Удалённо · **до 8 000 €** | `Golang`, архитектура highload-систем | **`go-outbox-dispatcher`**, **`go-sse-gateway`**, **`aegis-llm-gateway v0.2.0`**, **`subrelay`** | [Хабр Карьера](https://career.habr.com/vacancies/1000168197) |
| 2 | **Джетлин** | **ML developer + GO** | Удалённо | `Golang`, `LLM`, `Python`, `gRPC` | **`aegis-llm-gateway v0.2.0`**, **`llm-cache-edge v0.1.0`**, **`go-sse-gateway`**, **`geo-dmp-engine`** | [Хабр Карьера](https://career.habr.com/vacancies/1000169171) |
| 3 | **Джетлин** | **AppSec-инженер / Исследователь безопасности ПО (Senior)** | Удалённо | AppSec, AST/supply-chain, Web/API security | **`dep-xray v0.2.0`**, **`mcp-guard v0.2.0`**, PRs в `OpenAI codex-security` & `OpenSandbox` | [Хабр Карьера](https://career.habr.com/vacancies/1000169623) |
| 4 | **Базис** | **Системный архитектор SDN** | Москва · **до 500 000 ₽** | `Golang`, сетевые/распределённые системы | **`go-sse-gateway`**, **`go-outbox-dispatcher`**, **`Mozilla neqo`** (QUIC/HTTP3), **`aegis-llm-gateway`** | [Хабр Карьера](https://career.habr.com/vacancies/1000167247) |
| 5 | **RWB** | **Golang Tech Lead в Корпоративный портал** | Удалённо | `Golang`, архитектура, highload | **`go-outbox-dispatcher`**, **`go-sse-gateway`**, **`aegis-llm-gateway v0.2.0`** | [Хабр Карьера](https://career.habr.com/vacancies/1000169525) |
| 6 | **RWB** | **Golang-разработчик в команду Рекламной платформы** | Москва | `Golang`, `ClickHouse`, `Kafka`, `PostgreSQL`, Highload | **`geo-dmp-engine`** (OOH/AdTech analytics, asyncpg/PostgreSQL), **`go-outbox-dispatcher`** | [Хабр Карьера](https://career.habr.com/vacancies/1000170103) |
| 7 | **Яндекс** | **Старший LLM-разработчик в сервис Нейроюрист** | Удалённо | `Python`, `NLP`, `LLM`, `Langgraph` | **`aegis-llm-gateway v0.2.0`**, **`llm-cache-edge v0.1.0`**, **`mcp-guard v0.2.0`** | [Хабр Карьера](https://career.habr.com/vacancies/1000164856) |
| 8 | **Top Selection** | **AI исследователь** | Удалённо · **260 000 – 300 000 ₽** | `Python`, `NLP`, `LLM`, `LangChain`, `SQL` | **`aegis-llm-gateway`**, **`llm-cache-edge`**, **`geo-dmp-engine`**, **`deadhead-dispatcher`** | [Хабр Карьера](https://career.habr.com/vacancies/1000168339) |

**Живые поисковые ленты для ежедневного дожима:**
- hh.ru Senior Rust (удалённо): `https://hh.ru/search/vacancy?text=Rust&experience=between3And6&experience=moreThan6&schedule=remote`
- hh.ru Senior Golang Highload (удалённо): `https://hh.ru/search/vacancy?text=Golang+Highload&experience=between3And6&experience=moreThan6&schedule=remote`
- RustJobs.dev / TopGenAIJobs: `https://rustjobs.dev/` · `https://topgenaijobs.com/`

---

## 3. Готовые персонализированные сопроводительные письма (Copy-Paste)

### A. Supabase — *Software Engineer, AI Tooling Infrastructure* (`Remote, Global`)
> Hi Supabase AI Tooling team,
>
> Seeing that your team runs the **Supabase MCP server** and agent tooling in production makes this role an unusually direct match for what I have built over the last few months:
> - **`mcp-guard` (`v0.2.0`)**: An open-source `#![forbid(unsafe_code)]` Rust security firewall and capability proxy for MCP servers (`stdio`/SSE/HTTP), enforcing path-jails (anti-symlink escape), DNS-rebinding/SSRF checks, JSON-RPC batch filtering, `tools/list` schema controls, and streaming secret redaction (`github.com/markankamaransheogarat-sys/mcp-guard`).
> - **`aegis-llm-gateway` (`v0.2.0`) & `llm-cache-edge` (`v0.1.0`)**: Sub-ms L1/L2 SimHash LLM reverse proxies with outbound DLP scrubbing, prompt-injection WAF, per-key RPM/USD caps, live `/admin` plane, and automated Stripe/webhook license provisioning.
> - **OSS Track Record**: Active contributor to **TabularisDB** (including MCP parameter/SSH fixes in `#1660`), **OpenAI `codex-security`**, **OpenSandbox** (symlink-escape fix in `#2391`), and **Mozilla `neqo`**.
>
> My 1-page resume (`RESUME_EN.pdf`) is attached. Happy to dive into MCP sandboxing, agent reliability, or gateway scaling anytime.
>
> Best,  
> Konstantin (`@amadeus1827` · `markankamaransheogarat@gmail.com`)

### B. Inferact — *Member of Technical Staff, Exceptional Generalist* (`Remote`) / Poolside (*Inference Infrastructure*)
> Hi Inferact / Poolside team,
>
> I'm a Systems & AI Infrastructure Engineer focused on squeezing maximum throughput and predictability out of LLM serving and distributed Rust/Go runtimes:
> - **`tensor-gateway-rs`**: Implemented Orca-style iteration continuous batching, a **PagedAttention** 16-token physical block allocator with Copy-on-Write sharing, and **Radix prefix caching** (`9,400+ tok/s`, `P50 TTFT: 2.24ms`, `P50 ITL: 1.00ms`).
> - **`llm-cache-edge` (`v0.1.0`) & `aegis-llm-gateway` (`v0.2.0`)**: Sub-ms L1 (`178 ns`) / L2 SimHash (`1.72 µs`) semantic reverse proxy with zero-copy SSE stream tee/replay and bounded LRU/TTL eviction (`4.64M tok/s` benchmarked with Criterion).
> - **Low-level GPU / Systems OSS**: Built automated Tesla T4 headless Vulkan/SPIR-V verification harnesses and toolchain fixes in **Leonida** (`#908`, `#909`, `#910`, `#995`), plus merged QUIC/HTTP3 PRs in **Mozilla `neqo`**.
>
> Resume attached (`RESUME_EN.pdf`). I work asynchronously across US/EU time zones and would love to discuss inference engine/runtime bottlenecks you're tackling next.
>
> Best,  
> Konstantin (`github.com/markankamaransheogarat-sys`)

### C. Nebius (`Remote - Europe`) / Blockstream (`Remote`) — *Security & Systems Infra*
> Hi [Team / Hiring Manager],
>
> Sharing my application for **[Role Name]**:
> - **AI & Cloud Security Tooling**: Built **`mcp-guard` (`v0.2.0`)** (anti-SSRF/DNS-rebinding, symlink-escape jail, output sanitization), **`dep-xray` (`v0.2.0`)** (`tree-sitter` AST supply-chain diffing with SARIF 2.1.0), and **`aegis-llm-gateway` (`v0.2.0`)** (`#![forbid(unsafe_code)]` DLP + prompt-injection WAF + RPM rate limiting).
> - **Security OSS Contributions**: Submitted patches to **OpenAI `codex-security`** (`#2711`, `#2717`), **OpenSandbox** (`#2391` symlink escape in execd), and **Mozilla `neqo`** (QUIC transport in Rust).
> - *(For Blockstream Rust-Simplicity, combine with `/root/.gemini/antigravity-cli/scratch/blockstream_rust_simplicity_cover_letter.md`)*
>
> Attached `RESUME_EN.pdf`. Happy to walk through architecture and threat-model tradeoffs on a call.
>
> Best,  
> Konstantin (`markankamaransheogarat@gmail.com`)

### D. Джетлин (`ML developer + GO` / `AppSec Senior`) / Vital Partners (`Go Architect`) / RWB (`Golang Tech Lead`)
> Здравствуйте!
>
> Откликаюсь на позицию **[Название вакансии]**. Специализируюсь на высоконагруженных системах на **Go / Rust**, инфраструктуре вокруг **LLM** и **AppSec**:
> - **Go High-Load & Архитектура**: спроектировал **`go-outbox-dispatcher`** (транзакционный outbox на `pgx` с `FOR UPDATE SKIP LOCKED`, circuit breaker и Prometheus) и **`go-sse-gateway`** (zero-alloc SSE/HTTP прокси с 64-шардовым rate limiter и атомарным failover).
> - **LLM-инфраструктура на практике**: **`aegis-llm-gateway` `v0.2.0`** и **`llm-cache-edge` `v0.1.0`** — прокси-шлюз перед LLM с L1/L2 семантическим кэшем, DLP-редакцией секретов и ПДн (152-ФЗ), WAF от prompt-injection, RPM/бюджет-лимитами и автобиллингом (ЮKassa / Stripe / CryptoBot).
> - **AdTech / Аналитика / AppSec** *(под RWB / Джетлин AppSec)*: **`geo-dmp-engine`** (OTS/Reach на сыром `asyncpg` и PostgreSQL) + **`dep-xray` `v0.2.0`** (AST-анализ зависимостей на `tree-sitter` с выгрузкой SARIF 2.1.0) и **`mcp-guard` `v0.2.0`**, а также PR в **OpenAI `codex-security`**, **OpenSandbox** и **Mozilla `neqo`**.
>
> Резюме (`RESUME_RU.pdf`) прикрепил, весь код, тесты и бенчмарки открыты на GitHub (`github.com/markankamaransheogarat-sys`). Буду рад пообщаться на техническом интервью!
>
> Константин · Telegram: `@amadeus1827` · Email: `markankamaransheogarat@gmail.com`

---

## 4. Тактический план откликов (чтобы дойти до оффера)

1. **День 1 (сегодня — горячая десятка):**
   - Global: податься в **Supabase** (все 3 роли: `AI Tooling`, `AI Platform`, `Product Security`), **Inferact**, **Poolside** (2 роли), **Blockstream** (2 роли — для `Rust-Simplicity` использовать заготовку [`blockstream_rust_simplicity_cover_letter.md`](file:///root/.gemini/antigravity-cli/scratch/blockstream_rust_simplicity_cover_letter.md)), **Nebius** (`Token Factory SRE` + `Cloud Security`). Прикладывать `RESUME_EN.pdf` + 3-строчный персональный питч выше.
   - РФ/Европа: податься на Хабр Карьере в **Vital Partners** (`до 8000 €`), **Джетлин** (`ML + GO` и `AppSec Senior`), **RWB** (`Golang Tech Lead`), **Базис** (`до 500 000 ₽`), **Яндекс** (`Нейроюрист`). Прикладывать `RESUME_RU.pdf`.
2. **День 2–3 (прямой дожим через ЛПР):**
   - По каждому отклику в Ashby/Greenhouse найти в LinkedIn/X **Engineering Manager / CTO / Founder** компании (например, founders Inferact / Poolside / Supabase AI team) и отправить короткий DM на 4–5 строк со ссылкой на `github.com/markankamaransheogarat-sys` и `aegis-llm-gateway` live demo.
3. **Чек-лист перед интервью:**
   - Держать открытыми архитектуру **`aegis-llm-gateway v0.2.0`**, **`mcp-guard v0.2.0`**, **`tensor-gateway-rs`** и **`go-outbox-dispatcher`** — по ним легче всего вести систем-дизайн интервью на уровне Staff/Senior.
