---
title: Copy an EVAM view configuration
description: Copy an existing Entity View Action Mapper \(EVAM\) view configuration and modify it to customize the search result display in your AI Search application. Copying an EVAM is more efficient than creating an EVAM, especially if the changes are minimal.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customizing the result-card interface in AI Search by using EVAM, Using AI SearchAdmin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Copy an EVAM view configuration

Copy an existing Entity View Action Mapper \(EVAM\) view configuration and modify it to customize the search result display in your AI Search application. Copying an EVAM is more efficient than creating an EVAM, especially if the changes are minimal.

## Before you begin

Role required: admin or ais\_admin

## About this task

If the view configuration is shared and you need to modify the result-card interface without impacting other shared instances, you must copy the EVAM view configuration. For more information, see [Track how your EVAM view configurations are used](ais-admin-console-evam-viewusage.md).

![Copy view config dialog box in the AI Search Admin console, where you can review the configuration, along with a button to copy it.](../image/copy-evam-view-config-ais.png)

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Applications** tab, select the application card that you want to copy.

3.  On the sidebar tab, select **Result-card Interface**.

4.  From the Select a bundle to edit list, select an EVAM configuration bundle.

    The list of view configurations that are associated with the selected bundle are displayed.

5.  Hover over the desired view configuration and select the More Actions icon \(![](../../localization-framework/image/more-actions-icon.png)\) and then select **Create a copy**.

6.  In the Copy view config dialog box, review the auto-populated values and then select **Copy**.


## Result

A copy of the view configuration is added to the list.

## What to do next

After copying a view configuration, you can modify it based on your requirements, such as updating the EVAM definition for the result-card interface. For more information, see [Create or edit an EVAM view definition](ais-admin-console-evam-configurations.md).

**Parent Topic:**[Customizing the result-card interface in AI Search by using EVAM](../concept/ais-admin-console-managing-evam.md)

