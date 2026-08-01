---
name: Reconcile PayJoy transactions
description: Pull transactions in a time window and reconcile them against merchant/clerk records.
api: openapi/payjoy-partner-api-openapi.yml
operations: [getTransactions, getMerchants, getSalesClerks]
---

# Reconcile PayJoy transactions (Partner API V2)

Use this flow to reconcile PayJoy financing activity into a partner's ledger.

## Auth
`X-PayJoy-ApiKey` header on every request.

## Steps
1. **List transactions** — `GET /v2/transactions` (`getTransactions`). `startTime` and `endTime`
   (Unix ms timestamps) are **required** to bound the window. Each record has a `type`
   (finance / cash / adjustment), `time`, `amount`, `currency`, and embedded `merchant`, `salesClerk`,
   `device`, and `financeOrder` objects.
2. **Resolve merchants** — `GET /v2/merchants` (`getMerchants`) to map `merchant.id` → store details.
3. **Resolve clerks** — `GET /v2/clerks` (`getSalesClerks`) to map `salesClerk.id` → clerk details.

## Rules
- Cash/payment records may carry a negative `amount` (money received) — respect the sign.
- Object IDs and Tags can be up to 255 chars; store case-sensitively.
- Retry 429 with exponential backoff. Log `X-Request-ID` for support.
