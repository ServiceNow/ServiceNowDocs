---
title: Monitoring cloud capacity in Subscription Management
description: View an account-level summary of your cloud capacity and track usage across all the instances associated with your account in Subscription Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/monitoring-cloud-entitlements.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Viewing account-level entitlements, Explore, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Monitoring cloud capacity in Subscription Management

View an account-level summary of your cloud capacity and track usage across all the instances associated with your account in Subscription Management.

## Key benefits

-   View the total amount of cloud capacity purchased for your account.
-   View the total amount of cloud capacity consumed across all your instances.
-   View the available cloud capacity for your account.
-   Stay in compliance by monitoring excess cloud capacity consumption.

\[Omitted image "subscription-management-cloud-account.png"\] Alt text: Cloud entitlements.

## Required ServiceNow AI Platform roles

The usage\_admin, sn\_sub\_man.admin, or admin role is required to view and edit Subscription Management.

## Accessing cloud capacity details

Access details about cloud capacity by navigating to **Admin** &gt; **Subscription Management** &gt; **Subscriptions** &gt; **Cloud capacity**.

## Use cases

-   View the total amount of capacity purchased by your account by checking the **Total purchased pool capacity \(TB\)** card.
-   View the total amount of capacity used by checking the **Used pool capacity \(TB\)** card.
-   Monitor available capacity or overage by checking the value in the **Excess pool capacity \(TB\)** card.
-   View cloud capacity usage for the instances associated with your account in the **Instances** list.

    -   View the amount of capacity each instance has consumed in the **Used pool capacity \(TB\)** column. This applies to shared, dedicated, and hybrid capacity types.
    -   View whether an instance's capacity is included with the instance or added separately in the **Hosting** column.
    In some scenarios, data isn't displayed in the **Instances** list.

    -   If data sharing is restricted on an instance, usage data for that instance is hidden. You can disable the restriction by updating the trust configuration on that instance. See [Share subscription data from another instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/share-subscription-data.md).
    -   Capacity values are displayed only for instances on Xanadu or higher. If an instance appears in the list but isn't on at least Xanadu, the capacity value appears as Not available.
    The sum of all the values in the **Used pool capacity \(TB\)** column equals the value in the Used pool capacity \(TB\) card. Only instances on at least Xanadu are included in the count.

-   View details about your cloud capacity, including the purchased quantity, capacity per unit, and total pool capacity purchased in the **Subscriptions** list.
    -   The total pool capacity purchased is calculated by multiplying the number of capacity environments you purchased by the capacity per unit.
    -   The sum of all the values in **Total purchased primary pool capacity \(TB\)** column equals the value in the **Total purchased pool capacity \(TB\)** card.
    -   The **Subscriptions** list includes both instance-level entitlements \(capacity included with an instance\) and account-level entitlements \(additional capacity purchased separately\). The **Total purchased pool capacity \(TB\)** card reflects the sum of both.
    -   With shared capacity, additional capacity you might receive based on your purchase history appears in the **Subscriptions** list without an end date. The amount of additional capacity you receive can fluctuate depending on your future purchases and renewals of existing subscriptions.
-   Identify which tables are driving storage growth on specific instances from the Data management Console. You can access the Data Management Console by selecting the **Data Management Console** link included in the Cloud Capacity report in Subscription Management, or by navigating to **All** &gt; **System Data Management** &gt; **Data Management Console**. For more information about the Data Management Console, see [Data Management overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/data-management-overview.md).

