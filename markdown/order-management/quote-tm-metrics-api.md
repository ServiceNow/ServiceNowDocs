---
title: Quote Experience metrics API
description: Reference for the Quote Experience metrics API, including query parameters, default behavior, and metric definitions for views, session time, and stage time in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-metrics-api.html
release: australia
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Quote Experience metrics API

Reference for the Quote Experience metrics API, including query parameters, default behavior, and metric definitions for views, session time, and stage time in ServiceNow CPQ.

## Overview of metrics

The Quote Experience metrics API retrieves usage data on transactions, including views by user, session time by user, and stage time. Administrators and implementers use this API to understand how users interact with quotes and how long transactions spend at each stage.

You can query a single transaction by providing its transaction ID. If no transaction ID is provided, the API returns data for all transactions within the specified time period.

## Endpoint

```
GET {{baseUrl}}/api/txn/metrics/v1/overview
```

## Query parameters

|Parameter|Type|Required|Description|
|---------|----|--------|-----------|
|`txnId`|String|No|The ID of the transaction to query. When provided, the response contains metrics for that transaction only. When omitted, the response contains metrics for all transactions in the specified time period.|
|`days`|Integer|No|The number of days to include in the query, counting back from `toDate`. The queried period is `(toDate - days) → toDate`. Defaults to `30` when not specified.|
|`toDate`|Timestamp|No|The end date and time for the query period in UTC format — for example, `2025-09-18T15:28:04Z`. When omitted, the current time is used.|

## Required headers

|Header|Value|
|------|-----|
|`X-Logik-Customer-Id`|Your tenant ID.|
|`Content-Type`|`application/json`|

## Example call

```
curl -X GET \
  "{{baseUrl}}/api/txn/metrics/v1/overview?txnId={{transactionId}}&days=30&toDate=2025-09-18T15:28:04Z" \
  -H "X-Logik-Customer-Id: <tenant-id>" \
  -H "Content-Type: application/json"
```

## Metric definitions

<table><thead><tr><th>

Metric

</th><th>

Description

</th><th>

Unit

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Views by user

</td><td>

The total number of sessions for a user in the specified time period.

</td><td>

Count

</td><td>

When filtered to a single transaction using `txnId`, sessions are counted for that transaction only.

</td></tr><tr><td>

Session time by user

</td><td>

The average time per session for each user in the specified time period.

</td><td>

Minutes

</td><td>

Sessions are calculated using activity windows based on common events, including transaction created or edited, stage enter or exit, upsert lines, and custom transaction events. A session ends five minutes after the last recorded event.

 When filtered to a single transaction, the total time for a user can be calculated as: `views per user × session time per user`.

</td></tr><tr><td>

Stage time

</td><td>

The average time a transaction spends in a specified stage.

</td><td>

Minutes

</td><td>

When filtered to a single transaction, the metric reflects the time that specific transaction spent in the specified stage.

</td></tr></tbody>
</table>**Related topics**  


[ServiceNow Quote Experience runtime API calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-runtime-api-calls.md)

