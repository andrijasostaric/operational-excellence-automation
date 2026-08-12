# Automation Design

## Example Power Automate-style logic

```text
Trigger: new vendor request submitted
  → Validate mandatory fields
  → If incomplete: return to requester with missing fields
  → If complete: create tracking record
  → Determine risk tier
      → Low: standard approval path
      → Medium/High: route to required control owners
  → Wait for approvals
      → If rejected: notify requester and close
      → If approved: route to Finance / Operations setup
  → Confirm setup
  → Store evidence links and approval history
  → Notify requester of completion
  → Create periodic review date
```

## Automation candidates

| Step | Automate? | Rationale |
|---|---|---|
| Intake validation | Yes | Rules are repeatable and objective |
| Routing by risk tier | Yes | Reduces manual coordination |
| Approval reminders | Yes | Prevents avoidable delays |
| Risk judgement itself | No | Requires accountable human assessment |
| Final risk acceptance | No | Must remain an explicit human decision |
| Status notifications | Yes | Reduces manual chasing |
| Periodic review trigger | Yes | Date-driven and repeatable |

## Exception handling

Automation should not hide exceptions. Any request exceeding its SLA, missing an owner or failing an approval should be surfaced in an exception view for human action.

## Auditability

Each automated step should retain enough information to answer:
- who initiated the request;
- which checks were required;
- who approved or rejected it;
- when each decision occurred;
- where supporting evidence is stored;
- when the next review is due.
