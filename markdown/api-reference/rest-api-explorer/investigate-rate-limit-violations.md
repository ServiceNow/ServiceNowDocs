---
title: Investigate inbound REST API rate limit violations
description: Investigate rate limit violations to determine which rate limit rules are being exceeded and which users are exceeding those rate limits.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inbound REST API rate limiting, REST APIs, Web services, API implementation, API implementation and reference]
---

# Investigate inbound REST API rate limit violations

Investigate rate limit violations to determine which rate limit rules are being exceeded and which users are exceeding those rate limits.

## Before you begin

Role required: rate\_limit\_admin

## About this task

Violations are created when inbound REST API requests reach the maximum allowed request count for a specific REST API for that hour.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST** &gt; **Rate Limit Violations**.

2.  On the Rate Limit Violations page, select the rate limit rule that you want to investigate.

3.  On the Rate Limit Violations related list, review the violations by user. This list is cleared biweekly.


## What to do next

You may need to reevaluate the **Request limit per hour** value for a rate limit rule, depending on the number of violations of that rule. You may also need to educate users about rate limits, depending on how many times specific users violate rate limit rules.

**Parent Topic:**[Inbound REST API rate limiting](../concept/inbound-REST-API-rate-limiting.md)

