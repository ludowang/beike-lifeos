# Resource map

Copy this file to `RESOURCE_MAP.md` in your private deployment repository. Never commit the completed private file to a public repository.

| Alias | Type | Purpose | Private identifier source | Read | Write |
| --- | --- | --- | --- | --- | --- |
| diary | Feishu document | Life events and emotional weather | server secret/config | yes | append/section insert |
| ideas | Feishu document | Product and creative ideas | server secret/config | yes | append/section insert |
| reflections | Feishu document | Reading and knowledge reflections | server secret/config | yes | append/section insert |
| projects | Bitable table | Stage-based outcomes | server secret/config | yes | field patch |
| tasks | Bitable table | One-off actions | server secret/config | yes | create/field patch |
| habits | Bitable table | Repeated behaviors | server secret/config | yes | create/field patch |
| logs | Bitable table | Completed activities | server secret/config | yes | create/field patch |

## Required live-schema notes

- Primary text field:
- Status field and current options:
- Date fields and timezone:
- Relation fields:
- Read-only formula fields:
- Fields the agent must never invent:
