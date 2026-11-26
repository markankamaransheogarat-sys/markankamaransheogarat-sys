# B2B Go-To-Market & Outreach Playbook — `aegis-llm-gateway v0.2.0`
*Витрина и калькулятор: `https://markankamaransheogarat-sys.github.io/aegis-llm-gateway/` · Релиз: `v0.2.0`*

---

## 1. Продуктовая матрица монетизации (Global + РФ/СНГ)

| Тариф | Global (USD) | РФ & СНГ (RUB) | Что получает клиент | Канал оплаты / автовыдачи |
|---|---|---|---|---|
| **Community (OSS)** | `$0` | `0 ₽` | 12 MB Rust бинарник / Docker, L1+L2 SimHash кэш, базовый DLP/WAF, `/metrics` | GitHub Releases (`v0.2.0`) |
| **Pro / Team** | **`$49 / mo`** | **`4 900 ₽ / мес`** | Оффлайн-ключ `AEGIS-PRO-...`, per-key RPM + USD/RUB лимиты, live `/admin` UI, приоритетный фикс WAF-правил | `POST /webhooks/stripe` · `POST /webhooks/yookassa` · `POST /webhooks/cryptobot` |
| **Enterprise / 152-ФЗ** | **`$299 / mo`** | **`29 900 ₽ / мес`** | Ключ `AEGIS-ENTERPRISE-...`, on-prem установка за корпоративный периметр (GigaChat / YandexGPT / vLLM), кастомные DLP-правила (ИНН/СНИЛС/паспорта/секреты), SLA | Договор / инвойс / СБП юрлица + оффлайн-генерация ключа (`aegis license issue`) |

---

## 2. Целевые B2B-компании и AI-проекты (проверены на GitHub / Web)

### A. РФ и СНГ (фокус: 152-ФЗ, 1С/бизнес-данные, GigaChat/YandexGPT + экономия на OpenAI/Anthropic)

| # | Проект / Команда | Масштаб | Боль, которую закрывает `aegis-llm-gateway` | Контакт / Площадка |
|---|---|---|---|---|
| 1 | **1С + MCP (`feenlace/mcp-1c`)** | `261★` · Go · `feenlace.ru` | Разработчики и компании на 1С подключают AI к базам/конфигурациям — критичен риск утечки ключей/ПДн и повторный контекст | `https://feenlace.ru` · `github.com/feenlace/mcp-1c` *(связка `aegis-llm-gateway` + `mcp-guard`)* |
| 2 | **AI Frontier / `humanizer-ru`** | `618★` · `humanizer-ru.aifrontier.tech` | Массовая обработка русского текста через LLM API — высокий чек на токены, нужен семантический кэш и RPM-лимитинг | `https://humanizer-ru.aifrontier.tech/` · `github.com/ilyautov/humanizer-ru` |
| 3 | **Chibi Bot (`s-nagaev/chibi`)** | `57★` · `chibi.bot` | Self-hosted Telegram-оркестратор нескольких LLM провайдеров — нужны per-user RPM/бюджет квоты и биллинг подписок | `https://chibi.bot` · `github.com/s-nagaev/chibi` |
| 4 | **Telegram LLM боты (`SirChatalot` и др.)** | Open-source AI боты | Повторяющиеся системные промпты и защита от злоупотребления ключом без написания своего прокси | `github.com/sazonovanton/SirChatalot` |
| 5 | **Интеграторы 1С / FinTech / LegalTech в РФ (из раздела вакансий)** | Enterprise / SaaS | Корпоративные ассистенты на GigaChat / YandexGPT / гибриде OpenAI с требованием 152-ФЗ и безналом по РФ | Прямой питч CTO / Tech Lead после техсобесов |

### B. Global Remote / AI SaaS & Agent Teams (фокус: `-40–70%` LLM API чек, DLP утечек ключей, Stripe / Crypto)

| # | Проект / Команда | Масштаб | Боль, которую закрывает `aegis-llm-gateway` | Контакт / Площадка |
|---|---|---|---|---|
| 1 | **Switch AI (`sandbox-quantum/switch`)** | `4,818★` · `switchagents.ai` | AI-тиммейты в Slack/Teams/Telegram с Claude Code — многопоточные циклы сжигают бюджет и могут светить корпоративные секреты в промптах | `https://www.switchagents.ai` · `github.com/sandbox-quantum/switch` |
| 2 | **Oracle (`steipete/oracle`)** | `4,077★` · `askoracle.sh` | Передача крупных контекстов и файлов в GPT-5 Pro / OpenAI — идеальная точка для DLP-очистки `.env`/API-ключей и кэширования контекста | `https://askoracle.sh` · `github.com/steipete/oracle` |
| 3 | **GoClaw (`nextlevelbuilder/goclaw`)** | `3,723★` · Go · `goclaw.sh` | Мультитенантная агентная платформа с 5 слоями изоляции — `aegis-llm-gateway` как внешний DLP + L1/L2 LLM firewall & billing plane | `https://goclaw.sh` · `github.com/nextlevelbuilder/goclaw` |
| 4 | **CascadeFlow (`lemony-ai/cascadeflow`)** | `3,921★` · `cascadeflow.ai` | Снижение стоимости и латентности агентных запросов — совместимость с внешним L1/L2 кэш-шлюзом на Rust | `https://cascadeflow.ai` · `github.com/lemony-ai/cascadeflow` |
| 5 | **Acontext (`memodb-io/Acontext`)** | `3,697★` · `acontext.io` | Слой памяти для агентных скиллов — защита от prompt-injection и утечек секретов + контроль RPM | `https://acontext.io` · `github.com/memodb-io/Acontext` |

