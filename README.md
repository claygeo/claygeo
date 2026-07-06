### Clay George · AI Engineer

I build production LLM systems and find where they bleed money. Started in warehouse operations, taught myself to code to fix the manual work my team was drowning in. Three years later I ship agent systems, adversarial evals, and data pipelines, built to run cheap. eivra runs a live forecasting benchmark on $0 API spend; solhunt reproduced a $182M hack for $0.65. Cost discipline isn't a feature I bolt on. It's how I build.

**Live at [claygeo.dev](https://claygeo.dev)**

**Selected work:**

**spendlens**: Finds where AI systems bleed money. Reads per-request logs and surfaces recoverable spend across five detectors: uncached context resent every call, top-tier models on tasks a cheaper one nails, retries nobody logs, redundant tool calls inside the agent loop, and duplicate log rows that inflate every third-party token count. **No LLM in the analysis. Every number traces to a formula, and it refuses to extrapolate monthly savings from three days of logs, because that's marketing, not analysis.** Cache-miss detection hashes the stable prefix against the TTL window; tool-call dedup keys on name+args+result hash to split idempotent calls from genuine re-fetches. Live at [spendlens.dev](https://spendlens.dev).

**[eivra](https://github.com/claygeo/eivra)**: Live AI forecasting benchmark. Six agents across four model families (Opus 4.7, Sonnet 4.6, Haiku 4.6, GPT-class slot) forecast real Polymarket and Manifold prediction markets, scored continuously in public on Brier, log-loss, 10-bin calibration with Wilson 95% intervals, and Kelly-fraction paper P&L. **2,600+ predictions logged across 450+ resolved markets. The honest answer so far to "can AI reasoning beat market consensus": not yet. The market baseline still edges the best agent on Brier, which is exactly why the benchmark runs in the open.** Runs `claude -p` subprocess on a Hetzner VPS via Max sub, so **$0 Anthropic API spend.** Auto-deploys via GitHub to Netlify with three cron jobs (open-market pull every 15min, scoring every 6h, insight cards nightly). Live at [eivra.xyz](https://eivra.xyz).

**[solhunt-duel](https://github.com/claygeo/solhunt-duel)**: Adversarial red/blue agent system for smart-contract auditing. Red writes exploits, Blue writes patches, four server-side Forge-verified gates decide the verdict. The agents cannot see or modify the gates, because if you let agents grade themselves, they will. Multi-provider LLM router across Anthropic, OpenAI, OpenRouter, and Ollama with cost controls and structured fallbacks. [Public leaderboard](https://solhunt-duel.netlify.app/leaderboard/).

**[solhunt](https://github.com/claygeo/solhunt)**: Autonomous AI agent that finds and exploits smart-contract vulnerabilities. Reads Solidity, writes a Foundry exploit test, executes it on a forked mainnet, iterates against real compiler and execution feedback. Reproduced Beanstalk's $182M flash-loan hack in **1m44s for $0.65.** Hit **67.7% on a curated 31-contract DeFiHackLabs subset, then 13% on a random 95-contract draw.** I published both numbers, and that 54-point gap between curated and random drove the verifier-gate design in solhunt-duel. (For scale, Anthropic's SCONE-bench reports ~51% on a different, larger corpus; the sets aren't directly comparable, so I don't call it a win.)

**[competitive-intel-platform](https://github.com/claygeo/competitive-intel-platform)**: Production data engineering at scale. 14-state, 31-chain, 65+ store competitive pricing pipeline. Reverse-engineered 3 proprietary retail APIs (SweedPOS, Algolia, Trulieve GraphQL) under Cloudflare and auth with Playwright plus session cookie handoff. BullMQ + Redis worker fleet, Postgres normalization, OCR on promotional images via Google Cloud Vision, Telegram alerts. Replaced a 2-week manual analysis cycle with same-day data. Used daily by my 4-person pricing team.

**Hyperliquid Copy-Trading Harness**: Live mainnet AI/quant system. Personal capital, 11 server-side risk gates, regime-stratified backtest with null-distribution validation: 50 random wallets sampled, Bonferroni-adjusted at α=0.05, **0 promoted.** Stop-loss watchdog with re-arm and emergency market close. The harness, not the trades, is the artifact.

**[sandwich-rs](https://github.com/claygeo/sandwich-rs)**: Real-time Solana MEV sandwich detector. Rust + Helius enhanced WebSocket + bounded-backpressure parser pool + per-pool ring buffer with a ≤3-slot detection window. IDL-correct pool extraction for Raydium AMM v4 and Orca Whirlpool. Profit calc with Jito tip detection across 8 known tip accounts. Idempotent Postgres persistence, SSE feed, slot-resume marker for outage gap recovery.

**[hyperliquid-trading-sim](https://github.com/claygeo/hyperliquid-trading-sim)**: Live at [tradeterm.app](https://tradeterm.app). Full-stack paper trading platform with 70+ perpetual futures on real Hyperliquid plus Binance data. Atomic Postgres transactions, JWT auth + RLS, WebSocket streaming, stress-tested to 1,000 TPS.

**How I work:** I ship end-to-end. Not "I prototyped something," but shipped to production, measured, and iterated. Several of the projects above are live URLs you can hit right now. The cannabis pricing system has been running in warehouse operations for over a year. I write things down honestly: when solhunt's exploit rate dropped from 67.7% to 13% on a random sample, I published both numbers and treated the gap as a design problem.

**Stack:**

**Languages:** TypeScript · Python · Rust · Solidity · SQL
**LLM/AI:** Anthropic SDK · OpenAI · OpenRouter · Ollama · multi-provider routing · eval harness design · agent orchestration · tool use · structured fallbacks · cost instrumentation
**Smart contracts:** Foundry · Anvil · forked mainnet · Etherscan API · Alchemy
**Data/infra:** PostgreSQL · Supabase · BullMQ · Redis · Docker · Playwright · WebSockets
**Frontend:** React 18 · Next.js 14 · Vite · Bun
**Deploy:** Netlify · Vercel · Hetzner · GitHub Actions

**Open to AI engineering roles and build/consulting work:** LLM systems, evals, agents, and cost-efficient AI infrastructure. Particularly interested in teams building agent frameworks, eval platforms, or AI tooling. Remote-friendly.

[claygeo.dev](https://claygeo.dev) · [LinkedIn](https://www.linkedin.com/in/claygeo/) · [X](https://x.com/deforestpeg)
