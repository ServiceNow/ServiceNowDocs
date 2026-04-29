---
title: Hide contextual side panel
description: Set the hideContextualSidebar page property to determine when to hide the default primary contextual side panel for specific table-tab combinations, showing the tab's embedded contextual side panel in its place.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Service Operations Workspace for ITSM to improve your experience, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Hide contextual side panel

Set the **hideContextualSidebar** page property to determine when to hide the default primary contextual side panel for specific table-tab combinations, showing the tab's embedded contextual side panel in its place.

## About this task

The feature helps in increasing the focus and utilizing the workspace area in an efficient way. For example, when viewing the **Schedule** tab in a user group page, setting the **hideContextualSidebar** UX page property to true, hides the default contextual side panel for the user group to avoid overlap with the contextual side panel of the **Schedule** tab. If enabled, users can benefit from a streamlined, less cluttered interface that reduces confusion and improves focus on relevant contextual information.

**Note:** The contextual sidebar for the **Schedule** tab is hidden by default in the base system. However, you can unhide the sidebar as required.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  On the SOW Admin Center page, navigate to **Initial setup** &gt; **SOW properties**.

3.  On the SOW properties page, in the **Hide contextual side panel for specific table and tab combinations** tile, select **Configure**.

    The **hideContextualSidebar** UX property page opens on a separate tab.

    Alternatively, you can also access the **hideContextualSidebar** UX property page by navigating to **All** &gt; **Now Experience Framework** &gt; **Experiences**. From the list of UX applications, select **Service Operations Workspace** and then from the UX Page Properties related list, select the **hideContextualSidebar** UX property.

4.  On the UX Page Property page, edit the **Value** field to add the table and tab combination.

    The input of the **hideContextualSidebar** property is JSON key value pair. You can add multiple json objects with different table and tab combinations to hide the contextual side panel for the table and tab combinations.

    ![Hide contextual sidepanel UX property](../image/hide-contextual-sidepanel-ux-property-sow.png)


**Parent Topic:**[Configuring Service Operations Workspace for ITSM to improve your experience](../concept/configuring-sow-to-improve-experience.md)

