# Privacy and release checklist

Personalization becomes valuable because the system sees private context. That makes privacy architecture part of the product, not a cleanup step.

## Never publish

- Feishu app ID or secret;
- access or refresh tokens;
- tenant URLs and internal account identifiers;
- document, folder, base, table, view or record IDs;
- unredacted chat screenshots;
- real names, companies, applications, schedules or health information;
- full private policy files that contain allowlisted URLs.

## Public examples

The case cards in this repository are truthful excerpts from real use, but they are re-typeset and redacted. They are not raw screenshots and should not be used to reconstruct the original conversation.

## Before every release

1. Search tracked files for tokens, IDs, tenant domains and local paths.
2. Review every image at full resolution.
3. Confirm that browser chrome and sidebars do not expose unrelated chats.
4. Confirm that examples cannot be linked back to a specific employer, application, address or account.
5. Keep the private implementation and public blueprint in separate repositories.
6. Verify that production deployment is unchanged.
