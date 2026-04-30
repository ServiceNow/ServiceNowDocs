---
title: Viewing instance-level entitlements in Subscription Management
description: View a complete list of the product subscriptions purchased for your current instance.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Explore, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Viewing instance-level entitlements in Subscription Management

View a complete list of the product subscriptions purchased for your current instance.

## Key benefits

-   View details for product subscriptions, including purchase information and usage history by selecting the product name.
-   Plan for future purchases and keep subscriptions current by monitoring the start and end dates for each of your product subscriptions.
-   Stay in compliance by monitoring the subscription allocation values in the **Status** column.

![All product subscriptions on the current instance.](../image/subscription-management-instance-level.png "Instance-level entitlements")

## Accessing your instance-level entitlements

Access your instance-level entitlements by navigating to **Admin** &gt; **Subscription Management** &gt; **Subscriptions** or **All** &gt; **Subscription Management** &gt; **All Subscriptions**.

## Subscription types

Identify which type of subscriptions you have and whether to allocate subscriptions manually by viewing the values in the **Type** column.

-   **Per-User**

    Provides entitlements to users according to their assigned roles and associated access rights. You allocate per-user subscriptions manually by adding groups with metered roles or access rights to a product subscription. Subscription Management helps you with the allocation process by recommending groups based on their role assignments.

-   **Unrestricted User**

    Provides entitlements for an organization's number of active users regardless of their role assignments. An active user is any user whose record in the Users \[sys\_user\] table has a value in the **User ID** field and has the **Active** field set to true.

-   **Capacity**

    Automatically tracks measured units, and counts of transactions, records created, or resources managed such as devices, software, or nodes.

-   **Unlimited**

    Provides entitlements for active users, with no limit to the number of users that can be allocated. An active user is any user whose record in the Users \[sys\_user\] table has a value in **User ID** field and has the **Active** field set to true.

-   **Display Only**

    Displays information. This type of subscription doesn't support allocation.


## Subscription status

Determine whether your subscription allocations are in compliance by viewing the values in the **Status** column.

-   **Compliant**

    The number of allocated subscriptions is below the number of purchased subscriptions.

-   **Near capacity**

    The number of allocated subscriptions exceeds the threshold for your instance. You define the threshold on the **Settings** tab.

-   **Even**

    The number of allocated subscriptions equals the number of purchased subscriptions.

-   **Over-allocated**

    The number of allocated subscriptions exceeds the number of purchased subscriptions.

-   **Account-level only**

    The subscription allocation status isn't calculated. Only applies to Creator Plus products.


## Missing subscriptions

Purchased subscriptions might not appear on the **Subscriptions** tab for one or more of the following reasons:

-   Subscription data arrives on production instances only.
-   Self-hosted instances don't receive subscription information. Contact your account manager for assistance.
-   Subscription data might not yet have arrived. The data is downloaded daily.

