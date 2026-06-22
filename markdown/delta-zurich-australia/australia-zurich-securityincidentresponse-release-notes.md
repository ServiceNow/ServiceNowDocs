---
title: Combined Security Incident Response release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Security Incident Response from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-securityincidentresponse-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Security Incident Response release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Security Incident Response from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Security Incident Response release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Security Incident Response to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Security Incident Response.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Security Incident Response Integration with Cortex XSIAM by Palo Alto Networks](https://www.servicenow.com/docs/access?context=cortex-xsiam-siem&family=zurich&ft:locale=en-US)**

As a profile admin:

    -   Create profiles for incident ingestion.
    -   Filter Cortex XSIAM incidents.
    -   Map Cortex XSIAM **Incident**, **Alert**, and **Event** fields to SIR security incident fields.
    -   Aggregate incidents to existing open security incidents to avoid having to create duplicate security incidents.
    -   Synchronize ServiceNow instance Work notes with Palo Alto Networks XSIAM comments.
-   **[Set up Splunk environment](https://www.servicenow.com/docs/access?context=splunk-es-addon&family=zurich&ft:locale=en-US)**

The ServiceNow Security Operations Event Ingestion Add-on for Splunk ES enables seamless integration between Splunk and ServiceNow Security Operations, allowing you to send security-related events from Splunk ES to a ServiceNow security incident.

-   **[LLM-powered SIR integration builder](https://www.servicenow.com/docs/access?context=sir-integration-builder-now-assist&family=zurich&ft:locale=en-US)**

With the ServiceNow platform's latest LLM powered integrations, you can create product-ready integration quickly. The LLM-powered integration builder has the following capabilities:

    -   Automatically generates integration code from a public API documentation.
    -   Provides guided setup built on existing capabilities.
    -   Provides easy edit and maintenance of the generated auto code.
-   **[Deny rule for phishing emails](https://www.servicenow.com/docs/access?context=urp-about&family=zurich&ft:locale=en-US)**

The security admin can add rules to prevent the conversion of phishing emails such as false positives or low-risk messages into security incidents. Any new phishing email is verified first with the deny rules to avoid unwanted security incidents.

-   **[MITRE D3FEND framework](https://www.servicenow.com/docs/access?context=mitre-d3fend-framework&family=zurich&ft:locale=en-US)**

Security administrators can now ingest MITRE D3FEND data. Security analysts can explore MITRE ATT&amp;CK and D3FEND techniques through an interactive, node-based visualization that maps attack techniques, defense techniques, and related artifacts within a Security Incident Response \(SIR\) record.

-   **[Update information in security incident related records](https://www.servicenow.com/docs/access?context=edit-related-records-in-list&family=zurich&ft:locale=en-US)**

The security analysts can now edit related records such as associated observables, for a security incident directly from the Related Records list view. Security analysts can quickly update the records without leaving their current context.

-   **[Advanced Work Assignment for SIR](https://www.servicenow.com/docs/access?context=awa-for-sir&family=zurich&ft:locale=en-US)**

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
-   **[Prevent duplicate security incidents for IT incidents](https://www.servicenow.com/docs/access?context=si-creation&family=zurich&ft:locale=en-US)**

Prevent the creation of duplicate security incidents when ITIL users escalate an IT incident to a security incident, the system by enabling the `sn_si.disable_duplicate_security_incident` system property.

-   **[Ingest third-party risk scores](https://www.servicenow.com/docs/access?context=define-risk-score-calculator-rules-sir&family=zurich&ft:locale=en-US)**

Factor third-party risk scores into security incident risk calculation by ingesting and mapping those scores for better prioritization of high-risk threats.

-   **[Simplified adding categories and sub-categories for security incidents](https://www.servicenow.com/docs/access?context=category-management-sir&family=zurich&ft:locale=en-US)**

Admin can create categories and subcategories in Security Incident Response Workspace based on threat types, compliance requirements, or reporting needs.

Security analysts can assign these categories and subcategories to security incidents.

-   **[Security incident Details tab](https://www.servicenow.com/docs/access?context=security-incident-details-form&family=zurich&ft:locale=en-US)**

Include the **Functional Impact**, **Recoverability** and **Information Impact** fields on the Details tab of a security incident to improve triage accuracy, incident handling efficiency, and executive reporting for calculating the risk score.


-   **[Close multiple security incidents](https://www.servicenow.com/docs/access?context=close-multiple-incidents-sir&family=zurich&ft:locale=en-US)**

Close security incidents in bulk with predefined closure comments or codes to reduce the time that would be spent on manually closing individual incidents. Closure candidates might include multiple incidents with common root causes such as alert misconfiguration, duplicates, or changes in system behavior.

-   **[Process Mining for security incidents](https://www.servicenow.com/docs/access?context=sir-process-mining&family=zurich&ft:locale=en-US)**

Identify factors contributing to delays in processing SIR incidents that take a long time to close or resolve by scanning historical SIR records through Process Mining. Time-consuming factors can include multiple reassignments, prolonged hold times, and periods of inactivity. Use analysis methods to identify these factors such as multi-hop analysis or bottleneck analysis.

-   **[Send Observables to TISC](https://www.servicenow.com/docs/access?context=tisc-context-in-sir-workspace&family=zurich&ft:locale=en-US)**

Add metadata to the observables such as confidence score, Traffic Light Protocol value, notes and TISC tags before sending them to TISC.

-   **[Add indirectly linked VITs to CVEs](https://www.servicenow.com/docs/access?context=configure-mitre-att-ck-properties&family=zurich&ft:locale=en-US)**

In MITRE-ATT&amp;CK framework, identify all third-party entities \(TPEs\) associated with common vulnerabilities and exposures \(CVEs\) and then calculate and display the total number of vulnerable items \(VITs\) indirectly linked to those CVEs through the TPEs by setting the **sn\_ti.include\_cve\_vit\_indirect\_relation** system property.

-   **[Configure on-call schedules](https://www.servicenow.com/docs/access?context=on-call-schedule-sir&family=zurich&ft:locale=en-US)**

As an admin, manage on-call schedules through the following activities:

    -   Create a shift and assign or remove members to or from the shift.
    -   Create and edit on-call schedules for groups.
    -   View any group’s on-call schedule.
As an analyst, track your on-call responsibilities through the following activities:

    -   Specify your availability and preferred contact methods.
    -   View your on-call schedule.
    -   See other members of your shift.
-   **[Users accessing the same incident](https://www.servicenow.com/docs/access?context=security-incident-overview&family=zurich&ft:locale=en-US)**

When you open an incident, the initials of all the users currently accessing the same incident are displayed to avoid conflicts.

-   **[Universal search field for linking observables](https://www.servicenow.com/docs/access?context=sir-records&family=zurich&ft:locale=en-US)**

Search across all the field values of the associated observables for an incident.

-   **[CrowdStrike Next-Gen SIEM integration](https://www.servicenow.com/docs/access?context=crowdstrike-next-gen-integration-secops&family=zurich&ft:locale=en-US)**

As a Profile Admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM Detection and Events Fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so that you don't have to create duplicate security incidents.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **[Create an event profile](https://www.servicenow.com/docs/access?context=splunk-event-ingest-create-profile-security&family=zurich&ft:locale=en-US)**
    -   Enables bidirectional updates and closure synchronization between Splunk ES and Splunk integrations.
    -   Enables retrieval of historical, and ongoing data including closed events, with an option to pull the closed events into the ServiceNow Splunk ES instance.
    -   Receive updates for the mapped fields in SIR.
-   **[Components installed with Security Incident Response](https://www.servicenow.com/docs/access?context=installed-with-sir&family=zurich&ft:locale=en-US)**

A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and to create, edit, delete, and manage profiles for the Splunk, Splunk ES, and Azure Sentinel Integration for Security Operations application.

-   **[Enhancements to relationship graphs](https://www.servicenow.com/docs/access?context=sir-relationship-graph&family=zurich&ft:locale=en-US)**

As an admin:

    -   Define default child nodes to populate in the relationship graph.
    -   Configure relationship labels.
As an analyst:

    -   Add or remove child nodes at the parent node level.
    -   Save the state of the relationship graph.
    -   Retrieve updated data.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[CrowdStrike Next-Gen SIEM integration](https://www.servicenow.com/docs/access?context=crowdstrike-next-gen-integration-secops&family=australia&ft:locale=en-US)**

As a profile admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM detection and events fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so you don't have to create duplicate security incidents.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **[Components installed with Security Incident Response](https://www.servicenow.com/docs/access?context=installed-with-sir&family=australia&ft:locale=en-US)**

A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and enables you to create, edit, delete, and manage profiles for Splunk ES, Splunk Enterprise Event Ingestion, and Microsoft Azure Sentinel integration for Security Operations application.

-   **[Add unmatched affected user for security incidents](https://www.servicenow.com/docs/access?context=view-unmatched-affected-user-for-si&family=australia&ft:locale=en-US)**

The new “Security Incident Unmatched Users” table captures unmatched affected user records for security incidents, enabling analysts to identify and address discrepancies when user records don't match existing system records.

-   **[LLM-powered SIR integration builder](https://www.servicenow.com/docs/access?context=sir-integration-builder-now-assist&family=australia&ft:locale=en-US)**

With the latest LLM-powered integrations on the ServiceNow AI Platform, you can create product-ready integration quickly. The LLM-powered integration builder has the following capabilities:

    -   Automatically generates integration code from a public API documentation
    -   Provides guided setup built on existing capabilities
    -   Provides easy edit and maintenance of the generated auto code
-   **[MITRE D3FEND framework](https://www.servicenow.com/docs/access?context=mitre-d3fend-framework&family=australia&ft:locale=en-US)**

Security administrators can now ingest MITRE D3FEND data. Security analysts can explore MITRE ATT&amp;CK and D3FEND techniques through an interactive, node-based visualization that maps attack techniques, defense techniques, and related artifacts within a Security Incident Response record.

-   **[Preserve manual security tags and restrict removal](https://www.servicenow.com/docs/access?context=create-class-group-and-tags&family=australia&ft:locale=en-US)**

Manual security tags applied by analysts are preserved when automatic tagging rules execute on security incidents, avoiding inadvertent tag removal during automated processes. Analysts can no longer manually remove security tags once applied to an incident, ensuring tag consistency throughout the incident life cycle.

-   **[Assign parent relationships to similar security incidents](https://www.servicenow.com/docs/access?context=show-related-items-for-si&family=australia&ft:locale=en-US)**

Select multiple similar security incidents from the Similar Security Incidents related list and link them as children to the current security incident using the **Link as children** button.

-   **[View and update Security Incident Response system properties](https://www.servicenow.com/docs/access?context=view-update-sirw-system-properties&family=australia&ft:locale=en-US)**

View and update system properties specific to the Security Incident Response workspace directly from the workspace administration settings interface.

-   **[Create quick filters for Security Incidents and Response Tasks lists](https://www.servicenow.com/docs/access?context=create-quick-filters-for-security-incidents&family=australia&ft:locale=en-US)**

Enable rapid filtering of security incident lists based on predefined criteria by creating and managing quick filters for the Security incident \[sn.si.incident\] and Response tasks \[sn\_si\_task\] tables within the SIR Workspace. Filters are stored in the Quick Filters \[sn\_si\_aw\_quick\_filters\] table.

-   **[Configure auto refresh interval for security incident lists](https://www.servicenow.com/docs/access?context=configure-auto-refresh-for-security-incident-lists&family=australia&ft:locale=en-US)**

Set up refreshing of the security incident list at specified intervals by using the `sn_si_incident.auto_refresh_interval` system property. The default refresh rate is five minutes.

-   **[Control external user access to security incident](https://www.servicenow.com/docs/access?context=t_CreateResponseTask&family=australia&ft:locale=en-US)**

SOC users can grant read-only access to specific security incidents for defined external users through the **Access to security incident** field in the SIR workspace.

-   **[Configure default landing tab for security analysts](https://www.servicenow.com/docs/access?context=configure-default-landing-tab&family=australia&ft:locale=en-US)**

Customize the default landing tab for security analysts and security managers when they open a security incident.

-   **[Compose emails from Response Tasks and Investigation tabs](https://www.servicenow.com/docs/access?context=t_CreateResponseTask&family=australia&ft:locale=en-US)**

Send emails without having to switch tabs by composing them directly from the Response Tasks and the Investigation tabs of a security incident.

-   **[Configure default view for contextual menu](https://www.servicenow.com/docs/access?context=configure-default-view-for-contextual-menu&family=australia&ft:locale=en-US)**

Determine whether the contextual menu panel for a security incident is expanded or collapsed by default when a security analyst opens a security incident.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Security Incident Response features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Security Incident Response Other Records](https://www.servicenow.com/docs/access?context=security-incident-response-other-records&family=zurich&ft:locale=en-US)**

Add  multiple ITSM incidents, problems, or change requests to a security incident for which multiple IT actions are needed. For more information, see the "Link multiple ITSM incidents" section.

-   **[Modify attachments of a closed security incident](https://www.servicenow.com/docs/access?context=t_ClosingSecIncidents&family=zurich&ft:locale=en-US)**

You cannot modify the attachments of a security incident once the security incident is closed.


</td></tr><tr><td>

Australia

</td><td>

-   **[Assign groups in PIR user assignment rules](https://www.servicenow.com/docs/access?context=create-pir-assignment-rules&family=australia&ft:locale=en-US)**

User Assignment Rules for Post-Incident Review \(PIR\) assessments in the SIR module now support group-based assignment in addition to individual user selection. You can configure assignment rules using groups. The PIR automatically reflects group membership updates without requiring manual edits to the assignment rules configuration.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Security Incident Response features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Security Incident Response features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Security Incident Response.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

Install Security Incident Response by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Security Incident Response we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Security Incident Response we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Security Incident Response, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Security Incident Response we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Security Incident Response we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

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

 See [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Enable automated response actions by integrating CrowdStrike Next-Gen SIEM with the ServiceNow Security Incident Response platform to retrieve detections and convert them into security incidents.
-   Fetch closed offenses from IBM QRadar into Security Incident Response.
-   Rapidly build integrations for Security Incident Response using auto-code generation through the Now Assist LLM-powered integration builder.
-   Ingest MITRE D3FEND data and visualize attack–defense relationships through an interactive graph directly within a security incident.
-   Starting in version 14.1.0, you can do the following:
    -   Integrate Microsoft Defender with ServiceNow® SIR to turn incidents into actionable incidents, thus accelerating response from detection to closure.
    -   Added support for fetching closed incidents from IBM QRadar into Security Incident Response.
    -   View a chronological timeline of activities for a security incident — including state transitions, task updates, approvals, and MITRE ATT&amp;CK mappings directly within Security Incident Response Workspace.

 See [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

