# Public Architecture

## Purpose

NOMOS XRPL Agentic Payments separates payment intent, governance review, settlement and evidence generation into explicit stages.

```text
1. Agent creates a payment intent
2. NOMOS validates identity, authority, scope and policy context
3. A quote binds asset, amount, destination context and expiry
4. Human approval remains available for regulated or irreversible actions
5. The XRPL transaction is submitted by an authorized execution component
6. Settlement evidence is matched to the original request and quote
7. A structured receipt is produced for independent review
```

## Logical components

### Payment intent

A machine-readable declaration of the proposed economic action. It contains a public-safe request identifier, asset, amount, purpose and expiry. It contains no secret signing material.

### Governance preflight

An advisory evaluation of identity, declared authority, scope, spending constraints, reversibility and evidence readiness.

A positive advisory result is not itself authorization to move funds.

### Quote and request binding

The quote identifies the expected payment context and is bound to the originating request. This reduces the risk of reusing a valid payment as evidence for a different request.

### Execution boundary

Transaction signing and submission remain outside the public repository. Production execution requires separate operator-controlled authorization and safety gates.

### Settlement verification

Verification compares the observed XRPL transaction context with the expected request and quote context. Mismatches are reported rather than silently accepted.

### Evidence receipt

The receipt records the relationship between request, quote, verification result and transaction evidence. A receipt is technical evidence; it is not legal, regulatory or accounting approval.

## Trust boundaries

```text
Public client
    |
    v
Public-safe request schema
    |
    v
Advisory governance and binding layer
    |
    +----> operator approval when required
    |
    v
Private execution boundary
    |
    v
XRPL
    |
    v
Public-safe verification result and receipt
```

## Design principles

- fail closed on missing authority or mismatched evidence
- never infer successful settlement from an unverified claim
- do not expose wallet secrets or production routing
- separate advisory decisions from execution authority
- make internal/self-pay demonstrations distinguishable from external usage
- preserve clear evidence of what was checked and what remains unknown
