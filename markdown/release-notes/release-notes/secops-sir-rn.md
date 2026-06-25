---
title: Security Incident Response release notes
description: The ServiceNow Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and efficiently to threats, and gain insight into your organization's security posture. Security Incident Response was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
---

# Security Incident Response release notes

The ServiceNow® Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and efficiently to threats, and gain insight into your organization's security posture. Security Incident Response was enhanced and updated in the Australia release.

## Security Incident Response highlights for the Australia release

-   Enable automated response actions by integrating CrowdStrike Next-Gen SIEM with the ServiceNow Security Incident Response platform to retrieve detections and convert them into security incidents.
-   Fetch closed offenses from IBM QRadar into Security Incident Response.
-   Rapidly build integrations for Security Incident Response using auto-code generation through the Now Assist LLM-powered integration builder.
-   Ingest MITRE D3FEND data and visualize attack–defense relationships through an interactive graph directly within a security incident.
-   Starting in version 14.1.0, you can do the following:
    -   Integrate Microsoft Defender with ServiceNow® SIR to turn incidents into actionable incidents, thus accelerating response from detection to closure.
    -   Added support for fetching closed incidents from IBM QRadar into Security Incident Response.
    -   View a chronological timeline of activities for a security incident — including state transitions, task updates, approvals, and MITRE ATT&amp;CK mappings directly within Security Incident Response Workspace.

See [Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sir-landing-page.md) for more information.

**Important:** Security Incident Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Microsoft Defender integration for Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/ms-defender.md)**

    As a profile admin:

    -   Create flexible event‑forwarding profiles to ingest Microsoft Defender incidents into ServiceNow® Security Incident Response.
    -   Map Microsoft Defender incident, alert, and event fields directly to SIR security incident fields.
    -   Filter out noisy or low‑value alerts and bring only actionable notable events into SIR.
    -   Ingest historical, ongoing, new, and updated notable events on configurable intervals.
    -   Bi-directional synchronization of status, and work notes between Microsoft Defender and ServiceNow® SIR.
-   **[Preview security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/splunk-event-ingest-preview-security.md)**

    The Profile Preview now displays Unmatched Affected Users and Unmatched Configuration Items in related lists when no CMDB or identity match is found, allowing you to quickly review and validate unmapped data directly within the profile without navigating to external records.

    This enhancement is implemented across Splunk Enterprise Security, Splunk Enterprise Event Ingestion, and IBM QRadar integrations.

-   ****

    Track the complete history of a security incident events on a visual timeline within Security Incident Response Workspace. View event types as point or range events in chronological order such as state transitions, task creation and closure, approvals, observable additions, MITRE ATT&amp;CK and D3FEND mappings, and capability and playbook executions. Select any event to view details in a popover, filter by event type to focus on relevant activities. Administrators can configure custom event types, control how event data is retrieved, and define the fields displayed in event popovers.

-   **[Precedence-based override mode for threat lookup findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-lookup-finding-calculators.md)**

    A new precedence override mode for observable findings lets security teams control how the automated threat lookups interact with an existing finding severity. When enabled, severity upgrades from threat intelligence sources are applied immediately, while downgrades are deferred until a configurable expiry window elapses. You can configure the override mode and finding priority order on the Threat Intelligence Properties page.

-   **[Create OT change requests from security incidents and response tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/t_CrtChgOrPrbFromSI.md)**

    You can now create OT change requests directly from a security incident or a response task using the Create OT Change Request option in the form context menu.

    **Note:** The Create OT Change Request option is available only when the Operational Technology Change Management plugin \(com.sn\_ot\_chg\_mgmt\) and the Operational Technology Security Incident Response plugin \(com.sn\_ot\_sir\) are installed and activated on your instance.

-   **[Dedicated role and enhanced security for the Setup Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/setup-assistant-reference.md)**

    The Setup Assistant now requires the dedicated sn\_secops\_setup.admin role for full access to setup configuration. Users with the sn\_si.admin role automatically inherit this role. The Setup Status \(sn\_secops\_setup\_status\) table fields are enforced as strict read-only to prevent unauthorized modifications.


