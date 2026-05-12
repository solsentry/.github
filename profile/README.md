# 🛡️ SolSentry

> **The autonomous threat-intelligence layer for Solana.**
> *RugCheck tells you a fire is burning. SolSentry tells you who lit it.*

We map the **operators** behind Solana scams — the wallets that deploy serial rugs — and turn that graph into pre-trade signals for wallets, bots, and AI agents.

🔴 **Live**: [solsentry.app](https://solsentry.app) · [api.solsentry.app/v1/stats](https://api.solsentry.app/v1/stats) · **28+ days** continuous on Hetzner VPS
📊 **Current snapshot**: **88.1% accuracy** · **51K+ scans** · **5,512 operators tracked** · **1,279 serial deployers** · **18,987 confirmed rugs** · zero confirmed false positives at CRITICAL

---

## The case we keep telling

`4kxscute` — known wallet, **2,532 tokens deployed, 2,352 confirmed rugs (92.9% rug rate)**. Zero indexed mentions on Twitter, Reddit, Solscan labels, RugCheck, or Nansen until SolSentry tagged the operator. We made hundreds of predictions on this wallet, with average lead time of **~19 minutes** between deploy and CRITICAL alert.

Queryable now:
```bash
curl https://api.solsentry.app/v1/operator/4kxscuteRLQdNiTXA33YYsvywAPNA6DQTifswxjL5pH1
```

That's the product.

---

## What just shipped (Frontier 2026, last 7 days)

| Integration | Status | What it does |
|---|---|---|
| **Dune Sim SVM API** | Production | 4 forensics modules consume real-time tx data (1,824 LOC of consumers) |
| **Covalent / GoldRush** | Deployed VPS | Wallet portfolio enrichment + spam cross-validation (cross-chain ready) |
| **Zerion CLI** | Deployed VPS | Autonomous-agent enrichment — multi-chain portfolio + PnL via shell command |
| **RPC Fast** | Deployed VPS | Tier-0 round-robin peer in our 11-endpoint RPC pool |
| **Cloak shielded transfers** | Scaffold + rapport | "Privacy without impunity" — operator-screen before private transfer |
| **Umbra privacy rail** | Scaffold | Second privacy rail, same operator-screen substrate (rail-agnostic) |
| **x402 payment enforcement** | Production | Mainnet-ready paid endpoints + Cloak/Zerion pay-per-call |
| **Self-heal pipeline** | Production | 2,400+ auto-repair attempts on missing dev_wallet / token symbol |

---

## Public repositories

| Repo | What it is |
|------|------------|
| [**solsentry-app**](https://github.com/solsentry/solsentry-app) | Next.js 15 web app — landing, live operator lookup, x402 dashboard |
| [**solsentry-mcp**](https://github.com/solsentry/solsentry-mcp) | Zero-install MCP server — 11 tools for AI agents (`@solsentry/mcp` on NPM) |
| [**solsentry-docs**](https://github.com/solsentry/solsentry-docs) | Technical documentation, integration guides, threat model, roadmap |
| [**solsentry-nansen-cli**](https://github.com/solsentry/solsentry-nansen-cli) | CLI tool from the Drift Protocol $285M hack investigation |
| [**thegarage**](https://github.com/solsentry/thegarage) | PFP/banner duotone generator for Superteam Brasil's THE/GARAGE cohort |

The core product code (`solsentry/solsentry`) lives in a private repository. Hackathon judges and review partners get access on request — contact `hello@solsentry.app`.

---

## Roadmap (short horizon, Q2–Q3 2026)

**Now → Frontier deadline (May 12, 2026):**
- ✅ Multi-source data layer (Helius + Dune Sim + Covalent + Zerion)
- ✅ Two privacy rails wired (Cloak + Umbra)
- ✅ 11-endpoint RPC pool with health-aware load balancing
- ✅ x402 mainnet enforcement scaffold

**Post-Frontier (May–July 2026):**
- Public dashboard refactor → solsentry.app/v2 with operator graph visualization
- `@solsentry/jupiter-shield` SDK — operator-aware routing for Jupiter Strict Mode v2
- `@solsentry/privacy-shield` SDK — rail-agnostic operator-screen middleware
- Cross-chain investigation walker (Solana → EVM via Covalent + Zerion)
- Pricing tier launch on x402 (`$0.001–$0.01` per `/v1/operator/{wallet}` micropayment)

**Q3 2026:**
- Multi-tenant API + customer-specific scoring deltas
- Phantom / Backpack wallet integration
- 1-2 trading bot integrations (Trojan, BONKbot)
- Audit (target: Adevar Labs, OtterSec, or Neodyme)

---

## Where SolSentry fits in the Solana security stack

| Layer | What it covers | Example tools |
|---|---|---|
| Token classification | Single mint at a time | RugCheck, GoPlus |
| Wallet classification | Single wallet at a time | Webacy, Chainabuse |
| **Operator intelligence** | **The human/wallet cluster behind N tokens, over time** | **SolSentry** |
| Compliance | KYC, sanctions, AML | Chainalysis, TRM |

The operator-intelligence layer was missing. SolSentry sits below RugCheck/Webacy in the data flow — they classify the artifacts, we classify the deployers. Cross-attack memory is what makes the difference.

---

## Market opportunity (honest seed-scale projections)

**TAM** — every Solana wallet interaction needing operator-risk pre-check:
- $125M ARR consumer end (25M wallet MAUs × $5/user/year analog)
- $30M–$150M ARR B2B end ($600B annualized DEX volume × 1–5 bps fraud-tool benchmark)

**SAM** — Solana-native integrations reachable in 18 months:
- 3 major wallets + top 5 trading bots + 2 aggregators
- $600K–$6M ARR at $0.001–$0.01 per operator check, 50M checks/month

**SOM** — 12-month capture at 10–25%:
- Conservative: $600K ARR · Target: $1.5M ARR · Stretch: $3M ARR

These are floor numbers, not the moonshot. Consistent with Helius's early traction trajectory.

---

## Where to find us

🌐 **Web**: [solsentry.app](https://solsentry.app)
🐦 **X / Twitter**: [@solsentryapp](https://x.com/solsentryapp)
✈️ **Telegram**: [t.me/solsentryai](https://t.me/solsentryai)
📦 **NPM**: [`@solsentry/mcp`](https://www.npmjs.com/package/@solsentry/mcp)
📧 **Email**: hello@solsentry.app
🇧🇷 **Built by** Crash Diniz, solo founder, Ribeirão Preto / São Paulo, Brazil

**Hackathon**: Colosseum Frontier 2026 · [Arena profile](https://arena.colosseum.org/projects/explore/solsentry-3)