---

## 3. Готовые B2B-питчи (RU + EN)

### 1) Питч под РФ-рынок (1С, SaaS, агентские команды, 152-ФЗ)
> Привет, [Имя]!
>
> Увидел ваш проект **[Название]** — круто решаете [конкретная задача проекта]. Когда команды гоняют [1С-конфигурации / пользовательские запросы / Telegram-трафик] в LLM API, обычно сразу вылезают две проблемы:
> 1. **Утечки секретов и ПДн** (ключи, токены, телефоны/ФИО уходят во внешние модели в сыром виде — риск по 152-ФЗ).
> 2. **Перерасход бюджета** на однотипные системные промпты и циклы агентов + отсутствие per-user лимитов RPM.
>
> Я написал лёгкий self-hosted шлюз на Rust (**`aegis-llm-gateway v0.2.0`**, один бинарник 12 МБ / `docker compose up -d`), который ставится за 2 минуты перед OpenAI, Anthropic, GigaChat, YandexGPT или локальным vLLM/Ollama:
> - вырезает ключи и ПДн до отправки запроса наружу + блокирует prompt-injection (`403`);
> - режет чек на токены на 40–60% за счёт субмиллисекундного L1 (SHA-256) + L2 (SimHash) кэша;
> - даёт live-панель `/admin`, RPM/USD лимиты и автовыдачу лицензий через **ЮKassa / CryptoBot**.
>
> Витрина и калькулятор экономии: https://markankamaransheogarat-sys.github.io/aegis-llm-gateway/
> Могу развернуть вам тестовый стенд на вашем трафике за 10 минут и выдать Pro-ключ на тест (`4 900 ₽/мес` или Enterprise on-prem с 152-ФЗ за `29 900 ₽/мес`). Актуально?

### 2) Питч под Global AI Startups / Agent Builders (EN)
> Hey [Name],
>
> Big fan of **[Project / Company]** ([site/repo]). Running multi-step LLM/Claude/GPT workflows at scale usually burns **40–65% of API spend** on repeated system prompts & retry loops—and carries the constant risk of an engineer's `.env` / `sk-` / `AKIA` key leaking into an upstream prompt.
>
> I built **Aegis AI Gateway (`v0.2.0`)** — a 12 MB `#![forbid(unsafe_code)]` Rust drop-in proxy (`http://localhost:8080/v1`, `docker compose up -d`):
> - **L1 SHA-256 + L2 SimHash-64 semantic cache** with real-time SSE stream tee/replay;
> - **Outbound DLP scrubbing** + **prompt-injection WAF** (`403`) + **per-key RPM (`429`) & daily USD caps**;
> - **Live `/admin` dashboard**, Prometheus `/metrics`, and automated **Stripe / CryptoBot** license provisioning.
>
> Live ROI calculator & docs: https://markankamaransheogarat-sys.github.io/aegis-llm-gateway/
> Happy to share a complimentary Pro license key (`$49/mo` tier) to benchmark your exact token savings in 10 minutes. Interested?

---

## 4. Чек-лист запуска платного приёма за 15 минут (как принимать деньги уже сегодня)

1. Поднять один VPS (`1 vCPU / 1 GB RAM`, ~5 €/мес) и запустить `aegis-llm-gateway v0.2.0` с реальными секретами:
   ```bash
   export AEGIS_LICENSE_SECRET="<random-32-byte-secret>"
   export AEGIS_WEBHOOK_SECRET="<random-webhook-secret>"
   export AEGIS_MAX_RPM=120
   aegis-llm-gateway serve --bind 0.0.0.0:8080 --upstream https://api.openai.com
   ```
2. Поставить перед ним Caddy/Nginx с HTTPS и пробросить webhook в платёжках:
   - **РФ (рубли / СБП):** ЮKassa webhook → `https://<domain>/webhooks/yookassa` (заголовок `X-Aegis-Webhook-Secret`).
   - **Крипта (USDT / TON):** `@CryptoBot` Pay webhook → `https://<domain>/webhooks/cryptobot`.
   - **Global (USD карты):** Stripe `checkout.session.completed` → `https://<domain>/webhooks/stripe`.
3. В [`docs/index.html`](https://markankamaransheogarat-sys.github.io/aegis-llm-gateway/) при появлении боевой платёжной ссылки заменить `mailto:` / GitHub Issue CTA на прямую оплату Stripe / ЮKassa / CryptoBot.
