---
title: Reset an inbound REST API rate limit
description: Reset a rate limit rule to reset the rate limit count to zero \(0\) and delete any violations for the current hour.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inbound REST API rate limiting, REST APIs, Web services, API implementation, API implementation and reference]
---

# Reset an inbound REST API rate limit

Reset a rate limit rule to reset the rate limit count to zero \(0\) and delete any violations for the current hour.

## Before you begin

Role required: rate\_limit\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST** &gt; **Rate Limit Rules**.

2.  Select the rate limit rule for which you want to reset the rate limit count.

3.  Click the **Reset Rate Limit Counts** related link.


## Result

For the current hour, the system resets the rate limit count for the rate limit rule to zero \(0\) and removes all violations. The system begins incrementing the rate limit counts and violations as REST API requests are received for processing.

**Parent Topic:**[Inbound REST API rate limiting](../concept/inbound-REST-API-rate-limiting.md)

