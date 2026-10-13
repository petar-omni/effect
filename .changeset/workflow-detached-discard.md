---
"effect": patch
---

Add a `detached` option to `Workflow.execute` for fire-and-forget child workflows: `MyWorkflow.execute(payload, { discard: true, detached: true })`.

A detached execution started inside another workflow still records that workflow as its parent, but its completion never wakes the parent and interrupting the parent does not interrupt it. `detached` is only accepted alongside `discard: true`, in the types and at runtime. A detached execution cannot be awaited later: a subsequent `execute` of the same payload joins it and is not woken when it completes.
