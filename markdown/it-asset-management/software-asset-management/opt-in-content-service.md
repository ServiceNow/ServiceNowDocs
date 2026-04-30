---
title: Opt in to Content Service
description: Opt in to Content Service for Software Spend Transactions to get more accurate predictions in Software Spend Detection by sharing financial transaction data with the ServiceNow Content Service team.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management]
---

# Opt in to Content Service

Opt in to Content Service for Software Spend Transactions to get more accurate predictions in Software Spend Detection by sharing financial transaction data with the ServiceNow Content Service team.

## Before you begin

Role required: sam\_admin

## About this task

Opting in to Content Service for Software Spend Transactions means that you agree to have a copy of your financial transaction data securely sent to ServiceNow. Your data is used only to improve future publisher and product predictions when importing data into Software Spend Detection. You can opt out of Content Service at any time.

If you already opted in to Software Asset Management Content Service, you still need to manually enable data sharing for Software Spend Detection by selecting the Software Spend Transactions toggle button on the Content Service Setup page. Software Spend Transactions data sharing is disabled by default.

If you opt in after you've already imported data into Software Spend Detection, data from previous imports is shared as well as data from future imports.

**Note:** If you want to hide the ability to opt in, a user with the admin role can set the glide.samp.spend\_detection\_opt\_in.enabled system property to **false**. Setting this value to **false** hides the toggle button used to turn on sharing for software spend transactions. Also, if this property is set to **false** when you're already opted in, your transaction data is no longer shared.

## Procedure

1.  Navigate to **All** &gt; **Software Spend Detection** &gt; **Administration** &gt; **Content Service Setup**.

2.  Select the check the box to accept the opt-in agreement and then select **Opt-in**.

    **Note:** If you already opted in to Content Service through Software Asset Management, you don't see the opt-in screen.

    Data sharing for Software Discovery Models, Software Model Lifecycles, Part Numbers and Discovery Maps, and Processor Names KPIs is automatically enabled after opting in. If you don't want to share data for some KPIs, individually disable sharing by selecting the toggle button next to the KPI and then selecting **Save**. For more information about Content Service KPIs, see [Software Asset Management Content Service](../concept/c_SAMContentService.md).

3.  To turn on sharing for software spend transaction data, select the toggle button next to Software Spend Transactions and then select **Save**.


## What to do next

You can return to the Content Service Setup page to adjust your data sharing settings for each KPI. You can completely opt out by selecting **I would like to opt my company out of the Software Asset Management Content Service Program**. After opting out, you can opt back in at any time.

-   **[Content Service for Software Spend Detection](../concept/content-service-spend-detection.md)**  
Opt in to Software Asset Management Content Service for Software Spend Transactions to get more accurate predictions in Software Spend Detection by sharing financial transaction data with the ServiceNow Content Service team.

**Parent Topic:**[Software Spend Detection](../concept/software-spend-detection.md)

