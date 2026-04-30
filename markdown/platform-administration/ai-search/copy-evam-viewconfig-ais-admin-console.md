---
title: Create a copy of an EVAM view configuration
description: Modify the search results of your AI Search application by creating a copy of an existing Entity View Action Mapper \(EVAM\) view and then changing the copy. Copying an EVAM is more efficient than creating an EVAM, especially when the changes are minimal.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Customizing the result-card, Using AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Create a copy of an EVAM view configuration

Modify the search results of your AI Search application by creating a copy of an existing Entity View Action Mapper \(EVAM\) view and then changing the copy. Copying an EVAM is more efficient than creating an EVAM, especially when the changes are minimal.

## Before you begin

Role required: ais\_admin

## About this task

If the view configuration is shared and you need to modify the result-card interface without impacting other shared instances, you must create a copy of it. You can verify if the view configuration is shared. For more information, see [Track how your EVAM view configurations are used](ais-admin-console-evam-viewusage.md).

## Procedure

1.  Navigate to **All** &gt; **AI Search Admin** &gt; **AI Search Admin Home**.

2.  On the **Applications** tab, select the application card that you want to copy.

3.  In the left pane, select **Result-card Interface**.

4.  From the Select a bundle to edit list, select an EVAM configuration bundle.

    The list of view configurations that are associated with the selected bundle are displayed.

5.  Hover over the desired view configuration and select the **More Actions icon \(![More Actions.](../../localization-framework/image/more-actions-icon.png)\)** &gt; **Create a copy**.

6.  In the Copy view config dialog box, review the auto-populated values and then select **Copy**.


## Result

A copy of the view configuration is added to the list.

## What to do next

After copying a view configuration, you can modify it based on your requirements, such as updating the EVAM definition for the result-card interface. For more information, see [Create or edit an EVAM view definition](ais-admin-console-evam-configurations.md).

**Parent Topic:**[Customizing the result-card interface of an AI Search application by using EVAM](../concept/ais-admin-console-managing-evam.md)

