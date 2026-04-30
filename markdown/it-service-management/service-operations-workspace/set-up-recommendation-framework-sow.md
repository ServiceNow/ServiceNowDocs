---
title: Configuring Recommendation Framework in Service Operations Workspace
description: You can enable an agent working on an incident to view predictions provided by Recommendation Framework.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configuring Recommendation Framework in Service Operations Workspace

You can enable an agent working on an incident to view predictions provided by Recommendation Framework.

Recommendation Framework is now deprecated and no longer supported or available for new activation. Recommended Actions for ITSM feature provides the latest experience for this functionality. To get the advanced version, you must install the Advanced Recommended actions for ITSM \(com.snc.uib.sow\_itsm\_ra\_advanced\) plugin and you must procure ITSM Pro package subscription.

**Note:** The best practice to get the advanced version is to install the Task Intelligence for ITSM \(com.snc.itsm\_ml\_task\) plugin and procure the ITSM Pro package subscription. For more information, see [Exploring Recommended Actions for ITSM in Service Operations Workspace](exploring-recommended-actions-for-itsm-in-service-operations-workspace.md).

You must ensure that the following requirements are met:

-   Install the Service Operations Workspace ITSM Applications \(sn\_sow\_itsm\_cont\) application from [ServiceNow Store.](https://store.servicenow.com/sn_appstore_store.do#!/store/home) For information about this installation, see [Getting started with Service Operations Workspace for ITSM](getting-started-sow.md). With this installation, the following Recommendation Framework applications are also installed.

    |Application|Description|
    |-----------|-----------|
    |Recommendation Framework \(sn\_rf\)|Provides the framework for dynamic and contextual recommendations in a configurable workspace.|
    |Recommendations for Incident Management \(sn\_sow\_incident\_rf\)|Provides configurations, for example, recommendation rules, to predict recommendations for an incident in Service Operations Workspace.|

-   Install the Predictive Intelligence for Incident plugin \(com.snc.incident.ml\) to install the Relevant problems solution definition. For information about this plugin installation, see [Request Predictive Intelligence for Incident](../../incident-management/task/request-predictive-intelligence-for-im.md).
-   Install the Predictive Intelligence for Major Incident Management plugin \(com.snc.incident.mim.ml\_solution\) to install the following IT Service Management solution definitions. For information about this plugin installation, see [Request Predictive Intelligence for Major Incident Management](../../incident-management/task/request-pred-intelli-mim.md).
-   Install the Predictive Intelligence for Incident Management plugin \(com.snc.incident.ml\_solution\) to install the following IT Service Management solution definitions. For information about this plugin installation, see [Request Predictive Intelligence for Incident Management](../../incident-management/task/request-pred-intelli-inc-mgmt.md).
    -   Similar Knowledge Articles
    -   Similar Open Incidents
    -   Incident Service
    -   Incident Configuration Item
    -   Incident Assignment
    -   Similar Resolved Incidents
-   Train solution definitions to predict recommendations for an incident. For information about training solution definitions, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

-   **[Configure Recommendation Framework for an incident in Service Operations Workspace](../task/configure-rf-properties.md)**  
Enable recommendations at field level or from the contextual sidebar for an incident in Service Operations Workspace.

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

[Configure the display of requester related records in an interaction](../task/configure-order-related-records-interaction.md)

[On-call Scheduling in Service Operations Workspace](../task/on-call-scheduling-in-service-operations-workspace.md)

[Configure the experts On-call panel](../task/customize-experts-on-call-tab.md)

[Setting up Service Desk assisted Password Reset in Service Operations Workspace](setup-password-reset-sow.md)

[Enable Computer Telephony Integration providers to interact with the Service Operations Workspace](../task/integrate-cti-sow.md)

[Configure the task record information in the MS Teams Import tab](../task/configure-record-details-import-chat-sow.md)

[Specify the refresh duration for user presence in Service Operations Workspace](../task/specify-refresh-duration-user-presence.md)

[Install Universal Request for Service Operations Workspace](../task/install-ur-sow.md)

[Install Universal Task for Service Operations Workspace](../task/install-ut-sow.md)

[Configuring Interaction Management in Service Operations Workspace](configure-interaction-management-sow.md)

