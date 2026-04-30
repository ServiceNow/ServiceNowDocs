---
title: Enable Computer Telephony Integration providers to interact with the Service Operations Workspace
description: Enable an agent \(with the sn\_openframe\_user role\) to receive inbound calls and place outbound calls using the Computer Telephony Integration \(CTI\) interface.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Enable Computer Telephony Integration providers to interact with the Service Operations Workspace

Enable an agent \(with the sn\_openframe\_user role\) to receive inbound calls and place outbound calls using the Computer Telephony Integration \(CTI\) interface.

## Before you begin

Enable the following plugins.

-   com.snc.notify
-   com.snc.cti
-   com.sn\_openframe

For more information about installing and enabling a plugin, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Role required: admin

## About this task

The CTI integration helps an agent call a user using the phone number in the user profile and contact cards. The ServiceNow application uses the OpenFrame API when an agent initiates a call. The OpenFrame API helps the ServiceNow AI Platform® communicate with the connectors, such as an Amazon connector, already configured in the application.

For more information about CTI integration, see [Integrating with Computer Telephony Integration \(CTI\)](https://www.servicenow.com/docs/access?context=cti-csm-integration&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

For more information on the various OpenFrame APIs, see [openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

## Procedure

1.  From the **All** &gt; **sys\_properties.list**.

2.  Open the **sn\_sow.default\_call\_from\_contact\_page** property.

3.  In the **Value** field, specify `CTI`.

4.  Select **Update**.


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

[Configure the task record information in the MS Teams Import tab](configure-record-details-import-chat-sow.md)

[Specify the refresh duration for user presence in Service Operations Workspace](specify-refresh-duration-user-presence.md)

[Install Universal Request for Service Operations Workspace](install-ur-sow.md)

[Install Universal Task for Service Operations Workspace](install-ut-sow.md)

[Configuring Interaction Management in Service Operations Workspace](../concept/configure-interaction-management-sow.md)

