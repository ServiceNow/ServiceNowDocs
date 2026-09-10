---
title: Combined Security Incident Response release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Security Incident Response from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-securityincidentresponse-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 14
breadcrumb: [Products combined by family]
---

# Combined Security Incident Response release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Security Incident Response from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Security Incident Response release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Security Incident Response to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

-   **[CrowdStrike Next-Gen SIEM integration](https://www.servicenow.com/docs/access?context=crowdstrike-next-gen-integration-secops&family=yokohama&ft:locale=en-US)**

As a Profile Admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM Detection and Events Fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so that you don't have to create duplicate security incidents.
    -   Schedule ongoing detection ingestion.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **[Create an event profile](https://www.servicenow.com/docs/access?context=splunk-event-ingest-create-profile-security&family=yokohama&ft:locale=en-US)**
    -   Enables bidirectional updates and closure synchronization between Splunk ES and Splunk integrations.
    -   Enables retrieval of historical, and ongoing data including closed events, with an option to pull the closed events into the ServiceNow Splunk ES instance.
    -   Receive updates for the mapped fields in SIR.
-   **[Components installed with Security Incident Response](https://www.servicenow.com/docs/access?context=installed-with-sir&family=yokohama&ft:locale=en-US)**

A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and create, edit, delete, and manage profiles for the Splunk, Splunk ES, and Azure Sentinel Integration for Security Operations application.

-   **[Configure report templates in Security Incident Response](https://www.servicenow.com/docs/access?context=daily-status-sir&family=yokohama&ft:locale=en-US)**

As an admin, create report templates that can be used to generate an incident summary or an executive summary for analysis and sharing.

As an analyst, use the templates to generate analyst summary or executive summary reports for a SIR incident that can be shared over email.

-   **[Security Incident Response conference call integration](https://www.servicenow.com/docs/access?context=sir-conf-call-capability&family=yokohama&ft:locale=en-US)**

Initiate conference calls using communication channels such as Microsoft Teams, Cisco Webex, or Zoom with customers and peer agents to resolve security incidents over a call by using the SIR conference call feature.

-   **[Proofpoint integration for Security Operations](https://www.servicenow.com/docs/access?context=proofpoint-integration-secops-landing&family=yokohama&ft:locale=en-US)**

Proofpoint integration for Security Operations supports integration between SOAR \(Security Orchestration, Automation, and Response\) and Proofpoint Targeted Attack Protection \(TAP\) software. This integration provides the following benefits:

    -   Detect and block threats such as business email compromise and tags suspicious emails for tracking, analysis, and audit.
    -   Import data to automatically create security incidents for email events that are not captured by TAP products.
-   **[Data Loss Prevention Incident Response Analyst Workspace](https://www.servicenow.com/docs/access?context=using-dlp-ops-portal&family=yokohama&ft:locale=en-US)**

Preview the evidence file of the incident from either the Data Loss Prevention analyst workspace or the DLP end user workspace.


</td></tr><tr><td>

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

-   **[Configure the preview modal for attachment upload](https://www.servicenow.com/docs/access?context=configure-attachment-upload-preview-modal&family=australia&ft:locale=en-US)**

Configure whether the upload preview modal appears or not when security analysts attach files to a security incident record. Set the sn\_si\_aw.attachment.show\_preview\_modal system property to true to display the preview modal, or false \(default\) to upload files directly without displaying the modal.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Security Incident Response features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Start a Sidebar chat in Security Incident Response](https://www.servicenow.com/docs/access?context=initiate-chat-sidebar-sir&family=yokohama&ft:locale=en-US)**

The **Discuss** option has been renamed **Start Chat** and moved under the **Collaborate** option.


 -   **[Security Operations](https://www.servicenow.com/docs/access?context=security-operations-landing-page&family=yokohama&ft:locale=en-US)**

<table><thead><tr><th>

Integration name

</th><th>

Integration changes

</th></tr></thead><tbody><tr><td>

Microsoft Teams Chat

</td><td>

Simplified the setup of Microsoft Teams Chat integration with Major Security Incident Management Workspace. For more information, see [Integrate Major Security Incident Management with Microsoft SharePoint](https://www.servicenow.com/docs/access?context=integrate-msim-sharepoint&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Microsoft SharePoint

</td><td>

Simplified the setup of Microsoft SharePoint integration with Major Security Incident Management Workspace. For more information, see [Integrate Major Security Incident Management with Microsoft Teams](https://www.servicenow.com/docs/access?context=integrate-teams-msim&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Security Incident Response Integrations

</td><td>

Workflow was migrated to Workflow Studio. For more information, see the following:-   [Get Log Data Flow](https://www.servicenow.com/docs/access?context=get-threat-log-data&family=yokohama&ft:locale=en-US)
-   [Get WildFire Data Enrichment Flow](https://www.servicenow.com/docs/access?context=enrich-wildfire-data&family=yokohama&ft:locale=en-US)
-   [Configure](https://www.servicenow.com/docs/access?context=activate-configure-ms-exch-on-prem-integ&family=yokohama&ft:locale=en-US)
-   [Microsoft Exchange - Perform Email Search and Deletion flow](https://www.servicenow.com/docs/access?context=ms-exch-perform-email-search-deletion-wf&family=yokohama&ft:locale=en-US)
-   [Get AutoFocus Session Info Enrichment Flow](https://www.servicenow.com/docs/access?context=search-for-malicious-content&family=yokohama&ft:locale=en-US)


</td></tr><tr><td>

Security Incident Response Orchestration

</td><td>

Workflow was migrated to Workflow Studio in the section [Run procdump flow](https://www.servicenow.com/docs/access?context=invoke_procdump&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Security Operations common functionality

</td><td>

Workflow was migrated to Workflow Studio. For more information, see the following:-   [Integration capabilities](https://www.servicenow.com/docs/access?context=integration-capabilities&family=yokohama&ft:locale=en-US)
-   [Security Operations Integration- Block Request capability](https://www.servicenow.com/docs/access?context=block-request-capability&family=yokohama&ft:locale=en-US)
-   [Security Operations Integration- Email Search and Delete capability](https://www.servicenow.com/docs/access?context=email-search-capability&family=yokohama&ft:locale=en-US)
-   [Security Operations Integration- Enrich CI capability](https://www.servicenow.com/docs/access?context=enrich-ci-capability&family=yokohama&ft:locale=en-US)
-   [Security Operations Integration- Enrich Observable capability](https://www.servicenow.com/docs/access?context=enrich-observable-capability&family=yokohama&ft:locale=en-US)
-   [Security Operations Integration- Get Network Statistics capability](https://www.servicenow.com/docs/access?context=get-network-statistics-capability&family=yokohama&ft:locale=en-US)
-   [Security Operations Integration- Get Running Processes capability](https://www.servicenow.com/docs/access?context=get-running-processes-capability&family=yokohama&ft:locale=en-US)
-   [Security Operations Integration- Isolate Host capability](https://www.servicenow.com/docs/access?context=isolate-host-capability&family=yokohama&ft:locale=en-US)
-   [Security Operations Integration- Publish to Watchlist capability](https://www.servicenow.com/docs/access?context=pubish-to-watchlist-capability&family=yokohama&ft:locale=en-US)
-   [Security Operations Integration- Sightings Search capability](https://www.servicenow.com/docs/access?context=sightings-search-capability&family=yokohama&ft:locale=en-US)
-   [Security Operations Integration - Threat Lookup capability](https://www.servicenow.com/docs/access?context=sec-ops-threat-lookups-capability&family=yokohama&ft:locale=en-US)
-   [Change the order of flow execution](https://www.servicenow.com/docs/access?context=change-wf-execution-order&family=yokohama&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Other additional Security Incident Response setup tasks](https://www.servicenow.com/docs/access?context=t_ConfigureSIM&family=yokohama&ft:locale=en-US)**

View security incidents with read access and update security incidents with write access without any defined security role.


</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


 -   **[Security Incident Response Other Records](https://www.servicenow.com/docs/access?context=security-incident-response-other-records&family=zurich&ft:locale=en-US)**

Add  multiple ITSM incidents, problems, or change requests to a security incident for which multiple IT actions are needed. For more information, see the "Link multiple ITSM incidents" section.

-   **[Modify attachments of a closed security incident](https://www.servicenow.com/docs/access?context=t_ClosingSecIncidents&family=zurich&ft:locale=en-US)**

You cannot modify the attachments of a security incident once the security incident is closed.


</td></tr><tr><td>

Australia

</td><td>

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://www.servicenow.com/docs/access?context=sn-ai-implementation-landing&family=australia&ft:locale=en-US)**

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Security Incident Response features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

-   **Activation information**

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

    -   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&family=yokohama&ft:locale=en-US)**

The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

    -   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&family=zurich&ft:locale=en-US)**

The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

    -   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&family=australia&ft:locale=en-US)**

The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Security Incident Response we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

-   Identify inefficiencies and optimize the resolution process of security incidents for faster closure by using Process MIning.
-   Implemented CrowdStrike Next-Gen SIEM integration enabling real-time ingestion of correlated detections, and enrichment data.
-   Enhanced Splunk ES integrations to improve incident classification and enable efficient retrieval of historical data and alerts.
-   Include the number of VITs indirectly associated with a CVE through TPEs.
-   Help managers ensure there are no gaps in coverage and analysts are always available to address security incidents by configuring shifts for analysts.
-   Define default child nodes to populate in the relationship graph, and add or remove child nodes at the parent node level.

 See [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

