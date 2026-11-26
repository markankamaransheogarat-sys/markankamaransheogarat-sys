# КОНСТАНТИН
**Staff / Principal Backend & High-Load Systems Architect (Rust / Go / Python / AI Infra)**  
`markankamaransheogarat@gmail.com` · Telegram: `@amadeus1827` · GitHub: `github.com/markankamaransheogarat-sys` · Удалённо / Релокация

---

## ПРОФИЛЬ
Системный и High-Load архитектор с фокусом на **высоконагруженные распределённые бэкенды, low-latency прокси и AI-инфраструктуру** на **Rust (`#![forbid(unsafe_code)]`), Go, Python (`FastAPI`/`asyncpg`) и TypeScript**. Проектирую отказоустойчивые системы с измеримой производительностью, сквозной наблюдаемостью (Prometheus) и строгими гарантиями безопасности. Автор **30+ pull requests** в крупные международные open-source проекты (`mozilla/neqo`, `TabularisDB/tabularis`, `ubiquitarianism/leonida`, `MoonshotAI/kimi-code`, `openai/codex-security`).

---

## КЛЮЧЕВОЙ СТЕК
- **Языки и рантаймы**: Rust (Tokio, Axum, DashMap, Soroban SDK, Tree-sitter), Go (`pgx`, `net/http`, zero-alloc), Python (FastAPI, `asyncpg`, ClickHouse), TypeScript / Node.js / React.
- **Хранилища и брокеры**: PostgreSQL (`FOR UPDATE SKIP LOCKED`, Haversine SQL), ClickHouse (`ReplacingMergeTree`, `SummingMergeTree`), SQLite, WebSockets / SSE.
- **Инфраструктура и AppSec**: Docker (distroless multi-stage), GitHub Actions CI/CD, Prometheus, WAF/SSRF/PII защита, анализ цепочек поставок (AST + SARIF 2.1.0).

---

## КЛЮЧЕВЫЕ СИСТЕМЫ И ПРОЕКТЫ

### **1. Высоконагруженные брокеры, БД и гео-аналитика**
- **`synapse-chat-core`** *(Rust, Tokio, CRDT)*: Распределённый чат-брокер и offline-first движок синхронизации состояний (Vector Clocks, LWW-Element-Set, PN-Counters) с бинарным протоколом **RFC 2026-SYN-01** — пропускная способность **145,294 msg/s** при задержке маршрутизации **6.88 µs**.
- **`market-columnar-engine`** *(Python, raw asyncpg, ClickHouse)*: Колоночный конвейер приёма и аналитики маркетплейс-заказов без ORM на параметризованном SQL + `ReplacingMergeTree`/`SummingMergeTree` — скорость загрузки **1,563,986 ord/s**.
- **`go-outbox-dispatcher`** *(Go, pgx, Prometheus)*: Транзакционный outbox-диспетчер вебхуков на `FOR UPDATE SKIP LOCKED` с per-host circuit breaker и экспоненциальным backoff.
- **`go-sse-gateway`** *(Go)*: Zero-alloc SSE/HTTP reverse proxy с 64-шардовым token-bucket rate limiter и атомарным failover апстримов.
- **`geo-dmp-engine`** *(Python, FastAPI, asyncpg, PostgreSQL)*: Движок гео-аудиторной OOH/Indoor аналитики (OTS, Reach, Frequency) на сыром `asyncpg` и Haversine SQL (CI с PostgreSQL 16).

### **2. AI-инфраструктура и снижение стоимости LLM API**
- **`aegis-llm-gateway` `v0.2.0`** *(Rust, Tokio, Axum)* · [Live-витрина и ROI-калькулятор](https://markankamaransheogarat-sys.github.io/aegis-llm-gateway/):
  - Промышленный шлюз перед OpenAI/Anthropic/GigaChat/Ollama: **L1 SHA-256** + **L2 64-bit SimHash & Sparse Cosine** кэш, экономия 40–70% токен-бюджета, потоковый SSE tee/replay.
  - Встроенный **WAF и control plane**: авто-редакция утечек секретов (`sk-`, `AKIA`, `ghp_`, JWT, PEM) до выхода из VPC, блокировка prompt-injection (`403`), per-key RPM rate limits + дневные USD-лимиты (`429`), live-панель `/admin`, Prometheus `/metrics` и автовыдача лицензий через Stripe / ЮKassa / CryptoBot.
- **`llm-cache-edge` `v0.1.0`** & **`tensor-gateway-rs`** *(Rust, Tokio)*: Sub-ms кэш (**178 ns** L1 / **1.72 µs** L2, **4.64M tok/s**) и inference-шлюз с continuous batching, PagedAttention и Radix prefix caching (**9,400+ tok/s**).

### **3. Информационная безопасность и FinTech / Quant**
- **`mcp-guard` `v0.2.0`** *(Rust)*: Firewall и capability-sandbox для MCP-серверов (`stdio`/SSE/HTTP): path-jail (защита от symlink escape), SSRF + DNS-rebinding фильтр, защита JSON-RPC batch-запросов, фильтрация `tools/list`, `/_mcp_guard/metrics`.
- **`dep-xray` `v0.2.0`** *(Rust, Tree-sitter AST)*: Поведенческий AST-анализатор обновлений зависимостей (`Cargo.lock`, `package-lock.json`, `pnpm-lock.yaml`) с правилами `Cargo.toml` (`DX015`/`DX016`), политикой `.dep-xray.toml` и выгрузкой SARIF 2.1.0.
- **`malcrypto-aladdin`** & **`bounty-sniper-rs` `v0.2.0`**: 24/7 граф причинно-следственных связей (Granger causality, Sharpe/Sortino, VaR, GitHub Actions Watchdog) и высокочастотный Rust-сканер баунти.

---

## OPEN-SOURCE ВКЛАД
- **`mozilla/neqo`** *(QUIC/HTTP3 на Rust)* и **`hiero-ledger/hiero-sdk-js`** *(Linux Foundation)*: принятые PR в транспортный слой и SDK.
- **`TabularisDB/tabularis`** *(Tauri v2 / Rust / React, 5k★)*: **8+ влитых фич** и доработок (включая SSH user override `#1660`, 13/13 зелёных проверок CI).
- **`ubiquitarianism/leonida`** *(RDNA2→SPIR-V, D3D12→Vulkan)*: **4 активных PR** (`#908`, `#909`, `#910`, `#995`) и GPU-телеметрия на Tesla T4 (`198/249` тестов).
- **`MoonshotAI/kimi-code`** (4 PR) и **`openai/codex-security`** (2 PR).
