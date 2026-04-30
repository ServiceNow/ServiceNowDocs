---
title: Monitoring cloud capacity in Subscription Management
description: View an account-level summary of your cloud capacity and track usage across all the instances associated with your account in Subscription Management.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Viewing account-level entitlements, Explore, Subscription Management, Get started, Administer]
---

# Monitoring cloud capacity in Subscription Management

View an account-level summary of your cloud capacity and track usage across all the instances associated with your account in Subscription Management.

## Key benefits

-   View the total amount of cloud capacity purchased across all your instances.
-   View the total amount of cloud capacity consumed across all your instances.
-   View the available cloud capacity across all your instances.
-   Stay in compliance by monitoring excess cloud capacity consumption.

![Cloud entitlements.](../image/subscription-management-cloud-account.png "Cloud capacity")

## Required ServiceNow AI Platform roles

The usage\_admin, sn\_sub\_man.admin, or admin role is required to view and edit Subscription Management.

## Accessing cloud capacity details

Access details about cloud capacity by navigating to **Admin** &gt; **Subscription Management** &gt; **Subscriptions** &gt; **Cloud capacity**.

## Capacity types

The capacity type depends on the entitlements that you purchased.

-   **Shared**

    You purchased one or more instances each with an initial capacity allotment. In a shared capacity type, each of your instances are created with an initial capacity allotment, but the instances can't share that capacity. If an instance requires more capacity, you can purchase additional capacity as needed. Additional capacity that you purchase can be shared among your instances.

-   **Dedicated**

    You purchased a dedicated amount of shared capacity for all of your instances. In a dedicated capacity type, your instances aren't created with an initial capacity allotment. Instead, you purchase additional capacity environments as needed.


You might have a combination of shared capacity and dedicated cloud capacity. Because you purchased dedicated capacity, your account's cloud capacity is still considered dedicated in Subscription Management. This means that instances provisioned with an initial capacity allotment can share their available capacity with your other instances. When your account has a combination of dedicated and shared capacity, an instance with included capacity contributes to the total purchased pool capacity. In this scenario, the amount of included capacity for each instance is displayed in the Subscriptions list.

## Use cases

-   View the total amount of capacity purchased by your account by checking the **Total purchased pool capacity \(TB\)** card.
-   View the total amount of capacity used by checking the **Used pool capacity \(TB\)** card.
-   Monitor available capacity by checking the value in the **Available pool capacity \(TB\)** card.
-   If the used pool capacity exceeds the total purchased pool capacity, review the overage in the **Excess pool capacity \(TB\)** card.
-   View cloud capacity usage for the instances associated with your account in the **Instances** list.

    -   In a dedicated capacity type, view the amount of capacity each instance has consumed in the **Used pool capacity \(TB\)** column.
    -   In a shared capacity type, view the total amount of capacity consumed by an instance in the **Used capacity \(TB\)** column. View the amount of capacity initially included in each instance in the **Included capacity column \(TB\)**. View the amount of capacity each instance has consumed beyond its included capacity in the **Used pool capacity \(TB\)** column.
    In some scenarios, data isn't displayed in the **Instances** list.

    -   If data sharing is restricted on an instance, usage data for that instance is hidden. You can disable the restriction by updating the trust configuration on that instance. See [Share subscription data from another instance](../task/share-subscription-data.md).
    -   Capacity values are displayed only for instances on Xanadu or higher. If an instance appears in the list but isn't on at least Xanadu, the capacity value appears as Not available.
    The sum of all the values in the **Used pool capacity \(TB\)** column equals the value in the Used pool capacity \(TB\) card. Only instances on at least Xanadu are included in the count.

-   View details about your cloud capacity, including the purchased quantity, capacity per unit, and total pool capacity purchased in the **Subscriptions** list.
    -   The total pool capacity purchased is calculated by multiplying the number of capacity environments you purchased by the capacity per unit.
    -   The sum of all the values in **Total purchased pool capacity \(TB\)** column equals the value in the **Total purchased pool capacity \(TB\)** card.
    -   With shared capacity, additional capacity you might receive based on your purchase history appears in the **Subscriptions** list without an end date. The amount of additional capacity you receive can fluctuate depending on your future purchases and renewals of existing subscriptions.
-   View the tables consuming the most amount of capacity on your current instance by selecting the **Top 10 table view** link.
-   After identifying the tables consuming the most amount of capacity, manage the growth of data on your instance by selecting the **Data management policies** link and reviewing each table's data management policy.

