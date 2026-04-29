---
title: Opt-in or opt-out of HAM license resource categories
description: Opt in the Hardware Asset Management \(HAM\) license resource categories that are part of the HAM subscription. You can purchase and opt in the resource categories that you use, and you can opt out and not pay for the categories that you don't use.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [HAM licensing, Hardware Asset Management licensing]
breadcrumb: [Manage Hardware Asset Management subscriptions, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Opt-in or opt-out of HAM license resource categories

Opt in the Hardware Asset Management \(HAM\) license resource categories that are part of the HAM subscription. You can purchase and opt in the resource categories that you use, and you can opt out and not pay for the categories that you don't use.

## Before you begin

Role required: admin or HAM admin

## About this task

This procedure is a one-time activity. If you’re upgrading from HAM 1.0 or 2.0 version, then all resource categories are by default opted in. The exception is the Mobile Device resource category.

If you’re a new user, manually opt in all the resource categories that are part of the HAM subscription.

**Important:** The Mobile Device resource category is only accessible with HAM Mobile Device License entitlement. Resource categories are available irrespective of entitlements in non-production instances. However, in production instances, you would find the resource categories available only with their associated entitlements.

Hardware assets belonging to a category that you don't opt in are excluded by default. For example, if you don't opt in for the End User Computer category, all End user computers would be excluded. For more information, see [Hardware Asset Management license exclusion](../concept/ham-license-exclusion.md).

**Note:** All the HAM license resource categories are opted in by default when you load demo data in an instance. You must deselect the resource categories that you don't want to opt in for.

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Hardware Model Normalization** &gt; **HAM Resource categories**.

2.  Open a resource category.

    Each resource category lists the model categories associated with it.

3.  To opt in or opt out of the resource category, do one of the following:

    -   If you want to opt in the resource category, select **Opt in**.
    -   If you want to opt out of the resource category, select **Opt out**.
    A pop-up message appears and asks if you want to opt in or opt out.

4.  Select **Ok**.


## Result

The resource category is opted in or opted out. A one time run job execution executes the following updates:

-   Sets the License opt in column on the models that have the model categories belonging to the opted in or opted out resource categories.
-   Sets the exclusion flag on the assets of these models. For more information, see [Hardware Asset Management license exclusion](../concept/ham-license-exclusion.md).
-   A normalization job is triggered for the models that are associated with the resource category.

**Parent Topic:**[Manage Hardware Asset Management subscriptions](../concept/managing-ham-subscriptions.md)

**Related topics**  


[View the license report for the Hardware Asset Management application](view-license-report-ham.md)

[Exclude assets](exclude-assets.md)

