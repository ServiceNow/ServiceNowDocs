---
title: Combined Security Incident Response release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Security Incident Response from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-securityincidentresponse-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Security Incident Response release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Security Incident Response from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Security Incident Response release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Security Incident Response to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Security Incident Response.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Configure the preview modal for attachment upload](https://www.servicenow.com/docs/access?context=configure-attachment-upload-preview-modal&family=australia&ft:locale=en-US)**

Configure whether the upload preview modal appears or not when security analysts attach files to a security incident record. Set the sn\_si\_aw.attachment.show\_preview\_modal system property to true to display the preview modal, or false \(default\) to upload files directly without displaying the modal.


 -   **[Microsoft Defender integration for Security Operations](https://www.servicenow.com/docs/access?context=ms-defender&family=australia&ft:locale=en-US)**

As a profile admin:

    -   Create flexible event‑forwarding profiles to ingest Microsoft Defender incidents into ServiceNow® Security Incident Response.
    -   Map Microsoft Defender incident, alert, and event fields directly to SIR security incident fields.
    -   Filter out noisy or low‑value alerts and bring only actionable notable events into SIR.
    -   Ingest historical, ongoing, new, and updated notable events on configurable intervals.
    -   Bi-directional synchronization of status, and work notes between Microsoft Defender and ServiceNow® SIR.
-   **[Preview security incident](https://www.servicenow.com/docs/access?context=splunk-event-ingest-preview-security&family=australia&ft:locale=en-US)**

The Profile Preview now displays Unmatched Affected Users and Unmatched Configuration Items in related lists when no CMDB or identity match is found, allowing you to quickly review and validate unmapped data directly within the profile without navigating to external records.

This enhancement is implemented across Splunk Enterprise Security, Splunk Enterprise Event Ingestion, and IBM QRadar integrations.

-   **[\[Placeholder link text to key bundle-security.security-incident-timeline\]](https://www.servicenow.com/docs/access?context=security-incident-timeline&family=australia&ft:locale=en-US)**

Track the complete history of a security incident events on a visual timeline within Security Incident Response Workspace. View event types as point or range events in chronological order such as state transitions, task creation and closure, approvals, observable additions, MITRE ATT&amp;CK and D3FEND mappings, and capability and playbook executions. Select any event to view details in a popover, filter by event type to focus on relevant activities. Administrators can configure custom event types, control how event data is retrieved, and define the fields displayed in event popovers.

-   **[Precedence-based override mode for threat lookup findings](https://www.servicenow.com/docs/access?context=threat-lookup-finding-calculators&family=australia&ft:locale=en-US)**

A new precedence override mode for observable findings lets security teams control how the automated threat lookups interact with an existing finding severity. When enabled, severity upgrades from threat intelligence sources are applied immediately, while downgrades are deferred until a configurable expiry window elapses. You can configure the override mode and finding priority order on the Threat Intelligence Properties page.

-   **[Create OT change requests from security incidents and response tasks](https://www.servicenow.com/docs/access?context=t_CrtChgOrPrbFromSI&family=australia&ft:locale=en-US)**

You can now create OT change requests directly from a security incident or a response task using the Create OT Change Request option in the form context menu.

**Note:** The Create OT Change Request option is available only when the Operational Technology Change Management plugin \(com.sn\_ot\_chg\_mgmt\) and the Operational Technology Security Incident Response plugin \(com.sn\_ot\_sir\) are installed and activated on your instance.

-   **[Dedicated role and enhanced security for the Setup Assistant](https://www.servicenow.com/docs/access?context=setup-assistant-reference&family=australia&ft:locale=en-US)**

The Setup Assistant now requires the dedicated sn\_secops\_setup.admin role for full access to setup configuration. Users with the sn\_si.admin role automatically inherit this role. The Setup Status \(sn\_secops\_setup\_status\) table fields are enforced as strict read-only to prevent unauthorized modifications.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


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

The new “Security Incident Unmatched Users” table captures unmatched affected user records for security incidents. This enables analysts to identify and address discrepancies when user records don't match existing system records.

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


</td></tr><tr><td>

Brazil

</td><td>

-   **[MITRE ATLAS framework](https://www.servicenow.com/docs/access?context=about-mitre-atlas&family=brazil&ft:locale=en-US)**

Detect, classify, and respond to AI- and ML-specific threats — such as prompt injection, model poisoning, data extraction, and adversarial attacks — using the MITRE ATLAS framework alongside MITRE-ATT&amp;CK. ATLAS techniques associated with a security incident appear in the MITRE node map, incident timeline, and MITRE info card with a distinct icon. This lets you tell MITRE-ATT&amp;CK and ATLAS techniques apart at a glance. Administrators can configure ATLAS-related properties on the Threat Intelligence Properties page.

-   **[Analyze security incident data](https://www.servicenow.com/docs/access?context=analyze-data-sir&family=brazil&ft:locale=en-US)**

Ask questions about your security incident data in a conversational language, without writing queries or knowing how reports are structured. Ask follow-up questions in the same session or move to a different question. AI-generated responses include insights and recommendations rather than only direct answers.

-   **[Review Security Incident AI ROI Summary dashboard](https://www.servicenow.com/docs/access?context=ai-roi-summary-dashboard&family=brazil&ft:locale=en-US)**

Track the value your team realizes from the AI features under Security Incident Response Management. The metrics include time saved per capability, total assists consumed, assists per resolved incident, and daily unique users, so you can see which capabilities are adopted.

-   **[Map incident fields](https://www.servicenow.com/docs/access?context=pan-cortex-xsiam-mapping&family=brazil&ft:locale=en-US)**

Build Cortex XSIAM field mappings from a known incident. Select the Incident ID ingestion method and enter an ID in the XSIAM Incident ID field to retrieve its actual field values.

-   **[Automate incident updates and closures](https://www.servicenow.com/docs/access?context=pan-xsiam-automate-inc-updates&family=brazil&ft:locale=en-US)**

Map Security Incident fields to Cortex XSIAM on the new **SIR to XSIAM Mapping** panel using drag-and-drop, override, and transformation scripts. When the check box is selected, any new or updated data from SIR Incident will automatically sync with the corresponding fields in the XSIAM portal.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Security Incident Response features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


 -   **[Assign groups in PIR user assignment rules](https://www.servicenow.com/docs/access?context=create-pir-assignment-rules&family=australia&ft:locale=en-US)**

User Assignment Rules for Post-Incident Review \(PIR\) assessments in the SIR module now support group-based assignment in addition to individual user selection. You can configure assignment rules using groups. The PIR automatically reflects group membership updates without requiring manual edits to the assignment rules configuration.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Explore Security incident quality assessment](https://www.servicenow.com/docs/access?context=na-sir-quality-assessment&family=brazil&ft:locale=en-US)**

Customize or regenerate entire draft reports or specific sections within it, before you share it with stakeholders.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Security Incident Response features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Security Incident Response features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Now LLM service deprecation**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Security Incident Response.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

    -   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&family=australia&ft:locale=en-US)**

The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


**Important:** Security Incident Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).

Install ServiceNow Otto for Security Incident Response \(SIR\) to use the AI features.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Security Incident Response we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Additional requirements**

The Security Support Common plugin is activated automatically when any of the plugins for the main Security Operations applications are activated. These applications include Security Incident Response, Vulnerability Response, Threat Intelligence, and Configuration Compliance.


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Security Incident Response we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Security Incident Response \(SIR\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   Enable automated response actions by integrating CrowdStrike Next-Gen SIEM with the ServiceNow Security Incident Response platform to retrieve detections and convert them into security incidents.
-   Fetch closed offenses from IBM QRadar into Security Incident Response.
-   Rapidly build integrations for Security Incident Response using auto-code generation through the Now Assist LLM-powered integration builder.
-   Ingest MITRE D3FEND data and visualize attack–defense relationships through an interactive graph directly within a security incident.
-   Starting in version 14.1.0, you can do the following:
    -   Integrate Microsoft Defender with ServiceNow® SIR to turn incidents into actionable incidents, thus accelerating response from detection to closure.
    -   Added support for fetching closed incidents from IBM QRadar into Security Incident Response.
    -   View a chronological timeline of activities for a security incident — including state transitions, task updates, approvals, and MITRE ATT&amp;CK mappings directly within Security Incident Response Workspace.

 See [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Connect security and IT teams to respond faster and more efficiently to security threats.
-   Gain insight into your organization's security posture.
-   Automatically create and enrich security incidents by integrating with third-party detection and SIEM sources such as CrowdStrike Next-Gen SIEM and Microsoft Defender.
-   Rapidly build new integrations using Now Assist LLM-powered auto-code generation.
-   Visualize attack-defense relationships using MITRE-ATT&amp;CK and MITRE D3FEND data directly within a security incident.

 See [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

