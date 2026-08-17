---
title: Unified Security Exposure Management release notes
description: The ServiceNow Unified Security Exposure Management application enhances exposure management with role-based views, enabling faster decision-making, efficient task handling, and streamlined approvals. It centralizes workflows, improves visibility across exposures, and enforces governance through configurable rules. With consistent navigation and integrated configuration, USEM boosts productivity, collaboration, and control across security operations, delivering a unified experience for exposures across assets. Unified Security Exposure Management is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-07-31"
reading_time_minutes: 10
---

# Unified Security Exposure Management release notes

The ServiceNow® Unified Security Exposure Management application enhances exposure management with role-based views, enabling faster decision-making, efficient task handling, and streamlined approvals. It centralizes workflows, improves visibility across exposures, and enforces governance through configurable rules. With consistent navigation and integrated configuration, USEM boosts productivity, collaboration, and control across security operations, delivering a unified experience for exposures across assets. Unified Security Exposure Management is a new application in the Zurich release.

## Unified Security Exposure Management highlights for the Zurich release

Starting with Zurich Patch 12, Now Assist for Vulnerability Response is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. The change is reflected in the name of ServiceNow® products, including Now Assist for Vulnerability Response which is called ServiceNow Otto for Unified Security Exposure Management with these enhancements for the new AI experience. See [ServiceNow Otto for Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-usem-landing-ties.md) for more information.

-   Experience a standardized data model and modular workflows for Vulnerability Response applications with Unified Security Exposure Management. This transformation and architectural design ensures consistent features across all modules, simplifies configuration, and enables flexible, role-based experiences. The modular approach allows faster updates and seamless integration, creating a scalable and future-ready platform.
-   Manage security exposures with Findings and Remediation views with a centralized platform in the Security Exposure Management Workspace.
-   Configure all USEM apps, including rules, email templates, email notifications, and severity mapping for integrations with the Administration console.
-   Enhanced exception management: Streamlined exception request and approval workflows with comprehensive tracking and audit trails.
-   Use generative AI with features in the SEM workspace that are included with the ServiceNow Otto for Unified Security Exposure Management application.

See [Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/unified-security-exposure-management-landing-page.md) for more information.

## Important upgrade information for Unified Security Exposure Management

Unified Security Exposure Management is available to all customers who are entitled to Vulnerability Response. However, migrating to USEM is a major upgrade that introduces a unified architecture for improved performance, scalability, and streamlined workflows. Before upgrading, leverage the Migration assistant for Unified Security Exposure Management that is available as an update set. See the [Migration Guidance to Unified Security Exposure Management \[KB2556844\]](https://support.servicenow.com/kb?sys_kb_id=8652717893a8ba94f538fb2d6cba1078&id=kb_article_view) Knowledge Base article for more information. This tool provides a guided experience for plugin installation, data mapping, rule migration, and post-migration validation, reducing risk and manual effort. Ensure that all integrations and workflows are reviewed for compatibility before initiating migration. For more information, see [Migrating from Vulnerability Response to Unified Security Exposure Management \(USEM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/migrating-to-usem.md) and [Migrate to Unified Security Exposure Management \(USEM\) from Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/migrate-to-usem.md).

## Unified Security Exposure Management features

-   **[Remediation task rule execution mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-grouping-multiple-findings-remediation-tasks-processing.md)**

    You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/ms-defender-sem.md)**

    The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[GitHub Application Vulnerability Integration – Generic secrets support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/github-vuln-integration.md)**

    The GitHub Secret Scanning Integration now imports generic secrets in addition to standard secrets from your GitHub repositories. A new Manage generic secrets in ServiceNow configuration option lets you control whether generic secrets are ingested. Imported secrets are mapped to Application Vulnerable Items \(AVIs\) with the scan type Secret, while generic secrets are mapped with the scan type Generic Secret.

-   **[Optimized Tenable.io Compliance Results ingestion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/tenable-io-integrations-list.md)**

    Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/qualys-rest-messages-cc.md)**

    Qualys Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[Improved vulnerability assessment workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/vr-ws-vuln-assessment.md)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Enhanced Compensatory controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/requesting-approving-risk-reduction.md)**

    When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.

-   **[Enhanced security exposure management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-workspace-user-interface.md)**

    Introduced Security Exposure Management Workspace for all security personas, providing a centralized platform for managing security exposures. It includes the following views:

    -   Findings view: Comprehensive filtering, dashboard creation, and visualization controls enable efficient analysis and prioritization.
    -   Remediation view: Multiple work modes \(tasks, findings, assets\) facilitate effective remediation strategies.
    -   Approval view: The Exception Management UI now provides enhanced insights directly within the Change Approval record, enabling approvers to make informed decisions without navigating to related records. Additionally, the Approver landing page has been redesigned with an improved table view and additional columns, delivering better visibility and context for all findings. These enhancements streamline the approval workflow, reduce manual effort, and accelerate decision-making for exception requests.
-   **[Streamlined administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-administration-console.md)**

    Introduced Administration console to enable one-stop configuration for all Unified Security Exposure Management applications, including assignment rules, classification rules, and remediation targets. It provides consistent workflows across Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance applications.

-   **[Centralised Approval Experience via Employee Service Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/employee-center-vr-overview.md)**

    The Employee Service Center ESC now provides a standardized approval experience for Business Unit Heads, Service Owners, and IT Heads who may not regularly access the USEM platform. This enhancement ensures that vulnerability-related approvals can be managed from a single, central location, improving efficiency and transparency.

