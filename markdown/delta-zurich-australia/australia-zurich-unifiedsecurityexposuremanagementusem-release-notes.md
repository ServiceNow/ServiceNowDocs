---
title: Combined Unified Security Exposure Management \(USEM\) release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Unified Security Exposure Management \(USEM\) from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-unifiedsecurityexposuremanagementusem-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 17
breadcrumb: [Products combined by family]
---

# Combined Unified Security Exposure Management \(USEM\) release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Unified Security Exposure Management \(USEM\) from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Unified Security Exposure Management \(USEM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Unified Security Exposure Management \(USEM\) to Australia

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

Starting with Australia Patch 5, Now Assist for Vulnerability Response is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

 ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including the Now Assist for Vulnerability Response product name, which will be replaced with ServiceNow Otto for Unified Security Exposure Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 To access the new AI native experience in the Unified Security Exposure Management \(USEM\) workspace, you must upgrade to the Australia release.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 Unified Security Exposure Management is available to all customers who are entitled to Vulnerability Response. Migrating to USEM is a major upgrade that introduces a unified architecture for improved performance, scalability, and streamlined workflows. Before upgrading, leverage the Migration assistant for Unified Security Exposure Management that is available as an update set. See the [Migration Guidance to Unified Security Exposure Management \[KB2556844\]](https://support.servicenow.com/kb?sys_kb_id=8652717893a8ba94f538fb2d6cba1078&id=kb_article_view) Knowledge Base article for more information. This tool provides a guided experience for plugin installation, data mapping, rule migration, and post-migration validation, reducing risk and manual effort. Ensure that all integrations and workflows are reviewed for compatibility before initiating migration. For more information, see [Migrating to USEM](https://www.servicenow.com/docs/access?context=migrating-to-usem&family=australia&ft:locale=en-US) and [Migrate to USEM](https://www.servicenow.com/docs/access?context=migrate-to-usem&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Unified Security Exposure Management \(USEM\).

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

-   **[Enhancements to ServiceNow Otto for Unified Security Exposure Management](https://www.servicenow.com/docs/access?context=now-assist-review-vulnerability-exposure-data&family=australia&ft:locale=en-US)**

USEM was enhanced and updated in the Australia release to support the new AI native experience.

    -   Links to Records: Select the counts and findings in the Security Exposure 360 output to link you directly to the underlying vulnerable item \(VITs\) and records in your instance.
    -   Suggested follow-up questions: Follow-up questions are provided that help you drill down.
-   **[Fix Intelligence for Security Exposure Management](https://www.servicenow.com/docs/access?context=fix-intel-for-usem-landing&family=australia&ft:locale=en-US)**

Fix Intelligence for Security Exposure Management is a new application that enriches your host findings with normalized fix information from Armis Centrix™ for Vulnerability Prioritization and Remediation \(ViPR\). Detections are de-duplicated into Fix records that are linked to the findings and assets each fix resolves, with a rolled-up risk score per fix. Your team can remediate by fix instead of one finding at a time.

Prioritize fixes from the **Fix Intelligence** tab, the **Findings View**, and the **Remediation View**, and group the findings that share a fix into a single remediation task. In this release, fixes are identified for host vulnerabilities from Qualys, Rapid7, Tenable.io, Wiz, and Microsoft Defender Vulnerability Management.

-   **[Enhancements to the Vulnerability Response Integration with Wiz Test Results Integration](https://www.servicenow.com/docs/access?context=wiz-test-result-tab-filters&family=australia&ft:locale=en-US)**

Enhancements to the Wiz integration that imports cloud configuration findings as Test Results in Configuration Compliance. Configuration issues related to AI assets, such as AI models and agents are routed into AI security exposure management tables \(AI posture findings\).

This enhancement helps with better visibility within AI Control Tower and for any AI-specific remediation workflows to be added in the future. The 'Send AI security findings to AI security exposure management' configuration setting has been added to the Wiz Test Results integration configuration page so that AI security findings are routed into AI security exposure management.

-   **[View impacted findings in exception rule approvals](https://www.servicenow.com/docs/access?context=sem-exception-rules-overview&family=australia&ft:locale=en-US)**

Use the **Impacted findings** metric in the approval form's Overview tab to assess the scope and impact of an exception rule before approval. The metric displays the number of existing findings that match the rule's conditions. The impacted findings count is also included in exception rule approval emails, allowing you to make informed approval decisions without leaving your inbox.

-   **[Streamline Microsoft SCCM data ingestion with JDBC](https://www.servicenow.com/docs/access?context=mspatch-integration&family=australia&ft:locale=en-US)**

Connect to Microsoft SCCM using JDBC \(Java Database Connectivity\) to query the SCCM database directly for collection, device, patch update, and deployment status data. Opening a firewall port for WMI \(Windows Management Instrumentation\) RPCs \(remote procedure calls\) is no longer required for these queries. A WMI connection remains required to deploy patches, because patch deployment continues to use the Microsoft SCCM API over WMI.

-   **[Enhancements to the Invicti Vulnerability Integration](https://www.servicenow.com/docs/access?context=invicti-vuln-integration&family=australia&ft:locale=en-US)**

Added the Invicti Platform Integration. Support for the Invicti Platform APIs introduces three new integration jobs that connect directly to the Invicti Platform cloud service:

    -   Application Integration — Imports the list of applications being scanned in Invicti Platform into your ServiceNow AI Platform® instance as discovered applications.
    -   Scan Integration — Pulls scan records from Invicti Platform, providing scan metadata to correlate with vulnerability findings.
    -   Vulnerability Integration — Imports application vulnerability findings from Invicti Platform and creates or updates application vulnerable items in Vulnerability Response in your ServiceNow AI Platform®.
Enhancements to Application life-cycle management: When an application is deleted or decommissioned in Invicti Platform, your ServiceNow AI Platform® automatically deactivates the corresponding discovered application and closes all associated application vulnerable items \(AVITs\), keeping your vulnerability inventory accurate without manual cleanup.

-   **[Enhancements to AI Security Exposure Management](https://www.servicenow.com/docs/access?context=exploring-ai-security-exposure&family=australia&ft:locale=en-US)**

Remediation tasks are supported for the following AI Security Exposure Management findings:

    -   AI Vulnerability Finding \(AIVUL\)
    -   AI Validation Finding \(AIVF\)
    -   AI Posture Finding \(AIPF\)
You can view these findings along with other Unified Security Exposure Management \(USEM\) findings and remediation tasks in the List module in the Security Exposure Management workspace organized by finding type.

-   **[Enhancements to Exception Management for Unified Security Exposure Management](https://www.servicenow.com/docs/access?context=sem-configure-exp-mngmt-vr&family=australia&ft:locale=en-US)**
    -   Added bulk edit support for Risk modification requests that permit you to evaluate and process multiple vulnerable items at once.
    -   Added Smart Assessment support to the Risk Reduction option in Request Exception workflows.
-   **[Evaluate vulnerability exposure with AI-powered analysis](https://www.servicenow.com/docs/access?context=now-assist-review-vulnerability-exposure-data&family=australia&ft:locale=en-US)**

The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to Unified Security Exposure Management \(USEM\). Users can now ask questions in plain language and get answers grounded in their own ServiceNow data — across all types of findings within USEM.

-   **[AI Security Exposure Management](https://www.servicenow.com/docs/access?context=exploring-ai-security-exposure&family=australia&ft:locale=en-US)**

Vulnerability management teams can use AI Security Exposure Management to reduce the AI attack surface by efficiently remediating security exposures in AI assets.

The AI Exposures dashboard provides you with a view into the critical security vulnerabilities of your AI attack surface. You have the option to use a generative AI skill to help you determine if any of the threats might be already mitigated and help you prioritize high risk exposures and defer lower risk exposures that have mitigations or guardrails already in place.

AI Security Exposure Management uses imported data with the following integrations that are available in the ServiceNow® Store:

    -   The Cisco AI Defense Integration for AI Security Exposure Management
    -   The AI Service Graph Connector for Palo Alto Prisma AIRS
    -   The AI Service Graph Connector for HiddenLayer
    -   The Palo Alto Prisma AIRS Integration
-   **[Risk reduction requests for multiple findings](https://www.servicenow.com/docs/access?context=sem-bulk-edit-request-exception&family=australia&ft:locale=en-US)**

You can now submit risk reduction requests for multiple findings at once using Bulk Edit in the Security Exposure Management Workspace. This reduces manual effort and simplifies the risk acceptance workflow.

-   **[Smart Assessment support for exception requests](https://www.servicenow.com/docs/access?context=sem-configure-exp-mngmt-vr&family=australia&ft:locale=en-US)**

The Request Exception option now supports Smart Assessment. When you select Request for Risk Reduction, the compensating control questionnaire takes priority and is displayed instead of the exception questionnaire, based on your exception management configuration.

-   **[Enhancements to the Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&family=australia&ft:locale=en-US)**

Added support for certificate-based authentication in the Microsoft Threat and Vulnerability Management \(TVM\) integration.

-   **[Enhancements to Security Posture Control and supported applications](https://www.servicenow.com/docs/access?context=spc-install&family=australia&ft:locale=en-US)**
    -   Configuration Compliance is now a supported dependency for Security Posture Control Core, expanding the policy framework for compliance-driven asset evaluation. It is installed automatically when you install Security Posture Control.
    -   With enhancements to the asset profile framework, you might see improved coverage for service graph connector-sourced data.
    -   Enhancements to the API Connector builder for Security Posture Control streamline the process for your custom-built connectors. You might see improvements for the request/response mapping steps.
    -   Expanded support for additional authentication patterns when building custom API connectors.
-   **[Activate the Wiz Asset Integration and identify resource types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&family=australia&ft:locale=en-US)**

Enhancements to the Wiz integration include:

    -   Starting with version 32.1 \(USEM\) and version 4.1 \(non-USEM\), the Asset integration is deactivated by default and is not a mandatory prerequisite for the other Wiz integration imports.

If you choose to activate it, the Asset integration will retrieve assets for all resource types if you don't specify the ones you want on the **Asset Integration Configuration** tab. To avoid importing vulnerability data you don't need, identify only the resources \(assets\) that you want to import with this integration.

    -   Resource Type is no longer a mandatory field for configuring the Vulnerability Response Integration with Wiz. You can now save Wiz configurations for the integrations without specifying a Resource Type, simplifying setup for use cases where specifying a Resource Type isn't appropriate.
-   **[Configuring lookup rules](https://www.servicenow.com/docs/access?context=sem-configure-lookup-rules&family=australia&ft:locale=en-US)**

The Applies to field is added to the Rules page for Configuration \(CI\) lookup rule records. For third-party and ServiceNow® integrations that support both Application Vulnerability Response \(AVR\) and Vulnerability Response \(VR\) lookup rules, like the Vulnerability Response Integration with Wiz, for example, select one for a rule:

    -   **Discovered Application** for Application Vulnerability Response lookup rules.
    -   **Discovered Item** for Vulnerability Response lookup rules.
**Note:** The field is left empty by default. If you leave this field empty for lookup rules that support both VR and AVR integrations, background jobs for both applications apply changes on the same set of lookup rules. This state might cause a conflict and set the reapply flag incorrectly. With this distinction set, after the respective background jobs for AVR and VR are completed, the system resets the flag only for the lookup rules for the background job that was run.

-   **[Auto-close rules now run in parallel, reducing processing time for large datasets](https://www.servicenow.com/docs/access?context=sem-configure-auto-close-rules&family=australia&ft:locale=en-US)**

Previously, auto-close rules ran as a single sequential job. Starting with v30.3.3, the system automatically splits processing into multiple concurrent jobs based on data volume — no configuration required. Simply enable an auto-close rule and the system handles the rest.

-   **[Deferred migration option for Unified Security Exposure Management \(USEM\)](https://www.servicenow.com/docs/access?context=migrate-to-usem&family=australia&ft:locale=en-US)**

If you're not ready to migrate to Unified Security Exposure Management \(USEM\), you can select **Upgrade later** button to defer the process. The Migration Assistant will be hidden from the main view but remains accessible via the Filter Navigator whenever you're ready to proceed.

-   **[Configure users and groups in Security Exposure Management Workspace](https://www.servicenow.com/docs/access?context=sem-configure-users-groups-overview&family=australia&ft:locale=en-US)**

Administrators can now assign and remove product-specific roles for users and groups directly from the Security Exposure Management workspace. This workspace-based experience provides a consistent, centralized interface for controlling access across supported exposure management products.

-   **[Security tag groups and tags for organized security content](https://www.servicenow.com/docs/access?context=sem-create-class-group-and-tags&family=australia&ft:locale=en-US)**

Administrators can now create and manage security tag groups and tags directly from the Security Exposure Management Workspace. Tags can be applied to security incidents, response tasks, vulnerable items, observables, IoCs, and security cases to attach metadata to responding records and define access controls for specific types of security content.

-   **[Watchdog configuration](https://www.servicenow.com/docs/access?context=sem-watchdog-configure&family=australia&ft:locale=en-US)**

Administrators can now create and manage watchdogs from the Security Exposure Management Workspace. Each watchdog monitors a specified table for conditions you define, and can be configured to notify designated users or groups when those conditions are met.

-   **[Severity mapping for third-party integrations](https://www.servicenow.com/docs/access?context=sem-configure-severity-map&family=australia&ft:locale=en-US)**

Administrators can now create and manage severity maps from the Security Exposure Management Workspace. Severity mapping normalizes source-specific severity fields from third-party integrations into the standardized severity scale used by Unified Security Exposure Management. This ensures consistent severity representation across all integrated data sources.

-   **[Background job configuration](https://www.servicenow.com/docs/access?context=vr-background-framework&family=australia&ft:locale=en-US)**

A new Background Job Configuration tile is now available in the Other section of the Security Exposure Management Workspace Administration console. Selecting the tile opens the Background Job Configuration page providing a consistent workspace-based entry point for managing background job settings.

-   **[Advanced settings](https://www.servicenow.com/docs/access?context=sem-advanced-settings&family=australia&ft:locale=en-US)**

Administrators can now configure advanced system-level settings from the Security Exposure Management Workspace. The Advanced Settings page provides a single location for managing behavior across exposure management, remediation workflows, compliance handling, and service impact calculations.

-   **[Bulk approval and rejection](https://www.servicenow.com/docs/access?context=sem-approve-ex-rule-request&family=australia&ft:locale=en-US)**

Approvers can now process multiple exception requests simultaneously from a single list view, which can help with significantly reducing manual effort for high-volume approval workflows.

-   **[New KPI tiles for exception management](https://www.servicenow.com/docs/access?context=sem-unified-approval-rules-explore&family=australia&ft:locale=en-US)**

Added new KPI tiles to the Exception Management dashboard for Expiring Exceptions, Exception Extensions, and Repeated Rejections, giving approvers and managers additional visibility into exception health and lifecycle trends.

-   **[AWS Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=aws-integration-for-security-exposure-management-overview&family=australia&ft:locale=en-US)**

The AWS Integration for Security Exposure Management supports integrations with the following AWS services:

    -   AWS Inspector is an automated vulnerability management service that continuously scans EC2 instances, ECR container images, and Lambda functions for software vulnerabilities \(CVEs\) and unintended network exposure. The Vulnerability Response integration with AWS Inspector imports host and container vulnerability findings from AWS Inspector.
    -   AWS Security Hub is a security service that is used to centralize and update security checks across AWS accounts. It provides a unified view of security alerts and compliance status by integrating with various AWS services. The Vulnerability Response integration with AWS Security Hub imports host, container vulnerabilities, and misconfigurations from AWS Security Hub.
-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&family=australia&ft:locale=en-US)**

The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenableIntegration&family=australia&ft:locale=en-US)**

Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=c_QualysVulnIntegration&family=australia&ft:locale=en-US)**

The Qualys Vulnerability Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[GitHub Application Vulnerability Integration – Generic secrets support](https://www.servicenow.com/docs/access?context=github-vuln-integration&family=australia&ft:locale=en-US)**

The GitHub Secret Scanning Integration now imports generic secrets in addition to standard secrets from your GitHub repositories. A new Manage generic secrets in ServiceNow configuration option lets you control whether generic secrets are ingested. Imported secrets are mapped to Application Vulnerable Items \(AVIs\) with the scan type, `Secret`, while generic secrets are mapped with the scan type, `Generic Secret`.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Unified Security Exposure Management \(USEM\) features.

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

-   **[ITSM Advanced plugin required for change request options in the Remediation view](https://www.servicenow.com/docs/access?context=sem-ws-CRs&family=australia&ft:locale=en-US)**

Use the **Create Change** and **Add to existing change** options in the Remediation view of the Security Exposure Management Workspace to manage remediation tasks through Change Management. These options now require the ITSM Advanced plugin to be active on your instance. If you have migrated to an ITSM AI Native SKU without ITSM Advanced, upgrade to ITSM Advanced SKU to restore access to these options.

-   **[Create remediation tasks directly from the Security Exposure Management Workspace list view](https://www.servicenow.com/docs/access?context=sem-workspace-list-page&family=australia&ft:locale=en-US)**

Remediation owners can now create remediation tasks directly from list views in the Security Exposure Management Workspace by selecting the Create Remediation Task action from the list toolbar in the Assigned to me and Assigned to my group views for host vulnerable items, application vulnerable items, container vulnerable items, and configuration test results. Previously, this action was available only for managers.

-   **[Improved vulnerability assessment workflows](https://www.servicenow.com/docs/access?context=vr-ws-vuln-assessment&family=australia&ft:locale=en-US)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&family=australia&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Enhanced Compensatory controls](https://www.servicenow.com/docs/access?context=requesting-approving-risk-reduction&family=australia&ft:locale=en-US)**

When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Unified Security Exposure Management \(USEM\) features or functionality were removed.

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

Between your current release family and Australia, some Unified Security Exposure Management \(USEM\) features or functionality were deprecated.

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

Review information on how to activate Unified Security Exposure Management \(USEM\).

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

Install Unified Security Exposure Management by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Unified Security Exposure Management \(USEM\) we have noted them here.

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

If any specific browser requirements were introduced or changed for Unified Security Exposure Management \(USEM\) we have noted them here.

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

Review details on accessibility information for Unified Security Exposure Management \(USEM\), such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Unified Security Exposure Management \(USEM\) we have noted them here.

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

If there are specific highlight considerations for Unified Security Exposure Management \(USEM\) we have noted them here.

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

-   Vulnerability management teams can use AI Security Exposure Management and supported integrations to reduce the AI attack surface by efficiently remediating security exposures in AI assets.
-   USEM was enhanced and updated in the Australia release to support the new AI native experience.
-   Administrators can manage user and group role assignments, create/update watchdogs with custom conditions, and access a centralized Advanced Settings page — all directly from the Security Exposure Management Workspace, eliminating the need to navigate multiple configuration pages.
-   Assign tags to security incidents, response tasks, vulnerable items, observables, IoCs, and security cases to define metadata and access control all directly from the Security Exposure Management Workspace.
-   Third-party source severity fields are now normalized into standard ServiceNow severity values all directly in the Security Exposure Management Workspace.
-   Approvers can bulk approve or reject multiple requests in a single action.
-   The AWS Integration for Security Exposure Management supports integrations with AWS Inspector and AWS Security Hub.

 See [Unified Security Exposure Management](https://www.servicenow.com/docs/access?context=unified-security-exposure-management-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

