---
title: Configure a record page tab in Service Operations Workspace
description: Configure the display order of a record page tab in Service Operations Workspace.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
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

    If the UX App Route form doesn’t contain the Order field, add the Order field to the form. For more information about adding a field to the form, see [Show or hide fields on a form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&section=t_ConfigureAForm&ft:locale=en-US).

4.  Select **Update**.


**Parent Topic:**[Configuring Service Operations Workspace for ITSM](../concept/configure-sow.md)

**Related topics**  


[Admin Center in Service Operations Workspace for ITSM](../concept/admin-center-sow.md)

[Customize the Service Operations Workspace for ITSM landing page](../concept/customize-sow-landing-page.md)

[Assign the service desk agent role to the user in Service Operations Workspace](assign-service-desk-agent-role-sow.md)

[Reorder the navigation pane modules in Service Operations Workspace for ITSM](reorder-left-navigation-pane-modules.md)

[Configure a task record form in Service Operations Workspace](configure-form-layout-task.md)

[Configure the inbox in Service Operations Workspace](configure-inbox-in-sow.md)

[AI Search in Service Operations Workspace for ITSM](../concept/ai-search-sow.md)

[Configure Standard Record Page in Service Operations Workspace](../concept/srp-service-operations-workspace.md)

[Configure the SOW list page](incident-list-page.md)

[Define and customize activity stream tags](define-customize-activity-stream-tags.md)

[Configure the Assign or Resolve dialog box for an incident or change request in Service Operations Workspace](configure-assign-resolve-modals-incident.md)

[Customize the incident record page](../concept/customize-the-incident-record-page.md#)

[Setting up Investigation Framework in Service Operations Workspace](../concept/set-up-investigate.md)

[Create a task type for problem or change in Service Operations Workspace](create-task-type-sow.md)

[Configuring Recommendation Framework in Service Operations Workspace](../concept/set-up-recommendation-framework-sow.md)

[Configure the display of requester related records in an interaction](configure-order-related-records-interaction.md)

[On-call Scheduling in Service Operations Workspace](on-call-scheduling-in-service-operations-workspace.md)

[Configure the experts On-call panel](customize-experts-on-call-tab.md)

[Setting up Service Desk assisted Password Reset in Service Operations Workspace](../concept/setup-password-reset-sow.md)

[Enable Computer Telephony Integration providers to interact with the Service Operations Workspace](integrate-cti-sow.md)

[Configure the task record information in the MS Teams Import tab](configure-record-details-import-chat-sow.md)

[Specify the refresh duration for user presence in Service Operations Workspace](specify-refresh-duration-user-presence.md)

[Install Universal Request for Service Operations Workspace](install-ur-sow.md)

[Install Universal Task for Service Operations Workspace](install-ut-sow.md)

[Configuring Interaction Management in Service Operations Workspace](../concept/configure-interaction-management-sow.md)

