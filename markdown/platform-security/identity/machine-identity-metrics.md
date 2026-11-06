---
title: Metrics
description: Metrics of the machine identities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/identity/machine-identity-metrics.html
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Exploring Machine Identity Console, Machine Identity Console, Identity]
---

# Metrics

Metrics of the machine identities.

## Timing and retention

Metrics and scores are computed once a day at 00:01 and don't include the current day. The list pages can therefore show data that is about one day ahead of the metrics.

Request records are flushed after 30 days. User tracker records are kept for 180 days.

## Unique API calls in last 7 days

The following results are unique API calls in the last 7 days. Records collected in this table are in real-time.

**Note:** Accounts that have the **Internal Integration User** field set to `true` in their `sys_user` record will not populate data in the Machine Identity Console.

## Machine identity accounts

The following results are the machine integration accounts used for integrations. Records collected in this table are in real time.

\[Omitted image "metrics-mic-accounts.png"\] Alt text: Machine identity accounts

## High Privilege machine accounts

The following results are the high privilege machine integration accounts used for integrations. Records collected in this table are in real-time.

\[Omitted image "metrics-high-privilege.png"\] Alt text: High Privilege machine accounts

## Requests that aren't counted

The following requests are excluded from metrics. All other requests are counted and shown in the Machine Identity Console.

|Request type|Shown in the Machine Identity Console|
|------------|-------------------------------------|
|Maintenance sessions|No|
|Impersonation sessions|No|
|Failed logins|No|
|Responses with status 400, 401, or 500|No|
|MID Server traffic|No|
|Requests from internal IP addresses|No|
|GraphQL requests|No|
|OAuth requests that use the authorization code grant type|No|

The `sys_mi_resource_filter` table can include or exclude specific APIs.

