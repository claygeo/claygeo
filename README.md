### Clay George — AI Engineer

I build production LLM systems and the data infrastructure they sit on top of. Started in warehouse operations, taught myself to code to fix the manual work my team was drowning in. Three years later I'm shipping adversarial agent evals, production data pipelines, and live trading systems.

**Live at [claygeo.dev](https://claygeo.dev)**

**Selected work:**

**[eivra](https://github.com/claygeo/eivra)** — Live AI forecasting benchmark. Six agents across four model families (Opus 4.7, Sonnet 4.6, Haiku 4.6, GPT-class slot) forecast real Polymarket and Manifold prediction markets. Every prediction scored with Brier, log-loss, 10-bin calibration plots with Wilson 95% intervals, and Kelly-fraction paper P&L. **175 predictions, 31 resolved markets, Hawk (contrarian) leads at 0.037 Brier on 28 resolutions and 96% win rate.** Runs `claude -p` subprocess on a Hetzner VPS via Max sub — **$0 Anthropic API spend.** Auto-deploys via GitHub→Netlify CD with three cron jobs (open-market pull every 15min, scoring every 6h, insight cards nightly). Live at [eivra.xyz](https://eivra.xyz).

**[solhunt-duel](https://github.com/claygeo/solhunt-duel)** — Adversarial red/blue agent system for smart-contract auditing. Red writes exploits, Blue writes patches, four server-side Forge-verified gates decide the verdict. The agents cannot see or modify the gates — because if you let agents grade themselves, they will. Multi-provider LLM router across Anthropic, OpenAI, OpenRouter, and Ollama with cost controls and structured fallbacks. [Public leaderboard](https://solhunt-duel.netlify.app/leaderboard/).

**[solhunt](https://github.com/claygeo/solhunt)** — Autonomous AI agent that finds and exploits smart-contract vulnerabilities. Reads Solidity, writes a Foundry exploit test, executes it on a forked mainnet, iterates against real compiler and execution feedback. Reproduced Beanstalk's $182M flash-loan hack in **1m44s for $0.65**. Hit **67.7% on a curated 32-contract DeFiHackLabs subset, beating Anthropic's SCONE-bench at 51.1%** — then collapsed to **13% on a random 95-contract draw**. I published both numbers. That 54-point honesty gap drove the verifier-gate design in solhunt-duel.

**[competitive-intel-platform](https://github.com/claygeo/competitive-intel-platform)** — Production data engineering at scale. 14-state, 31-chain, 65+ store competitive pricing pipeline. Reverse-engineered 3 proprietary retail APIs (SweedPOS, Algolia, Trulieve GraphQL) under Cloudflare/auth with Playwright + session cookie handoff. BullMQ + Redis worker fleet, Postgres normalization, OCR on promotional images via Google Cloud Vision, Telegram alerts. Replaced a 2-week manual analysis cycle with same-day data. Used daily by my 4-person pricing team.

**Hyperliquid Copy-Trading Harness** — Live mainnet AI/quant system. $1,554 personal capital, 11 server-side risk gates, regime-stratified backtest with null-distribution validation: 50 random wallets sampled, Bonferroni-adjusted at α=0.05, **0 promoted**. Stop-loss watchdog with re-arm and emergency market close. The harness, not the trades, is the artifact.

**[sandwich-rs](https://github.com/claygeo/sandwich-rs)** — Real-time Solana MEV sandwich detector. Rust + Helius enhanced WebSocket + bounded-backpressure parser pool + per-pool ring buffer with ≤3-slot detection window. IDL-correct pool extraction for Raydium AMM v4 + Orca Whirlpool. Profit calc with Jito tip detection across 8 known tip accounts. Idempotent Postgres persistence, SSE feed, slot-resume marker for outage gap recovery.

**[hyperliquid-trading-sim](https://github.com/claygeo/hyperliquid-trading-sim)** — Live at [tradeterm.app](https://tradeterm.app). Full-stack paper trading platform with 70+ perpetual futures on real Hyperliquid + Binance data. Atomic Postgres transactions, JWT auth + RLS, WebSocket streaming, stress-tested to 1,000 TPS.

**How I work:** I ship end-to-end. Not "I prototyped something" — I ship to production, measure it, iterate. Three of the projects above are live URLs you can hit right now. The cannabis inventory system has been running in warehouse operations for over a year. I write things down honestly — when solhunt's exploit rate dropped from 67.7% to 13% on a random sample, I published both numbers and treated the gap as a design problem.

**Stack:**

**Languages:** TypeScript · Python · Rust · Solidity · SQL
**LLM/AI:** Anthropic SDK · OpenAI · OpenRouter · Ollama · multi-provider routing · eval harness design · agent orchestration · tool use · structured fallbacks
**Smart contracts:** Foundry · Anvil · forked mainnet · Etherscan API · Alchemy
**Data/infra:** PostgreSQL · Supabase · BullMQ · Redis · Docker · Playwright · WebSockets
**Frontend:** React 18 · Next.js 14 · Vite · Bun
**Deploy:** Netlify · Vercel · Hetzner · GitHub Actions

**Currently looking for** AI engineering roles — LLM systems, evals, agents, production AI infrastructure. Particularly interested in teams building agent frameworks, eval platforms, or AI security. Remote-friendly.

[claygeo.dev](https://claygeo.dev) · [LinkedIn](https://www.linkedin.com/in/claygeo/) · [@claygdev](https://x.com/claygdev)
