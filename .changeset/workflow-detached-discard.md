---
"effect": patch
---

Add `Workflow.execute(payload, { discard: true, detached: true })` for fire-and-forget child workflows. Detached children neither wake their parent on completion nor get interrupted with it. The cluster engine retains the parent for observability.

`detached` requires `discard: true`. Do not await a detached execution later: executing the same payload joins it, but its completion will not wake the awaiting workflow.
