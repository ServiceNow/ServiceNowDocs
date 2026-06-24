---
title: Combined Security Incident Response release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Security Incident Response from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-securityincidentresponse-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-24"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Security Incident Response release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Security Incident Response from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Security Incident Response release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Security Incident Response to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Security Incident Response.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Security Incident Response integration with AWS Security Hub](https://www.servicenow.com/docs/access?context=aws-security-hub-integration&family=xanadu&ft:locale=en-US)**

Security Incident Response supports the AWS Security Hub findings integration. This enables you to ingest AWS Security Hub findings and automatically create security incidents in Security Incident Response.

Security Incident Response supports a bidirectional exchange of data with AWS Security Hub. SIR ingests findings from AWS Security Hub to create aggregated security incidents. Simultaneously, any change in a security incident is also updated on the related AWS Security Hub findings.

-   **[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](https://www.servicenow.com/docs/access?context=icap-dlp-integration&family=xanadu&ft:locale=en-US)**

Internet Content Adaption Protocol \(ICAP\) integration helps you to track the usage and movement of sensitive data on various platforms.

    -   Configure and schedule DLP alerts ingestion from the specified Amazon S3 buckets which includes the capability to perform the delta imports to ensure only new or modified data is ingested.
    -   Display the ingested alerts in the DLP workspace by providing the key details on each alert such as the match content, alert severity, and relevant metadata.
    -   Download associated evidence files directly from the DLP workspace for further investigation or review.
    -   Enable users to apply automatic responses based on predefined criteria such as alert escalation, notifications, or enforcement policies.
    -   Remediate response actions such as blocking or quarantining sensitive data, or sending out alerts to stakeholders.
    -   Customize and define the severity mapping between ICAP DLP incidents with ServiceNow incidents.
-   **[Playbook for zero-day vulnerability](https://www.servicenow.com/docs/access?context=playbook-for-zero-day&family=xanadu&ft:locale=en-US)**

Get step-by-step procedure to address and mitigate zero-day threats—vulnerabilities in the software that are unknown to the vendor, leaving systems exposed to attacks.

-   **[Configure Shift Handover Templates](https://www.servicenow.com/docs/access?context=configure-shift-handover-templates&family=xanadu&ft:locale=en-US)**

Provide detailed communication of critical information, tasks, and updates between outgoing and incoming personnel for a seamless transition between shifts by using the Shift Handover feature. Improve operational continuity, reduce errors, and increase overall efficiency in the workplace.

-   **[Configure Slack chat connector for major security incidents](https://www.servicenow.com/docs/access?context=configure-slack-chat-connector-msi&family=xanadu&ft:locale=en-US)**

View and filter collaboration chat activities on Slack to more efficiently collaborate to resolve major security incidents.

-   **[Playbook for Legal Request](https://www.servicenow.com/docs/access?context=playbook-legal-request&family=xanadu&ft:locale=en-US)**

Get step-by-step guidance on how you can inform the legal team about the latest summary of a major security incident so they can notify the SEC in the 4-day time frame that is required for material breaches.

-   **[Add Zscaler Internet Access URL category lists](https://www.servicenow.com/docs/access?context=create-zscaler-internet-access-url-category-manually&family=xanadu&ft:locale=en-US)**

Enable Zscaler approvers to add observables to the list of required approvals or remove them when the Require Approval option is selected.

-   **[Configure how an automatic event is created](https://www.servicenow.com/docs/access?context=configure-automatic-event-creation-profile&family=xanadu&ft:locale=en-US) and [MISP event data](https://www.servicenow.com/docs/access?context=misp-event-data&family=xanadu&ft:locale=en-US)**

Add security tags during automatic MISP profile configuration.

-   **[Mapping DLP incident status with Netskope](https://www.servicenow.com/docs/access?context=map-incident-status&family=xanadu&ft:locale=en-US)**

Provide the mappings between the DLP Incident status in your ServiceNow instance and the Netskope Object status.

-   **[Define the new Risk Score Calculator Rules](https://www.servicenow.com/docs/access?context=define-risk-score-calculator-rules-sir&family=xanadu&ft:locale=en-US)**

The Risk score configuration in the Security Incident Response workspace has been enhanced with the following capabilities:

    -   Set up a Risk Score Calculator from either script or condition builders.
    -   Apply multiple conditions while setting up rule-based scoring.
    -   Apply weightage to each scoring line. Weights should add up to 100.
    -   For rule-based scoring, select table fields and values for setting up a condition.
    -   Capture conditions and scoring via scripts.
    -   Manually execute risk score calculators to recalculate after making changes.
-   **[Managing MSIM status reports](https://www.servicenow.com/docs/access?context=reports-and-metrics&family=xanadu&ft:locale=en-US)**

Share mobile-friendly Executive Status Reports with users outside your ServiceNow instance, including third-party vendors, other entities, or email distribution lists.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Process Mining for security incidents](https://www.servicenow.com/docs/access?context=sir-process-mining&family=yokohama&ft:locale=en-US)**

Identify factors contributing to delays in processing Security Incident Response \(SIR\) incidents that take a long time to close or resolve by scanning historical SIR records through Process Mining. Time-consuming factors can include multiple reassignments, prolonged hold times, and periods of inactivity.

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
-   **[Use](https://www.servicenow.com/docs/access?context=splunk-event-ingest-create-profile-security&family=yokohama&ft:locale=en-US)**
    -   Enables bidirectional updates and closure synchronization between Splunk ES and Splunk integrations.
    -   Enables retrieval of historical, and ongoing data including closed events, with an option to pull the closed events into the ServiceNow Splunk ES instance.
    -   Receive updates for the mapped fields in SIR.
-   **[Components installed with Security Incident Response](https://www.servicenow.com/docs/access?context=installed-with-sir&family=yokohama&ft:locale=en-US)**

A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and create, edit, delete, and manage profiles for the Splunk, Splunk ES, and Azure Sentinel Integration for Security Operations application.

-   **[Add indirectly linked VITs to CVEs](https://www.servicenow.com/docs/access?context=configure-mitre-att-ck-properties&family=yokohama&ft:locale=en-US)**

Identify all the Third-Party Entities \(TPEs\) associated with a Common Vulnerabilities and Exposures \(CVE\) and then calculate and display the total number of vulnerable items \(VITs\) indirectly linked to those CVEs through the TPEs by setting the sn\_ti.include\_cve\_vit\_indirect\_relation property.

-   **[Configure on-call schedules](https://www.servicenow.com/docs/access?context=on-call-schedule-sir&family=yokohama&ft:locale=en-US)**

As an admin:

    -   Create a shift and assign or remove members to/from the shift.
    -   Create/edit on-call schedules for groups.
    -   View any group’s on-call schedule, including those to which they belong.
As an analyst:

    -   Specify your availability and preferred contact methods.
    -   View your on-call schedule and see other members of your shift.
-   **[Configure report templates in Security Incident Response](https://www.servicenow.com/docs/access?context=daily-status-sir&family=yokohama&ft:locale=en-US)**

As an admin, create report templates that can be used to generate an incident summary or an executive summary for analysis and sharing.

As an analyst, use the templates to generate analyst summary or executive summary reports for a SIR incident that can be shared over email.

-   **[Security Incident Response conference call integration](https://www.servicenow.com/docs/access?context=sir-conf-call-capability&family=yokohama&ft:locale=en-US)**

Initiate conference calls using communication channels such as Microsoft Teams, Cisco Webex, or Zoom with customers and peer agents to resolve security incidents over a call by using the SIR conference call feature.

-   **[Enhancements to relationship graphs](https://www.servicenow.com/docs/access?context=sir-relationship-graph&family=yokohama&ft:locale=en-US)**

As an admin:

    -   Define default child nodes to populate in the relationship graph.
    -   Configure relationship labels.
As an analyst:

    -   Add or remove child nodes at the parent node level.
    -   Save the state of the relationship graph.
    -   Retrieve updated data.
-   **[Proofpoint integration for Security Operations](https://www.servicenow.com/docs/access?context=proofpoint-integration-secops-landing&family=yokohama&ft:locale=en-US)**

Proofpoint integration for Security Operations supports integration between SOAR \(Security Orchestration, Automation, and Response\) and Proofpoint Targeted Attack Protection \(TAP\) software. This integration provides the following benefits:

    -   Detect and block threats such as business email compromise and tags suspicious emails for tracking, analysis, and audit.
    -   Import data to automatically create security incidents for email events that are not captured by TAP products.
-   **[Data Loss Prevention Incident Response Analyst Workspace](https://www.servicenow.com/docs/access?context=using-dlp-ops-portal&family=yokohama&ft:locale=en-US)**

Preview the evidence file of the incident from either the Data Loss Prevention analyst workspace or the DLP end user workspace.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Security Incident Response features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Security Incident Response Orchestration](https://www.servicenow.com/docs/access?context=c_SecIncRespOrchestration&family=xanadu&ft:locale=en-US)**

<table><thead><tr><th>

Integration Name

</th><th>

Integration Changes

</th></tr></thead><tbody><tr><td>

[Security Incident Response Orchestration flows and actions](https://www.servicenow.com/docs/access?context=sec-inc-resp-orchestration-workflows&family=xanadu&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Create Lookup Request for IoC Changes Flow](https://www.servicenow.com/docs/access?context=t_CreateScanRequestforIoCChanges&family=xanadu&ft:locale=en-US)
-   [Security Incident Response- Get Network Statistics Flow](https://www.servicenow.com/docs/access?context=obtain-network-statistics-workflow&family=xanadu&ft:locale=en-US)
-   [Security Incident Response - Get Running Services Flow](https://www.servicenow.com/docs/access?context=get-running-services-workflow&family=xanadu&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&family=xanadu&ft:locale=en-US)**

<table><thead><tr><th>

Integration Name

</th><th>

Integration Changes

</th></tr></thead><tbody><tr><td>

[Security Operations Integration- Block Request capability](https://www.servicenow.com/docs/access?context=block-request-capability&family=xanadu&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer flows in the following integrations:-   [Run Block Request](https://www.servicenow.com/docs/access?context=run-block-request&family=xanadu&ft:locale=en-US)
-   [Security Operations Integration - Block Request Flow](https://www.servicenow.com/docs/access?context=secops-integration-block-request-workflow&family=xanadu&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Get Network Statistics capability](https://www.servicenow.com/docs/access?context=get-network-statistics-capability&family=xanadu&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Execution Tracking - Begin \(CIs\) Flow Action](https://www.servicenow.com/docs/access?context=execution-tracking-begins-cis-activity&family=xanadu&ft:locale=en-US)
-   [Security Incident Response- Get Network Statistics Flow](https://www.servicenow.com/docs/access?context=obtain-network-statistics-workflow&family=xanadu&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Get Running Processes capability](https://www.servicenow.com/docs/access?context=get-running-processes-capability&family=xanadu&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Security Operations - Get Running Processes Flow](https://www.servicenow.com/docs/access?context=secops-integration-get-running-processes-workflow&family=xanadu&ft:locale=en-US)
-   [Security Operations Carbon Black Integration - Get Running Processes Flow](https://www.servicenow.com/docs/access?context=secops-integration-cb-get-running-processes-workflow&family=xanadu&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Isolate Host capability](https://www.servicenow.com/docs/access?context=isolate-host-capability&family=xanadu&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Security Operations - Isolate Host Flow](https://www.servicenow.com/docs/access?context=secops-integration-isolate-host-workflow&family=xanadu&ft:locale=en-US)
-   [Run Isolate Host](https://www.servicenow.com/docs/access?context=run-isolate-host&family=xanadu&ft:locale=en-US)
-   [Security Operations Carbon Black Integration - Isolate Host Flow](https://www.servicenow.com/docs/access?context=secops-integration-cb-isolate-host-workflow&family=xanadu&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Publish to Watchlist capability](https://www.servicenow.com/docs/access?context=pubish-to-watchlist-capability&family=xanadu&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following section:-   [Security Operations Integration - Publish to Watchlist Flow](https://www.servicenow.com/docs/access?context=secops-integration-publish-watchlist-workflow&family=xanadu&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Sightings Search capability](https://www.servicenow.com/docs/access?context=sightings-search-capability&family=xanadu&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following section:-   [Security Operations Integration - Sightings Search Flow](https://www.servicenow.com/docs/access?context=secops-integration-sightings-search-workflow&family=xanadu&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Security Incident Response integrations](https://www.servicenow.com/docs/access?context=sir_integrations&family=xanadu&ft:locale=en-US)**

<table><thead><tr><th>

Integration Name

</th><th>

Integration Changes

</th></tr></thead><tbody><tr><td>

[CrowdStrike Falcon Host integration](https://www.servicenow.com/docs/access?context=crowdstrike-falcon-host-landing-page&family=xanadu&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Get started with the CrowdStrike Falcon Host integration](https://www.servicenow.com/docs/access?context=activate-configure-crowdstrike-host&family=xanadu&ft:locale=en-US)
-   [Security Operations CrowdStrike Falcon Host - Publish to Watchlist Flow](https://www.servicenow.com/docs/access?context=secops-integration-crowdstrike-publish&family=xanadu&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Review and assign your DLP incidents](https://www.servicenow.com/docs/access?context=review-and-assign-dlp-incidents&family=xanadu&ft:locale=en-US)**

Providing a closure code when closing a DLP incident from the DLP IR analyst workspace is now mandatory.

-   **[Administer](https://www.servicenow.com/docs/access?context=data-loss-prevention-administration&family=xanadu&ft:locale=en-US)**

Adding users and groups is now accomplished through related lists rather than adding users from the respective configurations in the following Administration modules:

    -   DLP Default Configuration
    -   DLP Assignment Rules
    -   DLP Response Due Date Rules
    -   DLP Incident Assessment
    -   DLP User Instructions Templates
    -   DLP Record Level Restrictions
    -   DLP Field Level Restrictions
-   **[Install and configure the Netskope DLP integration for Data Loss Prevention](https://www.servicenow.com/docs/access?context=install-configure-netskope-dlp-integration&family=xanadu&ft:locale=en-US)**

The Netskope integration now supports DLP incident ingestion.

-   **[Manage incidents](https://www.servicenow.com/docs/access?context=data-loss-prevention-incident-management&family=xanadu&ft:locale=en-US)**

View the forensic details of DLP Incidents in both the DLP IR Analyst workspace and DLP End user workspace.

-   **[Download evidence files](https://www.servicenow.com/docs/access?context=download-files-netskope&family=xanadu&ft:locale=en-US)**

The Netskope integration supports downloading the evidence file directly on demand.


</td></tr><tr><td>

Yokohama

</td><td>

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


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Security Incident Response features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Security Incident Response features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Security Incident Response we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

-   Define and calculate the risk score of security incidents through the Risk Score Calculator, which is based on user-defined criteria. The risk score is auto-calculated for the security incident records.
-   Track the handover of important work items between shifts through the Shift Handover application.
-   Automatically create dedicated Slack channels for Incident Managers to engage with Incident Responders to manage major security incidents with the MSIM Slack integration.
-   Facilitate the ability of the Incident Manager to provide a summary of a major security incident to their Legal teams by using the MSIM Legal Request playbook. The Legal team can use that summary when filing an 8K or 10K form to comply with regulatory bodies such as the SEC when disclosing security breaches.
-   Share mobile-friendly MSIM Executive Status Reports generated in email format. You can also share the Executive Status Reports with users outside your ServiceNow® instance, including third-party vendors, other entities, or email distribution lists.

</td></tr><tr><td>

Yokohama

</td><td>

-   Identify inefficiencies and optimize the resolution process of security incidents for faster closure by using Process MIning.
-   Implemented CrowdStrike Next-Gen SIEM integration enabling real-time ingestion of correlated detections, and enrichment data.
-   Enhanced Splunk ES integrations to improve incident classification and enable efficient retrieval of historical data and alerts.
-   Include the number of VITs indirectly associated with a CVE through TPEs.
-   Help managers ensure there are no gaps in coverage and analysts are always available to address security incidents by configuring shifts for analysts.
-   Define default child nodes to populate in the relationship graph, and add or remove child nodes at the parent node level.

 See [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

