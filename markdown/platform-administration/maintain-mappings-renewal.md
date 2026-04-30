---
title: Maintain custom table and application mappings at renewal in Subscription Management
description: Ensure custom table and application mappings remain consistent throughout the renewal process.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing custom tables and apps, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Maintain custom table and application mappings at renewal in Subscription Management

Ensure custom table and application mappings remain consistent throughout the renewal process.

## Before you begin

Role required: usage\_admin, sn\_sub\_man.admin, oradmin

## About this task

When a subscription renews, a new product SKU might be added to your account. This SKU is treated as a new product subscription in Subscription Management, requiring you to re-map custom applications and custom tables to the subscription to stay in compliance.

## Procedure

1.  Before the renewal date, monitor the subscription end dates and document the current list of custom application and custom table mappings.

    See [Viewing product subscription details in Subscription Management](../concept/subscription-details-v2.md).

2.  After the renewal date, map the documented tables and applications to the renewed subscription in Subscription Management.

    See [Map a custom application to a product subscription in Subscription Management](map-custom-applications-v2.md) and [Map custom tables to a product subscription in Subscription Management](allocate-custom-table-subsc-app-v2.md).


## What to do next

Continue to monitor subscription renewal dates to ensure that your mappings are accurate throughout each renewal.

**Parent Topic:**[Managing custom tables and applications in Subscription Management](../concept/allocating-custom-tables-subscr-apps-v2.md)

