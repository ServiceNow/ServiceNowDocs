---
title: Security Incident Response release notes
description: The ServiceNow Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and efficiently to threats, and gain insight into your organization's security posture. Security Incident Response was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Security Incident Response release notes

The ServiceNow® Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and efficiently to threats, and gain insight into your organization's security posture. Security Incident Response was enhanced and updated in the Australia release.

## Security Incident Response highlights for the Australia release

-   Enable automated response actions by integrating CrowdStrike Next-Gen SIEM with the ServiceNow Security Incident Response platform to retrieve detections and convert them into security incidents.
-   Fetch closed offenses from IBM QRadar into Security Incident Response.
-   Rapidly build integrations for Security Incident Response using auto-code generation through the Now Assist LLM-powered integration builder.
-   Ingest MITRE D3FEND data and visualize attack–defense relationships through an interactive graph directly within a security incident.

See Security Incident Response for more information.

**Important:** Security Incident Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

-   **ServiceNow product tiers**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **CrowdStrike Next-Gen SIEM integration**

    As a profile admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM detection and events fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so you don't have to create duplicate security incidents.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **Components installed with Security Incident Response**

    A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and enables you to create, edit, delete, and manage profiles for Splunk ES, Splunk Enterprise Event Ingestion, and Microsoft Azure Sentinel integration for Security Operations application.

-   **Add unmatched affected user for security incidents**

    The new “Security Incident Unmatched Users” table captures unmatched affected user records for security incidents, enabling analysts to identify and address discrepancies when user records don't match existing system records.

-   **LLM-powered SIR integration builder**

    With the latest LLM-powered integrations on the ServiceNow AI Platform, you can create product-ready integration quickly. The LLM-powered integration builder has the following capabilities:

    -   Automatically generates integration code from a public API documentation
    -   Provides guided setup built on existing capabilities
    -   Provides easy edit and maintenance of the generated auto code
-   **MITRE D3FEND framework**

    Security administrators can now ingest MITRE D3FEND data. Security analysts can explore MITRE ATT&amp;CK and D3FEND techniques through an interactive, node-based visualization that maps attack techniques, defense techniques, and related artifacts within a Security Incident Response record.

-   **Preserve manual security tags and restrict removal**

    Manual security tags applied by analysts are preserved when automatic tagging rules execute on security incidents, avoiding inadvertent tag removal during automated processes. Analysts can no longer manually remove security tags once applied to an incident, ensuring tag consistency throughout the incident life cycle.

-   **Assign parent relationships to similar security incidents**

    Select multiple similar security incidents from the Similar Security Incidents related list and link them as children to the current security incident using the **Link as children** button.

-   **View and update Security Incident Response system properties**

    View and update system properties specific to the Security Incident Response workspace directly from the workspace administration settings interface.

-   **Create quick filters for Security Incidents and Response Tasks lists**

    Enable rapid filtering of security incident lists based on predefined criteria by creating and managing quick filters for the Security incident \[sn.si.incident\] and Response tasks \[sn\_si\_task\] tables within the SIR Workspace. Filters are stored in the Quick Filters \[sn\_si\_aw\_quick\_filters\] table.

-   **Configure auto refresh interval for security incident lists**

    Set up refreshing of the security incident list at specified intervals by using the `sn_si_incident.auto_refresh_interval` system property. The default refresh rate is five minutes.

-   **Control external user access to security incident**

    SOC users can grant read-only access to specific security incidents for defined external users through the **Access to security incident** field in the SIR workspace.

-   **Configure default landing tab for security analysts**

    Customize the default landing tab for security analysts and security managers when they open a security incident.

-   **Compose emails from Response Tasks and Investigation tabs**

    Send emails without having to switch tabs by composing them directly from the Response Tasks and the Investigation tabs of a security incident.

-   **Configure default view for contextual menu**

    Determine whether the contextual menu panel for a security incident is expanded or collapsed by default when a security analyst opens a security incident.


## Changed in this release

-   **Assign groups in PIR user assignment rules**

    User Assignment Rules for Post-Incident Review \(PIR\) assessments in the SIR module now support group-based assignment in addition to individual user selection. You can configure assignment rules using groups. The PIR automatically reflects group membership updates without requiring manual edits to the assignment rules configuration.


## Activation information

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **Security Operations common functionality**

    The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


## Plugin information

-   **Deprecated plugin**

    The following plugin is deprecated in Australia:

    Security Incident Response UI \(sn\_app\_secops\_ui\): This plugin is replaced by Security Incident Response Workspace \(sn\_si\_aw\).


## Related ServiceNow applications and features

-   **Vulnerability Response**

    Vulnerability Response is part of the Security Operations application suite. Together, these applications connect security to your IT department, increase the speed and efficiency of your response, and provide a definitive view of your security posture.

-   **Threat Intelligence**

    The ServiceNow® Threat Intelligence application enables you to find indicators of compromise \(IoC\) and enrich security incidents with threat intelligence data.


**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

