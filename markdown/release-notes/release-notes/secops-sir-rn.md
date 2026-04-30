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

See [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

**Important:** Security Incident Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Process Mining for security incidents](https://www.servicenow.com/docs/access?context=sir-process-mining&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Identify factors contributing to delays in processing Security Incident Response \(SIR\) incidents that take a long time to close or resolve by scanning historical SIR records through Process Mining. Time-consuming factors can include multiple reassignments, prolonged hold times, and periods of inactivity.

-   **[CrowdStrike Next-Gen SIEM integration](https://www.servicenow.com/docs/access?context=crowdstrike-next-gen-integration-secops&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    As a Profile Admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM Detection and Events Fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so that you don't have to create duplicate security incidents.
    -   Schedule ongoing detection ingestion.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **[Create and name an event profile for the Splunk Enterprise Security event ingestion integration](https://www.servicenow.com/docs/access?context=splunk-event-ingest-create-profile-security&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**
    -   Enables bidirectional updates and closure synchronization between Splunk ES and Splunk integrations.
    -   Enables retrieval of historical, and ongoing data including closed events, with an option to pull the closed events into the ServiceNow Splunk ES instance.
    -   Receive updates for the mapped fields in SIR.
-   **[Components installed with Security Incident Response](https://www.servicenow.com/docs/access?context=installed-with-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and create, edit, delete, and manage profiles for the Splunk, Splunk ES, and Azure Sentinel Integration for Security Operations application.

-   **[Add indirectly linked VITs to CVEs](https://www.servicenow.com/docs/access?context=configure-mitre-att-ck-properties&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Identify all the Third-Party Entities \(TPEs\) associated with a Common Vulnerabilities and Exposures \(CVE\) and then calculate and display the total number of vulnerable items \(VITs\) indirectly linked to those CVEs through the TPEs by setting the sn\_ti.include\_cve\_vit\_indirect\_relation property.

-   **[Configure on-call schedules](https://www.servicenow.com/docs/access?context=on-call-schedule-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    As an admin:

    -   Create a shift and assign or remove members to/from the shift.
    -   Create/edit on-call schedules for groups.
    -   View any group’s on-call schedule, including those to which they belong.
    As an analyst:

    -   Specify your availability and preferred contact methods.
    -   View your on-call schedule and see other members of your shift.
-   **[Configure report templates in Security Incident Response](https://www.servicenow.com/docs/access?context=daily-status-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    As an admin, create report templates that can be used to generate an incident summary or an executive summary for analysis and sharing.

    As an analyst, use the templates to generate analyst summary or executive summary reports for a SIR incident that can be shared over email.

-   **[Security Incident Response conference call integration](https://www.servicenow.com/docs/access?context=sir-conf-call-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Initiate conference calls using communication channels such as Microsoft Teams, Cisco Webex, or Zoom with customers and peer agents to resolve security incidents over a call by using the SIR conference call feature.

-   **[Enhancements to relationship graphs](https://www.servicenow.com/docs/access?context=sir-relationship-graph&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    As an admin:

    -   Define default child nodes to populate in the relationship graph.
    -   Configure relationship labels.
    As an analyst:

    -   Add or remove child nodes at the parent node level.
    -   Save the state of the relationship graph.
    -   Retrieve updated data.
-   **[Proofpoint integration for Security Operations](https://www.servicenow.com/docs/access?context=proofpoint-integration-secops-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Proofpoint integration for Security Operations supports integration between SOAR \(Security Orchestration, Automation, and Response\) and Proofpoint Targeted Attack Protection \(TAP\) software. This integration provides the following benefits:

    -   Detect and block threats such as business email compromise and tags suspicious emails for tracking, analysis, and audit.
    -   Import data to automatically create security incidents for email events that are not captured by TAP products.
-   **[Data Loss Prevention Incident Response Analyst Workspace](https://www.servicenow.com/docs/access?context=using-dlp-ops-portal&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Preview the evidence file of the incident from either the Data Loss Prevention analyst workspace or the DLP end user workspace.


## UI changes

-   **[Start a Sidebar chat in Security Incident Response](https://www.servicenow.com/docs/access?context=initiate-chat-sidebar-sir&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    The **Discuss** option has been renamed **Start Chat** and moved under the **Collaborate** option.


## Changed in this release

-   **[Security Operations](https://www.servicenow.com/docs/access?context=security-operations-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

<table id="table_h5p_xyl_sdc"><thead><tr><th>

Integration name

</th><th>

Integration changes

</th></tr></thead><tbody><tr><td>

Microsoft Teams Chat

</td><td>

Simplified the setup of Microsoft Teams Chat integration with Major Security Incident Management Workspace. For more information, see [Integrate Major Security Incident Management with Microsoft SharePoint](https://www.servicenow.com/docs/access?context=integrate-msim-sharepoint&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).

</td></tr><tr><td>

Microsoft SharePoint

</td><td>

Simplified the setup of Microsoft SharePoint integration with Major Security Incident Management Workspace. For more information, see [Integrate Major Security Incident Management with Microsoft Teams](https://www.servicenow.com/docs/access?context=integrate-teams-msim&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).

</td></tr><tr><td>

Security Incident Response Integrations

</td><td>

Workflow was migrated to Workflow Studio. For more information, see the following:-   [Get Log Data Flow](https://www.servicenow.com/docs/access?context=get-threat-log-data&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Get WildFire Data Enrichment Flow](https://www.servicenow.com/docs/access?context=enrich-wildfire-data&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Get started with the Microsoft Exchange On-Premises integration](https://www.servicenow.com/docs/access?context=activate-configure-ms-exch-on-prem-integ&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Microsoft Exchange - Perform Email Search and Deletion flow](https://www.servicenow.com/docs/access?context=ms-exch-perform-email-search-deletion-wf&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Get AutoFocus Session Info Enrichment Flow](https://www.servicenow.com/docs/access?context=search-for-malicious-content&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)


</td></tr><tr><td>

Security Incident Response Orchestration

</td><td>

Workflow was migrated to Workflow Studio in the section [Run procdump flow](https://www.servicenow.com/docs/access?context=invoke_procdump&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).

</td></tr><tr><td>

Security Operations common functionality

</td><td>

Workflow was migrated to Workflow Studio. For more information, see the following:-   [Integration capabilities](https://www.servicenow.com/docs/access?context=integration-capabilities&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Security Operations Integration- Block Request capability](https://www.servicenow.com/docs/access?context=block-request-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Security Operations Integration- Email Search and Delete capability](https://www.servicenow.com/docs/access?context=email-search-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Security Operations Integration- Enrich CI capability](https://www.servicenow.com/docs/access?context=enrich-ci-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Security Operations Integration- Enrich Observable capability](https://www.servicenow.com/docs/access?context=enrich-observable-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Security Operations Integration- Get Network Statistics capability](https://www.servicenow.com/docs/access?context=get-network-statistics-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Security Operations Integration- Get Running Processes capability](https://www.servicenow.com/docs/access?context=get-running-processes-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Security Operations Integration- Isolate Host capability](https://www.servicenow.com/docs/access?context=isolate-host-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Security Operations Integration- Publish to Watchlist capability](https://www.servicenow.com/docs/access?context=pubish-to-watchlist-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Security Operations Integration- Sightings Search capability](https://www.servicenow.com/docs/access?context=sightings-search-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Security Operations Integration - Threat Lookup capability](https://www.servicenow.com/docs/access?context=sec-ops-threat-lookups-capability&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Change the order of flow execution](https://www.servicenow.com/docs/access?context=change-wf-execution-order&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Other additional Security Incident Response setup tasks](https://www.servicenow.com/docs/access?context=t_ConfigureSIM&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    View security incidents with read access and update security incidents with write access without any defined security role.


## Activation information

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


## Related ServiceNow applications and features

-   **[Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Vulnerability Response is part of the Security Operations application suite. Together, these applications connect security to your IT department, increase the speed and efficiency of your response, and give you a definitive view of your security posture.

-   **[Threat Intelligence](https://www.servicenow.com/docs/access?context=threat-intel-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    The ServiceNow® Threat Intelligence application enables you to find indicators of compromise \(IoC\) and enrich security incidents with threat intelligence data.


**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

