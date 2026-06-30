# Security Boundary

## Public capabilities

This repository may describe:

- payment-intent and receipt schemas
- synthetic XRP and RLUSD examples
- request, quote and transaction-context binding
- replay-protection concepts
- operator approval and evidence-generation flows
- public demo behavior

## Non-public capabilities

This repository does not publish or grant access to:

- wallet seeds or signing keys
- production wallet addresses or routing tables
- unrestricted signing or settlement services
- private infrastructure, service topology or operational paths
- customer or user data
- internal anti-abuse thresholds
- autonomous production payment authority

## Approval boundary

Regulated, irreversible or high-impact actions remain subject to explicit operator approval. Public examples may show that approval is required, but they do not implement or bypass the private approval ceremony.

## Evidence boundary

A NOMOS receipt can show that a defined technical verification was performed against a declared payment context. It does not establish legal compliance, ownership, solvency, tax treatment or regulatory approval.

## Usage claims

Internal demonstrations, self-pay transactions and canary tests must be clearly distinguished from:

- independent external users
- organic demand
- customer revenue
- marketplace adoption
- production-scale payment volume

The project will publish such claims only when independently evidenced.
