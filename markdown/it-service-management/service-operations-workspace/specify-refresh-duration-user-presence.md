---
title: Specify the refresh duration for user presence in Service Operations Workspace
description: Define the duration after which the user presence should be refreshed for all collaboration channels in Service Operations Workspace.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Specify the refresh duration for user presence in Service Operations Workspace

Define the duration after which the user presence should be refreshed for all collaboration channels in Service Operations Workspace.

## Before you begin

Role required: admin

## About this task

The **sn\_sow\_collab.user\_presence\_refresh\_duration** property specifies the refresh duration of user presence for all collaboration channels in Service Operations Workspace. However, if the user presence refresh duration is also defined for an individual collaboration channel, then the maximum of these two values is considered for that channel.

For example, consider the following scenario where the user presence refresh duration is defined individually for Microsoft Teams and also for all collaboration channels in Service Operations Workspace.

-   The **sn\_tcm\_collab\_hook.teams.presence\_status\_cache\_invalidate\_duration** property value is set to 240 secs. For information about defining the user presence refresh duration for Microsoft Teams, see [Configure cache duration for the user presence status](https://www.servicenow.com/docs/access?context=configure-cache-duration&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).
-   The **sn\_sow\_collab.user\_presence\_refresh\_duration** property value is set to 180 secs.

In this case, the value specified for the **sn\_tcm\_collab\_hook.teams.presence\_status\_cache\_invalidate\_duration** property is considered to refresh the user presence in Microsoft Teams.

## Procedure

1.  From the **All** menu, navigate to **sys\_properties.list**.

2.  Select the **sn\_sow\_collab.user\_presence\_refresh\_duration** property.

3.  In the **Value** field, specify the duration after which you want the user presence to refresh.

4.  Click **Update**.


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

[Configure the task record information in the MS Teams Import tab](configure-record-details-import-chat-sow.md)

[Install Universal Request for Service Operations Workspace](install-ur-sow.md)

[Install Universal Task for Service Operations Workspace](install-ut-sow.md)

[Configuring Interaction Management in Service Operations Workspace](../concept/configure-interaction-management-sow.md)