-   **[Configure approval workflow with unified Approval Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-approval-rules-overiew.md)**

    The Approval Rules now provide a standardized way to configure approval workflows across multiple findings and remediation task tables in Security Exposure Management. Administrators can now define approval conditions, select applicable tables, and configure multi‑level approvers through a single, unified interface.

-   **[Cloud Exposure view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/vr-cloud-exposure-view-db.md)**

    View and act on all your cloud-related security findings from multiple vendors across your cloud environments with the Cloud Exposure View supported by USEM. The Cloud Exposure View provides a single location for your cloud security teams to monitor your cloud security posture.

-   **[Monitor integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/integrating-usem.md)**

    USEM introduces integration monitoring capabilities within the Security Exposure Management Workspace Administration console. Administrators can now view and troubleshoot integration run statuses for installed third-party applications, ensuring better visibility and operational health.

-   **[Generate insights to prioritize findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-insights-skill.md)**

    SEM Workspace uses Now Assist to bring generative AI to your dashboard. This capability helps you focus on critical risks and make informed decisions faster, improving overall security outcomes. It provides:

    -   Contextual summaries to quickly understand your security posture
    -   Actionable recommendations to address prioritized risks
-   **[Create custom widgets in the Visualization Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-create-widget.md)**

    Create and manage custom widgets in the finding view of the SEM workspace to visualize findings data that align with your organization’s reporting needs. The Visualization Library lets you define widget attributes such as chart type, visualization group, and data filters, enabling you to build dashboards that highlight the insights most relevant to your teams. This flexibility helps you focus on meaningful security metrics and make data-driven decisions.

-   **[Improved remediation target date handling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-configure-remediation-target-rules.md)**

    Remediation target \(RT\) dates now dynamically recalculate when a finding’s risk rating changes. When enabled, the system recalculates the SLA from the most recent risk rating update date, preventing RT dates from being set in the past and ensuring accurate SLA tracking.

-   **[Exception management configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-configure-exp-mngmt-vr.md)**
    -   Manual and automated exception request and approval workflow: Flexible, customizable workflows streamline submission, review, and approval of exception requests.
    -   Comprehensive exception tracking and audit trails: Detailed records of approvals, justifications, and timelines support compliance efforts and simplify regulatory reporting.
-   **Consistent remediation task management with [remediation views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-workspaces-ui-remediation-module.md) and [centralized findings configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-configure-rules-manage-findings.md)**

    Unified task management: Supports both manual task creation and automated rule-based task generation across all Unified Security Exposure Management applications.

    Centralized rule definition: Enables efficient management of tasks across Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance applications.

-   **[Advanced risk management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-vuln-calc-define-risk-rule-fields.md)**

    Risk calculators: Introduced for all Unified Security Exposure Management applications, enabling definition of risk rules based on multiple factors and calculation mechanisms.

    Risk rollup calculators: Aggregate scores from findings to higher-level entities, ensuring consistent risk scoring across applications.

-   **[Generate approval recommendations with generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-approval-recommendation-skill.md)**

    AI-powered recommendations for Exception and False Positive requests. Provides an on-demand recommendation to approve or reject a request using the Now Assist skill framework. The framework analyzes contextual data such as vulnerability details, risk factors, exploit availability, and related indicators. The recommendations are accessible directly from the Exception Change Approval record in the Security Exposure Management Workspace, enabling approvers to make faster, more consistent decisions while reducing the manual analysis effort.

-   **Exception Rule &amp; Change Approval Enhancements**
    -   [Change Approval Creation for Exception Rule submission](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-exception-rules-overview.md): Previously, Change Approval \(CA\) was created only for a few types of exception requests. Now, the Change Approval\(CA\) is also created during exception rule submission. This enhancement verifies consistency across exception workflows and improves traceability.
    -   [Vulnerability Intelligence Tile on Change Approval Record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-configure-approval-view.md): The Vulnerability Intelligence Tile is added to change approval records, displaying vulnerability intelligence such as CISA KEV information, Known ransomware indicators, and EPSS percentile. This tile is visible only when the Intelligence and App-Vuln NVD plugins are installed. This enhancement provides approvers with the critical threat context for informed decision-making.
    -   [Summary Tiles on Change Approval Record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-configure-approval-view.md). The Impact Tile is added in the overview tab of the Change Approval record to provide approvers with the visibility of the impacted count information such as, Impacted CIs, Total Findings, and Total Vulnerabilities on the Change Approval for a Remediation Task. This enhancement improves visibility of potential impact during approval or rejection of requests.
    -   [Application-Based Filtering on Approvals View](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-configure-approval-view.md): Added filtering capability on the Approvals view by application type such as: Application vulnerabilities \(AVR\), Container vulnerabilities \(CVR\), Infra Vulnerabilities \(VR\), and Misconfigurations \(CC\). This capability enables approvers to quickly drill down and manage approvals by category.
    -   [Reapply Assignment Rules for Deferred and Manually Assigned Items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-configure-assignment-rules.md): Introduced the ability to reapply assignment rules for Deferred items and Manually assigned items. This enhancement provides the flexibility to reassign items through the Re-evaluate action in the list view.

**Important:** Unified Security Exposure Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Activation information

Unified Security Exposure Management is a ServiceNow AI Platform feature that is available with activation of the Security Exposure Management \(com.snc.security\_support.core\). For details, see [Install Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/sem-install-and-configure.md).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Security Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/security-operations-rn-landing.md)

