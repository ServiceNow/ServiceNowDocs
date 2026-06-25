---
title: Service Level Management in Service Operations Workspace
description: You can access the service level agreement \(SLA\) information for an incident on the Service Operations Workspace landing page and incident record page.Monitor task service level agreements \(SLAs\) displayed on an incident record page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/slm-sow.html
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

On the Service Operations Workspace landing page, you can click the **Incident SLAs** card to view incidents grouped by their SLAs. This card displays SLA details only for incidents assigned to the agent. For information on possible customizations for this card, see [Configure the donut color in the Overview section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/customize-donut-color.md).

\[Omitted image "overview-section.png"\] Alt text: Overview section

For information about monitoring SLAs, see [Monitoring Service Level Agreement \(SLA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/c_SLAForTheEndUser.md).

**Parent Topic:**[Managing IT services in your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/managing-services-operations-in-organization.md)

**Related topics**  


[Knowledge Management in Service Operations Workspace]()

[Major Incident Management in Service Operations Workspace]()

[On-Call Scheduling in Service Operations Workspace]()

[Problem Management in Service Operations Workspace]()

[Recommendation Framework in Service Operations Workspace]()

[Recommended Actions for ITSM in Service Operations Workspace]()

[ServiceNow integrations with Microsoft Teams in Service Operations Workspace]()

[Walk-up Experience management in Service Operations Workspace]()

[Collaboration in Service Operations Workspace]()

[Computer Telephony Integration in Service Operations Workspace]()

[Universal Request in Service Operations Workspace]()

[Universal Task in Service Operations Workspace]()

[Resetting password using Service-desk assisted Password Reset in Service Operations Workspace]()

## View service level agreement information for an incident

Monitor task service level agreements \(SLAs\) displayed on an incident record page.

### Before you begin

Role required: itil or admin

The following SLA timer configurations display the response and resolution SLA for an incident.

-   Incident Response
-   Incident Resolution

You should configure SLA timer configuration mappings for these timer configurations. For information on how you can configure these mappings, see [Configure the SLA timer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/sla-timer-configurations.md).

### Procedure

1.  Open an incident record page.

2.  From the contextual side panel, select the record Information icon \(\[Omitted image "record-info-icon.png"\] Alt text: record Information icon\).

    -   The response and resolution SLAs are displayed.
    -   In case of multiple SLA timer configuration mappings for Incident Response and Incident Resolution timer configurations, only one response and resolution SLA record associated with the mapping with the least order is displayed.
    -   After the SLA is complete, the time taken to respond and resolve the incident are displayed.
    For information about configuring the display of SLA information, see [Customize the display of service level agreements for an incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/customize-the-incident-record-page.md).

    \[Omitted image "sla-info-sow.png"\] Alt text: SLA information for an incident

3.  To view all SLAs related to the incident, click **View more SLAs**.

    A list of all task SLAs is displayed.


