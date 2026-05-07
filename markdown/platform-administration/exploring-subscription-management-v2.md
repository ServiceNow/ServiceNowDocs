---
title: Exploring Subscription Management
description: Learn how Subscription Management helps you track and manage your product subscriptions and their applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Exploring Subscription Management

Learn how Subscription Management helps you track and manage your product subscriptions and their applications.

## Subscription Management Overview

Subscription Management gives you an accurate, consolidated view of your entitlements where you can proactively manage your subscriptions.

-   Gain visibility and control of your product subscriptions and their applications.
-   Access a real‑time view of your entitlement data.
-   Maximize subscription usage and make informed decisions about purchases by viewing insights.
-   Stay in compliance and avoid unexpected costs by tracking subscription usage and allocations over time.

## Subscription Management users

|User|Description|
|----|-----------|
|Usage admin|The usage admin allocates per-user subscriptions by adding groups to a product subscription. The usage admin maps custom tables and custom applications to subscriptions with available entitlements to maximize subscription usage and stay in compliance.|

## Subscription Management workflow

This infographic shows a sample end-to-end workflow of how different users in an organization work together to purchase, allocate, and manage subscriptions.

![Different users in an organization work together to purchase, allocate, and manage subscriptions. Refer to the following steps for details.](../image/MMASSET0021656.png "Managing subscriptions")

In this workflow:

1.  The chief information officer or service owner works with the ServiceNow platform owner to purchase new subscriptions.
2.  After the purchase is complete, the platform owner views the products and applications in Impact.
3.  The usage admin views the new product subscriptions in Subscription Management on the production instance. For more information, see [Product subscriptions overview](subscriptions-overview-v2.md).
4.  The usage admin performs the following tasks in Subscription Management:
    -   Allocates per-user subscriptions by adding groups to a product subscription, which grants entitlement to all group members. For more information, see [Managing per-user subscriptions in Subscription Management](managing-user-subscriptions-v2.md).
    -   Maps custom tables and custom applications to subscriptions with available entitlements to maximize subscription usage and stay in compliance. For more information, see [Managing custom tables and applications in Subscription Management](allocating-custom-tables-subscr-apps-v2.md).
5.  If the organization requires security approvals before adding users to groups or financial approvals before subscriptions are allocated to users, the usage admin works with group managers to create subscription approval workflows that determine who gets a subscription when new users are added to groups.
6.  The usage admin monitors subscription usage to stay in compliance and make informed decisions on future purchases, consistently monitoring the following data:
    -   Over-allocated subscriptions
    -   Unmapped custom applications and tables
    -   Usage patterns over time
    -   Application popularity
    -   Custom table usage

## Subscription Management benefits

|Benefit|Feature|User|
|-------|-------|----|
|Fix over-allocated subscriptions|[Insights](discovering-insights-subscription-management-v2.md)|Usage admin|
|View unallocated subscriptions|[Insights](discovering-insights-subscription-management-v2.md)|Usage admin|
|Allocate available subscriptions using recommended groups|[Allocate subscriptions](../task/allocate-subscriptions-v2.md)|Usage admin|
|Map global custom tables to a product subscription|[Issues](addressing-issues-subscription-management-v2.md)|Usage admin|
|Map custom applications to a product subscription|[Issues](addressing-issues-subscription-management-v2.md)|Usage admin|
|View a summary of subscription allocations|[Subscription details](subscription-details-v2.md)|Usage admin|
|View subscription allocation details over time|[Subscription details](subscription-details-v2.md)|Usage admin|
|View custom table usage over time|[Subscription details](subscription-details-v2.md)|Usage admin|

## What to explore next

To learn more about configuring and using Subscription Management, see:

-   [Configuring Subscription Management](configuring-subscription-management-v2.md)
-   [Managing per-user subscriptions in Subscription Management](managing-user-subscriptions-v2.md)
-   [Managing custom tables and applications in Subscription Management](allocating-custom-tables-subscr-apps-v2.md)
-   [Monitoring capacity subscriptions](monitoring-capacity-subscriptions.md)
-   [Subscription Management reference](../reference/subscription-management-reference-v2.md)

