---
title: Remove a group from a product subscription in Subscription Management
description: Fix an over-allocated subscription and free up entitlements by removing a group from a product subscription in Subscription Management.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing per-user subscriptions, Subscription Management, Get started, Administer]
---

# Remove a group from a product subscription in Subscription Management

Fix an over-allocated subscription and free up entitlements by removing a group from a product subscription in Subscription Management.

## Before you begin

Role required: usage\_admin, sn\_sub\_man.admin, or admin

## About this task

To simplify the Subscription Management experience, user-based subscriptions are automatically allocated based on role if you haven't manually allocated user-based subscriptions before. To resolve over-consumed user-based subscriptions, reduce the number of users with roles that provide access to the over-consumed subscription. For more information, see [Add a user to a group](../../users-and-groups/task/t_AddAUserToAGroup.md) and [Managing roles](../../roles/concept/ua-creating-roles.md).

If you have manually allocated user-based subscriptions before, you can still make manual changes to the subscribed groups using the following process.

## Procedure

1.  Navigate to Subscription Management in one of the following ways.

    -   Navigate to **Admin** &gt; **Subscription Management**.
    -   Navigate to **All** &gt; **Subscription Management** &gt; **Subscription Management**.
2.  Identify an over-allocated subscription by checking either the **Status** column on the **Overview** tab or the list of over-allocated subscriptions on the **Insights** tab.

3.  Select the over-allocated product subscription.

4.  On the subscription details page, select the **Subscribed Groups** tab.

5.  Select the check box next to one or more groups that you want to remove.

6.  Select **Remove**.

7.  In the dialog box, confirm that you want to remove entitlements for all users in the selected groups by selecting **Remove**.

    Subscribed users are updated during a daily scheduled job, so it might take up to a day for removal of groups to be reflected in Subscription Management.

8.  Verify that the subscription is no longer over-allocated by checking the value in the **Status** column on the **Subscriptions** tab.


## What to do next

The group is removed from the subscription. If the group still has a measured-role that requires a subscription, add the group to a different subscription or remove the measured-role from the group.

**Parent Topic:**[Managing per-user subscriptions in Subscription Management](../concept/managing-user-subscriptions-v2.md)

