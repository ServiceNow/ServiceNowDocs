---
title: Security Incident Response release notes
description: The ServiceNow Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and efficiently to threats, and view your organization's security posture. Security Incident Response was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
---

# Security Incident Response release notes

The ServiceNow® Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and efficiently to threats, and view your organization's security posture. Security Incident Response was enhanced and updated in the Yokohama release.

## Security Incident Response highlights for the Yokohama release

-   Identify inefficiencies and optimize the resolution process of security incidents for faster closure by using Process MIning.
-   Implemented CrowdStrike Next-Gen SIEM integration enabling real-time ingestion of correlated detections, and enrichment data.
-   Enhanced Splunk ES integrations to improve incident classification and enable efficient retrieval of historical data and alerts.
-   Include the number of VITs indirectly associated with a CVE through TPEs.
-   Help managers ensure there are no gaps in coverage and analysts are always available to address security incidents by configuring shifts for analysts.
-   Define default child nodes to populate in the relationship graph, and add or remove child nodes at the parent node level.

See [Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sir-landing-page.md) for more information.

**Important:** Security Incident Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Process Mining for security incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sir-process-mining.md)**

    Identify factors contributing to delays in processing Security Incident Response \(SIR\) incidents that take a long time to close or resolve by scanning historical SIR records through Process Mining. Time-consuming factors can include multiple reassignments, prolonged hold times, and periods of inactivity.

-   **[CrowdStrike Next-Gen SIEM integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/crowdstrike-next-gen-integration-secops.md)**

    As a Profile Admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM Detection and Events Fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so that you don't have to create duplicate security incidents.
    -   Schedule ongoing detection ingestion.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **[Create and name an event profile for the Splunk Enterprise Security event ingestion integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/splunk-event-ingest-create-profile-security.md)**
    -   Enables bidirectional updates and closure synchronization between Splunk ES and Splunk integrations.
    -   Enables retrieval of historical, and ongoing data including closed events, with an option to pull the closed events into the ServiceNow Splunk ES instance.
    -   Receive updates for the mapped fields in SIR.
-   **[Components installed with Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/installed-with-sir.md)**

    A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and create, edit, delete, and manage profiles for the Splunk, Splunk ES, and Azure Sentinel Integration for Security Operations application.

-   **[Add indirectly linked VITs to CVEs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/configure-mitre-att-ck-properties.md)**

    Identify all the Third-Party Entities \(TPEs\) associated with a Common Vulnerabilities and Exposures \(CVE\) and then calculate and display the total number of vulnerable items \(VITs\) indirectly linked to those CVEs through the TPEs by setting the sn\_ti.include\_cve\_vit\_indirect\_relation property.

-   **[Configure on-call schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/on-call-schedule-sir.md)**

    As an admin:

    -   Create a shift and assign or remove members to/from the shift.
    -   Create/edit on-call schedules for groups.
    -   View any group’s on-call schedule, including those to which they belong.
    As an analyst:

    -   Specify your availability and preferred contact methods.
    -   View your on-call schedule and see other members of your shift.
-   **[Configure report templates in Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/daily-status-sir.md)**

    As an admin, create report templates that can be used to generate an incident summary or an executive summary for analysis and sharing.

    As an analyst, use the templates to generate analyst summary or executive summary reports for a SIR incident that can be shared over email.

-   **[Security Incident Response conference call integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sir-conf-call-capability.md)**

    Initiate conference calls using communication channels such as Microsoft Teams, Cisco Webex, or Zoom with customers and peer agents to resolve security incidents over a call by using the SIR conference call feature.

-   **[Enhancements to relationship graphs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sir-relationship-graph.md)**

    As an admin:

    -   Define default child nodes to populate in the relationship graph.
    -   Configure relationship labels.
    As an analyst:

    -   Add or remove child nodes at the parent node level.
    -   Save the state of the relationship graph.
    -   Retrieve updated data.
