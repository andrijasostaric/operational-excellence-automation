# Future-State Workflow

```text
Business request
      ↓
Structured intake form
      ↓
Completeness validation
      ↓
Risk classification
      ↓
Compliance / security review if required
      ↓
Business owner approval
      ↓
Finance / Operations setup
      ↓
Evidence archive + status confirmation
      ↓
Periodic review trigger
```

## Ownership model

| Stage | Primary owner | Supporting functions |
|---|---|---|
| Intake | Requester | Operations |
| Completeness check | Operations | Requester |
| Risk classification | Operations / Risk | Compliance, Security |
| Due diligence | Relevant control owner | Legal, Security, Compliance |
| Business approval | Budget / service owner | Finance |
| Vendor setup | Finance / Operations | Procurement |
| Evidence retention | Operations | Control owners |
| Periodic review | Vendor owner | Risk / Compliance |

## Design principles

- Mandatory information collected once at the start.
- Risk level determines the depth of review.
- Workflow cannot move to setup before required approvals are complete.
- Exceptions are visible rather than hidden in email.
- Every approval has an owner, timestamp and outcome.
- Evidence is retained with the vendor record.
