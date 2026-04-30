---
title: Configure the task record information in the MS Teams Import tab
description: Customize the task record fields displayed when you view or import a Microsoft Teams chat conversation.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the task record information in the MS Teams Import tab

Customize the task record fields displayed when you view or import a Microsoft Teams chat conversation.

## Before you begin

Role required: admin

## About this task

When you view or import a Microsoft Teams chat conversation for a task record, the record details are displayed in the **Details** section of the **MS Teams Import** tab. These details are configured in the **Script** field of an implementation corresponding to the task record in the sn\_tcm\_collab\_hook.MSTeamsTaskInfoCardHandler extension point.

For information about collaborating on a task record using Microsoft Teams chat, see [Collaborate on a task record using Microsoft Teams in Service Operations Workspace](start-msteams-chat-sow.md).

![MS Teams Import tab.](../image/ms-teams-chat-page.png "MS Teams Import tab")

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  From the Extension Points list, select **sn\_tcm\_collab\_hook.MSTeamsTaskInfoCardHandler**.

3.  From the Implementations related list, select an implementation associated with the task record and modify the **Script** field.

4.  Edit the **Script** field.

5.  Click **Update**.


**Parent Topic:**[Configuring Service Operations Workspace for ITSM](../concept/configure-sow.md)

**Related topics**  


[Admin Center in Service Operations Workspace for ITSM](../concept/admin-center-sow.md)

[Customize the Service Operations Workspace for ITSM landing page](../concept/customize-sow-landing-page.md)

[Assign the service desk agent role to the user in Service Operations Workspace](assign-service-desk-agent-role-sow.md)

[Reorder the navigation pane modules in Service Operations Workspace for ITSM](reorder-left-navigation-pane-modules.md)

[Configure a record page tab in Service Operations Workspace](configure-record-page-tab.md)

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

[Specify the refresh duration for user presence in Service Operations Workspace](specify-refresh-duration-user-presence.md)

[Install Universal Request for Service Operations Workspace](install-ur-sow.md)

[Install Universal Task for Service Operations Workspace](install-ut-sow.md)

[Configuring Interaction Management in Service Operations Workspace](../concept/configure-interaction-management-sow.md)

