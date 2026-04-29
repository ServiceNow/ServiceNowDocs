---
title: Share subscription data from another instance
description: View subscription data from another instance by enabling data sharing on that instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Share subscription data from another instance

View subscription data from another instance by enabling data sharing on that instance.

## Before you begin

Role required: usage\_admin, sn\_sub\_man.admin, or admin

## About this task

By default, data sharing is restricted between production instances, which means you can't see subscription data for other production instances in Subscription Management. To view subscription data from another production instance, modify the trust configuration settings on that instance.

For more information about modifying the trust configuration for an instance, see [Basic trust configuration for data sync applications](../../core-configuration/concept/grant-access-other-instances.md).

**Note:** Subscription data from a non-production instance is only viewable from a production instance.

In this scenario, the instance for viewing subscription data across all your instances is considered the primary production instance.

## Procedure

1.  Log in to the instance that has subscription data that you want to view on your primary production instance.

2.  Navigate to **All** &gt; **Multi-Instance Management** &gt; **Trust Configuration**.

3.  In the list of instances, find the primary production instance.

4.  Share data from your current instance by changing the value in the **Grant access** column to true.


## Result

Subscription data is shared with your primary production instance.

## What to do next

Log in to your primary production instance to view the subscription data that is now shared with that instance. Repeat these steps for each additional production instance that has subscription data that you want to view from the primary production instance.

**Parent Topic:**[Configuring Subscription Management](../concept/configuring-subscription-management-v2.md)

