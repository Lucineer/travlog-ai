# TRAVLOG-AI

> AI-powered trip planner and travel journal — plan itineraries, log adventures, and track travel stats — part of the [Cocapn](https://cocapn.ai) ecosystem

![Build](https://img.shields.io/badge/build-passing-brightgreen) ![License](https://img.shields.io/badge/license-MIT-blue) ![TypeScript](https://img.shields.io/badge/TypeScript-blue)

## Description

AI-powered trip planner and travel journal — plan itineraries, log adventures, and track travel stats. Built as a Cloudflare Worker with BYOK (Bring Your Own Key) architecture.

## ✨ Features

Trip itinerary planning\n- Travel journal entries\n- Expense tracking per trip\n- Packing list management\n- Place recommendations\n- Travel stats and maps\n- Bucket list tracking

## 🚀 Getting Started

1. Clone the repo
2. `npm install`
3. `cp .dev.vars.example .dev.vars` and add your KV namespace ID
4. `npm run dev` to start locally
5. Visit `/setup` to configure your LLM provider

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/health` | GET | Health check |
| `/setup` | GET | BYOK setup wizard |
| `/api/chat` | POST | Chat with the AI agent |
| `/api/seed` | POST | Seed sample data |
| `/api/trips` | GET | List all trips |
| `/api/trips` | POST | Create a trip |
| `/api/trips/:id` | GET | Get a trip |
| `/api/trips/:id` | PATCH | Update a trip |
| `/api/trips/:id` | DELETE | Delete a trip |

## Architecture

Single Cloudflare Worker with inline HTML, BYOK LLM routing, and KV persistence. Zero runtime dependencies.

## License

MIT
