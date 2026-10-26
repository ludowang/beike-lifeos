# Build with your Agent

This guide assumes you already use Feishu and can give an agent controlled access to selected documents and Bitable bases.

## Phase 1: map what already exists

Ask the agent to inspect, read-only:

- which documents hold diary, ideas, reflections and principles;
- which tables hold projects, tasks, habits and activity logs;
- the live field names and select options;
- which resources the bot application can actually access.

The output should be a proposed `RESOURCE_MAP.md`. Do not paste tokens or secrets into it.

## Phase 2: choose one real path

Start with one capability, for example:

> “今天散步的时候想到了一件事……” → search today's diary → find the same event or create it → append the new expression → read back.

Test with content the owner is comfortable writing. Do not manufacture production records only to make a demo look complete.

Acceptance checks:

1. Repeating the same input does not duplicate it.
2. A later supplement goes under the original event.
3. Two similar candidate events cause a clarification.
4. A failed write is reported as failed or uncertain, not successful.

## Phase 3: add routing

Use `templates/LIFE_ROUTING_POLICY.md` as a starting point, then adapt it to the owner's actual system.

Recommended destinations:

- conversation only;
- future task;
- long-running habit;
- completed activity log;
- diary event;
- product or creative idea;
- reflection or knowledge note.

Do not classify ordinary emotion as a task. Do not turn every repeated activity into a new habit.

## Phase 4: add idea continuation

Structure idea documents with stable headings. Search by core problem, scenario, target user and mechanism. If one topic is a clear match, append a dated evolution note. Preserve the original version so the change in thinking remains visible.

## Phase 5: harden the system

Add:

- an operation ledger or equivalent idempotency key;
- per-resource write locks;
- stale-value checks before patches;
- readback verification;
- concise audit metadata without private body text;
- backups before broad structural changes.

## Prompt to start implementation

```text
Read this repository as a blueprint. First inspect my existing Feishu resources in read-only mode. Do not create, modify, deploy, or publish anything yet. Produce:
1. a resource map;
2. the smallest useful end-to-end path;
3. the exact permissions required;
4. five acceptance tests, including ambiguity and duplicate-message tests;
5. the privacy risks you found.
Wait for my confirmation before performing the first write.
```
