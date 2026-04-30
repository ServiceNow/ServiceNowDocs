---
title: Track how your EVAM view configurations are used
description: Track where Entity View Action Mapper \(EVAM\) view configurations are being used in the AI Search application. Tracking helps you to understand the search result layouts, identify the shared settings, and make the adjustments for better search results.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Customizing the result-card interface of an AI Search application by using EVAM, Using the AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Track how your EVAM view configurations are used

Track where Entity View Action Mapper \(EVAM\) view configurations are being used in the AI Search application. Tracking helps you to understand the search result layouts, identify the shared settings, and make the adjustments for better search results.

## Before you begin

Role required: ais\_admin or admin

## About this task

By tracking the usage of your EVAM view configurations, you can do the following tasks:

-   Understand the overall hierarchy of the view configuration and delve into each component directly from the ServiceNow AI Platform record page.
-   Identify if the view configuration is shared across search applications.

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Applications** tab, select the application card that you want to track the usage of.

3.  On the sidebar tab, select **Result-card Interface**.

4.  From the Select a bundle to edit list, select an EVAM configuration bundle.

    The list of view configurations that are associated with the selected bundle are displayed.

5.  Hover over the view configuration and select the More Actions icon \(![](../../localization-framework/image/more-actions-icon.png)\), and then select **View usage**.

6.  In the View usage dialog box, review the values.

7.  Select **Close**.


## Result

The EVAM view configuration usage is reviewed to assess its alignment with the search application requirements.

![View usage dialog box in the AI Search Admin console, where you can review the view configuration details.](../image/evam-view-usage-ais.png)

## What to do next

After reviewing the view configuration details and its usage, you can optimize or remove the configurations. For more information, see [Create or edit an EVAM view definition](ais-admin-console-evam-configurations.md), [Activate or deactivate an EVAM view configuration](enable-evam-config-ais-admin-console.md), [Delete an EVAM view configuration](delete-evam-config-ais-admin-console.md).

**Parent Topic:**[Customizing the result-card interface of an AI Search application by using EVAM](../concept/ais-admin-console-managing-evam.md)

