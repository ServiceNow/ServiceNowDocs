---
title: Configure the experts On-call panel
description: Configure the Experts on-call panel for an incident.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the experts On-call panel

Configure the **Experts on-call** panel for an incident.

## Before you begin

Role required: admin

To configure the Experts On-call panel, ensure that you have added an implementation for the **sn\_sow\_on\_call.ExpertsOnCallTabConfig** extension point.

**Note:**

-   Incident table extension point implementation is added by default. To customize it, edit the script to include **ExpertsOnCallTabConfigForIncident**.
-   Example: If you want to display only the assignment group in the Experts On-call panel, then update the **getRecommendedFieldWatchList** in the script.

## About this task

To add Experts On-call for Problem table, follow the steps:

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Select and open the **sn\_sow\_on\_call.ExpertsOnCallTabConfig** extension point.

3.  Select **Create implementation** from the related links section.

4.  Modify the **Script** as required:

<table id="table_sqq_cwx_dcc"><thead><tr><th>

Method

</th><th>

Inputs

</th><th>

Return

</th></tr></thead><tbody><tr><td>

**getTableName**

</td><td>

None

</td><td>

String – Table name for which an extension point is implemented

</td></tr><tr><td>

**getRecommendedFieldWatchList**

</td><td>

None

</td><td>

Array – List of fields that you want to show on the Experts On-call recommended groups panel.For example: **\[“assignment\_group”, “cmdb\_ci”\]**

</td></tr><tr><td>

**getRecommendedGroups**

</td><td>

-   recordGr – GlideRecord reference
-   fieldWatchList – Object containing all the fields and their respective values.
 For example: **\{ "assignment\_group": &lt;assignment\_group\_sys\_id&gt; \}**

</td><td>

Array – List of objects containing recommended group, sys\_id, and the respective message.For example: **\[ \{ : "Recommended based on assignment group" \} \]**

</td></tr><tr><td>

**isExpertOnCallTabSupported**

</td><td>

None

</td><td>

Boolean – return true to enable the Expert On-call for this table.

</td></tr></tbody>
</table>5.  Select **Update**.


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

[Setting up Service Desk assisted Password Reset in Service Operations Workspace](../concept/setup-password-reset-sow.md)

[Enable Computer Telephony Integration providers to interact with the Service Operations Workspace](integrate-cti-sow.md)

[Configure the task record information in the MS Teams Import tab](configure-record-details-import-chat-sow.md)

[Specify the refresh duration for user presence in Service Operations Workspace](specify-refresh-duration-user-presence.md)

[Install Universal Request for Service Operations Workspace](install-ur-sow.md)

[Install Universal Task for Service Operations Workspace](install-ut-sow.md)

[Configuring Interaction Management in Service Operations Workspace](../concept/configure-interaction-management-sow.md)