[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[CrowdStrike Next-Gen SIEM integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/crowdstrike-next-gen-integration-secops.md)**

    As a profile admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM detection and events fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so you don't have to create duplicate security incidents.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **[Components installed with Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/installed-with-sir.md)**

    A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and enables you to create, edit, delete, and manage profiles for Splunk ES, Splunk Enterprise Event Ingestion, and Microsoft Azure Sentinel integration for Security Operations application.

-   **[Add unmatched affected user for security incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/view-unmatched-affected-user-for-si.md)**

    The new “Security Incident Unmatched Users” table captures unmatched affected user records for security incidents, enabling analysts to identify and address discrepancies when user records don't match existing system records.

-   **[LLM-powered SIR integration builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sir-integration-builder-now-assist.md)**

    With the latest LLM-powered integrations on the ServiceNow AI Platform, you can create product-ready integration quickly. The LLM-powered integration builder has the following capabilities:

    -   Automatically generates integration code from a public API documentation
    -   Provides guided setup built on existing capabilities
    -   Provides easy edit and maintenance of the generated auto code
-   **[MITRE D3FEND framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/mitre-d3fend-framework.md)**

    Security administrators can now ingest MITRE D3FEND data. Security analysts can explore MITRE ATT&amp;CK and D3FEND techniques through an interactive, node-based visualization that maps attack techniques, defense techniques, and related artifacts within a Security Incident Response record.

-   **[Preserve manual security tags and restrict removal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/create-class-group-and-tags.md)**

    Manual security tags applied by analysts are preserved when automatic tagging rules execute on security incidents, avoiding inadvertent tag removal during automated processes. Analysts can no longer manually remove security tags once applied to an incident, ensuring tag consistency throughout the incident life cycle.

-   **[Assign parent relationships to similar security incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/show-related-items-for-si.md)**

    Select multiple similar security incidents from the Similar Security Incidents related list and link them as children to the current security incident using the **Link as children** button.

-   **[View and update Security Incident Response system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/view-update-sirw-system-properties.md)**

    View and update system properties specific to the Security Incident Response workspace directly from the workspace administration settings interface.

-   **[Create quick filters for Security Incidents and Response Tasks lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/create-quick-filters-for-security-incidents.md)**

    Enable rapid filtering of security incident lists based on predefined criteria by creating and managing quick filters for the Security incident \[sn.si.incident\] and Response tasks \[sn\_si\_task\] tables within the SIR Workspace. Filters are stored in the Quick Filters \[sn\_si\_aw\_quick\_filters\] table.

-   **[Configure auto refresh interval for security incident lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configure-auto-refresh-for-security-incident-lists.md)**

    Set up refreshing of the security incident list at specified intervals by using the `sn_si_incident.auto_refresh_interval` system property. The default refresh rate is five minutes.

-   **[Control external user access to security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/t_CreateResponseTask.md)**

    SOC users can grant read-only access to specific security incidents for defined external users through the **Access to security incident** field in the SIR workspace.

-   **[Configure default landing tab for security analysts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configure-default-landing-tab.md)**

    Customize the default landing tab for security analysts and security managers when they open a security incident.

-   **[Compose emails from Response Tasks and Investigation tabs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/t_CreateResponseTask.md)**

    Send emails without having to switch tabs by composing them directly from the Response Tasks and the Investigation tabs of a security incident.

-   **[Configure default view for contextual menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configure-default-view-for-contextual-menu.md)**

    Determine whether the contextual menu panel for a security incident is expanded or collapsed by default when a security analyst opens a security incident.


## Changed in this release

-   **[Assign groups in PIR user assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/create-pir-assignment-rules.md)**

    User Assignment Rules for Post-Incident Review \(PIR\) assessments in the SIR module now support group-based assignment in addition to individual user selection. You can configure assignment rules using groups. The PIR automatically reflects group membership updates without requiring manual edits to the assignment rules configuration.


## Activation information

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Security Operations common functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sec-ops-common-functionality.md)**

    The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


## Plugin information

-   **[Deprecated plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/components-installed-with-analyst-workspace.md)**

    The following plugin is deprecated in Australia:

    Security Incident Response UI \(sn\_app\_secops\_ui\): This plugin is replaced by Security Incident Response Workspace \(sn\_si\_aw\).


## Related ServiceNow applications and features

-   **[Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vuln-landing-page.md)**

    Vulnerability Response is part of the Security Operations application suite. Together, these applications connect security to your IT department, increase the speed and efficiency of your response, and provide a definitive view of your security posture.

-   **[Threat Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intel-landing-page.md)**

    The ServiceNow® Threat Intelligence application enables you to find indicators of compromise \(IoC\) and enrich security incidents with threat intelligence data.


**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/security-operations-rn-landing.md)

