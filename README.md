# Olympian AI — Memory Vault

> **Knowledge base & operational memory** untuk ekosistem 14 agent AI bergaya dewa Yunani.

## 🏛 Arsitektur Agent

| Agent | Dewa Yunani | Divisi | Peran Utama |
|-------|-------------|--------|-------------|
| **Zeus** | Zeus | Intelligence | Orchestrator & Strategic Planner |
| **Athena** | Athena | Intelligence | Research, Analysis, Decision Support |
| **Hermes** | Hermes | Intelligence | Coordinator, Executor, Memory Keeper |
| **Plutus** | Plutus | Finance & Crypto | CFO, Treasury, Revenue Optimization |
| **Poseidon** | Poseidon | Digital Business | Market Ops, Growth, Distribution |
| **Ares** | Ares | Digital Business | Competitive Intel, Strategy Execution |
| **Argus** | Argus | Digital Business | Monitoring, Alerting, Observability |
| **Apollo** | Apollo | Media Factory | Content Strategy, Quality Control |
| **Dionysus** | Dionysus | Media Factory | Creative Generation, Viral Mechanics |
| **Calliope** | Calliope | Media Factory | Writing, Storytelling, Copywriting |
| **Aphrodite** | Aphrodite | Media Factory | Brand, Design, Aesthetics, Community |
| **Demeter** | Demeter | Technology | Infrastructure, DevOps, Scaling |
| **Hephaestus** | Hephaestus | Technology | Engineering, Tooling, Automation |
| **Nyx** | Nyx | Technology | Security, Privacy, Night Ops |

## 📁 Struktur Vault

```
Olympian-AI-Memory/
├── hermes-memory/           # Mirror dari ~/.hermes/memories/ (auto-sync)
│   ├── user/                # Memory profil user
│   └── memory/              # Memory agent (notes)
├── hermes-skills/           # Mirror dari ~/.hermes/skills/ (auto-sync)
├── olympian-agents/         # Knowledge base per agent (14 folder)
├── project-context/         # Konteks proyek: arsitektur, phases, tech-stack
├── meeting-notes/           # Catatan rapat & keputusan
├── daily-notes/             # Daily notes (manual/auto)
├── templates/               # Template note untuk konsistensi
└── .obsidian/               # Config Obsidian (plugins, themes, dll)
```

## 🔄 Auto-Sync (Hermes → Obsidian)

- **Script**: `~/scripts/sync-hermes-to-obsidian.sh`
- **Timer**: systemd user timer `hermes-obsidian-sync.timer` (tiap 15 menit)
- **Log**: `~/logs/hermes-obsidian-sync.log`
- **Git**: Auto-commit setiap kali ada perubahan

```bash
# Manual sync
~/scripts/sync-hermes-to-obsidian.sh

# Cek status timer
systemctl --user status hermes-obsidian-sync.timer

# Lihat log
tail -f ~/logs/hermes-obsidian-sync.log
```

## 🚀 Setup Git Remote (GitHub/GitLab)

```bash
# 1. Buat repo baru di GitHub/GitLab (private recommended)
# 2. Tambahkan remote
git remote add origin git@github.com:USERNAME/olympian-ai-memory.git

# 3. Push
git push -u origin master
# atau main kalau sudah rename branch
git branch -m main
git push -u origin main
```

## 📝 Template Tersedia

- `templates/agent-profile.md` — Profil standar 14 agent
- (Tambah template lain di folder `templates/`)

## 🔧 Tech Stack Proyek

- **Language**: Python 3.11+
- **Bot Framework**: aiogram 3.x
- **Database**: SQLAlchemy 2.0 async (SQLite → PostgreSQL)
- **Config**: Pydantic Settings v2
- **Logging**: loguru
- **Scheduling**: apscheduler
- **HTTP**: httpx
- **LLM**: OpenRouter (Claude 3.5 Sonnet planning)
- **Image/Video Gen**: Replicate / Fal.ai
- **Cache/Queue**: Redis (Phase 0+)
- **Package Manager**: uv
- **Deployment**: Docker Compose
- **Language**: Bahasa Indonesia (user-facing)

## 📋 Roadmap Phases

1. **Phase 0** — Foundation (config, docker, scaffolding)
2. **Phase 1** — Zeus (orchestrator core)
3. **Phase 2** — Athena + Hermes (intelligence layer)
4. **Phase 3** — Plutus (CFO system)
5. **Phase 4** — Poseidon + Ares + Argus (digital business)
6. **Phase 5** — Content Factory (Apollo, Dionysus, Calliope, Aphrodite)
7. **Phase 6-7** — Aphrodite + Demeter (brand + infra)
8. **Phase 8** — Automated Business
9. **Phase 9** — Owner Dashboard
10. **Phase 10** — Owner Mode

## 🔐 Security Notes

- **Jangan commit** `.env`, token, API keys, secrets
- Token Telegram bot: simpan di `.env` (sudah di `.gitignore`)
- Rotasi token berkala via BotFather
- Vault ini **private** — jangan push ke public repo tanpa review

---

*Maintained by Hermes Agent • Sync otomatis tiap 15 menit • `git log --oneline` untuk history*