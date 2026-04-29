---
title: Configure subscription allocation status in Subscription Management
description: Identify when you're close to allocating all of your subscriptions by configuring an allocation status threshold if you prefer a threshold other than the default value of 90 percent in Subscription Management.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Configure subscription allocation status in Subscription Management

Identify when you're close to allocating all of your subscriptions by configuring an allocation status threshold if you prefer a threshold other than the default value of 90 percent in Subscription Management.

## Before you begin

Role required: usage\_admin, sn\_sub\_man.admin, or admin

## Procedure

1.  Navigate to the **Settings** tab in one of the following ways.

    -   Navigate to **Admin** &gt; **Subscription Management** &gt; **Settings**.
    -   Navigate to **All** &gt; **Subscription Management** &gt; **Settings**.
2.  In the **Allocation Status** tab, enter a percentage value that represents near capacity for your instance.

    If you want the **Status** column to display Near capacity before reaching the 90 percent threshold, enter a lower percentage value.

3.  Select **Save**.


## Result

When the number of allocated subscriptions exceeds the percentage you configured, the value Near capacity appears in the **Status** column throughout Subscription Management.

**Parent Topic:**[Configuring Subscription Management](../concept/configuring-subscription-management-v2.md)

