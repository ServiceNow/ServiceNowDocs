---
title: Exclude assets
description: Exclude an asset for which you don't want to use Hardware Asset Management licensed features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/exclude-assets.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [HAM licensing, Hardware Asset Management licensing]
breadcrumb: [Opt-in or opt-out of HAM license resource categories, Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Exclude assets

Exclude an asset for which you don't want to use Hardware Asset Management licensed features.

## Before you begin

Role required: admin

## About this task

You can only exclude assets whose resource category is opted in to Hardware Asset Management licensed features.

## Procedure

1.  Navigate to **Hardware Asset Workspace** &gt; **Asset estate** &gt; **Hardware assets**.

2.  Select a hardware asset that you want to exclude.

3.  On the asset form, select the **Exclude from HAM features** check box.

    **Note:**

    The **Exclude from HAM features** check box is automatically selected under these conditions:

    -   If the hardware asset belongs to a resource category that's opted out of Hardware Asset Management licensed features.
    -   If the hardware asset belongs to a custom model category whose parent model category is associated with an opted-out resource category.
4.  Select **Save**.

    **Note:** To exclude assets using other criteria — for example, a specific model — select the **Exclude from HAM features** check box on each asset record manually. You can't exclude assets automatically using custom criteria.


## Result

The asset is excluded from using the licensed Hardware Asset Management features.

**Parent Topic:**[Opt-in or opt-out of HAM license resource categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/optin-optout-ham-license-resource-categories.md)

