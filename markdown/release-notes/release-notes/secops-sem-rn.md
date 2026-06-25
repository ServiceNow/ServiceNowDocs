---
title: Unified Security Exposure Management \(USEM\) notes
description: The ServiceNow Unified Security Exposure Management \(USEM\) application enhances exposure management with role-based views, enabling faster decision-making, efficient task handling, and streamlined approvals. It centralizes workflows, improves visibility across exposures, and enforces governance through configurable rules. With consistent navigation and integrated configuration, USEM boosts productivity, collaboration, and control across security operations, delivering a unified experience for exposures across assets. USEM was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 12
keywords: [usem release notes]
---

# Unified Security Exposure Management \(USEM\) notes

The ServiceNow® Unified Security Exposure Management \(USEM\) application enhances exposure management with role-based views, enabling faster decision-making, efficient task handling, and streamlined approvals. It centralizes workflows, improves visibility across exposures, and enforces governance through configurable rules. With consistent navigation and integrated configuration, USEM boosts productivity, collaboration, and control across security operations, delivering a unified experience for exposures across assets. USEM was enhanced and updated in the Australia release.

## Unified Security Exposure Management highlights for the Australia release

-   Vulnerability management teams can use AI Security Exposure Management and supported integrations to reduce the AI attack surface by efficiently remediating security exposures in AI assets.
-   USEM was enhanced and updated in the Australia release to support the new AI native experience.
-   Administrators can manage user and group role assignments, create/update watchdogs with custom conditions, and access a centralized Advanced Settings page — all directly from the Security Exposure Management Workspace, eliminating the need to navigate multiple configuration pages.
-   Assign tags to security incidents, response tasks, vulnerable items, observables, IoCs, and security cases to define metadata and access control all directly from the Security Exposure Management Workspace.
-   Third-party source severity fields are now normalized into standard ServiceNow severity values all directly in the Security Exposure Management Workspace.
-   Approvers can bulk approve or reject multiple requests in a single action.
-   The AWS Integration for Security Exposure Management supports integrations with AWS Inspector and AWS Security Hub.

See [Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/unified-security-exposure-management-landing-page.md) for more information.

**Important:** Unified Security Exposure Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Unified Security Exposure Management to Australia

To access the new AI native experience in the Unified Security Exposure Management \(USEM\) workspace, you must upgrade to the Australia release.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


