<!-- ARC-Ecosystem-Hero-Marker -->
# EdgeStack Currency — Event-Sourced Multi-Currency Execution Spec

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status: Spec](https://img.shields.io/badge/status-specification-blue.svg)]()
[![Built on ARC-Core](https://img.shields.io/badge/built%20on-ARC--Core-5B6CFF)](https://github.com/GareBear99/ARC-Core)

> Canonical **system specification** for an event-sourced multi-currency
> execution and edge-stacking engine. An immutable append-only ledger of
> deposits, orders, fills, fees, FX conversions, transfers, settlement
> adjustments, and reconciliation corrections — designed to be auditable,
> replayable, and multi-venue.

## What this repo contains

-   `edge_stacking_system_spec.txt` — the canonical design document.
    Covers: core philosophy, global non-negotiables, system architecture,
    the event-sourced ledger, event schema, event type taxonomy, and
    reconciliation rules.
-   `AI_CANONICAL_IMPLEMENTATION_PROMPT.txt` — an implementation prompt that
    compresses the spec into instructions an AI implementer can consume
    without drift.

## Why this repo exists

Implementation trends toward drift. A crisp, version-controlled, prose-first
specification is the *only* reliable root-of-truth for a multi-currency trading
backbone. Any language, any runtime, any venue — everyone implements from the
same document, not from someone's memory.

## Core concepts (from the spec)

-   **Event-sourced ledger**: every balance change is an immutable event. No
    direct balance edits. Current state is a fold over events.
-   **Event schema**: `(event_id, timestamp, venue, currency,
    delta_available, delta_reserved, delta_pending, reference_id, event_type,
    notes)`.
-   **Event taxonomy**: `DEPOSIT`, `WITHDRAWAL`, `ORDER_PLACED`,
    `FILL_PARTIAL`, `FILL_COMPLETE`, `FEE`, `FX_CONVERSION`,
    `TRANSFER_INTERNAL`, `SETTLEMENT_ADJUSTMENT`, `RECONCILIATION_CORRECTION`.
-   **Reconciliation discipline**: every venue discrepancy is resolved via a
    named `RECONCILIATION_CORRECTION` event — never via silent balance edits.
-   **Edge stacking**: multiple simultaneously profitable edges (fee rebate,
    funding capture, FX spread, latency) are composed at the portfolio level.

## Reference implementations

This spec is intended to be implemented inside trading systems such as:

-   [Harvest](https://github.com/GareBear99/Harvest)
-   [BrokeBot](https://github.com/GareBear99/BrokeBot)
-   [Charm](https://github.com/GareBear99/Charm)
-   or your own trading stack.

When implemented on top of the [ARC-Core](https://github.com/GareBear99/ARC-Core)
event spine, the ledger gets tamper-evident receipts and verifiable replay for
free.

## Part of the ARC ecosystem

-   [ARC-Core](https://github.com/GareBear99/ARC-Core) — governed event +
    receipt spine.
-   [omnibinary-runtime](https://github.com/GareBear99/omnibinary-runtime) +
    [Arc-RAR](https://github.com/GareBear99/Arc-RAR) — any-OS portability.
-   [Portfolio](https://github.com/GareBear99/Portfolio) — full project index.

## Keywords
`event sourcing` · `trading ledger` · `multi-currency` · `fx conversion` ·
`execution engine` · `reconciliation` · `order management system` ·
`quantitative finance spec` · `immutable audit trail` ·
`edge stacking` · `venue aggregator`

## License

MIT — see `LICENSE`. This is a specification and is not financial advice.

---

<!-- ARC-Official-Docs-Link-Marker -->
## 📖 Official docs

[**Open the rendered official docs → https://garebear99.github.io/EdgeStack_Currency/official/edge_stacking_system_spec.txt**](https://garebear99.github.io/EdgeStack_Currency/official/edge_stacking_system_spec.txt)

Also available under [`docs/official/`](https://github.com/GareBear99/EdgeStack_Currency/tree/main/docs/official) in-tree, and through the Pages landing at [https://garebear99.github.io/EdgeStack_Currency/](https://garebear99.github.io/EdgeStack_Currency/). (Plain-text spec; the AI-implementation prompt is at `official/AI_CANONICAL_IMPLEMENTATION_PROMPT.txt`.)



<!-- ARC-Trading-Fleet-Nav-Marker -->
## 🧭 ARC Trading Fleet

Six sibling repositories. Same ARC event-and-receipt doctrine. Each has its
own live GitHub Pages docs site, source, and README.

| Repo | One-liner | Source | Docs site |
|---|---|---|---|
| [BrokeBot](https://github.com/GareBear99/BrokeBot) | TRON Funding-Rate Arbitrage (CEX, Python) | [source](https://github.com/GareBear99/BrokeBot) | [https://garebear99.github.io/BrokeBot/](https://garebear99.github.io/BrokeBot/) |
| [Charm](https://github.com/GareBear99/Charm) | Uniswap v3 Spot Bot on Base (Node.js) | [source](https://github.com/GareBear99/Charm) | [https://garebear99.github.io/Charm/](https://garebear99.github.io/Charm/) |
| [Harvest](https://github.com/GareBear99/Harvest) | Multi-Timeframe Crypto Research Platform (Python) | [source](https://github.com/GareBear99/Harvest) | [https://garebear99.github.io/Harvest/](https://garebear99.github.io/Harvest/) |
| [One-Shot-Multi-Shot](https://github.com/GareBear99/One-Shot-Multi-Shot) | Binary-Options 3-Hearts Engine (JS) | [source](https://github.com/GareBear99/One-Shot-Multi-Shot) | [https://garebear99.github.io/One-Shot-Multi-Shot/](https://garebear99.github.io/One-Shot-Multi-Shot/) |
| [DecaGrid](https://github.com/GareBear99/DecaGrid) | Capital-Ladder Grid Trading Docs Pack | [source](https://github.com/GareBear99/DecaGrid) | [https://garebear99.github.io/DecaGrid/](https://garebear99.github.io/DecaGrid/) |
| **EdgeStack Currency** (you are here) | Event-Sourced Multi-Currency Execution Spec | [source](https://github.com/GareBear99/EdgeStack_Currency) | [https://garebear99.github.io/EdgeStack_Currency/](https://garebear99.github.io/EdgeStack_Currency/) |

### Upstream + meta
- [ARC-Core](https://github.com/GareBear99/ARC-Core) — governed event + receipt spine the fleet plugs into.
- [omnibinary-runtime](https://github.com/GareBear99/omnibinary-runtime) + [Arc-RAR](https://github.com/GareBear99/Arc-RAR) — any-OS portability for deployment.
- [Portfolio](https://github.com/GareBear99/Portfolio) — full project index (audio plugins, games, simulators, AI runtimes, robotics, trading).

---

<!-- ARC-Funding-Badges-Marker -->
## 💖 Support the fleet

If this repo helps you, the maintainer runs the entire ARC ecosystem solo.
Any of the following keep the lights on:

[![Sponsor](https://img.shields.io/badge/GitHub%20Sponsors-GareBear99-ea4aaa?logo=githubsponsors&logoColor=white)](https://github.com/sponsors/GareBear99)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-garebear99-FFDD00?logo=buymeacoffee&logoColor=black)](https://www.buymeacoffee.com/garebear99)
[![Ko-fi](https://img.shields.io/badge/Ko--fi-garebear99-FF5E5B?logo=ko-fi&logoColor=white)](https://ko-fi.com/garebear99)

- **GitHub Sponsors**: <https://github.com/sponsors/GareBear99>
- **Buy Me a Coffee**: <https://www.buymeacoffee.com/garebear99>
- **Ko-fi**: <https://ko-fi.com/garebear99>

Every dollar funds hardening across **ARC-Core + the 15 consumer repos + the four roadmap repos**. One author, one funding pool.
