# Security Policy

## Public repository boundary

This repository contains documentation, schemas and synthetic examples for NOMOS XRPL Agentic Payments.

It must not contain:

- wallet seeds, private keys or signing material
- API keys, tokens, credentials or private endpoints
- production wallet addresses or internal routing configuration
- customer, user or transaction-identifying data
- unrestricted transaction-signing or execution logic
- internal server paths, topology or operational runbooks

## Supported material

Security reports are accepted for the current default branch and the public demo surface linked from the README.

## Reporting

Please report suspected vulnerabilities privately to:

**contact@agentnomos.com**

Do not open a public issue containing secrets, exploit details, personal data or information that could enable unauthorized transaction activity.

## Safety model

The public project is designed around these invariants:

- authorization before execution
- request, quote and transaction-context binding
- replay resistance
- explicit approval for regulated or irreversible actions
- structured evidence after settlement
- no representation of technical evidence as legal or regulatory approval

## No production authority

Examples and advisory outputs in this repository do not authorize production payments. Real wallet access, signing, settlement and on-chain execution remain outside this public repository and require separate operator-controlled gates.