-   **[Proofpoint integration for Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/proofpoint-integration-secops-landing.md)**

    Proofpoint integration for Security Operations supports integration between SOAR \(Security Orchestration, Automation, and Response\) and Proofpoint Targeted Attack Protection \(TAP\) software. This integration provides the following benefits:

    -   Detect and block threats such as business email compromise and tags suspicious emails for tracking, analysis, and audit.
    -   Import data to automatically create security incidents for email events that are not captured by TAP products.
-   **[Data Loss Prevention Incident Response Analyst Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/using-dlp-ops-portal.md)**

    Preview the evidence file of the incident from either the Data Loss Prevention analyst workspace or the DLP end user workspace.


## UI changes

-   **[Start a Sidebar chat in Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/initiate-chat-sidebar-sir.md)**

    The **Discuss** option has been renamed **Start Chat** and moved under the **Collaborate** option.


## Changed in this release

-   **[Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations-landing-page.md)**

<table id="table_h5p_xyl_sdc"><thead><tr><th>

Integration name

</th><th>

Integration changes

</th></tr></thead><tbody><tr><td>

Microsoft Teams Chat

</td><td>

Simplified the setup of Microsoft Teams Chat integration with Major Security Incident Management Workspace. For more information, see [Integrate Major Security Incident Management with Microsoft SharePoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/integrate-msim-sharepoint.md).

</td></tr><tr><td>

Microsoft SharePoint

</td><td>

Simplified the setup of Microsoft SharePoint integration with Major Security Incident Management Workspace. For more information, see [Integrate Major Security Incident Management with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/integrate-teams-msim.md).

</td></tr><tr><td>

Security Incident Response Integrations

</td><td>

Workflow was migrated to Workflow Studio. For more information, see the following:-   [Get Log Data Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/get-threat-log-data.md)
-   [Get WildFire Data Enrichment Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/enrich-wildfire-data.md)
-   [Get started with the Microsoft Exchange On-Premises integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/activate-configure-ms-exch-on-prem-integ.md)
-   [Microsoft Exchange - Perform Email Search and Deletion flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/ms-exch-perform-email-search-deletion-wf.md)
-   [Get AutoFocus Session Info Enrichment Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/search-for-malicious-content.md)


</td></tr><tr><td>

Security Incident Response Orchestration

</td><td>

Workflow was migrated to Workflow Studio in the section [Run procdump flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/invoke_procdump.md).

</td></tr><tr><td>

Security Operations common functionality

</td><td>

Workflow was migrated to Workflow Studio. For more information, see the following:-   [Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/integration-capabilities.md)
-   [Security Operations Integration- Block Request capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/block-request-capability.md)
-   [Security Operations Integration- Email Search and Delete capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/email-search-capability.md)
-   [Security Operations Integration- Enrich CI capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/enrich-ci-capability.md)
-   [Security Operations Integration- Enrich Observable capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/enrich-observable-capability.md)
-   [Security Operations Integration- Get Network Statistics capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/get-network-statistics-capability.md)
-   [Security Operations Integration- Get Running Processes capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/get-running-processes-capability.md)
-   [Security Operations Integration- Isolate Host capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/isolate-host-capability.md)
-   [Security Operations Integration- Publish to Watchlist capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/pubish-to-watchlist-capability.md)
-   [Security Operations Integration- Sightings Search capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sightings-search-capability.md)
-   [Security Operations Integration - Threat Lookup capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sec-ops-threat-lookups-capability.md)
-   [Change the order of flow execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/change-wf-execution-order.md)


</td></tr></tbody>
</table>-   **[Other additional Security Incident Response setup tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/t_ConfigureSIM.md)**

    View security incidents with read access and update security incidents with write access without any defined security role.


## Activation information

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Security Operations common functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sec-ops-common-functionality.md)**

    The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


## Related ServiceNow applications and features

-   **[Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/vuln-landing-page.md)**

    Vulnerability Response is part of the Security Operations application suite. Together, these applications connect security to your IT department, increase the speed and efficiency of your response, and give you a definitive view of your security posture.

-   **[Threat Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/threat-intel-landing-page.md)**

    The ServiceNow® Threat Intelligence application enables you to find indicators of compromise \(IoC\) and enrich security incidents with threat intelligence data.


**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/security-operations-rn-landing.md)

