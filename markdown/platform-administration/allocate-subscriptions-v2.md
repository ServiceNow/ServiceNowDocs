---
title: Allocate subscriptions in Subscription Management
description: Give users entitlement to ServiceNow products by allocating subscriptions in Subscription Management.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing per-user subscriptions, Subscription Management, Get started, Administer]
---

# Allocate subscriptions in Subscription Management

Give users entitlement to ServiceNow products by allocating subscriptions in Subscription Management.

## Before you begin

Role required: usage\_admin, sn\_sub\_man.admin, oradmin

## About this task

To simplify the Subscription Management experience, the manual allocation workflow for user-based subscriptions is unavailable if you have never used it. Automatic allocation of user-based subscriptions is based on user and group roles.

If you have manually allocated user-based subscriptions before, you can still make manual allocations.

## Procedure

1.  Navigate to Subscription Management in one of the following ways.

    -   Navigate to **Admin** &gt; **Subscription Management**.
    -   Navigate to **All** &gt; **Subscription Management** &gt; **Subscription Management**.
2.  Select a product with subscriptions that you want to allocate.

3.  Allocate subscriptions by adding recommended groups based on role type.

    1.  On the details page, select **Add groups**.

    2.  Select the check box next to one or more groups.

        The User group includes all user accounts in the `sys_user` table. The Active user group excludes users who haven't logged in to the instance in the last 365 days, users assigned Web service access only, or users with an empty User ID.

    3.  Select **Add groups**.


## Result

All group members are allocated subscriptions, giving each member entitlement to use the product. Subscribed users are updated during a daily scheduled job, so it might take up to a day for the changed to be reflected in Subscription Management.

**Parent Topic:**[Managing per-user subscriptions in Subscription Management](../concept/managing-user-subscriptions-v2.md)

