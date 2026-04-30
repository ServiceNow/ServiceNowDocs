---
title: Security Incident Response release notes
description: The ServiceNow Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and efficiently to threats, and gain insight into your organization's security posture. Security Incident Response was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
---

# Security Incident Response release notes

The ServiceNow® Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and efficiently to threats, and gain insight into your organization's security posture. Security Incident Response was enhanced and updated in the Zurich release.

## Security Incident Response highlights for the Zurich release

-   Integrate Cortex XSIAM by Palo Alto Networks with ServiceNow Security Incident Response platform to turn SIEM insights into actionable incidents, thus accelerating response from detection to closure.
-   Use Advanced Work Assignment \(AWA\) to automatically assign incidents to your security analysts, based on their availability, capacity, and skills.
-   Ingest third-party risk scores in Security Incident Response to factor these scores when calculating risk scores.
-   Starting in version 13.9.33, you can do the following:
    -   Fetch closed offenses from IBM QRadar into Security Incident Response.
    -   Set the batch size for correlation rules during IBM QRadar offense polling to optimize performance.
    -   Use the Now Assist LLM-powered integration builder to rapidly build integrations for Security Incident Response using auto-code generation.
    -   Ingest MITRE D3FEND data and visualize attack–defense relationships through an interactive graph directly within a security incident.
-   Starting in version 13.9.21, you can do the following:
    -   Integrate CrowdStrike Next-Gen SIEM integration with ServiceNow Security Incident Response platform to retrieve detections and convert them into security incidents, thus enabling automated response actions.
    -   Improve incident classification and enable efficient retrieval of historical data and alerts through enhanced Splunk ES integrations.
    -   Configure and use on-call scheduling to prevent gaps in coverage and ensure analysts are available to address security incidents by configuring shifts for analysts.

