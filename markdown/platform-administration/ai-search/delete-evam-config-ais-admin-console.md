---
title: Delete an EVAM view configuration
description: Delete an unnecessary Entity View Action Mapper \(EVAM\) view configuration from your AI Search application at any time helps to improve the search result performance.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customizing the result-card interface in AI Search by using EVAM, Using AI SearchAdmin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Delete an EVAM view configuration

Delete an unnecessary Entity View Action Mapper \(EVAM\) view configuration from your AI Search application at any time helps to improve the search result performance.

## Before you begin

Role required: admin or ais\_admin

## About this task

Deleting unnecessary EVAM view configurations from the configuration bundle makes search faster in the AI Search application. For example, If the Q&amp;A Genius Result view configuration is rarely used in your search application and causes the search results to load slowly, deleting this configuration can improve the search result performance and simplify the interface.

![Delete view configuration dialog box in the AI Search Admin console allows you to confirm the deletion of the view configuration using the Delete button.](../image/delete-evam-view-config-ais.png)

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Applications** tab, select the application card that you want to delete.

3.  Select **Result-card Interface**.

4.  From the Select a bundle to edit list, select an EVAM configuration bundle.

    The list of view configurations that are associated with the selected bundle are displayed.

5.  Select the More Actions icon \(![](../../localization-framework/image/more-actions-icon.png)\), and then select **Delete** at the end of the view configuration row that you want to delete.


## Result

The selected view configuration is permanently deleted.

**Parent Topic:**[Customizing the result-card interface in AI Search by using EVAM](../concept/ais-admin-console-managing-evam.md)

