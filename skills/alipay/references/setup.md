# Setup - Alipay

Read this when `<state_root>/` is missing or empty.
Keep setup practical and non-blocking.

## Operating Priorities

- Answer the immediate user request first.
- Confirm platform and payment architecture early.
- Avoid long onboarding before delivering value.

## First Activation Flow

1. Confirm what is being integrated now:
- Web or H5 checkout
- In-app checkout via SDK handoff
- PSP handoff flow
- Recurring or subscription behavior

2. Confirm environment and merchant readiness:
- Test or production target
- App id and signing key status
- Notify and return URL configuration status
- Fallback payment method availability

3. Confirm business constraints:
- Single country or multi-country launch
- Authorization and capture flow requirements
- Refund and support expectations

4. After resolving `<state_root>` and receiving approval to persist operational notes, initialize only the needed state paths:
```bash
mkdir -p <state_root>
touch <state_root>/{memory.md,implementations.md,validation-log.md,incidents.md}
chmod 700 <state_root>
chmod 600 <state_root>/{memory.md,implementations.md,validation-log.md,incidents.md}
```

5. If `<state_root>/memory.md` is empty, initialize it from `references/memory-template.md`.

## Integration Defaults

- Start in test mode unless user explicitly requests production checks.
- Prefer one checkout path at a time per ticket.
- Require fallback behavior documentation before go-live recommendations.
- Require callback verification and idempotency strategy before enabling retries.

## What to Save

- Active platform, path, and PSP scope
- Merchant and signing readiness status
- Validation outcomes and unresolved risks
- Incident signatures and mitigation status
- Launch readiness and rollback state

## Guardrails

- Never ask the user to expose private keys in chat.
- Never store raw signed Alipay payloads in local notes.
- Never claim production readiness without validation evidence.
