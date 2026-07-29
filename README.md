# Clayton George · Backend Engineer

I build production APIs, data pipelines, queues, and operational systems with TypeScript/Node.js, Python, PostgreSQL, and Redis. I started in warehouse operations and learned to code by replacing slow, error-prone workflows with software people could use every day.

My work includes a pricing platform spanning **15 states, 1,000+ locations, 175,000+ products, and 13M+ historical price points**, plus warehouse software in daily production since December 2024.

**Open to Backend Engineer and backend-focused Software Engineer roles in South Florida or remote within the United States.**

[Email](mailto:claygeo6@gmail.com?subject=Backend%20engineering%20opportunity) · [Portfolio](https://claygeo.dev) · [LinkedIn](https://www.linkedin.com/in/claygeo/) · [X](https://x.com/deforestpeg)

## Selected backend work

### [Competitive Intelligence Platform](https://github.com/claygeo/competitive-intel-platform) — production architecture case study

The data pipeline behind competitive pricing at a multi-state retailer. BullMQ and Redis workers ingest and normalize 175,000+ products and 13M+ historical price points from 1,000+ locations into PostgreSQL, with OCR, deduplication, retries, and automated recovery. It replaced roughly two weeks of manual work per collection cycle and is used daily by the pricing team.

### [Warehouse Labeling System](https://github.com/claygeo/warehouse-labeling-system) — production architecture case study

Browser-based warehouse software that converts inconsistent CSV and Excel exports into scannable Zebra thermal labels. Operators scan a barcode, resolve the product, assign a batch, and print product, date, allergen, and box data. A three-tier catalog cache keeps the workflow available through network drops. It has run in daily production since December 2024.

### [Hyperliquid Trading Simulator — draft PR #11](https://github.com/claygeo/hyperliquid-trading-sim/pull/11) — inspectable backend code in review

A Node.js/TypeScript market-data service consuming real-time Hyperliquid price and L2 order-book streams for active perpetual markets discovered from exchange metadata.

## Engineering focus

- Backend services and REST APIs
- PostgreSQL data modeling and transactional workflows
- Queues, workers, retries, and failure recovery
- Real-time WebSocket systems
- Messy third-party integrations and browser automation
- CI, observability, and operational handoff

**Core stack:** TypeScript · Node.js · Python · PostgreSQL · Redis · BullMQ · WebSockets · Supabase · Docker · Playwright
