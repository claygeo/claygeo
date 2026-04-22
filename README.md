### Hey, I'm Clay

I started in warehouse operations, noticed my team was drowning in manual work, and taught myself to code to fix it. That turned into building full production systems — scrapers, data pipelines, dashboards, and automation tools that replaced weeks of manual work with code that runs on autopilot.

**Things I've built:**

**[solhunt-duel](https://github.com/claygeo/solhunt-duel)** — Adversarial red/blue agent system for smart contract auditing. Red finds exploits, blue writes patches, four server-side forge-verified gates prevent the LLMs from faking success. Real convergence on the $2M Dexible exploit.

**[solhunt](https://github.com/claygeo/solhunt)** — Autonomous AI agent that finds and exploits smart contract vulnerabilities. Reads Solidity, writes Foundry exploit tests, executes on forked mainnet. Beanstalk ($182M hack) exploited in 1m 44s for $0.65. Learned that a curated benchmark (67.7%) collapsed to ~13% on random samples — that evaluation gap drove me to build solhunt-duel (adversarial red/blue with server-side verification).

**[Hyperliquid Trading Sim](https://github.com/claygeo/hyperliquid-trading-sim)** — Live at [tradeterm.app](https://tradeterm.app). Paper trading 70+ crypto perpetual futures on real Hyperliquid + Binance data. TradingView charts with 6 timeframes, 15-level live orderbook, whale position tracking, global leaderboard. Atomic PostgreSQL transactions with row-level locking, JWT auth + RLS, stress-tested at 1,000 TPS. React 18 + Express + Supabase.

**[Competitive Intelligence Platform](https://github.com/claygeo/competitive-intel-platform)** — Replaced my team's 2-week manual pricing analysis with a fully automated pipeline. Reverse-engineered 3 proprietary retail APIs (REST, GraphQL, Algolia), scrapes **50,000+ products across 31 chains in 14 states**, pushes Telegram alerts. 65+ scraper jobs staggered across 6-hour cycles. Six spreadsheets → one C-suite dashboard with same-day data.

**[Chess Benchmark](https://github.com/claygeo/chess-benchmark)** — Live at [chessbenchmark.netlify.app](https://chessbenchmark.netlify.app). Freelance client delivery in 4 days. Three cognitive training exercises: spatial memory (animated opening playback → recall), verbal memory (notation recall), coordinate vision (board recognition). Four difficulty tiers from Beginner (10s study) to Master (4s study), independent sliders for study time and animation speed, scoring with streak bonuses. Next.js 14 + bun.

**[Cannabis Inventory System](https://github.com/claygeo/cannabis-inventory-system)** — Production React app running in warehouse operations since 2024, currently v7.4.1. Barcode scanning with multi-source product lookup, thermal label generation optimized for Zebra ZT610 at 203 DPI, automatic allergen detection, cloud-synced master list via Supabase with offline localStorage fallback. Multi-source CSV/Excel imports (Main Inventory, Sweed Reports, Import Reports).

**Tech stack:**

**Languages:** TypeScript · Python · Solidity
**Frameworks:** Next.js 14 · React 18 · Express · Vite · Foundry · Bun
**AI/ML:** Claude · Qwen · OpenRouter · Anthropic SDK · custom agent loops
**Blockchain:** Anvil · Foundry · Etherscan API · Alchemy · EVM forking · Hyperliquid API
**Data/Infra:** PostgreSQL · Redis · Supabase · BullMQ · Docker · Playwright · WebSocket · Zustand
**Deployment:** Netlify · Render · Hetzner · GitHub Actions CI

**How I work:** I ship end-to-end. Not "I prototyped something" — I ship it to production, measure it, iterate. Three of the projects above are live URLs you can hit right now. The warehouse inventory system has been running in production for over a year. I also write things down honestly — when solhunt's exploit rate dropped from 67.7% on curated contracts to 13% on a random sample, I published both numbers.

**Currently looking for** AI engineering, blockchain security, data engineering, or platform engineering roles (remote). Particularly interested in teams building agent frameworks, DeFi security tooling, or trading infrastructure. Also open to contract work and smart contract audits.

[LinkedIn](https://www.linkedin.com/in/claygeo/)
