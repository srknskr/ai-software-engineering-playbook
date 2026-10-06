# User Flows

## Create an entry

```text
Open app
  ↓
Authenticated?
  ├─ No → Sign in → Dashboard
  └─ Yes
       ↓
  Tap New entry
       ↓
  Enter title and notes
       ↓
  Optional image upload
       ├─ Fails → Explain error → Retry or continue without image
       └─ Succeeds
       ↓
  Save
       ├─ Invalid → Keep input → Show field errors
       ├─ Network failure → Keep draft → Offer retry
       └─ Success → Entry detail
```

## Request an AI summary

```text
Open entry detail
  ↓
Tap Generate summary
  ↓
Show progress and disable duplicate requests
  ├─ Success → Show summary with AI label
  ├─ Timeout → Show retry action
  └─ Provider error → Show safe message and preserve notes
```

## Delete an entry

```text
Open entry detail → Delete → Confirmation dialog
  ├─ Cancel → Return to detail
  └─ Confirm → Delete owned entry → Return to list
```

## Flow rules

- Every destructive action requires confirmation.
- Every asynchronous action has loading, success, and failure states.
- A failed secondary action must not erase successful primary data.
- Deep links to private entries require authentication and ownership.
