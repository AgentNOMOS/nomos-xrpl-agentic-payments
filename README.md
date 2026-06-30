# NOMOS XRPL Agentic Payments

> Verified agentic payments on the XRP Ledger with governance before execution and evidence after settlement.

NOMOS XRPL Agentic Payments is a public-safe demonstration and developer reference for AI-agent payment flows on the XRP Ledger.

AI agents can initiate economic actions, but businesses still need verifiable controls around identity, authorization, intent, spending boundaries, replay protection and audit evidence. NOMOS adds that control layer around XRP and RLUSD payment workflows.

## What the project does

```text
Agent payment request
        |
        v
Identity -> Authority -> Intent binding -> Policy checks -> Human gate when required
        |
        v
XRPL payment flow
        |
        v
Transaction-bound, verifiable receipt
```

The design focuses on:

- binding a payment request to a specific quote and transaction context
- preventing replay and mismatched settlement evidence
- keeping regulated or irreversible actions behind explicit approval gates
- producing structured receipts that can be independently reviewed
- supporting agent-native discovery and integration patterns

## Current status

- Public XRPL demo: [agentnomos.com/xrpl-agentic-payments](https://agentnomos.com/xrpl-agentic-payments/)
- XRP Ledger Mainnet payment flow: internally demonstrated
- Request/quote/transaction binding: implemented and tested in the private production stack
- XRP and RLUSD integration work: active development
- External customer payments: not yet claimed
- Revenue or marketplace adoption: not yet claimed
- Autonomous wallet execution: not exposed by this public repository

This repository documents the public architecture, contracts and synthetic examples. It does **not** publish production credentials, wallet seeds, private infrastructure, customer data or unrestricted execution paths.

## Why XRPL

XRPL provides fast settlement, deterministic transaction identifiers, low transaction costs and native support for issued assets. These properties make it suitable for machine-to-machine payment workflows where each economic action must be traceable and linked to a specific authorization context.

## Repository structure

```text
docs/       Public architecture, security model and evidence model
examples/   Synthetic payment intents and receipts
schemas/    Public-safe machine-readable contracts
```

## Public demo

The public demonstration explains the payment lifecycle and the governance boundary:

- Demo: [https://agentnomos.com/xrpl-agentic-payments/](https://agentnomos.com/xrpl-agentic-payments/)
- AgentNOMOS: [https://agentnomos.com](https://agentnomos.com)

## Safety boundary

The public repository must never:

- contain wallet seeds, signing keys, credentials or private endpoints
- expose production wallet addresses or internal payment routing
- initiate or sign real transactions
- bypass spending limits, authorization or human approval gates
- claim external users, revenue or adoption without evidence
- present a technical receipt as regulatory approval

See [SECURITY.md](SECURITY.md) and [docs/security-boundary.md](docs/security-boundary.md).

## Make Waves on XRPL

This project is being developed for the Make Waves on XRPL program. The competition work focuses on turning the existing proof into a developer-ready public product, improving integration documentation and onboarding genuine external usage without weakening the governance boundary.

## Roadmap

- [x] Public XRPL agentic-payments demo
- [x] Mainnet proof of the core payment lifecycle
- [x] Request-to-quote-to-transaction binding tests
- [ ] Public developer SDK and verifier
- [ ] Controlled external inbound pilot
- [ ] Independent external users and transactions
- [ ] Public metrics with clear self-pay/internal exclusions
- [ ] RLUSD production-readiness review

## License

Licensed under the [MIT No Attribution License](LICENSE) (`MIT-0`).

The license applies only to material published in this repository. It does not grant access to private AgentNOMOS infrastructure, credentials, hosted services, customer data or non-public execution capabilities.
