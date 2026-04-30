---
title: Apply rate limit on REST APIs
description: Apply rate limit to REST APIs to avoid excessive use or abuse of publicly available catalog items.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enable public access on REST APIs, Enable public access for a catalog item, Submit catalog item as a guest, Configure the Customer and Consumer Service Portals, Set up self-service, Configure, Customer Service Management]
---

# Apply rate limit on REST APIs

Apply rate limit to REST APIs to avoid excessive use or abuse of publicly available catalog items.

## Before you begin

Role required: admin, catalog\_admin, web\_service\_admin

## About this task

Rate limit restricts the uncontrolled creation of publicly available catalog items, mitigating risks associated with malicious actors and automated bots.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Rate Limit Rules**.

2.  Select **New**.

    ![showing rate limit rules form](../image/ratelimit-rules.png)

3.  On the REST API Rate Limit Rule form, fill in the fields.

    For a description of the field values, see [Rate limit rule form for guest user access to catalog items](../reference/rate-limit-for-guest-user-access-to-catalog-items.md).

4.  Select **Submit**.


## Result

A rate limit is applied to the publicly available APIs.

**Parent Topic:**[Enable public access on REST APIs](enable-publicaccess-for-restapis-csm-portal.md)

**Related topics**  


[Create an inbound REST API rate limit](https://www.servicenow.com/docs/access?context=create-REST-API-rate-limits&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

