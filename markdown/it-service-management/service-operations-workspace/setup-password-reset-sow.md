---
title: Setting up Service Desk assisted Password Reset in Service Operations Workspace
description: The Password Reset application provides a mechanism for end users to either unlock the account or reset their password with the help of service desk support. This feature enables a secure and an efficient password management system. The users must reach out to the service desk agents to update their login credentials.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Setting up Service Desk assisted Password Reset in Service Operations Workspace

The Password Reset application provides a mechanism for end users to either unlock the account or reset their password with the help of service desk support. This feature enables a secure and an efficient password management system. The users must reach out to the service desk agents to update their login credentials.

Before you configure the password reset, you must define the password reset process. For more information, see [Plan your Password Reset processes](https://www.servicenow.com/docs/access?context=t_PlanPasswordReset&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

The password reset feature is available in the base system. Alternatively, you can customize the password reset process to meet your organization's needs.

-   **[Assign the Password Reset Service Desk role to the user](../task/assign-sd-role-pr-sow.md)**  
Assign the password reset service desk agent \(password\_reset\_service\_desk\) role to the users to work on the incidents or interactions related to the password reset issues.
-   **[Create credential store for Password Reset in Service Operations Workspace](../task/create-cred-store-pr-sow.md)**  
Create a password reset credential store record to configure access to your credential store server while a user is changing or resetting a password.
-   **[Create password reset process in Service Operations Workspace](../task/create-password-reset-process-sow.md)**  
Create configure credentials, verification methods and settings, and enrollment settings to create a password reset process.
-   **[Configure the verification methods for service desk process in Service Operations Workspace](configuring-verification-methods-pr-sow.md)**  
Create and edit verification methods to ensure they align with service desk processes, and map each verification to a specific process. Upon mapping the processes, integrate them with UXF routes to complete an end-to-end flow for resetting a password in Service Operations Workspace.
-   **[Configure the password policies](../task/configure-password-policies-pr-sow.md)**  
Create a password policy to ensure that all passwords are strong and secure.
-   **[Configure the session properties](../task/configure-session-properties-pr-sow.md)**  
Configure the password reset properties based on the requirement.

**Parent Topic:**[Configuring Service Operations Workspace for ITSM](configure-sow.md)

**Related topics**  


[Admin Center in Service Operations Workspace for ITSM](admin-center-sow.md)

[Customize the Service Operations Workspace for ITSM landing page](customize-sow-landing-page.md)

[Assign the service desk agent role to the user in Service Operations Workspace](../task/assign-service-desk-agent-role-sow.md)

[Reorder the navigation pane modules in Service Operations Workspace for ITSM](../task/reorder-left-navigation-pane-modules.md)

[Configure a record page tab in Service Operations Workspace](../task/configure-record-page-tab.md)

[Configure a task record form in Service Operations Workspace](../task/configure-form-layout-task.md)

[Configure the inbox in Service Operations Workspace](../task/configure-inbox-in-sow.md)

[AI Search in Service Operations Workspace for ITSM](ai-search-sow.md)

[Configure Standard Record Page in Service Operations Workspace](srp-service-operations-workspace.md)

[Configure the SOW list page](../task/incident-list-page.md)

[Define and customize activity stream tags](../task/define-customize-activity-stream-tags.md)

[Configure the Assign or Resolve dialog box for an incident or change request in Service Operations Workspace](../task/configure-assign-resolve-modals-incident.md)

[Customize the incident record page](customize-the-incident-record-page.md#)

[Setting up Investigation Framework in Service Operations Workspace](set-up-investigate.md)

[Create a task type for problem or change in Service Operations Workspace](../task/create-task-type-sow.md)

[Configuring Recommendation Framework in Service Operations Workspace](set-up-recommendation-framework-sow.md)

[Configure the display of requester related records in an interaction](../task/configure-order-related-records-interaction.md)

[On-call Scheduling in Service Operations Workspace](../task/on-call-scheduling-in-service-operations-workspace.md)

[Configure the experts On-call panel](../task/customize-experts-on-call-tab.md)

[Enable Computer Telephony Integration providers to interact with the Service Operations Workspace](../task/integrate-cti-sow.md)

[Configure the task record information in the MS Teams Import tab](../task/configure-record-details-import-chat-sow.md)

[Specify the refresh duration for user presence in Service Operations Workspace](../task/specify-refresh-duration-user-presence.md)

[Install Universal Request for Service Operations Workspace](../task/install-ur-sow.md)

[Install Universal Task for Service Operations Workspace](../task/install-ut-sow.md)

[Configuring Interaction Management in Service Operations Workspace](configure-interaction-management-sow.md)

