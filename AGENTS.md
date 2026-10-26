# Instructions for the implementing agent

Your job is to help the owner build their own LifeOS. Do not copy the original owner's resource identifiers, private records, wording, or assumptions.

## Required order

1. Read `README.md`, `docs/ARCHITECTURE.md`, `docs/PRIVACY.md`, and `templates/LIFE_ROUTING_POLICY.md`.
2. Inventory the new owner's existing Feishu documents and Bitable tables using read-only access.
3. Draft `RESOURCE_MAP.md` from `templates/RESOURCE_MAP.example.md`.
4. Show the owner the proposed resource map, routing rules, permissions, and test plan.
5. Wait for explicit approval before creating documents, changing schemas, or writing real records.
6. Implement one narrow path first: natural input → search → one safe write → readback.
7. Test ambiguous matches, repeated messages, failed writes, and user-specified destinations.
8. Expand to diary, ideas, tasks, habits, and activity logs only after the first path passes.

## Non-negotiable safety rules

- Never commit app secrets, access tokens, tenant identifiers, document IDs, table IDs, user names, or private text.
- Never assume the example field names match the owner's Feishu schema. Read the live schema first.
- Never create fields or select options merely to make an input fit.
- Never overwrite an entire document when append or local patch is possible.
- Never report success from an API response alone. Read the target back and compare the relevant content.
- If the user says “只聊不记”, perform no persistent write.
- If the user names a destination, that destination overrides automatic classification.
- If there are multiple plausible old records, ask one short clarification question and do not write.
- Preserve the owner's wording separately from the agent's interpretation.

## Definition of done

The system is not done because prompts or policy files exist. A capability is done only when a real, owner-approved test proves:

- the correct existing content was found;
- the intended record was created or updated;
- a duplicate message did not duplicate data;
- the stored result was read back successfully;
- ambiguity caused a clarification rather than a wrong write;
- no unrelated resource or schema was changed.
