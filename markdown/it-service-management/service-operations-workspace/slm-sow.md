---
title: Service Level Management in Service Operations Workspace
description: You can access the service level agreement \(SLA\) information for an incident on the Service Operations Workspace landing page and incident record page.Monitor task service level agreements \(SLAs\) displayed on an incident record page.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Use, Service Operations Workspace for ITSM, IT Service Management]
---

# Service Level Management in Service Operations Workspace

You can access the service level agreement \(SLA\) information for an incident on the Service Operations Workspace landing page and incident record page.

## SLA information on the Service Operations Workspace landing page

On the Service Operations Workspace landing page, you can click the **Incident SLAs** card to view incidents grouped by their SLAs. This card displays SLA details only for incidents assigned to the agent. For information on possible customizations for this card, see [Configure the donut color in the Overview section](../task/customize-donut-color.md).

![Overview section](../image/overview-section.png "Overview section")

For information about monitoring SLAs, see [Monitoring Service Level Agreement \(SLA\)](../../service-level-management/concept/c_SLAForTheEndUser.md).

**Parent Topic:**[Using Service Operations Workspace for ITSM](use-sow.md)

**Related topics**  


[Add a user-specific quick link on the ITSM landing page](../task/add-quick-link.md)

[Create a list in Service Operations Workspace](../task/create-list-sow.md)

[View and approve records in Service Operations Workspace](../task/view-approvals-sow.md)

[Change Management in Service Operations Workspace](change-sow.md)

[Incident Management in Service Operations Workspace](incident-sow.md)

[Interaction Management in Service Operations Workspace](interaction-sow.md)

[Knowledge Management in Service Operations Workspace](knowledge-articles-sow.md)

[On-Call Scheduling in Service Operations Workspace](on-call-scheduling-in-sow.md)

[Problem Management in Service Operations Workspace](problem-sow.md)

[Recommendation Framework in Service Operations Workspace](recommendation-framework-sow.md)

[Recommended Actions for ITSM in Service Operations Workspace](recommended-actions-for-itsm-in-service-operations-workspace.md)

[Request Management in Service Operations Workspace](request-sow.md)

[ServiceNow integrations with Microsoft Teams in Service Operations Workspace](msteams-sow.md)

[Walk-up Experience management in Service Operations Workspace](walkup-sow.md)

[Workforce Optimization for ITSM in the Service Operations Workspace](wfo-itsm-service-operations-workspace.md)

[Collaboration in Service Operations Workspace](collaboration-sow.md)

[Computer Telephony Integration in Service Operations Workspace](configure-cti-sow.md)

[Live Agent chat in Service Operations Workspace](configure-liveagent-sow.md)

[Using Universal Request in Service Operations Workspace](using-ur-sow.md)

[Using Universal Task in Service Operations Workspace](using-ut-sow.md)

[Resetting password using Service-desk assisted Password Reset in Service Operations Workspace](resetting-password-pr-sow.md)

## View service level agreement information for an incident

Monitor task service level agreements \(SLAs\) displayed on an incident record page.

### Before you begin

Role required: itil or admin

The following SLA timer configurations display the response and resolution SLA for an incident.

-   Incident Response
-   Incident Resolution

You should configure SLA timer configuration mappings for these timer configurations. For information on how you can configure these mappings, see [Configure the SLA timer](../../service-level-management/task/sla-timer-configurations.md).

### Procedure

1.  Open an incident record page.

2.  From the contextual side panel, select the record Information icon \(![record Information icon](../image/record-info-icon.png)\).

    -   The response and resolution SLAs are displayed.
    -   In case of multiple SLA timer configuration mappings for Incident Response and Incident Resolution timer configurations, only one response and resolution SLA record associated with the mapping with the least order is displayed.
    -   After the SLA is complete, the time taken to respond and resolve the incident are displayed.
    For information about configuring the display of SLA information, see [Customize the display of service level agreements for an incident](customize-the-incident-record-page.md#).

    ![SLA information for an incident](../image/sla-info-sow.png "SLA information for an incident")

3.  To view all SLAs related to the incident, click **View more SLAs**.

    A list of all task SLAs is displayed.


