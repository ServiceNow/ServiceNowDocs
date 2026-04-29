---
title: Transaction Manager: Transaction metrics API
description: Use an API call to obtain user views, user session time, and time spent at a stage.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager: Transaction metrics API

Use an API call to obtain user views, user session time, and time spent at a stage.

Transaction Manager provides an API to retrieve metrics on transactions. Metrics include views by user, session time by user, and stage time.

You can query a single transaction by sending the transaction ID. If no transaction ID is provided, all transaction data is returned.

By default, a call returns metrics for the last 30 days. Different periods can be specified by including a date range parameter. The date range parameter specifies `toDate` and `days`, which get statistics from `(toDate - days) -> toDate`. If no `toDate` is provided, the current time is assumed.

Example call:

```
curl -X GET "{{baseUrl}}/api/txn/metrics/v1/overview?txnId={{transactionId}}&days=30&toDate=2025-09-18T15:28:04Z" \
  -H "X-Logik-Customer-Id: <tenant-id>" \
  -H "Content-Type: application/json"
```

## Metrics details

Views by user:

-   The total sessions for a user in the specified time period
-   Unit: count

If filtered to a single transaction, sessions are for only that transaction.

Session time by user:

-   The average time per session of each user
-   Unit: minutes

Sessions are calculated using activity windows based on common events, including transaction created or edited, stage enter or exit, upsert lines, and custom transaction events. There is a five-minute threshold after the last event to end the session.

If filtered to a single transaction, the total time for a user can be calculated by multiplying the views per user by the session time per user.

Stage time:

-   The average time that a transaction spends in a specified stage
-   Unit: minutes

If filtered to a single transaction, the metric reflects the time that the transaction was in the specified stage.

