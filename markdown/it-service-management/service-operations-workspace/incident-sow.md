---
title: Incident Management in Service Operations Workspace
description: You can create and manage your incidents in Service Operations Workspace.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Incident Management in Service Operations Workspace

You can create and manage your incidents in Service Operations Workspace.

Introduction to incident management 

![Tabs of an incident record](../image/sow-incident-tabs-header-new.gif "Tabs of an incident record page in Service Operations Workspace")

## Overview tab

This tab displays the following information about an incident:

-   Summary
-   Impact
-   Cause
-   Resolution

From the Compose section, you can add comments and work notes for the incident.

The Overview tab displays the field information along with the field labels, including when you're in read mode.

For more information on the fields displayed on the **Overview** tab, see [View and update incident information on the Overview tab in SOW](../task/view-update-inc-overview-tab.md).

You can customize the display of the information on the **Overview** tab. For more information, see [Customize the Overview tab for an incident](customize-the-incident-record-page.md#).

## Investigation tab

This tab enables you to investigate any affected CIs with the ci\_computer or ci\_server class associated with the incidents. The tab displays the metrics information of the associated primary CI or any affected CI that is selected, which helps you to analyze and resolve the issue. You can use the various remedial actions on this tab to resolve the CI-related issues.

By default, the tab displays metrics information of the primary affected CI associated with the incident. But you can also select and view the information for any affected CI with the ci\_computer or ci\_server class that is associated with the incident. For information about how you can set up Investigation Framework, see [Setting up Investigation Framework in Service Operations Workspace](set-up-investigate.md).

**Note:**

-   The tab is visible only if the Agent Client Collector \(ACC\) or Microsoft Endpoint Configuration Manager \(MECM\) adapters are installed and configured.
-   The tab displays the metrics information for the CI only in the following conditions:
    -   Agent Client Collector or Microsoft Endpoint Configuration Manager \(MECM\) is installed for the associated CI. This helps to retrieve the metrics data for the CI.
    -   The associated CI class is a CMDB CI computer.
-   This feature supports only the macOS, Windows, and Linux operating systems.

You can also customize the display of the metrics information on this tab. For more information, see [Customize the Investigate tab](customize-the-incident-record-page.md#).

For more information on the metrics displayed on this tab, see [Features of the Investigation tab](../reference/features-of-investigation-tab.md).

## Communicate tab

This tab displays all the communication tasks and options that enable you to communicate with the stakeholders in the various phases of an incident. This tab is available only if any of the following conditions are met:

-   For a major incident - The Major Incident Management \(sn-sow-mim\) plugin is active and configured in Admin Center, for Service Operations Workspace. For more information, see [Setting up Major Incident Management in Service Operations Workspace](setup-mim-sow.md).
-   For Incident – The Task Communications Management and Incident Communications Management applications are installed, active, and configured in the instance and you select the **New Communication** option from the **More Actions** \(![More actions icon](../image/mim-more-actions-top-icon.png)\) icon of the Incident record page. For more information, see Task Communications Management and [Incident Communications Management](../../incident-alert-management/concept/c_IncidentAlertManagement.md).

For more information on the features of the **Communicate** tab, see [Communicating with stakeholders about incidents and major incidents in SOW](communicating-with-stakeholders-sow.md).

## Post incident report tab

This tab enables you to generate, configure, publish, and export a post incident report for a major incident after it's resolved. The post incident report enables you to review the cause and resolution of the major incident and also identify potential process gaps. Based on this information, you can take preventive measures to avoid the issue in the future or to handle the major incident in a better way. This tab is available only if the following conditions are met:

-   Major Incident Management is active and configured in Admin Center for Service Operations Workspace. For more information, see [Setting up Major Incident Management in Service Operations Workspace](setup-mim-sow.md).
-   The major incident is in the **Resolved** state.

For more information on the features of the **Post incident report** tab, see [Review and update a post incident report](../task/review-update-pir-mim-sow.md).

## Details tab

This tab displays detailed information about the incident. For example, the short description, assignment details, and related records. For more information on how you can configure fields in this tab, see [Configure a task record form in Service Operations Workspace](../task/configure-form-layout-task.md).

## Related records tab

This tab provides a list view of the records associated with the incident. For example, task SLAs and affected CIs.

## Contextual side panel

From this section, you can view record information and recommendations, collaborate using Microsoft Teams, and reach out to experts on-call to resolve incidents quickly.

For more information about Incident Management, see [Incident Management](../../incident-management/concept/c_IncidentManagement.md).

-   **[Create an incident in Service Operations Workspace](../task/create-incident-sow.md)**  
Track the investigation, possible solutions, and resolution of a problem for a customer.
-   **[View and update incident information on the Overview tab in SOW](../task/view-update-inc-overview-tab.md)**  
View and update the incident information, such as summary, impact, cause, and resolution, from the **Overview** tab. This incident information helps you analyze the issue and resolve the incident quickly.
-   **[Viewing incident record information using the Contextual side panel](view-inc-record-info-contextual-sidepanel.md)**  
View the incident record information, such as caller details and assets, from the Contextual side panel. Use this information to help manage an incident more efficiently.
-   **[Work on an incident list page in Service Operations Workspace](../task/work-incident-list-page-sow.md)**  
Perform various actions on an incident from the incident list page in Service Operations Workspace \(SOW\).
-   **[Work on an incident record in Service Operations Workspace](../task/work-on-incident-sow.md)**  
If resolving the incident involves creating a problem, change, service request, and so on, you can create them directly from the incident record.
-   **[Remedial actions using Playbook](remedial-actions-playbook.md)**  
Resolve the CI-related issues using the remedial actions using Playbook in the Investigate tab.
-   **[Close resolved incident](../task/close-resolved-incident-sow.md)**  
Close an resolved incident when the user is satisfied with the provided resolution.
-   **[Reopen an incident in Service Operations Workspace](../task/reopen-incident-sow.md)**  
Reopen a resolved incident from the incident record in Service Operations Workspace \(SOW\).
-   **[Incident Management in Service Operations Workspace reference](sow-im-reference.md)**  
Reference topics provide additional information about Incident Management in Service Operations Workspace.

**Parent Topic:**[Operating IT services in your organization](enhancing-services-operations-in-organization.md)

**Related topics**  


[Play a guided tour in Service Operations Workspace](../task/play-guided-tour-sow.md)

[Add a user-specific quick link on the ITSM landing page](../task/add-quick-link.md)

[Create a list in Service Operations Workspace](../task/create-list-sow.md)

[Live Agent chat in Service Operations Workspace](configure-liveagent-sow.md)

[Interaction Management in Service Operations Workspace](interaction-sow.md)

[Request Management in Service Operations Workspace](request-sow.md)

[Change Management in Service Operations Workspace](change-sow.md)

