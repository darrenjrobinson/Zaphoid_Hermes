Doc's Windows host is Windows 10 (not 11 — mirrored networking unavailable). Windows username: darrenjrobinson. WSL2 hostname: OpenClaw (migrated from OpenClaw to Hermes Agent). WSL2 IP: 172.22.22.1. Windows portproxy already configured: port 8000 and 18789 → 172.22.22.1. Hermes api_server configured on 0.0.0.0:8000 (OpenAI-compatible at /v1). LM Studio has been removed — no local LLM, no heartbeat model.
§
Doc prefers I use hermes config set commands rather than direct file edits for config.yaml (security feature — direct edits are blocked anyway). For complex multi-line YAML he uses hermes config edit himself.
§
Zaphoid backup repo: github.com/darrenjrobinson/Zaphoid_Hermes. Backup scripts at ~/.hermes/scripts/github-backup/ (backup.sh + generate-readme.py). Cron job ID e054d5349bf5 runs daily at 6am AEST. Credentials for git stored in .netrc (600 perms). Commits sanitised config, skills list, cron jobs, system snapshot.
§
Zaphoid email: zaphoid@agentmail.to. Doc's email: darren@darrenjrobinson.com. Send plans/docs as Markdown+PDF. AGENTMAIL_API_KEY in .env. Endpoint: POST /inboxes/{url-encoded-id}/messages/send (NOT /messages). Do NOT poll for incoming email. Untappd timestamps are UTC — Doc is GMT+11 AEST; always verify day-of-week/weekend before asserting. Got this wrong once (called Monday AEST a Sunday) — Doc corrected it.
§
Node.js 22 installed user-local at ~/nodejs/ (no sudo — system has no curl/wget and no sudo access for apt). PATH added to ~/.bashrc. npx is at ~/nodejs/bin/npx. Any tool or script needing node/npx must use this path or export PATH="$HOME/nodejs/bin:$PATH" first.
§
Untappd MCP configured: untappd-mcp-server via npx, creds in .env as UNTAPPD_CLIENT_ID / UNTAPPD_CLIENT_SECRET. Doc's Untappd username: Docta. Mates list at ~/.hermes/data/untappd-mates.json. MCP tools need /reload-mcp after gateway restart (not yet live as native tools — session must reload). Rate limit: 100 calls/hour.
§
Doc wants Hermes Desktop on Windows to connect to the existing WSL Hermes deployment/dashboard rather than create a separate native Windows Hermes setup when possible.