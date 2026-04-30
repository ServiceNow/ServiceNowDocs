---
title: Managing per-user subscriptions in Subscription Management
description: Manage your per-user subscription allocations using Subscription Management.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Managing per-user subscriptions in Subscription Management

Manage your per-user subscription allocations using Subscription Management.

## Overview of managing per-user subscriptions

To successfully manage your per-user subscriptions, follow the process in this infographic.

![The usage administrator allocates subscriptions by adding groups, tracks usage, and monitors end dates prior to renewal.](../image/mmasset0021657-subscription-management-workflow-manage-subscriptions-landing.png "Managing per-user subscriptions")

-   [Allocate subscriptions in Subscription Management](../task/allocate-subscriptions-v2.md)

    Subscriptions are managed in Subscription Management using groups. Subscriptions are measured and audited in Subscription Management using roles. You allocate subscriptions by adding one or more groups with measured roles to a product subscription.

-   [Remove a group from a product subscription in Subscription Management](../task/remove-group-from-subscription-v2.md)

    You can potentially over-allocate subscriptions, meaning more users possess an entitlement than the number of purchased subscriptions. Subscription Management flags over-allocated subscriptions for you. To stay in compliance, remove users or groups from the subscription or purchase more subscriptions.

-   [Maintain per-user subscription allocations in Subscription Management at renewal](../task/maintain-allocations-renewal.md)

    When a per-user subscription renews, a new product SKU might be added to your account. Maintain your current allocations during the renewal process by documenting your allocations before the renewal date.


## Recommended groups

Allocate per-user subscriptions by adding groups recommended by Subscription Management based on their roles. For example:

-   If the Service Desk group has a fulfiller-type role in the ITSM application, you can add the Service Desk group to the ITSM product subscription to allocate the fulfiller subscriptions included with ITSM to all the users in the group.
-   If you have available ITSM subscriptions, you can add groups that are recommended by Subscription Management based on the types of roles they have.

Groups that you add to a product subscription are considered subscribed groups. Consider assigning a group manager who is responsible for managing group membership and role assignments.

## Measured roles

Roles that require a subscription are considered measured roles. Measured roles grant users access to an application and are categorized by the level of access they provide.

When possible, simplify role administration by assigning measured roles to groups instead of assigning roles directly to individual users.

-   **[Allocate subscriptions in Subscription Management](../task/allocate-subscriptions-v2.md)**  
Give users entitlement to ServiceNow products by allocating subscriptions in Subscription Management.
-   **[Remove a group from a product subscription in Subscription Management](../task/remove-group-from-subscription-v2.md)**  
Fix an over-allocated subscription and free up entitlements by removing a group from a product subscription in Subscription Management.
-   **[Maintain per-user subscription allocations in Subscription Management at renewal](../task/maintain-allocations-renewal.md)**  
Ensure subscription allocations remain consistent throughout the renewal process.

**Parent Topic:**[Subscription Management](../reference/subscription-management-landing-page-v2.md)