Unified Security Exposure Management is available to all customers who are entitled to Vulnerability Response, however, migrating to USEM is a major upgrade that introduces a unified architecture for improved performance, scalability, and streamlined workflows. Before upgrading, leverage the Migration assistant for Unified Security Exposure Management that is available as an update set. See the [Migration Guidance to Unified Security Exposure Management \[KB2556844\]](https://support.servicenow.com/kb?sys_kb_id=8652717893a8ba94f538fb2d6cba1078&id=kb_article_view) Knowledge Base article for more information. This tool provides a guided experience for plugin installation, data mapping, rule migration, and post-migration validation, reducing risk and manual effort. Ensure that all integrations and workflows are reviewed for compatibility before initiating migration. For more information, see [Migrating from Vulnerability Response to Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/migrating-to-usem.md) and [Migrate to Unified Security Exposure Management \(USEM\) from Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/migrate-to-usem.md).

## New in the Australia release

-   **[Evaluate vulnerability exposure with AI-powered analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/now-assist-review-vulnerability-exposure-data.md)**

    The Security Exposure 360 agentic workflow brings AI-powered exposure analysis to Unified Security Exposure Management \(USEM\). Users can now ask questions in plain language and get answers grounded in their own ServiceNow data — across all types of findings within USEM.

-   **[AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/exploring-ai-security-exposure.md)**

    Vulnerability management teams can use AI Security Exposure Management to reduce the AI attack surface by efficiently remediating security exposures in AI assets.

    The AI Exposures dashboard provides you with a view into the critical security vulnerabilities of your AI attack surface. You have the option to use a generative AI skill to help you determine if any of the threats might be already mitigated and help you prioritize high risk exposures and defer lower risk exposures that have mitigations or guardrails already in place.

    AI Security Exposure Management uses imported data with the following integrations that are available in the ServiceNow® Store:

    -   The Cisco AI Defense Integration for AI Security Exposure Management
    -   The AI Service Graph Connector for Palo Alto Prisma AIRS
    -   The AI Service Graph Connector for HiddenLayer
    -   The Palo Alto Prisma AIRS Integration
-   **[Risk reduction requests for multiple findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-bulk-edit-request-exception.md)**

    You can now submit risk reduction requests for multiple findings at once using Bulk Edit in the Security Exposure Management Workspace. This reduces manual effort and simplifies the risk acceptance workflow.

-   **[Smart Assessment support for exception requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-configure-exp-mngmt-vr.md)**

    The Request Exception option now supports Smart Assessment. When you select Request for Risk Reduction, the compensating control questionnaire takes priority and is displayed instead of the exception questionnaire, based on your exception management configuration.

-   **[Enhancements to the Microsoft Defender Integration for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/ms-defender-sem.md)**

    Added support for certificate-based authentication in the Microsoft Threat and Vulnerability Management \(TVM\) integration.

-   **[Enhancements to Security Posture Control and supported applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/spc-install.md)**
    -   Configuration Compliance is now a supported dependency for Security Posture Control Core, expanding the policy framework for compliance-driven asset evaluation. It is installed automatically when you install Security Posture Control.
    -   With enhancements to the asset profile framework, you might see improved coverage for service graph connector-sourced data.
    -   Enhancements to the API Connector builder for Security Posture Control streamline the process for your custom-built connectors. You might see improvements for the request/response mapping steps.
    -   Expanded support for additional authentication patterns when building custom API connectors.
-   **[Activate the Wiz Asset Integration and identify resource types for import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/wiz-assets-resources-tab.md)**

    Enhancements to the Wiz integration include:

    -   Starting with version 32.1 \(USEM\) and version 4.1 \(non-USEM\), the Asset integration is deactivated by default and is not a mandatory prerequisite for the other Wiz integration imports.

        If you choose to activate it, the Asset integration will retrieve assets for all resource types if you don't specify the ones you want on the **Asset Integration Configuration** tab. To avoid importing vulnerability data you don't need, identify only the resources \(assets\) that you want to import with this integration.

    -   Resource Type is no longer a mandatory field for configuring the Vulnerability Response Integration with Wiz. You can now save Wiz configurations for the integrations without specifying a Resource Type, simplifying setup for use cases where specifying a Resource Type isn't appropriate.
-   **[Configuring lookup rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-configure-lookup-rules.md)**

    The Applies to field is added to the Rules page for Configuration \(CI\) lookup rule records. For third-party and ServiceNow® integrations that support both Application Vulnerability Response \(AVR\) and Vulnerability Response \(VR\) lookup rules, like the Vulnerability Response Integration with Wiz, for example, select one for a rule:

    -   **Discovered Application** for Application Vulnerability Response lookup rules.
    -   **Discovered Item** for Vulnerability Response lookup rules.
    **Note:** The field is left empty by default. If you leave this field empty for lookup rules that support both VR and AVR integrations, background jobs for both applications apply changes on the same set of lookup rules. This state might cause a conflict and set the reapply flag incorrectly. With this distinction set, after the respective background jobs for AVR and VR are completed, the system resets the flag only for the lookup rules for the background job that was run.

-   **[Auto-close rules now run in parallel, reducing processing time for large datasets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-configure-auto-close-rules.md)**

    Previously, auto-close rules ran as a single sequential job. Starting with v30.3.3, the system automatically splits processing into multiple concurrent jobs based on data volume — no configuration required. Simply enable an auto-close rule and the system handles the rest.

-   **[Deferred migration option for Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/migrate-to-usem.md)**

    If you're not ready to migrate to Unified Security Exposure Management \(USEM\), you can select **Upgrade later** button to defer the process. The Migration Assistant will be hidden from the main view but remains accessible via the Filter Navigator whenever you're ready to proceed.

-   **[Configure users and groups in Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-configure-users-groups-overview.md)**

    Administrators can now assign and remove product-specific roles for users and groups directly from the Security Exposure Management workspace. This workspace-based experience provides a consistent, centralized interface for controlling access across supported exposure management products.

-   **[Security tag groups and tags for organized security content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-create-class-group-and-tags.md)**

    Administrators can now create and manage security tag groups and tags directly from the Security Exposure Management Workspace. Tags can be applied to security incidents, response tasks, vulnerable items, observables, IoCs, and security cases to attach metadata to responding records and define access controls for specific types of security content.

-   **[Watchdog configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-watchdog-configure.md)**

    Administrators can now create and manage watchdogs from the Security Exposure Management Workspace. Each watchdog monitors a specified table for conditions you define, and can be configured to notify designated users or groups when those conditions are met.

-   **[Severity mapping for third-party integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-configure-severity-map.md)**

    Administrators can now create and manage severity maps from the Security Exposure Management Workspace. Severity mapping normalizes source-specific severity fields from third-party integrations into the standardized severity scale used by Unified Security Exposure Management. This ensures consistent severity representation across all integrated data sources.

-   **[Background job configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vr-background-framework.md)**

    A new Background Job Configuration tile is now available in the Other section of the Security Exposure Management Workspace Administration console. Selecting the tile opens the Background Job Configuration page providing a consistent workspace-based entry point for managing background job settings.

-   **[Advanced settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-advanced-settings.md)**

    Administrators can now configure advanced system-level settings from the Security Exposure Management Workspace. The Advanced Settings page provides a single location for managing behavior across exposure management, remediation workflows, compliance handling, and service impact calculations.

-   **[Bulk approval and rejection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-approve-ex-rule-request.md)**

    Approvers can now process multiple exception requests simultaneously from a single list view, which can help with significantly reducing manual effort for high-volume approval workflows.

-   **[New KPI tiles for exception management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-unified-approval-rules-explore.md)**

    Added new KPI tiles to the Exception Management dashboard for Expiring Exceptions, Exception Extensions, and Repeated Rejections, giving approvers and managers additional visibility into exception health and lifecycle trends.

-   **[AWS Integration for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/aws-integration-for-security-exposure-management-overview.md)**

    The AWS Integration for Security Exposure Management supports integrations with the following AWS services:

    -   AWS Inspector is an automated vulnerability management service that continuously scans EC2 instances, ECR container images, and Lambda functions for software vulnerabilities \(CVEs\) and unintended network exposure. The Vulnerability Response integration with AWS Inspector imports host and container vulnerability findings from AWS Inspector.
    -   AWS Security Hub is a security service that is used to centralize and update security checks across AWS accounts. It provides a unified view of security alerts and compliance status by integrating with various AWS services. The Vulnerability Response integration with AWS Security Hub imports host, container vulnerabilities, and misconfigurations from AWS Security Hub.
-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/ms-defender-sem.md)**

    The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Optimized Tenable.io Compliance Results ingestion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/tenableIntegration.md)**

    Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/c_QualysVulnIntegration.md)**

    The Qualys Vulnerability Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[GitHub Application Vulnerability Integration – Generic secrets support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/github-vuln-integration.md)**

    The GitHub Secret Scanning Integration now imports generic secrets in addition to standard secrets from your GitHub repositories. A new Manage generic secrets in ServiceNow configuration option lets you control whether generic secrets are ingested. Imported secrets are mapped to Application Vulnerable Items \(AVIs\) with the scan type, `Secret`, while generic secrets are mapped with the scan type, `Generic Secret`.


## Changed in this release

-   **[ITSM Advanced plugin required for change request options in the Remediation view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-ws-CRs.md)**

    Use the **Create Change** and **Add to existing change** options in the Remediation view of the Security Exposure Management Workspace to manage remediation tasks through Change Management. These options now require the ITSM Advanced plugin to be active on your instance. If you have migrated to an ITSM AI Native SKU without ITSM Advanced, upgrade to ITSM Advanced SKU to restore access to these options.

-   **[Create remediation tasks directly from the Security Exposure Management Workspace list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-workspace-list-page.md)**

    Remediation owners can now create remediation tasks directly from list views in the Security Exposure Management Workspace by selecting the Create Remediation Task action from the list toolbar in the Assigned to me and Assigned to my group views for host vulnerable items, application vulnerable items, container vulnerable items, and configuration test results. Previously, this action was available only for managers.

-   **[Improved vulnerability assessment workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vr-ws-vuln-assessment.md)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Remediation task rule execution mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-grouping-multiple-findings-remediation-tasks-processing.md)**

    You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Enhanced Compensatory controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/requesting-approving-risk-reduction.md)**

    When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.


## Activation information

Install Unified Security Exposure Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/security-operations-rn-landing.md)

