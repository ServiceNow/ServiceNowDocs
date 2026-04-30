---
title: Product subscriptions overview
description: View a summary of your product subscriptions in Subscription Management.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Explore, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Product subscriptions overview

View a summary of your product subscriptions in Subscription Management.

## Key benefits

-   Determine whether you have any over-allocated subscriptions.
-   Check for unallocated subscriptions that you can allocate to maximize usage and give users entitlement to ServiceNow products.
-   Determine whether any custom tables in the global scope or any custom applications aren't mapped to subscriptions.
-   Stay in compliance by monitoring the **Status** column in the list of product subscriptions.

![Overview of product subscriptions.](../image/subscription-management-overview.png "Subscriptions overview")

## Required ServiceNow AI Platform roles

The usage\_admin, sn\_sub\_man.admin, or admin roles are required to view and edit Subscription Management.

## Accessing product subscription overview information

View subscription overview information on the **Overview** tab in Subscription Management by navigating to **Admin** &gt; **Subscription Management** or **All** &gt; **Subscription Management** &gt; **Subscription Management**.

## Accessing user-based subscription information

Allocation details and status for user-based subscriptions are hidden from the Subscription Management overview to help prevent inaccuracy when allocations are incomplete. Contact your account executive for complete user-based subscription allocation details.

## Use cases

View a summary of your instance-level entitlements in the **Instance entitlements** tab.

-   Identify when subscriptions are over-allocated and view insights into actions you can take to maximize subscription usage.
-   Determine whether any custom tables and custom applications on your instance aren't mapped to a valid product subscription. You must map custom tables and custom applications that you create to a product subscription.
-   View product subscription details by selecting the product name.
-   Identify which type of subscriptions you have by viewing the values in the **Type** column. The subscription type determines the properties and attributes of the product subscriptions that your company receives and whether to allocate subscriptions manually.

    -   Product subscription types include per-user, capacity, unrestricted user, unlimited, and display only.
    -   Per-user subscriptions require manual allocation by an administrator. Capacity, unrestricted user, and unlimited subscriptions are allocated on your instance automatically. Display-only subscriptions aren't measured on your instance.
    -   Product subscriptions provide entitlements for different applications and can include different add-ons.
    For more information, see [Types of subscriptions in Subscription Management](../reference/types-subscription-v2.md).

-   Determine whether your subscription allocations are in compliance by viewing the values in the **Status** column. Adjust allocations if subscriptions are over-allocated.

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

    You can customize the near capacity threshold for your instance in the **Settings** tab. For more information, see [Configure subscription allocation status in Subscription Management](../task/configure-subscription-allocation-status-v2.md).

-   View a summary of the Creator Plus subscriptions on the instance that you're currently accessing.
    -   View the total number of Creator Plus subscriptions that your company has purchased in the **Purchased** column.
    -   Contact your account executive for up-to-date information about per-user subscription allocations.

View a summary of your account-level entitlements in the **Account entitlements** tab.

-   View an account-level summary of Now Assist usage.
    -   View the aggregated total of Now Assist usage entitlements from all the subscriptions that your account has purchased in the **Purchased** column.
    -   View the total number of Now Assist usage entitlements consumed across all your instances in the **Allocated** column.
    -   View additional details about Now Assist usage by selecting the product name.
-   View an account-level summary of Now Assist creators.
    -   View the total number of Creator Plus subscriptions that your account has purchased in the **Purchased** column.
    -   View additional details about Now Assist creators by selecting the product name.
-   View an account-level summary of your cloud capacity.
    -   View the total amount of cloud capacity that your account has purchased in the **Purchased** column.
    -   View the total amount of cloud capacity consumed across all your instances in the **Allocated** column.
    -   View additional details about cloud capacity by selecting the product name.

## Reports

|Title|Type|Source Table|Description|
|-----|----|------------|-----------|
|Insights|List|Subscription Insights definition \[sn\_sub\_man\_st\_subscription\_insights\]|List of over-allocated subscriptions and available subscriptions|
|Unmapped global custom tables|Single Score|Custom Table Inventory \[ua\_custom\_table\_inventory\]|Count of custom tables that aren't mapped to a subscription|
|Unmapped custom applications|Single Score|Custom Table Inventory \[ua\_custom\_table\_inventory\]|Count of custom applications that aren't mapped to a subscription|

