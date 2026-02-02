---
id: STD-001
title: ISO-8601 Date Compliance
status: mandatory
channels: [api, events, a2a, mcp]
last_updated: 2023-10-27
---

# ISO-8601 Date Compliance

## Definition
All timestamps transmitted across any interface **MUST** follow the ISO-8601 format using UTC.

## Standard
`YYYY-MM-DDTHH:mm:ssZ`

## Guardian Rule (for AI Agents)
- **Constraint:** Reject any payload using Unix Epoch or local timezone offsets.
- **Reference:** [RFC 3339](https://datatracker.ietf.org)

## Examples
### ✅ Correct
```json
{ "created_at": "2023-10-27T10:00:00Z" }
```

### ❌ Incorrect
```json
{ "created_at": "1698393600" }
```
