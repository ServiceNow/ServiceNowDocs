---
title: Viewing product subscription details in Subscription Management
description: View a summary of your subscription allocations, allocation totals over time, and track your custom table entitlements in Subscription Management.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Explore, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Viewing product subscription details in Subscription Management

View a summary of your subscription allocations, allocation totals over time, and track your custom table entitlements in Subscription Management.

## Key benefits

-   See how a product subscription is measured by viewing the subscription's meter type.
-   Match a product subscription in Subscription Management to your purchase order.
-   View the groups and users that you've added to a subscription.
-   View your entitlements for custom tables, portal visits, or transactions.
-   View the custom tables and applications that you've mapped to a product subscription.

![Subscription details](../image/subscription-details-no-tables.png "Subscription details")

## Required ServiceNow AI Platform roles

The usage\_admin role is required to view and edit Subscription Management.

## Accessing subscription details

View subscription details on the details page by navigating to **Admin** &gt; **Subscription Management** or **All** &gt; **Subscription Management** &gt; **Subscription Management**, and selecting a product or a subscription from the list.

## Use cases

-   See how a subscription is measured and the type of entitlement it provides by checking the **Meter Type** field.

    -   Entitlements for users with fulfiller-type access are tracked through a per-user subscription with a Fulfiller User meter type.
    -   Entitlements for users who have fewer access rights than fulfiller users are tracked through a per-user subscription with a Business Stakeholder User meter type.
    -   Entitlements for users with the now.assist.creator role are tracked through a per-user subscription with a Creator User meter type.
    -   The creation and retention of platform objects such as custom tables is tracked through a capacity subscription with a Capacity meter type.
    For more information, see [Types of subscriptions in Subscription Management](../reference/types-subscription-v2.md).

-   See how a capacity subscription total is calculated by selecting the Capacity Definition record and viewing the definition details. For more information, see [Monitor capacity subscription calculations in Subscription Management](../task/view-how-totals-calculated-capacity-subscriptions-v2.md).
-   View the groups you've added to a subscription in the **Subscribed groups** tab. View the total number of users who belong to each group in the **Users** column.

    View the total number of active users in the **Active users** column. The count of active users excludes those who haven't logged into the instance in the last 365 days, those assigned Web service access only, or those with an empty User ID.

    Only active users count toward the subscription allocation totals that appear throughout Subscription Management.

-   View eachactive user who belongs to the subscribed groups in the **Subscribed users** tab. Only active users with allocated subscriptions appear in this list.
-   Stay in compliance by monitoring your product subscription add-on usage on the **Bundled Items** tab. Product subscription add-ons can include bundled custom tables, portal visits, and transaction entitlements.
-   Plan for future purchases and keep your subscriptions current by monitoring the start and end dates for each of your product subscriptions in the **Purchase History** tab. Note that multiple entries for the same product might appear if modifications are made to a product.
-   View the applications that are included with a product subscription on the **Subscription applications** tab.
    -   View application entitlement details, including the application's related plugins and associated roles by selecting an application.
    -   Determine whether an application is available to install from the current product subscription by checking the **Installation status** column.
-   Maximize subscription usage and grant entitlement to the right users by allocating per-user subscriptions. You allocate per-user subscriptions by adding one or more groups to a product subscription. Subscription Management helps you with the allocation process by recommending groups based on their assigned roles. For more information, see [Allocate subscriptions in Subscription Management](../task/allocate-subscriptions-v2.md).

## Consolidated subscriptions

When you purchase multiple qualifying subscriptions for certain types of products, such as Integration Hub, those individual subscriptions combine into a single subscription pool. Any usage against that subscription deducts from the common pool.

-   Capacity subscriptions with a common capacity definition are consolidated into one capacity subscription. For example, if you purchased two different Integration Hub subscriptions that are measured using the same capacity definition, they're consolidated into one Integration Hub Pool capacity subscription. Other types of capacity subscriptions with matching definitions are consolidated as well, but aren't labeled as a pool. For any consolidated capacity subscription, you can view the combined products in the **Subscription line items** tab on the details page.
-   Capacity subscriptions can also consolidate entitlements for secondary line items such as custom tables, transactions, or portal visits from other product subscriptions. For example, if you have two Integration Hub transaction subscriptions combined in a pool, transaction entitlements that are included as a secondary line item from another capacity subscription are added to the pool if the capacity definition matches. In this scenario, three separate entries appear on the **Subscription line items** tab, one for each product that contributes to the pool.
-   Custom table entitlements that come with per-user subscriptions can also be consolidated under one product subscription. When custom table entitlements are consolidated under one subscription, the total number of custom tables appears in the **Purchased** column on the **Bundled Items** tab. The **Bundled Items** tab only appears on one of the product subscriptions that contributed to the pool of custom tables.
-   Unrestricted User subscriptions aren't consolidated into a single product subscription.

## Reports

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Allocation summary|Donut|Subscription license detail definition \[sn\_sub\_man\_st\_subscription\_license\_detail\_metric\] table|View a real-time summary of your subscription allocation. If an allocation is nearing capacity, consider reducing the number of allocated subscriptions or purchasing more subscriptions.|
|Account-level allocations|Donut|Account level entitlements \[sn\_sub\_man\_st\_account\_level\_entitlement\] table|View a summary of Creator Plus allocations across all of your instances. If the account-level allocation is nearing capacity, consider reducing the number of allocated subscriptions or purchasing more subscriptions.|
|Allocation history|Bar|Subscription license detail definition \[sn\_sub\_man\_st\_subscription\_license\_detail\_metric\] table|View subscription allocation details over time. Prepare for future purchases or plan for changes according to the allocation trends.|

