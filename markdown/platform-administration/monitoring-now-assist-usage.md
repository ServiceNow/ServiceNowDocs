---
title: Monitoring Now Assist usage in Subscription Management
description: View a summary of your Now Assist entitlements and track Now Assist usage across all of your instances in Subscription Management.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Viewing account-level entitlements, Explore, Subscription Management, Get started, Administer]
---

# Monitoring Now Assist usage in Subscription Management

View a summary of your Now Assist entitlements and track Now Assist usage across all of your instances in Subscription Management.

## Key benefits

-   View an account-level summary of your Now Assist entitlements.
-   Track Now Assist usage across your production and non-production instances.
-   Track Now Assist usage by domain in domain-separated instances.
-   View a summary of Now Assist usage by skill.
-   Plan for future purchases by analyzing Now Assist usage over time.

![Now Assist usage.](../image/subscription-management-now-assist-account.png "Now Assist usage")

## Required ServiceNow AI Platform roles

The usage\_admin, sn\_sub\_man.admin, or admin role is required to view and edit Subscription Management.

## Accessing Now Assist usage details

Access details about Now Assist usage by navigating to **Admin** &gt; **Subscription Management** &gt; **Subscriptions** &gt; **Now Assist usage**.

## Use cases

-   Compare the total number of Now Assist entitlements that your company has purchased to the total number of Now Assist entitlements consumed across all your instances. Monitor the available number of Now Assist entitlements for your account.
-   Visualize Now Assist consumption over time by selecting **View details** in the Total used assists card. Monitor compliance for your account for the current contract period or determine when Now Assist usage exceeded the total purchased count.

    **Note:** Assists used in demo instances are excluded from total used assists.

-   View the number of assists consumed by each of your instances in the **Used assists** column in the **Instances** list.

    In some scenarios, data isn't displayed in the **Instances** list.

    -   Only instances on Washington DC Patch 2 and higher are listed in the **Instances** list.
    -   If data sharing is restricted on an instance, usage data for that instance is hidden. You can disable the restriction by updating the trust configuration on that instance. See [Share subscription data from another instance](../task/share-subscription-data.md).
-   View details for each of your products that include assists in the **Subscriptions** list.
    -   Determine whether assists are the primary or secondary line item in a purchase according to the value in the **Entitlement type** column.
    -   Verify the start date and end date for each product.
    -   View the total number of entitlements provided by each product in the **Purchased assists** column.
-   View and filter the number of assists used by domain from the **Used assists** column of the **Domain** list. The **Domain** list is only available if domain separation is enabled and there are domain values other than global.
-   Determine cumulative Now Assist usage by skill on your current instance. Data in the table is updated nightly. If your current instance doesn’t have any active subscriptions with assists, the list of skills is empty.
    -   View the number of times a skill has been used in the **Number of actions** column.
    -   View the relative cost for each assist in the **Assist ratio** column.
    -   Determine which skills are consuming the most Now Assist entitlements by checking the **Total assists** column. Total assists are calculated by multiplying values in the **Number of actions** column by values in the **Assist ratio** column.
    -   Analyze Now Assist usage over time on your current instance by viewing the Utilization history chart. Monitor monthly or daily usage using the filter. Look for trends related to Now Assist skills. If usage continues to grow every month, consider purchasing more entitlements to stay in compliance.

