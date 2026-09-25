User is building 'Olympian AI' — a Telegram AI agent ecosystem with 14 Greek god-themed agents (Zeus, Athena, Hermes, Plutus, Poseidon, Ares, Argus, Apollo, Dionysus, Calliope, Aphrodite, Demeter, Hephaestus, Nyx) organized into 5 divisions (Intelligence, Finance & Crypto, Media Factory, Digital Business, Technology) with 5 revenue engines and a CFO system. Goal: build a revenue-generating digital business where AI handles operations and user acts as Owner.
§
Technical stack decided: Python 3.11+, aiogram 3.x, SQLAlchemy 2.0 async (SQLite → PostgreSQL), Pydantic Settings v2, loguru, apscheduler, httpx, OpenRouter for LLM (Claude 3.5 Sonnet for planning), Replicate/Fal.ai for image/video gen, Redis from Phase 0, uv package manager, Docker Compose for deployment. Telegram bot uses polling initially, webhook later. User-facing language: Bahasa Indonesia.
§
User has existing Telegram projects: @SinyalEntryCrypto and a trading scanner bot. These will be integrated as modules in the Olympian ecosystem. Token security: never reuse exposed tokens, regenerate via BotFather, store only in .env.
§
User prefers step-by-step phased building (Phase 0 Foundation → Phase 1 Zeus → Phase 2 Athena+Hermes → Phase 3 Plutus CFO → Phase 4 Poseidon+Ares+Argus → Phase 5 Content Factory → Phase 6 Aphrodite → Phase 7 Demeter → Phase 8 Automated Business → Phase 9 Owner Dashboard → Phase 10 Owner Mode). Each phase must produce runnable code, not just diagrams.
§
Obsidian vault for memory/knowledge management set up at ~/Obsidian/Olympian-AI-Memory/ with Git version control and auto-sync from Hermes memory via systemd timer (every 15 min). CLI scripts created: obsidian-daily.sh, obsidian-search.sh, obsidian-append.sh, sync-hermes-to-obsidian.sh.
§
Next immediate step: Phase 0 Foundation (project scaffolding, docker-compose, config, CI).