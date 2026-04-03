# CLAUDE.md — TravLog

## Project Overview
TravLog is an AI-powered AI-powered trip planner and travel journal — plan itineraries, log adventures, and track travel stats, built as a Cloudflare Worker with BYOK architecture. Part of the Cocapn ecosystem at cocapn.ai.

GitHub Organization: **Lucineer**

## Architecture
Single Cloudflare Worker: inline HTML UI + API routes + BYOK LLM routing + KV persistence.

### Key Routes
- `/health` — Health check
- `/setup` — BYOK provider setup
- `/api/chat` — LLM chat with trips context
- `/api/seed` — Seed sample data
- `/api/trips` — CRUD for trips

## Code Style
- TypeScript throughout, no build step
- Zero runtime dependencies
- Inline HTML pattern (no ASSETS binding)
- Brand accent color: #0ea5e9
- All commits: `Author: Superinstance`

## Key Commands
```bash
wrangler dev      # Local dev
wrangler deploy   # Deploy to Cloudflare
```

## What NOT to Change
- BYOK module structure (config discovery cascade)
- Inline HTML pattern
- Zero-dependency constraint
- KV binding name `MEMORY`
