# KittyPunch-Analytics

Comprehensive on-chain analytics for **PunchSwap V2/V3** on the **Flow EVM** network.  
This repository contains SQL queries and dashboards used for analysis on [Dune Analytics](https://dune.com/databomb/kittypunch-flow-evm).

---

## Overview

The project aggregates activity data from 'flow.traces' and 'flow.traces_decoded' tables to measure and compare user engagement across decentralized exchange (DEX) protocols:

| Protocol | Source Table | Description |
|-----------|---------------|-------------|
| **PunchSwap V2** | 'flow.traces_decoded', https://defillama.com/protocol/kittypunch-punchswap| Aggregated decoded function calls |
| **PunchSwap V3** | 'flow.traces', https://defillama.com/protocol/kittypunch-punchswap-v3 | Low-level on-chain traces for all V3 core contracts |

---

## Metrics Tracked

| Metric | Description |
|--------|-------------|
| **User Activity** | **DAU (Daily Active Users)** | Number of unique wallets interacting with PunchSwap V2/V3 each day |
| **WAU (Weekly Active Users)** | Number of unique wallets interacting within a rolling 7-day period |
| **MAU (Monthly Active Users)** | Number of unique wallets active during each month |
| **DEX Performance** | **TVL (Total Value Locked)** | The total USD value of all assets locked across PunchSwap liquidity pools |
| **Cumulative Volume** | Total trading volume (USD) since the protocol launch |
| **Cumulative Fees** | Total fees collected by liquidity providers and protocol since inception |
| **Daily DEX Volume** | Day-by-day trading activity across all pairs on PunchSwap |
| **Daily Fees** | Fees generated per day across all protocol pools |
| **Comparative Insights** | **V2 vs V3 Activity** | Evaluates user adoption and liquidity migration between versions |
| **Growth Rate** | Measures user and TVL growth momentum over time |
| **Ecosystem Scope** | **Kitty + PunchSwap Aggregates** | Combined view of total ecosystem TVL, fees, and user base |

---

## Data Sources

| Dataset | Description |
|----------|-------------|
| 'flow.traces' | Raw execution-level transactions (V3, core calls) |
| 'flow.traces_decoded' | Decoded contract interactions (V2) |

---

## Methodology

All queries normalize 'to' and 'from' addresses via 'FROM_HEX()' and 'TO_HEX()' for proper joining and user tracking.  
Metrics are grouped using 'DATE_TRUNC()' for day, week, and month granularity.  
Each protocol is mapped to its verified contract addresses on Flow EVM.

---

## Dune Dashboard

Explore the full dashboard:  
[PunchSwap V2/V3 Overview Dune](https://dune.com/databomb/kittypunch-flow-evm)

---

## Files

| File | Purpose |
|------|----------|
| **queries.yml** | Contains parameterized Dune SQL queries used in the dashboard |
| **README.md** | Project overview and documentation |

---

## Contact

Maintained by **@ilyutkinn**  
Built for transparent analytics in the Flow ecosystem
oleg.miller223@gmail.com

---
