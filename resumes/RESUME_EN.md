# KONSTANTIN
**Staff Systems, High-Load Infrastructure & AI Platform Architect**  
`markankamaransheogarat@gmail.com` · Telegram: `@amadeus1827` · GitHub: `github.com/markankamaransheogarat-sys` · Remote (US / EU / Global)

---

## SUMMARY
Staff-level Systems & AI Infrastructure Engineer specializing in **Rust (`#![forbid(unsafe_code)]`), Go, TypeScript, and Python** high-throughput backends, LLM cost/security gateways, distributed brokers, and supply-chain security tooling. Proven track record shipping production-grade OSS systems with cross-platform CI/CD releases and **30+ pull requests** across Tier-1 repositories (`mozilla/neqo`, `TabularisDB/tabularis`, `hiero-ledger/hiero-sdk-js`, `ubiquitarianism/leonida`, `MoonshotAI/kimi-code`, `openai/codex-security`).

---

## CORE TECHNICAL SKILLS
- **Languages**: Rust (Tokio, Axum, DashMap, Soroban SDK, Tree-sitter), Go (`pgx`, net/http, zero-alloc concurrency), Python (FastAPI, raw `asyncpg`), TypeScript / Node.js / React.
- **Infrastructure & Data**: PostgreSQL (`SKIP LOCKED`, Haversine SQL), ClickHouse (`ReplacingMergeTree`), Docker (distroless multi-stage), Prometheus, GitHub Actions CI/CD, Vulkan / SPIR-V tooling.
- **AI & Security**: L1/L2 semantic caching (SHA-256 + SimHash-64 + Sparse Cosine), SSE stream teeing, MCP firewalls, prompt-injection WAF, outbound PII/secret redaction, AST supply-chain analysis (SARIF 2.1.0).

---

## FLAGSHIP SYSTEMS & PRODUCTS

### **Aegis AI Gateway (`aegis-llm-gateway`)** · Rust, Tokio, Axum, DashMap · `v0.2.0`
*Commercial-grade AI Cost & Security Reverse Proxy (OpenAI / Anthropic / Ollama)* · `github.com/markankamaransheogarat-sys/aegis-llm-gateway`
- Engineered a `#![forbid(unsafe_code)]` drop-in LLM gateway combining an **L1 SHA-256 exact cache** and **L2 64-bit SimHash + Top-32 Sparse Cosine** semantic cache (`>= 0.95` threshold) with bounded LRU/TTL eviction and real-time SSE teeing/replay.
- Implemented an **outbound security firewall & billing control plane**: scrubs leaked credentials (`sk-`, `AKIA`, `ghp_`, JWT, PEM) before prompts leave the VPC, blocks prompt injections (`403`), enforces per-key RPM rate limits & daily USD budgets (`429`), serves live `/admin` + `/metrics`, and auto-provisions signed Pro/Enterprise licenses via Stripe, YooKassa, and CryptoBot webhooks.

### **MCP Guard (`mcp-guard`)** · Rust, Tokio, Axum, Globset · `v0.2.0`
*Local Security Firewall & Capability Sandbox for Model Context Protocol (MCP) Servers* · `github.com/markankamaransheogarat-sys/mcp-guard`
- Built a `stdio` + SSE/HTTP reverse proxy enforcing ancestor-canonicalized path-jails (anti-symlink escape), SSRF & DNS-rebinding protection, JSON-RPC batch request WAF, `tools/list` schema filtering, and streaming secret/injection sanitization (`19/19` tests, Linux/macOS releases).

### **Dep-Xray (`dep-xray`)** · Rust, Tree-sitter AST, Reqwest · `v0.2.0`
*Behavioral AST Supply-Chain Diff Analyzer (`Cargo.lock`, `package-lock.json`, `pnpm-lock.yaml`)* · `github.com/markankamaransheogarat-sys/dep-xray`
- Concurrently fetches updated registry tarballs and runs `tree-sitter` AST behavioral diffing (Rust/JS/TS) plus `Cargo.toml` manifest checks (`DX015`/`DX016` custom `build.rs` / `proc-macro`), emitting SARIF 2.1.0, PR Markdown, and `.dep-xray.toml` baseline suppressions.

### **LLM Cache Edge & Tensor Gateway (`llm-cache-edge`, `tensor-gateway-rs`)** · Rust, Tokio
- **`llm-cache-edge` `v0.1.0`**: Sub-millisecond L1 (**178 ns**) / L2 SimHash (**1.72 µs** @ 1k) semantic proxy at **4.64M tokens/s** with Criterion microbenchmarks.
- **`tensor-gateway-rs`**: Orca-style continuous batching, PagedAttention 16-token block allocator with CoW sharing, and Radix prefix caching (`9,400+ tok/s`, `P50 TTFT: 2.24ms`).

### **Go High-Concurrency Infra (`go-outbox-dispatcher`, `go-sse-gateway`)** · Go, PostgreSQL
- **`go-outbox-dispatcher`**: Transactional webhook outbox worker using `pgx` `FOR UPDATE SKIP LOCKED`, per-host circuit breakers, exponential backoff, and Prometheus metrics.
- **`go-sse-gateway`**: Zero-alloc SSE/HTTP reverse proxy with 64-shard token-bucket rate limiting and atomic upstream failover.

---

## UPSTREAM OPEN-SOURCE CONTRIBUTIONS
- **`mozilla/neqo`** (Firefox QUIC/HTTP3 in Rust) & **`hiero-ledger/hiero-sdk-js`** (Linux Foundation): Core transport & SDK fixes merged upstream.
- **`TabularisDB/tabularis`** (Tauri v2 / Rust / React SQL workspace, 5k★): **8+ merged features** + SSH per-connection user override (`#1660`, 13/13 CI checks green).
- **`ubiquitarianism/leonida`** (Xbox→PC RDNA2/D3D12→Vulkan recompilation runtime): **4 active PRs** (`#908`, `#909`, `#910`, `#995` build-time supply-chain opt-in) + headless Tesla T4 Vulkan GPU test suite telemetry (`198/249` passed).
- **`MoonshotAI/kimi-code`** (4 active PRs) & **`openai/codex-security`** (2 active PRs): Agentic CLI/SDK correctness, Windows SSH path resolution, and Anthropic tool-use lowering.
