---
title: Combined Security Incident Response release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Security Incident Response from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-securityincidentresponse-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 23
breadcrumb: [Products combined by family]
---

# Combined Security Incident Response release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Security Incident Response from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Security Incident Response release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Security Incident Response to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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
-   **[Create an event profile](https://www.servicenow.com/docs/access?context=splunk-event-ingest-create-profile-security&family=yokohama&ft:locale=en-US)**
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


</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

