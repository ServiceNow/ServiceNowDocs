---
title: Service Level Management in Service Operations Workspace
description: You can access the service level agreement \(SLA\) information for an incident on the Service Operations Workspace landing page and incident record page.Monitor task service level agreements \(SLAs\) displayed on an incident record page.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Service Level Management in Service Operations Workspace

You can access the service level agreement \(SLA\) information for an incident on the Service Operations Workspace landing page and incident record page.

## SLA information on the Service Operations Workspace landing page

On the Service Operations Workspace landing page, you can click the **Incident SLAs** card to view incidents grouped by their SLAs. This card displays SLA details only for incidents assigned to the agent. For information on possible customizations for this card, see [Configure the donut color in the Overview section](../task/customize-donut-color.md).

![Overview section](../image/overview-section.png "Overview section")

For information about monitoring SLAs, see [Monitoring Service Level Agreement \(SLA\)](../../service-level-management/concept/c_SLAForTheEndUser.md).

**Parent Topic:**[Managing IT services in your organization](managing-services-operations-in-organization.md)

**Related topics**  


[Knowledge Management in Service Operations Workspace](knowledge-articles-sow.md)

[Major Incident Management in Service Operations Workspace](mim-in-sow.md)

[On-Call Scheduling in Service Operations Workspace](on-call-scheduling-in-sow.md)

[Problem Management in Service Operations Workspace](problem-sow.md)

[Recommendation Framework in Service Operations Workspace](recommendation-framework-sow.md)

[Recommended Actions for ITSM in Service Operations Workspace](recommended-actions-for-itsm-in-service-operations-workspace.md)

[ServiceNow integrations with Microsoft Teams in Service Operations Workspace](msteams-sow.md)

[Walk-up Experience management in Service Operations Workspace](walkup-sow.md)

[Collaboration in Service Operations Workspace](collaboration-sow.md)

[Computer Telephony Integration in Service Operations Workspace](configure-cti-sow.md)

[Universal Request in Service Operations Workspace](using-ur-sow.md)

[Universal Task in Service Operations Workspace](using-ut-sow.md)

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


