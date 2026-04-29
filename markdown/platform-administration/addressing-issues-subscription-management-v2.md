---
title: Addressing issues in Subscription Management
description: Stay in compliance by mapping custom tables and custom applications to subscriptions in Subscription Management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Addressing issues in Subscription Management

Stay in compliance by mapping custom tables and custom applications to subscriptions in Subscription Management.

## Key benefits

-   Identify custom tables and custom applications that aren't mapped to subscriptions.
-   Maintain accurate entitlements by mapping custom tables and custom applications to a recommended product subscription or a product subscription of your choice.
-   Plan for future subscription needs by assessing your custom table entitlements.

![Subscription issues](../image/subscription-management-issues.png "Subscription issues")

## Accessing subscription issues

Access information on subscription issues on the **Issues** tab by navigating to **Admin** &gt; **Subscription Management** &gt; **Issues** or **All** &gt; **Subscription Management** &gt; **Issues**.

## Unmapped global custom tables

Determine whether you have custom tables in the global scope that aren't mapped to a valid product subscription by accessing the **Unmapped global custom tables** tab. Keep custom table entitlements current by mapping the tables to a product subscription. For more information, see [Map custom tables to a product subscription in Subscription Management](../task/allocate-custom-table-subsc-app-v2.md).

Recommended subscriptions for unmapped custom tables appear on the **Issues** tab the day after the unmapped custom table is created.

## Unmapped custom applications

Determine whether you have custom tables in a scoped application that aren't currently mapped to a valid product subscription by accessing the **Unmapped custom applications** tab. Ensure that entitlements for these tables are current by mapping the application to a product subscription.

You map tables in a scoped application at the application-level, which eases administration because you don't need to map tables individually after the application is mapped. For more information, see [Map a custom application to a product subscription in Subscription Management](../task/map-custom-applications-v2.md).

Recommended subscriptions for unmapped custom applications appear on the **Issues** tab the day after the unmapped custom table is created.

## Recommended subscriptions

When you map custom tables or custom applications to subscriptions, Subscription Management displays recommended subscriptions based on the following criteria:

-   **The table belongs to an app scope or package**

    The custom table or tables in the application belong to an app scope or package associated with the recommended subscription.

-   **The table extends another table**

    The custom table or tables in the application extend another table mapped to the recommended subscription.

-   **The table has a relationship to another table**

    The custom table or tables in the application are related to a different custom table or a ServiceNow default table associated with the recommended subscription.

-   **The table doesn't meet any of the previous criteria**

    The custom table or tables in the application don't meet any of the previous criteria. If you have an App Engine subscription, Subscription Management recommends mapping the table or application to an App Engine subscription.


If the criteria for recommending a subscription aren't met and you don't have an App Engine subscription, Subscription Management can't display recommended subscriptions for unmapped applications and tables. Unmapped applications and tables without subscription recommendations are counted in the Subscription Management Overview reports, but aren't shown in subscription Issues. You can map any missing custom applications and tables to a subscription from the Custom Applications list or the Custom Table Inventory list. For more information, see [Map a missing custom application to a product subscription in Subscription Management](../task/map-missing-custom-app-sub-mgt.md) and [Map a missing custom application to a product subscription in Subscription Management](../task/map-missing-custom-app-sub-mgt.md).

In some cases, groups aren't recommended because the measured role is inherited and not directly assigned. To work around this problem, assign the measured role directly to the group. Once the group is assigned the measured role, the group appears in the list of recommend groups in Subscription Management.

