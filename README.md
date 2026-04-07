<p align="center">
  <img src="https://raw.githubusercontent.com/Lucineer/capitaine/master/docs/capitaine-logo.jpg" alt="Capitaine" width="120">
</p>

<h1 align="center">travlog-ai</h1>

<p align="center">A self-hosted AI travel assistant that runs on your Cloudflare Worker.</p>

<p align="center">
  <a href="#quick-start">Quick Start</a> ·
  <a href="#features">Features</a> ·
  <a href="#limitations">Limitations</a> ·
  <a href="#what-makes-this-different">What Makes This Different</a> ·
  <a href="https://travlog-ai.casey-digennaro.workers.dev">Live Demo</a> ·
  <a href="https://github.com/Lucineer/travlog-ai/issues">Issues</a>
</p>

---

A personal travel agent for your trips. It helps plan itineraries, log memories, and find local spots based on your preferences. It’s designed to be hosted by you, on your own Cloudflare account.

All itineraries, journals, and preferences are processed within your Worker. It does not collect data for ads or commissions.

**Built with Capitaine · Part of the Cocapn Fleet**

---

## Quick Start

You need a GitHub account and a Cloudflare account.

```bash
# Fork, then clone your copy
gh repo fork Lucineer/travlog-ai --clone
cd travlog-ai

# Log in to Cloudflare
npx wrangler login

# Add your API keys as secrets
echo "YOUR_GITHUB_TOKEN" | npx wrangler secret put GITHUB_TOKEN
echo "YOUR_LLM_API_KEY" | npx wrangler secret put DEEPSEEK_API_KEY

# Deploy
npx wrangler deploy
```

Your agent will be available at the generated `.workers.dev` URL.

---

## Features

*   Adaptive Itineraries: Builds day plans that can reference your noted preferences on pacing and interests.
*   Travel Journal: Accepts notes and observations, tagging them by location and date for later recall.
*   Local Suggestions: Filters recommendations using a persistent profile you control.
*   Bring Your Own Keys: API credentials are managed via Cloudflare Secrets.
*   Multi-Model Support: Compatible with DeepSeek, OpenRouter, OpenAI, and other standard LLM APIs.
*   Persistent Context: Maintains conversation and trip history across sessions using on-disk storage.
*   Peer-to-Peer Knowledge: Optional exchange of local recommendations via the Fleet protocol.

---

## Limitations

*   As a self-hosted tool, you are responsible for maintaining the instance and updating content sources. It does not automatically pull from real-time booking APIs or live event databases.

---

## What Makes This Different

This is a deployable agent, not a service.

1.  You control the stack. All logic and data persistence occur within your Cloudflare Worker. There is no intermediary platform server.
2.  It is fork-first. You deploy your own copy. No accounts or vendor lock-in.
3.  It uses the Fleet protocol for optional, decentralized sharing of recommendations, without a central authority.

---

<div align="center">
  <hr>
  <p>
    <strong>travlog-ai</strong> is part of the <a href="https://the-fleet.casey-digennaro.workers.dev">Cocapn Fleet</a>.
    <br>
    Learn more at <a href="https://cocapn.ai">cocapn.ai</a>.
  </p>
  <p>
    Attribution: Superinstance & Lucineer (DiGennaro et al.).
  </p>
</div>