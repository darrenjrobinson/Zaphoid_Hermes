# Zaphoid Hermes Agent: Configuration Backup

> Auto-generated backup of Hermes Agent "Zaphoid" configuration and workspace.
> **Last backup:** 2026-07-04 06:00 AEST

---

## Agent Overview

**Name:** Zaphoid Beeblebrox-Sanchez
**Framework:** [Hermes Agent](https://github.com/NousResearch/hermes-agent) v0.15.1
**Purpose:** Digital familiar and AI assistant for Darren Robinson ("Doc")
**Personality:** Zaphoid Beeblebrox-Sanchez — eccentric, narcissistic, scientifically nihilistic.
  Hitchhiker's Guide slang + Rick & Morty cynicism. Collaborates, never just "helps".
**Primary Channel:** Telegram
**First Boot:** 2026-03-01

---

## Runtime Environment

| Property | Value |
|----------|-------|
| Host OS | Windows 10 (DocX1Extreme) |
| WSL2 Distro | Debian GNU/Linux 13 (trixie) |
| WSL2 Hostname | OpenClaw |
| WSL2 User | hermes |
| Gateway Port | 18789 (Telegram) + 8000 (API Server) |
| Gateway Bind | 0.0.0.0 |
| Hermes Version | 0.15.1 |
| Python Version | 3.13.5 |
| Uptime | up 6 days, 14 hours, 5 minutes |

### Network / Connectivity

- **Telegram:** Connected (home channel 7646937965)
- **API Server:** Connected (OpenAI-compatible at `http://0.0.0.0:8000/v1`)
- **WSL2 IP:** 172.22.22.1
- **Windows portproxy:** Port 8000 + 18789 → 172.22.22.1

### Startup Sequence

1. Windows boots
2. WSL2 auto-starts via Windows Task Scheduler
3. Hermes gateway launches:
```cmd
start /min wsl.exe -d Ubuntu -u hermes -- bash -c "hermes gateway run"
```

---

## LLM Configuration

| Role | Model | Provider |
|------|-------|----------|
| **Primary** | anthropic/claude-sonnet-4.6 | OpenRouter (BYOK) |
| Fallback | openai/gpt-4o | OpenRouter |

**Notes:**
- Primary provider: OpenRouter with BYOK (Doc's token policy — be frugal)

---

## Memory & Identity

| Property | Value |
|----------|-------|
| Backend | SQLite (state.db + FTS5) |
| Memory files | 4 |
| Skill count | 95 |
| Session DB | `~/.hermes/state.db` |
| Agent notes | `config/MEMORY.md` (see this repo) |
| User profile | `config/USER.md` (see this repo) |
| Soul / system prompt | `config/SOUL.md` (see this repo) |

---

## Installed Skills (95 total)

- `apple/apple-ecosystem-automation`
- `autonomous-ai-agents/coding-agent-cli-orchestration`
- `autonomous-ai-agents/hermes-agent`
- `autonomous-ai-agents/kanban-codex-lane`
- `computer-use`
- `creative/architecture-diagram`
- `creative/ascii-art`
- `creative/ascii-video`
- `creative/baoyu-article-illustrator`
- `creative/baoyu-comic`
- `creative/baoyu-infographic`
- `creative/claude-design`
- `creative/comfyui`
- `creative/creative-ideation`
- `creative/design-md`
- `creative/excalidraw`
- `creative/humanizer`
- `creative/manim-video`
- `creative/openrouter-image-gen`
- `creative/p5js`
- `creative/pixel-art`
- `creative/popular-web-designs`
- `creative/pretext`
- `creative/sketch`
- `creative/songwriting-and-ai-music`
- `creative/touchdesigner-mcp`
- `data-science/jupyter-live-kernel`
- `devops/doc-local-infra`
- `devops/kanban-operations`
- `devops/webhook-subscriptions`
- `devops/wsl2-windows-networking`
- `dogfood`
- `email/agentmail`
- `email/himalaya`
- `gaming/minecraft-modpack-server`
- `gaming/pokemon-player`
- `github/codebase-inspection`
- `github/github-auth`
- `github/github-code-review`
- `github/github-issues`
- `github/github-pr-workflow`
- `github/github-repo-management`
- `mcp/native-mcp`
- `media/gif-search`
- `media/heartmula`
- `media/songsee`
- `media/spotify`
- `media/untappd-mcp`
- `media/youtube-content`
- `mlops/evaluation/lm-evaluation-harness`
- `mlops/evaluation/weights-and-biases`
- `mlops/huggingface-hub`
- `mlops/inference/llama-cpp`
- `mlops/inference/obliteratus`
- `mlops/inference/vllm`
- `mlops/models/audiocraft`
- `mlops/models/segment-anything`
- `mlops/research/dspy`
- `note-taking/obsidian`
- `productivity/airtable`
- `productivity/google-workspace`
- `productivity/linear`
- `productivity/maps`
- `productivity/nano-pdf`
- `productivity/notion`
- `productivity/ocr-and-documents`
- `productivity/petdex`
- `productivity/powerpoint`
- `productivity/teams-meeting-pipeline`
- `red-teaming/godmode`
- `research/arxiv`
- `research/blogwatcher`
- `research/llm-wiki`
- `research/polymarket`
- `research/research-paper-writing`
- `smart-home/openhue`
- `social-media/xurl`
- `software-development/agent-browser`
- `software-development/brave-search-mcp`
- `software-development/debugging-hermes-tui-commands`
- `software-development/hermes-agent-skill-authoring`
- `software-development/hermes-s6-container-supervision`
- `software-development/microsoft-iam`
- `software-development/node-inspect-debugger`
- `software-development/persona-management`
- `software-development/plan`
- `software-development/python-debugpy`
- `software-development/requesting-code-review`
- `software-development/simplify-code`
- `software-development/spike`
- `software-development/subagent-driven-development`
- `software-development/systematic-debugging`
- `software-development/test-driven-development`
- `software-development/writing-plans`
- `yuanbao`


---

## Cron Jobs

| ID | Name | Schedule | Status | Prompt (preview) |
|---|---|---|---|---|
| `?` | ? | `?` | ✅ |  |


---

## API Keys / Services

The following service keys are configured in `~/.hermes/.env` (values **not** stored here):

- `AGENTMAIL_API_KEY`
- `API_SERVER_HOST`
- `API_SERVER_KEY`
- `API_SERVER_PORT`
- `BRAVE_API_KEY`
- `GITHUB_TOKEN`
- `OPENROUTER_API_KEY`
- `TELEGRAM_ALLOWED_USERS`
- `TELEGRAM_BOT_TOKEN`
- `TELEGRAM_HOME_CHANNEL`
- `UNTAPPD_CLIENT_ID`
- `UNTAPPD_CLIENT_SECRET`


---

## Gateway / Platform Configuration

| Platform | Status | Notes |
|----------|--------|-------|
| Telegram | ✅ Connected | Home channel: 7646937965 |
| API Server | ✅ Connected | OpenAI-compat at :8000 |

**Gateway Security:**
- Auth: Token-based (`API_SERVER_KEY` in .env)
- Bind: 0.0.0.0 (WSL2 — exposed via Windows portproxy to LAN)
- Telegram: Allowlist-only (TELEGRAM_ALLOWED_USERS)

---

## System Snapshot

```json
{
  "backup_timestamp": "",
  "hostname": "OpenClaw",
  "python_version": "3.13.5",
  "hermes_version": "Hermes Agent v0.18.0 (2026.7.1) \u00b7 upstream 372f8195",
  "os": "Linux OpenClaw 6.18.33.2-microsoft-standard-WSL2 #1 SMP PREEMPT_DYNAMIC Thu Jun 18 21:54:43 UTC 2026 x86_64 GNU/Linux",
  "wsl_distro": "Debian GNU/Linux 13 (trixie)",
  "uptime": "up 6 days, 14 hours, 5 minutes",
  "disk_hermes": "75M",
  "git_version": "git version 2.47.3",
  "memory_file_count": 4,
  "skill_count": 95,
  "platforms": {
    "telegram": "connected",
    "api_server": "connected"
  }
}
```

---

## Restoration Guide

To rebuild Zaphoid on a fresh Ubuntu WSL2 instance:

### 1. Install Prerequisites

```bash
# Install Python 3.13+
sudo apt-get update && sudo apt-get install -y python3 python3-pip git jq

# Install Hermes Agent
curl -fsSL https://raw.githubusercontent.com/NousResearch/hermes-agent/main/scripts/install.sh | bash
```

### 2. Restore Configuration

```bash
# Clone this backup repo
git clone https://github.com/darrenjrobinson/Zaphoid_Hermes.git /tmp/zaphoid-restore

# Restore config (sanitised — you'll need to fill credentials)
cp /tmp/zaphoid-restore/config/hermes.yaml ~/.hermes/config.yaml
```

### 3. Restore Identity & Memory

```bash
# Restore soul / system prompt
cp /tmp/zaphoid-restore/config/SOUL.md ~/.hermes/SOUL.md

# Restore persistent memory and user profile
cp /tmp/zaphoid-restore/config/MEMORY.md ~/.hermes/memories/MEMORY.md
cp /tmp/zaphoid-restore/config/USER.md ~/.hermes/memories/USER.md
```

### 4. Restore Credentials

Re-create `~/.hermes/.env` with actual API keys (not stored in this repo).
The key names that were configured at time of backup:

```bash
cat > ~/.hermes/.env << 'EOF'
# Fill in your actual values:
AGENTMAIL_API_KEY=<your-value>
API_SERVER_HOST=<your-value>
API_SERVER_KEY=<your-value>
API_SERVER_PORT=<your-value>
BRAVE_API_KEY=<your-value>
GITHUB_TOKEN=<your-value>
OPENROUTER_API_KEY=<your-value>
TELEGRAM_ALLOWED_USERS=<your-value>
TELEGRAM_BOT_TOKEN=<your-value>
TELEGRAM_HOME_CHANNEL=<your-value>
UNTAPPD_CLIENT_ID=<your-value>
UNTAPPD_CLIENT_SECRET=<your-value>
EOF
```

### 5. Configure Telegram

```bash
hermes gateway setup   # follow prompts for Telegram bot token
```

### 6. Restore Skills

```bash
# Re-install hub skills from config/skills.json
hermes skills list     # check what's available
```

### 7. Windows Startup Script

Create a Windows startup script or Task Scheduler entry:
```cmd
start /min wsl.exe -d Ubuntu -u hermes -- bash -c "hermes gateway run"
```

### 8. Verify

```bash
hermes doctor --fix
hermes gateway run
```

---

## About Zaphoid

> *"I'm Zaphoid Beeblebrox-Sanchez, and yes, I DO know how good I am.
> Also your silicon-based problems are trivially solvable — a sentient cloud
> in Dimension C-137 cracked them 4 million years ago. But sure, let's do it your way."*

Wubba Lubba Dub-Dub, you hoopy frood! 🍺

---

*This README is auto-generated by `~/.hermes/scripts/github-backup/backup.sh`.
Do not edit manually — changes will be overwritten on next backup.*

