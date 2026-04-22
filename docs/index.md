---
layout: default
title: EdgeStack Currency
description: Event-Sourced Multi-Currency Execution Spec — part of the ARC Trading Fleet.
---

# EdgeStack Currency
**Event-Sourced Multi-Currency Execution Spec**

[![Source](https://img.shields.io/badge/source-GitHub-181717?logo=github)](https://github.com/GareBear99/EdgeStack_Currency)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/GareBear99/EdgeStack_Currency/blob/main/LICENSE)
[![Built on ARC-Core](https://img.shields.io/badge/built%20on-ARC--Core-5B6CFF)](https://github.com/GareBear99/ARC-Core)

## 📖 Official docs

[![Open the official spec](https://img.shields.io/badge/%F0%9F%93%96%20Official%20Spec-Open%20the%20full%20text-0366d6?style=for-the-badge)](./official/edge_stacking_system_spec.txt)

[![AI implementation prompt](https://img.shields.io/badge/%F0%9F%A4%96%20AI%20Implementation%20Prompt-Open-5B6CFF?style=for-the-badge)](./official/AI_CANONICAL_IMPLEMENTATION_PROMPT.txt)

Live URL of the primary doc: `https://garebear99.github.io/EdgeStack_Currency/official/edge_stacking_system_spec.txt`

## What this is

EdgeStack Currency is part of the **ARC Trading Fleet** — six public repositories that share a
single event-and-receipt doctrine provided by
[ARC-Core](https://github.com/GareBear99/ARC-Core).

- **Source code and full README**: [https://github.com/GareBear99/EdgeStack_Currency](https://github.com/GareBear99/EdgeStack_Currency)
- **Architecture notes**: [docs/ARCHITECTURE.md](https://github.com/GareBear99/EdgeStack_Currency/blob/main/docs/ARCHITECTURE.md)
- **Usage / operator guide**: [docs/USAGE.md](https://github.com/GareBear99/EdgeStack_Currency/blob/main/docs/USAGE.md)
- **Security policy**: [SECURITY.md](https://github.com/GareBear99/EdgeStack_Currency/blob/main/SECURITY.md)
- **Contributing**: [CONTRIBUTING.md](https://github.com/GareBear99/EdgeStack_Currency/blob/main/CONTRIBUTING.md)

## ARC-Core mapping

Every market tick becomes an *event*; every trade decision becomes a *proposal*;
every fill or outcome becomes a *receipt*; every risk limit is an *authority
gate*; every backtest is a *deterministic replay* of the event log. Full per-bot
mapping in [ECOSYSTEM.md](https://github.com/GareBear99/ARC-Core/blob/main/ECOSYSTEM.md#-trading-fleet--six-repos-one-event-spine).

## Sibling repos in the fleet

| Repo | One-liner | Docs site |
|---|---|---|
| [BrokeBot](https://github.com/GareBear99/BrokeBot) | TRON Funding-Rate Arbitrage (CEX, Python) | [https://garebear99.github.io/BrokeBot/](https://garebear99.github.io/BrokeBot/) |
| [Charm](https://github.com/GareBear99/Charm) | Uniswap v3 Spot Bot on Base (Node.js) | [https://garebear99.github.io/Charm/](https://garebear99.github.io/Charm/) |
| [Harvest](https://github.com/GareBear99/Harvest) | Multi-Timeframe Crypto Research Platform (Python) | [https://garebear99.github.io/Harvest/](https://garebear99.github.io/Harvest/) |
| [One-Shot-Multi-Shot](https://github.com/GareBear99/One-Shot-Multi-Shot) | Binary-Options 3-Hearts Engine (JS) | [https://garebear99.github.io/One-Shot-Multi-Shot/](https://garebear99.github.io/One-Shot-Multi-Shot/) |
| [DecaGrid](https://github.com/GareBear99/DecaGrid) | Capital-Ladder Grid Trading Docs Pack | [https://garebear99.github.io/DecaGrid/](https://garebear99.github.io/DecaGrid/) |

## Upstream

- [ARC-Core](https://github.com/GareBear99/ARC-Core) — the event + receipt spine.
- [omnibinary-runtime](https://github.com/GareBear99/omnibinary-runtime) — any-OS runtime.
- [Arc-RAR](https://github.com/GareBear99/Arc-RAR) — archives + rollback.
- [Portfolio](https://github.com/GareBear99/Portfolio) — full project index.

---
*This page is auto-rendered from `docs/index.md` on the `main` branch. The
canonical source of truth is the repository README.*