See [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

**Important:** Security Incident Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Security Incident Response Integration with Cortex XSIAM by Palo Alto Networks](https://www.servicenow.com/docs/access?context=cortex-xsiam-siem&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    As a profile admin:

    -   Create profiles for incident ingestion.
    -   Filter Cortex XSIAM incidents.
    -   Map Cortex XSIAM **Incident**, **Alert**, and **Event** fields to SIR security incident fields.
    -   Aggregate incidents to existing open security incidents to avoid having to create duplicate security incidents.
    -   Synchronize ServiceNow instance Work notes with Palo Alto Networks XSIAM comments.
-   **[Setup ServiceNow Security Operations Event Ingestion Addon for Splunk ES](https://www.servicenow.com/docs/access?context=splunk-es-addon&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The ServiceNow Security Operations Event Ingestion Add-on for Splunk ES enables seamless integration between Splunk and ServiceNow Security Operations, allowing you to send security-related events from Splunk ES to a ServiceNow security incident.

-   **[LLM-powered SIR integration builder](https://www.servicenow.com/docs/access?context=sir-integration-builder-now-assist&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    With the ServiceNow platform's latest LLM powered integrations, you can create product-ready integration quickly. The LLM-powered integration builder has the following capabilities:

    -   Automatically generates integration code from a public API documentation.
    -   Provides guided setup built on existing capabilities.
    -   Provides easy edit and maintenance of the generated auto code.
-   **[Deny rule for phishing emails](https://www.servicenow.com/docs/access?context=urp-about&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The security admin can add rules to prevent the conversion of phishing emails such as false positives or low-risk messages into security incidents. Any new phishing email is verified first with the deny rules to avoid unwanted security incidents.

-   **[MITRE D3FEND framework](https://www.servicenow.com/docs/access?context=mitre-d3fend-framework&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Security administrators can now ingest MITRE D3FEND data. Security analysts can explore MITRE ATT&amp;CK and D3FEND techniques through an interactive, node-based visualization that maps attack techniques, defense techniques, and related artifacts within a Security Incident Response \(SIR\) record.

-   **[Update information in security incident related records](https://www.servicenow.com/docs/access?context=edit-related-records-in-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The security analysts can now edit related records such as associated observables, for a security incident directly from the Related Records list view. Security analysts can quickly update the records without leaving their current context.

-   **[Advanced Work Assignment for Security Incident Response](https://www.servicenow.com/docs/access?context=awa-for-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Use Advanced Work Assignment \(AWA\) to streamline the security incident assignment process which ensure that critical incidents are handled by the most appropriate and available analysts. This improves overall response times and efficiency in security operations.

    As an admin, configure the following:

    -   Service channels
    -   Queues
    -   Assignment rules
    -   Presence states
    -   Rejection reasons
    As an analyst, do the following:

    -   Set your availability
    -   Accept or reject incoming security incidents
-   **[Prevent duplicate security incidents for IT incidents](https://www.servicenow.com/docs/access?context=si-creation&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Prevent the creation of duplicate security incidents when ITIL users escalate an IT incident to a security incident, the system by enabling the `sn_si.disable_duplicate_security_incident` system property.

-   **[Ingest third-party risk scores](https://www.servicenow.com/docs/access?context=define-risk-score-calculator-rules-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Factor third-party risk scores into security incident risk calculation by ingesting and mapping those scores for better prioritization of high-risk threats.

-   **[Simplified adding categories and sub-categories for security incidents](https://www.servicenow.com/docs/access?context=category-management-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Admin can create categories and subcategories in Security Incident Response Workspace based on threat types, compliance requirements, or reporting needs.

    Security analysts can assign these categories and subcategories to security incidents.

-   **[Security incident Details tab](https://www.servicenow.com/docs/access?context=security-incident-details-form&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Include the **Functional Impact**, **Recoverability** and **Information Impact** fields on the Details tab of a security incident to improve triage accuracy, incident handling efficiency, and executive reporting for calculating the risk score.


-   **[Close multiple security incidents](https://www.servicenow.com/docs/access?context=close-multiple-incidents-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Close security incidents in bulk with predefined closure comments or codes to reduce the time that would be spent on manually closing individual incidents. Closure candidates might include multiple incidents with common root causes such as alert misconfiguration, duplicates, or changes in system behavior.

-   **[Process Mining for security incidents](https://www.servicenow.com/docs/access?context=sir-process-mining&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Identify factors contributing to delays in processing SIR incidents that take a long time to close or resolve by scanning historical SIR records through Process Mining. Time-consuming factors can include multiple reassignments, prolonged hold times, and periods of inactivity. Use analysis methods to identify these factors such as multi-hop analysis or bottleneck analysis.

-   **[Send Observables to TISC](https://www.servicenow.com/docs/access?context=tisc-context-in-sir-workspace&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Add metadata to the observables such as confidence score, Traffic Light Protocol value, notes and TISC tags before sending them to TISC.

-   **[Add indirectly linked VITs to CVEs](https://www.servicenow.com/docs/access?context=configure-mitre-att-ck-properties&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    In MITRE-ATT&amp;CK framework, identify all third-party entities \(TPEs\) associated with common vulnerabilities and exposures \(CVEs\) and then calculate and display the total number of vulnerable items \(VITs\) indirectly linked to those CVEs through the TPEs by setting the **sn\_ti.include\_cve\_vit\_indirect\_relation** system property.

-   **[Configure on-call schedules](https://www.servicenow.com/docs/access?context=on-call-schedule-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    As an admin, manage on-call schedules through the following activities:

    -   Create a shift and assign or remove members to or from the shift.
    -   Create and edit on-call schedules for groups.
    -   View any group’s on-call schedule.
    As an analyst, track your on-call responsibilities through the following activities:

    -   Specify your availability and preferred contact methods.
    -   View your on-call schedule.
    -   See other members of your shift.
-   **[Users accessing the same incident](https://www.servicenow.com/docs/access?context=security-incident-overview&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    When you open an incident, the initials of all the users currently accessing the same incident are displayed to avoid conflicts.

-   **[Universal search field for linking observables](https://www.servicenow.com/docs/access?context=sir-records&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Search across all the field values of the associated observables for an incident.

-   **[CrowdStrike Next-Gen SIEM integration](https://www.servicenow.com/docs/access?context=crowdstrike-next-gen-integration-secops&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    As a Profile Admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM Detection and Events Fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so that you don't have to create duplicate security incidents.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **[Create and name an event profile for the Splunk Enterprise Security event ingestion integration](https://www.servicenow.com/docs/access?context=splunk-event-ingest-create-profile-security&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   Enables bidirectional updates and closure synchronization between Splunk ES and Splunk integrations.
    -   Enables retrieval of historical, and ongoing data including closed events, with an option to pull the closed events into the ServiceNow Splunk ES instance.
    -   Receive updates for the mapped fields in SIR.
-   **[Components installed with Security Incident Response](https://www.servicenow.com/docs/access?context=installed-with-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and to create, edit, delete, and manage profiles for the Splunk, Splunk ES, and Azure Sentinel Integration for Security Operations application.

-   **[Enhancements to relationship graphs](https://www.servicenow.com/docs/access?context=sir-relationship-graph&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    As an admin:

    -   Define default child nodes to populate in the relationship graph.
    -   Configure relationship labels.
    As an analyst:

    -   Add or remove child nodes at the parent node level.
    -   Save the state of the relationship graph.
    -   Retrieve updated data.

## UI changes

-   **[Shift Handover Records](https://www.servicenow.com/docs/access?context=manage-shift-handover-records&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The **Start date** and **End date** fields have been removed. You can now select the shift name instead when configuring the Shift Handover record.

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Security Incident Response Other Records](https://www.servicenow.com/docs/access?context=security-incident-response-other-records&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Add  multiple ITSM incidents, problems, or change requests to a security incident for which multiple IT actions are needed. For more information, see the "Link multiple ITSM incidents" section.

-   **[Modify attachments of a closed security incident](https://www.servicenow.com/docs/access?context=t_ClosingSecIncidents&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    You cannot modify the attachments of a security incident once the security incident is closed.


## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Vulnerability Response is part of the Security Operations application suite. Together, these applications connect security to your IT department, increase the speed and efficiency of your response, and give you a definitive view of your security posture.

-   **[Threat Intelligence](https://www.servicenow.com/docs/access?context=threat-intel-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The ServiceNow® Threat Intelligence application enables you to find indicators of compromise \(IoC\) and enrich security incidents with threat intelligence data.


**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

