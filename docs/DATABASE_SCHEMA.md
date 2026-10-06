# Database Schema

## Entities

```text
User 1 ─── N Entry 1 ─── 0..1 AISummary
                 │
                 └── N EntryAsset
```

## User

| Field | Type | Rule |
| --- | --- | --- |
| id | UUID | Primary key |
| email | text | Unique, normalized |
| password_hash | text | Never returned by API |
| created_at | timestamp | Server generated |
| updated_at | timestamp | Server generated |

## Entry

| Field | Type | Rule |
| --- | --- | --- |
| id | UUID | Primary key |
| user_id | UUID | Foreign key to User |
| title | text | Required, max 160 chars |
| notes | text | Required, max 50,000 chars |
| created_at | timestamp | Indexed with user_id |
| updated_at | timestamp | Server generated |
| deleted_at | timestamp | Nullable soft-delete marker |

## EntryAsset

| Field | Type | Rule |
| --- | --- | --- |
| id | UUID | Primary key |
| entry_id | UUID | Foreign key to Entry |
| object_key | text | Private storage key |
| content_type | text | Allowlisted image type |
| byte_size | integer | Maximum enforced at upload |

## AISummary

| Field | Type | Rule |
| --- | --- | --- |
| id | UUID | Primary key |
| entry_id | UUID | Unique foreign key |
| status | enum | queued, running, complete, failed |
| text | text | Nullable until complete |
| model | text | Provider/model identifier |
| created_at | timestamp | Server generated |
| updated_at | timestamp | Server generated |

## Invariants

- A user can read and mutate only their own entries.
- A deleted entry is excluded from ordinary reads.
- An AI summary cannot exist without its entry.
- Retrying a summary updates the existing job/summary state instead of creating duplicates.
