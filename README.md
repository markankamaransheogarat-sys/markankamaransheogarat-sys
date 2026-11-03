<div align="center">

# Konstantin
### Staff Systems, High-Load Infrastructure & AI Platform Architect
**Specializing in high-throughput distributed systems, low-latency Rust/Python platforms, LLM inference architectures, and zero-overhead networking.**

[![Telegram](https://img.shields.io/badge/Telegram-@amadeus1827-26A5E4?logo=telegram&logoColor=white)](https://t.me/amadeus1827)
[![Audited by](https://img.shields.io/badge/Audited%20by-Mozilla%20%7C%20Linux%20Foundation-black?logo=linux&logoColor=white)](#-selected-upstream-contributions)
[![Merged PRs](https://img.shields.io/badge/Merged%20PRs-25+-2ea44f?logo=git&logoColor=white)](#-selected-upstream-contributions)
[![Live Platform](https://img.shields.io/badge/Live%20Terminal-subtext24.com-E02424?logo=statuspage&logoColor=white)](https://subtext24.com)
[![Live Demos](https://img.shields.io/badge/Live%20Demos-WASM%20Canvas-4fd1c5?logo=webassembly&logoColor=white)](#-live-interactive-playgrounds-webassembly)
<br>
[![LLM Inference](https://img.shields.io/badge/LLM%20Inference-9.4k%20tok%2Fs%20%7C%20Orca%20Batcher-blueviolet?logo=rust&logoColor=white)](#-high-performance-ai-platform--inference-infrastructure)
[![Broker Routing](https://img.shields.io/badge/Broker%20Routing-145k%20msg%2Fs%20%7C%206.8%C2%B5s-orange?logo=apachekafka&logoColor=white)](#-high-load-distributed-brokers--offline-first-state-engines)
[![Columnar Engine](https://img.shields.io/badge/Columnar%20Ingestion-1.5M%20ord%2Fs-008080?logo=clickhouse&logoColor=white)](#-high-load-distributed-brokers--offline-first-state-engines)
[![Safety Standard](https://img.shields.io/badge/Zero--Unsafe-100%25-brightgreen)](#-algorithmic-reincarnations--physics-webassembly)

</div>

---

## ⚡ Proof, not promises

**25+ merged pull requests into Tier-1 open-source repositories**, audited and accepted by upstream maintainers:

| Ecosystem / Organization | Domain & Track Record |
| :--- | :--- |
| **[Mozilla neqo](https://github.com/mozilla/neqo)** · 2.2k★ | Firefox's QUIC / HTTP/3 stack in Rust |
| **[OpenRig](https://github.com/mvschwarz/openrig)** · 8k★ | Multi-agent autonomous orchestrator CLI |
| **[Tabularis](https://github.com/TabularisDB/tabularis)** · 5k★ | Desktop SQL workspace (Tauri v2, Rust, React): **8+ merged features & scheduler** |
| **[Hiero JS SDK](https://github.com/hiero-ledger/hiero-sdk-js)** · LF Decentralized Trust | Linux Foundation Decentralized Trust SDK: test harnesses & API fixes |
| **[OpenSandbox](https://github.com/opensandbox-group/OpenSandbox)** | High-density secure agent sandboxing: WebSocket lifecycle takeover fixes |

---

## 🚀 Flagship Systems & Distributed Platforms

### 1. High-Performance AI Platform & Inference Infrastructure
- **[`tensor-gateway-rs`](https://github.com/markankamaransheogarat-sys/tensor-gateway-rs)** `[Rust · Tokio · 9,400+ tok/s · PagedAttention]`  
  High-throughput distributed LLM streaming inference gateway & continuous dynamic batcher.
  - **Orca-Style Iteration Batching**: Dynamic token-level scheduling merging prefill and decode phases in microsecond steps.
  - **PagedAttention Virtual Memory**: 16-token physical block allocator, Copy-on-Write (CoW) page sharing, and GPU↔Host RAM swapping.
  - **Radix Prefix Caching**: Instant zero-compute reuse of shared prompt blocks via Trie hash matching.
  - **Production Guardrails**: Token Bucket rate limiter, Memory Circuit Breaker (95% high watermark), sub-millisecond SSE streaming (`P50 TTFT: 2.24ms`, `P50 ITL: 1.00ms`).
- **[`cortex-agent-rag`](https://github.com/markankamaransheogarat-sys/cortex-agent-rag)** `[Python 3.10+ · Zero-Dep · 0.01ms Cache]`  
  Production Multi-Agent Hybrid RAG engine with sub-millisecond semantic caching and self-correcting guardrails.
  - **Hybrid Sparse/Dense Search**: Exact BM25Okapi inverted index fused with normalized cosine vector search via Reciprocal Rank Fusion (RRF $k=60$).
  - **Two-Stage Reranking**: Cross-Encoder relevance scoring with length and exact-term coverage penalties.
  - **Vectorized Semantic Cache**: Sub-millisecond ($0.01\text{ ms}$) hit response with cosine threshold gating ($> 0.92$).
  - **Self-Correcting Multi-Agent Loop**: `HallucinationCriticAgent` verifying numeric claims, dates, and grounding before response emission.

### 2. High-Load Distributed Brokers & Offline-First State Engines
- **[`synapse-chat-core`](https://github.com/markankamaransheogarat-sys/synapse-chat-core)** `[Rust · Tokio · Kotlin Coroutines · RFC 2026-SYN-01]`  
  High-concurrency distributed chat broker & offline-first CRDT state synchronization engine (Wildberries & Windi architecture).
  - **Broker Throughput**: Benchmarked at **145,294 msg/sec** with **6.88 µs** routing latency on pure Tokio channels.
  - **Binary Wire Protocol RFC 2026-SYN-01**: Compact 17-byte header with magic `0x53594E31`, CRC-32 integrity, variable payload compression.
  - **Offline-First Multiplatform CRDT**: Vector Clock causal ordering, LWW-Element-Set (Last-Write-Wins), and PN-Counters (State-based conflict-free convergence).
- **[`market-columnar-engine`](https://github.com/markankamaransheogarat-sys/market-columnar-engine)** `[Python 3.10+ · Raw SQL · ClickHouse · 1.56M ord/s]`  
  High-throughput marketplace columnar ingestion pipeline & real-time analytics engine (Тензор Saby & Nepsell architecture).
  - **Zero-ORM Raw SQL Engine**: Zero reflection overhead utilizing parameterized batch queries via `asyncpg`.
  - **ClickHouse Analytics**: `ReplacingMergeTree` for idempotent deduplication, `SummingMergeTree` for real-time aggregations, and streaming `Materialized Views`.
  - **Ingestion Velocity**: **1,563,986 orders/sec** batch ingestion with sub-second analytical window rollups.

### 3. Quantitative Finance & High-Frequency Radars
- **[`aevum-intent-solver`](https://github.com/markankamaransheogarat-sys/aevum-intent-solver)** `[Rust · Tokio · 1.2M cycles/s]`  
  Sub-microsecond cross-DEX cyclic arbitrage & MEV intent solver engine. Constant-product & concentrated liquidity AMMs (Uniswap v2/v3, Curve), negative log-cycle Bellman-Ford solver, in-memory mempool simulation.
- **[`bounty-sniper-rs`](https://github.com/markankamaransheogarat-sys/bounty-sniper-rs)** `[Rust · Tokio · 24/7 Engine]`  
  Sub-second GitHub issue scanner & bounty verification radar. Deduplicates PR race conditions, parses reward escrows, and dispatches real-time Telegram alerts.
- **[`memetic-radar-rs`](https://github.com/markankamaransheogarat-sys/memetic-radar-rs)** `[Rust · Actix · WebSocket]`  
  Viral contagion social graph radar applying epidemiological SEIR differential equations to real-time DexScreener token sentiment.
- **[`bybit-smart-piggybank`](https://github.com/markankamaransheogarat-sys/bybit-smart-piggybank)** & **[`crypto-pulse-mcp`](https://github.com/markankamaransheogarat-sys/crypto-pulse-mcp)**  
  Automated quant risk-harvesting engines with Bollinger dip-buying guards, live order book feeds, and MCP plugins for Claude.

### 4. Zero-Trust Security, Tactical Mesh & DPI Circumvention
- **[`cyberdeck-mesh`](https://github.com/markankamaransheogarat-sys/cyberdeck-mesh)** `[Rust · BLE / Acoustic · Zero-Infra]`  
  Air-gapped acoustic & BLE mesh network for off-grid tactical operations. Ultrasonic FSK audio transport, AES-256-GCM encryption, distance-vector multi-hop routing, and terminal Cyberpunk HUD.
- **[`ghostclip`](https://github.com/markankamaransheogarat-sys/ghostclip)** `[Python · Rust · P2P · Zero-Cloud]`  
  Zero-cloud P2P universal clipboard and instant file drop between Linux, macOS, Android, and iOS over LAN/mDNS with ChaCha20-Poly1305 encryption.
- **[`pocketops`](https://github.com/markankamaransheogarat-sys/pocketops)** `[Python · Zero-Dep · Linux Sentinel]`  
  Zero-dependency Linux server sentinel & mobile Telegram HUD with authenticated command execution, disk guard, and real-time push alerts.
- **[`nodevortex`](https://github.com/markankamaransheogarat-sys/nodevortex)** `[Python · Asyncio · VLESS / Clash]`  
  High-performance proxy aggregator, TCP/TLS handshake latency benchmarker, and auto-subscription distributor.
- **[`ultradpi`](https://github.com/markankamaransheogarat-sys/ultradpi)** `[Rust · WinDivert · eBPF · RAW Sockets]`  
  Next-gen Deep Packet Inspection (DPI/TSPU) circumvention engine. 5x faster than GoodbyeDPI, mid-SNI TCP segmentation, low-TTL fake SNI hop injection, and Discord UDP voice patch.
- **[`ultradpi-android`](https://github.com/markankamaransheogarat-sys/ultradpi-android)**  
  Zero-config 1-click Android VpnService engine. Unblocks YouTube 4K, Discord & AI tools locally without remote VPN servers.

### 5. Algorithmic Reincarnations & Physics (WebAssembly)
- **[`rebirth-box2d`](https://github.com/markankamaransheogarat-sys/rebirth-box2d)** `[Rust · WASM · MIT]` · [Live Demo](https://markankamaransheogarat-sys.github.io/rebirth-box2d/)  
  Pure safe Rust reincarnation of Erin Catto's legendary Box2D-Lite. Sequential Impulses, SAT collision clipping, Baumgarte bias stabilization, zero allocations in solver loops.
- **[`rebirth-ik`](https://github.com/markankamaransheogarat-sys/rebirth-ik)** `[Rust · WASM · MIT]` · [Live Demo](https://markankamaransheogarat-sys.github.io/rebirth-ik/)  
  Complete rewrite of TheComet/ik. Multi-effector FABRIK bone-tree solver with joint limits, procedural tentacle/humanoid walkers, and analytic 2-bone solvers.
- **[`daejin-prediction-market-engine`](https://github.com/markankamaransheogarat-sys/daejin-prediction-market-engine)** · [Live Demo](https://markankamaransheogarat-sys.github.io/daejin-prediction-market-engine/)  
  Interactive bonding curve & dynamic share pricing simulator for automated prediction markets.

### 6. Autonomous Media Intelligence & News Forensics
- **[THE SUBTEXT // Forensic Narrative Terminal](https://subtext24.com/)** (`subtext24.com` · `sybtext24.com`) `[Python · FastAPI · DeepSeek AI · Autonomous 24/7 Engine]`  
  Autonomous institutional news agency and real-time narrative autopsy terminal.
  - **Live Platform**: [subtext24.com](https://subtext24.com/) · [sybtext24.com](https://sybtext24.com/)
  - **Forensic Engine**: Multi-wire automated ingestion (Reuters, Bloomberg, AP), deep narrative deconstruction uncovering PR spin vs. underlying reality, hidden financial beneficiaries, and real-time Hypocrisy Index calculation.
  - **Automated Multi-Modal Synthesis**: Generative pipeline creating dynamic OG cards, investigative infographics, automated video briefs for YouTube distribution, and instant breaking news dispatches to Telegram.
  - **Production Architecture**: Zero-human-intervention editorial pipeline operating 24/7 with strict rate limiting, SQLite/FastAPI indexing, triage queues, and sub-second edge web delivery via Cloudflare.

---

## 🎮 Live Interactive Playgrounds (WebAssembly)

Run these mathematical and physics engines directly in your browser without installation:

- 🕹️ **[rebirth-box2d Interactive Physics Simulator](https://markankamaransheogarat-sys.github.io/rebirth-box2d/)**  
  8 live physics testbeds (Pyramids, Suspension Bridges, Dominos, Teeter-Totter, Pendulums). Zero-dependency Sequential Impulses & Warm Starting in 100% `#![forbid(unsafe_code)]` Rust.
- 🦾 **[rebirth-ik Inverse Kinematics Canvas](https://markankamaransheogarat-sys.github.io/rebirth-ik/)**  
  Multi-effector FABRIK bone-tree solver with joint limits, procedural tentacle/humanoid walkers, and analytic 2-bone solvers.
- 📈 **[Daejin Prediction Market Simulator](https://markankamaransheogarat-sys.github.io/daejin-prediction-market-engine/)**  
  Interactive bonding curve & dynamic share pricing simulator.

---

## 🛠️ Core Engineering Stack

```
Systems & High-Load: Rust (Tokio, Actix, Rayon, Serde, bytes), C/C++, WebAssembly, Linux (eBPF, RAW sockets, systemd)
Distributed & Messaging: Orca Continuous Batching, PagedAttention, CRDT (Vector Clocks, LWW-Set, PN-Counter), SSE, gRPC
Databases & Storage:   ClickHouse (Replacing/SummingMergeTree, Materialized Views), PostgreSQL (Raw SQL, BRIN, Range Partitions)
AI & Inference:        BM25Okapi, Dense Embedding Vector Math, Reciprocal Rank Fusion, Cross-Encoder Reranking, Semantic Cache
Networks & Protocols:  QUIC / HTTP/3, WebSocket, TCP Mid-SNI Segmentation, Ultrasonic FSK Audio, Bluetooth Low Energy (BLE)
```

---

## 🤝 Work with me

I take fixed-scope engineering contracts and senior/staff roles where the output is deterministic, robust, and fully covered by tests:

| Domain | Deliverables |
| :--- | :--- |
| **High-Performance Rust** | Network proxies, parsers, mathematical algorithms, zero-copy engines, WASM modules |
| **Distributed & AI Platform Infrastructure** | Continuous batchers, PagedAttention memory managers, hybrid RAG systems, CRDT state sync |
| **High-Load Database & Data Pipelines** | Columnar ingestion engines (ClickHouse, PostgreSQL raw asyncpg), materialized views, high-TPS pipelines |
| **Systems & Reverse Engineering** | Protocol analysis, packet manipulation, DPI bypass, custom transport drivers |
| **HFT & Quant Automation** | Low-latency market recorders, exchange connectors (Bybit, Binance), Telegram alerting |

📩 **Direct Telegram: [@amadeus1827](https://t.me/amadeus1827)** · Superteam Earn: `jarvis-quant-agent`

---

## 📜 Selected Upstream Contributions

| Repository | What I shipped |
| :--- | :--- |
| [**TabularisDB / Tabularis**](https://github.com/TabularisDB/tabularis) · 5k★ | Scheduled database backups with DST-aware cron ([#1207](https://github.com/TabularisDB/tabularis/pull/1207)) · EXPLAIN CSV/NDJSON export ([#1184](https://github.com/TabularisDB/tabularis/pull/1184), [#1187](https://github.com/TabularisDB/tabularis/pull/1187)) · Grid undo/redo ([#1206](https://github.com/TabularisDB/tabularis/pull/1206)) · Query history pause ([#1186](https://github.com/TabularisDB/tabularis/pull/1186)) · Unix socket transport ([#1250](https://github.com/TabularisDB/tabularis/pull/1250)) |
| [**OpenSandbox**](https://github.com/opensandbox-group/OpenSandbox) | WebSocket frame collision prevention on runtime takeover ([#2378](https://github.com/opensandbox-group/OpenSandbox/pull/2378)) |
| [**Mozilla neqo**](https://github.com/mozilla/neqo) · 2.2k★ | Strict constant for PATH_CHALLENGE / PATH_RESPONSE frames ([#4116](https://github.com/mozilla/neqo/pull/4116)) |
| [**OpenRig**](https://github.com/mvschwarz/openrig) · 8k★ | Source-aware configuration parsing ([#1628](https://github.com/mvschwarz/openrig/pull/1628)) |
| [**Hiero JS SDK**](https://github.com/hiero-ledger/hiero-sdk-js) · LF Decentralized Trust | Network & Token API JSDoc fixes ([#4562](https://github.com/hiero-ledger/hiero-sdk-js/pull/4562)) · ContractInfo test harnesses ([#4570](https://github.com/hiero-ledger/hiero-sdk-js/pull/4570)) |
| [**Cypher GridPay**](https://github.com/johnephraim949-web/cypher-gridpay-contracts) | Strongly-typed `ContractError` decoder & diagnostic mapper ([#301](https://github.com/johnephraim949-web/cypher-gridpay-contracts/pull/301)) |

---

<details>
<summary>☕ Support the development / Поддержать разработку</summary>

| Network | Address |
| :--- | :--- |
| **Solana (SOL, USDC)** | `CmqpfPEXkksW7gvDRaMdKFv1vmdwupe8pBkDD8trkKwY` |
| **EVM (ETH, Base, Arbitrum)** | `0xfcef7bc3053ae9589da2c6b9084902bd9d2aa54a` |
| **Stellar (XLM, USDC)** | `GA7TXEBMEPQCLHIYCWDN7RKAO5IMRD2UV7O7TZXMEW6VZUMEXNR4XBB5` |
| **TON** | `UQBu8EMAjJhy_J-j8vTMhohn33tiubo8tnaCz76JQbMwHLtx` |
| **TRON (USDT TRC-20)** | `TPDC7YHRy72GjRh5sLGgp3tPu4uHfWq5cF` |

</details>
