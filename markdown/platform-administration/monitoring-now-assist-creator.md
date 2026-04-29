---
title: Monitoring Now Assist creators in Subscription Management
description: View a summary of your Creator Plus entitlements and track allocations for distinct users across all of your instances in Subscription Management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Viewing account-level entitlements, Explore, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Monitoring Now Assist creators in Subscription Management

View a summary of your Creator Plus entitlements and track allocations for distinct users across all of your instances in Subscription Management.

## Key benefits

-   View the total number of Creator Plus entitlements that you purchased across all your instances.
-   View the total number of Creator Plus entitlements allocated to unique users across all your instances.
-   Track the availability of the remaining Creator Plus entitlements that you can allocate to users.

![Now Assist creators.](../image/subscription-management-creator-account.png "Now Assist Creator Plus entitlements")

## Required ServiceNow AI Platform roles

The usage\_admin, sn\_sub\_man.admin, or admin role is required to view and edit Subscription Management.

## Accessing Creator Plus entitlements

Access details about Creator Plus entitlements by navigating to **Admin** &gt; **Subscription Management** &gt; **Subscriptions** &gt; **Now Assist creators**.

## Use cases

-   Compare the total number of Creator Plus entitlements that your company has purchased to the total number of Creator Plus entitlements allocated across all your instances.
-   Monitor the number of Creator Plus entitlements that are allocated to unique users across all your instances in the **Distinct allocated users** card.

    **Note:** Users allocated to a Creator Plus subscription on multiple instances are automatically de-duplicated in the total count. When a user is allocated to a Creator Plus subscription on more than one instance, that user counts toward the allocation total only once.

-   View Creator Plus allocations by instance in the **Allocated users** column in the **Instances** list.

    In some scenarios, data isn't displayed in the **Instances** list.

    -   Only instances on Washington DC Patch 2 and higher are listed in the **Instances** list.
    -   If data sharing is restricted on an instance, usage data for that instance is hidden. You can disable the restriction by updating the trust configuration on that instance. See [Share subscription data from another instance](../task/share-subscription-data.md).
-   View Creator Plus product subscription details by selecting a product in the **Subscriptions** list. On the details page, allocate available Creator Plus subscriptions by adding one or more groups with the Creator role.

