# SolSentry

> Threat intelligence for Solana, focused on the people behind the tokens.
>
> *RugCheck shows you a fire. SolSentry shows you who lit it.*

We map the operators behind Solana scams: the wallets that deploy rug after rug.
That operator graph becomes a pre-trade signal for wallets, bots and AI agents.

Live at [solsentry.app](https://solsentry.app). The API is at
[api.solsentry.app](https://api.solsentry.app/v1/stats).

We don't hard-code numbers in this README. CRITICAL precision and resolved predictions are
whatever [`/v1/stats`](https://api.solsentry.app/v1/stats) returns
right now. Each prediction can be checked one mint at a time at `/v1/predictions/{mint}`.

## What it does

Most tools score a token: is this contract dangerous right now. SolSentry scores the
operator. That means the wallet that deployed the token, what it deployed before, and the
cluster it belongs to. A bytecode audit can't answer that question.

Query it live, no key needed:

```bash
curl https://api.solsentry.app/v1/operator/<wallet>
curl https://api.solsentry.app/v1/token/<mint>
curl https://api.solsentry.app/v1/predictions/<mint>
```

## Open repos

| Repo | What it is |
|---|---|
| [solsentry-app](https://github.com/solsentry/solsentry-app) | The web app: landing page, operator and token lookup, live dashboards |
| [solsentry-docs](https://github.com/solsentry/solsentry-docs) | Methodology, install guides, API reference |
| [solsentry-mcp](https://github.com/solsentry/solsentry-mcp) | Zero-install MCP server that gives any AI agent SolSentry lookups ([`@solsentry/mcp`](https://www.npmjs.com/package/@solsentry/mcp) on npm) |
| [solsentry-guard](https://github.com/solsentry/solsentry-guard) | Risk checks before you sign a Solana transaction |
| [solana-counterparty-gate](https://github.com/solsentry/solana-counterparty-gate) | Operator-level counterparty risk, packaged as a coding-agent skill |

The core intelligence engine is private. The repos above are the parts you can install
and build on.

## Contact

Web: [solsentry.app](https://solsentry.app) ·
X: [@solsentryai](https://x.com/solsentryai) ·
Telegram: [t.me/solsentryai](https://t.me/solsentryai) ·
Email: hello@solsentry.app

Built in Brazil by Crash Diniz. We rank operators for human review and don't publish
accusations.
