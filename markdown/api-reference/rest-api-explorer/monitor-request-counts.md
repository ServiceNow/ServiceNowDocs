---
title: Monitor inbound REST API rate limit counts and violations
description: To determine if you have set a rate limit rule appropriately, monitor the counts and violations for inbound REST API requests that are restricted by the rule.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inbound REST API rate limiting, REST APIs, Web services, API implementation, API implementation and reference]
---

# Monitor inbound REST API rate limit counts and violations

To determine if you have set a rate limit rule appropriately, monitor the counts and violations for inbound REST API requests that are restricted by the rule.

## Before you begin

Role required: rate\_limit\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST** &gt; **Rate Limits**.

2.  Select the rate limit rule for which you want to monitor rate limit counts and violations.

3.  View the information in the following related lists:

    -   In the Rate Limit Counts related list, view the count of inbound REST API requests limited by the rule. This list is cleared daily.
    -   In the Rate Limit Violations related list, view the number of inbound REST API requests that exceeded the **Request limit per hour** value for the rule. This list is cleared biweekly.

**Parent Topic:**[Inbound REST API rate limiting](../concept/inbound-REST-API-rate-limiting.md)

