---
title: Maintain per-user subscription allocations in Subscription Management at renewal
description: Ensure subscription allocations remain consistent throughout the renewal process.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-10-07"
reading_time_minutes: 1
breadcrumb: [Managing per-user subscriptions, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Maintain per-user subscription allocations in Subscription Management at renewal

Ensure subscription allocations remain consistent throughout the renewal process.

## Before you begin

Role required: admin

## About this task

When a per-user subscription renews, a new product SKU might be added to your account. This SKU is treated as a new product subscription in Subscription Management, requiring you to re-allocate subscriptions by adding groups with measured roles to the subscription.

## Procedure

1.  Before the renewal date, monitor the subscription end dates on the details page and document the current group allocations.

    See [Viewing product subscription details in Subscription Management](../concept/subscription-details-v2.md).

2.  After the renewal date, add the documented groups to the renewed subscription in Subscription Management.

    See [Allocate subscriptions in Subscription Management](allocate-subscriptions-v2.md).


## What to do next

Continue to monitor subscription renewal dates to ensure that your allocations are accurate throughout each renewal.

**Parent Topic:**[Managing per-user subscriptions in Subscription Management](../concept/managing-user-subscriptions-v2.md)

