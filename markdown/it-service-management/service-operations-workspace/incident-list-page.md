---
title: Configure the SOW list page
description: Configure the fuzzyCount property to modify how the number of records is displayed on the SOW list page thus improving system performance.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-10-08"
reading_time_minutes: 5
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the SOW list page

Configure the **fuzzyCount** property to modify how the number of records is displayed on the SOW list page thus improving system performance.

## About this task

On the SOW list page, right-click on a record to use the following options:

-   Copy URL: Copy the URL of the record to a clipboard and share the record URL with other stakeholders.
-   Copy sys ID: Copy the sys ID of the record to a clipboard and share the sys ID of the record with other stakeholders

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

2.  From the list of UX applications, select **Service Operations Workspace**.

3.  On the UX Application form, from the UX Page Properties related list, select the **fuzzyCount** property.

4.  On the UX Page Property page, edit the **Value** field.

<table id="table_pgs_wcw_cdc"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\{"default":-1\}.

</td><td>

Displays the count of the total number of records in an application.![Count of incidents](../image/fuzzycount.png)

</td></tr><tr><td>

\{"default":&lt;integer&gt;\}.

</td><td>

Displays the count of the number of records in an application as &lt;integer+&gt;.For example, if the incident has 124 records, if you configure the value of the property as 10, the system displays the count of incidents as 10+.

![Count after updating the value of fuzzyCount property](../image/fuzzycount-2.png)

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

