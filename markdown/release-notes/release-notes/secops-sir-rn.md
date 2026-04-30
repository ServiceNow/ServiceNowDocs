---
title: Security Incident Response release notes
description: The ServiceNow Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and efficiently to threats, and view your organization's security posture. Security Incident Response was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-06-25"
reading_time_minutes: 7
---

# Security Incident Response release notes

The ServiceNow® Security Incident Response \(SIR\) application helps your organization connect security and IT teams, respond faster and efficiently to threats, and view your organization's security posture. Security Incident Response was enhanced and updated in the Xanadu release.

## Security Incident Response highlights for the Xanadu release

-   Define and calculate the risk score of security incidents through the Risk Score Calculator, which is based on user-defined criteria. The risk score is auto-calculated for the security incident records.
-   Track the handover of important work items between shifts through the Shift Handover application.
-   Automatically create dedicated Slack channels for Incident Managers to engage with Incident Responders to manage major security incidents with the MSIM Slack integration.
-   Facilitate the ability of the Incident Manager to provide a summary of a major security incident to their Legal teams by using the MSIM Legal Request playbook. The Legal team can use that summary when filing an 8K or 10K form to comply with regulatory bodies such as the SEC when disclosing security breaches.
-   Share mobile-friendly MSIM Executive Status Reports generated in email format. You can also share the Executive Status Reports with users outside your ServiceNow® instance, including third-party vendors, other entities, or email distribution lists.

