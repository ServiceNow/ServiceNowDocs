---
title: Configure a record page tab in Service Operations Workspace
description: Configure the display order of a record page tab in Service Operations Workspace.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring record pages in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM to improve your experience, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure a record page tab in Service Operations Workspace

Configure the display order of a record page tab in Service Operations Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, or admin

## About this task

The record pages \(incident, problem, change, and so on\) in Service Operations Workspace have multiple tabs. Few tabs such as the **Overview** tab of the incident record page are specific to a record page. Few other tabs are common across multiple record pages in multiple workspaces, for example, the **Details** tab. The Details tab is associated with incident, change, problem, and other record pages in multiple workspaces.

When you modify the order of a common tab in multiple record pages and workspaces, the changes are applicable in all those records and workspaces.

## Procedure

1.  From the **All** menu, navigate to **sys\_ux\_app\_route.list**.

2.  From the UX App Routes list, select the tab record that you want to modify.

    -   To modify the order of a common tab. For example, the **Details** tab, select **Record Details Tab**. Any changes that you make are applicable to the **Details** tab in all associated record pages in multiple workspaces.
    -   To modify the order of a record page-specific tab. For example, the **Overview** tab of the incident record page in Service Operations Workspace, select **Overview** whose **App Configuration** is **Service Operations Workspace** and **Parent macroponent** is **Record Page Tabs**. Any changes made are applicable only to the **Overview** tab of the incident record page in Service Operations Workspace.
3.  On the UX App Route form, modify the **Order** field.

    If the UX App Route form doesn’t contain the Order field, add the Order field to the form. For more information about adding a field to the form, see [Show or hide fields on a form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&section=t_ConfigureAForm&ft:locale=en-US).

4.  Select **Update**.


**Parent Topic:**[Configuring record pages in Service Operations Workspace for ITSM](../concept/configuring-record-pages-sow-itsm.md)