**Important:** Security Incident Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Security Incident Response integration with AWS Security Hub](https://www.servicenow.com/docs/access?context=aws-security-hub-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Security Incident Response supports the AWS Security Hub findings integration. This enables you to ingest AWS Security Hub findings and automatically create security incidents in Security Incident Response.

    Security Incident Response supports a bidirectional exchange of data with AWS Security Hub. SIR ingests findings from AWS Security Hub to create aggregated security incidents. Simultaneously, any change in a security incident is also updated on the related AWS Security Hub findings.

-   **[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](https://www.servicenow.com/docs/access?context=icap-dlp-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Internet Content Adaption Protocol \(ICAP\) integration helps you to track the usage and movement of sensitive data on various platforms.

    -   Configure and schedule DLP alerts ingestion from the specified Amazon S3 buckets which includes the capability to perform the delta imports to ensure only new or modified data is ingested.
    -   Display the ingested alerts in the DLP workspace by providing the key details on each alert such as the match content, alert severity, and relevant metadata.
    -   Download associated evidence files directly from the DLP workspace for further investigation or review.
    -   Enable users to apply automatic responses based on predefined criteria such as alert escalation, notifications, or enforcement policies.
    -   Remediate response actions such as blocking or quarantining sensitive data, or sending out alerts to stakeholders.
    -   Customize and define the severity mapping between ICAP DLP incidents with ServiceNow incidents.
-   **[Playbook for zero-day vulnerability](https://www.servicenow.com/docs/access?context=playbook-for-zero-day&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Get step-by-step procedure to address and mitigate zero-day threats—vulnerabilities in the software that are unknown to the vendor, leaving systems exposed to attacks.

-   **[Configure Shift Handover Templates](https://www.servicenow.com/docs/access?context=configure-shift-handover-templates&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Provide detailed communication of critical information, tasks, and updates between outgoing and incoming personnel for a seamless transition between shifts by using the Shift Handover feature. Improve operational continuity, reduce errors, and increase overall efficiency in the workplace.

-   **[Configure Slack chat connector for major security incidents](https://www.servicenow.com/docs/access?context=configure-slack-chat-connector-msi&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    View and filter collaboration chat activities on Slack to more efficiently collaborate to resolve major security incidents.

-   **[Playbook for Legal Request](https://www.servicenow.com/docs/access?context=playbook-legal-request&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Get step-by-step guidance on how you can inform the legal team about the latest summary of a major security incident so they can notify the SEC in the 4-day time frame that is required for material breaches.

-   **[Add Zscaler Internet Access URL category lists](https://www.servicenow.com/docs/access?context=create-zscaler-internet-access-url-category-manually&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Enable Zscaler approvers to add observables to the list of required approvals or remove them when the Require Approval option is selected.

-   **[Configure how an automatic event is created](https://www.servicenow.com/docs/access?context=configure-automatic-event-creation-profile&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) and [MISP event data](https://www.servicenow.com/docs/access?context=misp-event-data&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Add security tags during automatic MISP profile configuration.

-   **[Mapping DLP incident status with Netskope](https://www.servicenow.com/docs/access?context=map-incident-status&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Provide the mappings between the DLP Incident status in your ServiceNow instance and the Netskope Object status.

-   **[Define the new Risk Score Calculator Rules](https://www.servicenow.com/docs/access?context=define-risk-score-calculator-rules-sir&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The Risk score configuration in the Security Incident Response workspace has been enhanced with the following capabilities:

    -   Set up a Risk Score Calculator from either script or condition builders.
    -   Apply multiple conditions while setting up rule-based scoring.
    -   Apply weightage to each scoring line. Weights should add up to 100.
    -   For rule-based scoring, select table fields and values for setting up a condition.
    -   Capture conditions and scoring via scripts.
    -   Manually execute risk score calculators to recalculate after making changes.
-   **[Managing MSIM status reports](https://www.servicenow.com/docs/access?context=reports-and-metrics&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Share mobile-friendly Executive Status Reports with users outside your ServiceNow instance, including third-party vendors, other entities, or email distribution lists.


## UI changes

-   **[Configure how an automatic event is created](https://www.servicenow.com/docs/access?context=configure-automatic-event-creation-profile&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**
    -   A new **Security tags** field in automatic MISP profile configuration determines which observables with the security tags will not be attached to the automatic event created using the profile.
    -   Introduced local and global tags in Automatic MISP profile configuration to add the selected tags to the newly created automatic MISP event.

## Changed in this release

-   **[Security Incident Response Orchestration](https://www.servicenow.com/docs/access?context=c_SecIncRespOrchestration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

<table id="table_ffd_4lh_fdc"><thead><tr><th>

Integration Name

</th><th>

Integration Changes

</th></tr></thead><tbody><tr><td>

[Security Incident Response Orchestration flows and actions](https://www.servicenow.com/docs/access?context=sec-inc-resp-orchestration-workflows&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Create Lookup Request for IoC Changes Flow](https://www.servicenow.com/docs/access?context=t_CreateScanRequestforIoCChanges&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Incident Response- Get Network Statistics Flow](https://www.servicenow.com/docs/access?context=obtain-network-statistics-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Incident Response - Get Running Services Flow](https://www.servicenow.com/docs/access?context=get-running-services-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

<table id="table_jr2_h4h_fdc"><thead><tr><th>

Integration Name

</th><th>

Integration Changes

</th></tr></thead><tbody><tr><td>

[Security Operations Integration- Block Request capability](https://www.servicenow.com/docs/access?context=block-request-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer flows in the following integrations:-   [Run Block Request](https://www.servicenow.com/docs/access?context=run-block-request&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Operations Integration - Block Request Flow](https://www.servicenow.com/docs/access?context=secops-integration-block-request-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Get Network Statistics capability](https://www.servicenow.com/docs/access?context=get-network-statistics-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Execution Tracking - Begin \(CIs\) Flow Action](https://www.servicenow.com/docs/access?context=execution-tracking-begins-cis-activity&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Incident Response- Get Network Statistics Flow](https://www.servicenow.com/docs/access?context=obtain-network-statistics-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Get Running Processes capability](https://www.servicenow.com/docs/access?context=get-running-processes-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Security Operations - Get Running Processes Flow](https://www.servicenow.com/docs/access?context=secops-integration-get-running-processes-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Operations Carbon Black Integration - Get Running Processes Flow](https://www.servicenow.com/docs/access?context=secops-integration-cb-get-running-processes-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Isolate Host capability](https://www.servicenow.com/docs/access?context=isolate-host-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Security Operations - Isolate Host Flow](https://www.servicenow.com/docs/access?context=secops-integration-isolate-host-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Run Isolate Host](https://www.servicenow.com/docs/access?context=run-isolate-host&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Operations Carbon Black Integration - Isolate Host Flow](https://www.servicenow.com/docs/access?context=secops-integration-cb-isolate-host-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Publish to Watchlist capability](https://www.servicenow.com/docs/access?context=pubish-to-watchlist-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following section:-   [Security Operations Integration - Publish to Watchlist Flow](https://www.servicenow.com/docs/access?context=secops-integration-publish-watchlist-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Sightings Search capability](https://www.servicenow.com/docs/access?context=sightings-search-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following section:-   [Security Operations Integration - Sightings Search Flow](https://www.servicenow.com/docs/access?context=secops-integration-sightings-search-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Security Incident Response integrations](https://www.servicenow.com/docs/access?context=sir_integrations&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

<table id="table_wyv_zp3_fdc"><thead><tr><th>

Integration Name

</th><th>

Integration Changes

</th></tr></thead><tbody><tr><td>

[CrowdStrike Falcon Host integration](https://www.servicenow.com/docs/access?context=crowdstrike-falcon-host-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Get started with the CrowdStrike Falcon Host integration](https://www.servicenow.com/docs/access?context=activate-configure-crowdstrike-host&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Operations CrowdStrike Falcon Host - Publish to Watchlist Flow](https://www.servicenow.com/docs/access?context=secops-integration-crowdstrike-publish&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Review and assign your DLP incidents](https://www.servicenow.com/docs/access?context=using-dlp-ops-portal&version=xanadu&pubname=xanadu-security-management&section=review-and-assign-dlp-incidents&ft:locale=en-US)**

    Providing a closure code when closing a DLP incident from the DLP IR analyst workspace is now mandatory.

-   **[DLP Incident Response Administration](https://www.servicenow.com/docs/access?context=data-loss-prevention-administration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Adding users and groups is now accomplished through related lists rather than adding users from the respective configurations in the following Administration modules:

    -   DLP Default Configuration
    -   DLP Assignment Rules
    -   DLP Response Due Date Rules
    -   DLP Incident Assessment
    -   DLP User Instructions Templates
    -   DLP Record Level Restrictions
    -   DLP Field Level Restrictions
-   **[Install and configure the Netskope DLP integration for Data Loss Prevention](https://www.servicenow.com/docs/access?context=install-configure-netskope-dlp-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The Netskope integration now supports DLP incident ingestion.

-   **[Data Loss Prevention Incident Response Incident Management](https://www.servicenow.com/docs/access?context=data-loss-prevention-incident-management&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    View the forensic details of DLP Incidents in both the DLP IR Analyst workspace and DLP End user workspace.

-   **[Download evidence files](https://www.servicenow.com/docs/access?context=download-files-netskope&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The Netskope integration supports downloading the evidence file directly on demand.


## Activation information

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    When any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated, the Security Support Common plugin is activated.


## Related ServiceNow applications and features

-   **[Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Vulnerability Response is part of the Security Operations application suite. Together, these applications connect security to your IT department, increase the speed and efficiency of your response, and give you a definitive view of your security posture.

-   **[Threat Intelligence](https://www.servicenow.com/docs/access?context=threat-intel-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The ServiceNow® Threat Intelligence application enables you to find indicators of compromise \(IoC\) and enrich security incidents with threat intelligence data.


**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

