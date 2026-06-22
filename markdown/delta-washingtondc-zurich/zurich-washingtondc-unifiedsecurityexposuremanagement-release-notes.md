---
title: Combined Unified Security Exposure Management release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Unified Security Exposure Management from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-unifiedsecurityexposuremanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Unified Security Exposure Management release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Unified Security Exposure Management from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Unified Security Exposure Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Unified Security Exposure Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Unified Security Exposure Management is available to all customers who are entitled to Vulnerability Response, however, migrating to USEM is a major upgrade that introduces a unified architecture for improved performance, scalability, and streamlined workflows. Before upgrading, leverage the Migration assistant for Unified Security Exposure Management that is available as an update set. See the [Migration Guidance to Unified Security Exposure Management \[KB2556844\]](https://support.servicenow.com/kb?sys_kb_id=8652717893a8ba94f538fb2d6cba1078&id=kb_article_view) Knowledge Base article for more information. This tool provides a guided experience for plugin installation, data mapping, rule migration, and post-migration validation, reducing risk and manual effort. Ensure that all integrations and workflows are reviewed for compatibility before initiating migration. For more information, see [Migrating to USEM](https://servicenow-staging.fluidtopics.net/access?context=migrating-to-usem&family=zurich&ft:locale=en-US) and [Migrate to USEM](https://servicenow-staging.fluidtopics.net/access?context=migrate-to-usem&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Unified Security Exposure Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   **[Enhanced security exposure management](https://servicenow-staging.fluidtopics.net/access?context=sem-workspace-user-interface&family=zurich&ft:locale=en-US)**

Introduced Security Exposure Management Workspace for all security personas, providing a centralized platform for managing security exposures. It includes the following views:

    -   Findings view: Comprehensive filtering, dashboard creation, and visualization controls enable efficient analysis and prioritization.
    -   Remediation view: Multiple work modes \(tasks, findings, assets\) facilitate effective remediation strategies.
    -   Approval view: The Exception Management UI now provides enhanced insights directly within the Change Approval record, enabling approvers to make informed decisions without navigating to related records. Additionally, the Approver landing page has been redesigned with an improved table view and additional columns, delivering better visibility and context for all findings. These enhancements streamline the approval workflow, reduce manual effort, and accelerate decision-making for exception requests.
-   **[Streamlined administration](https://servicenow-staging.fluidtopics.net/access?context=sem-administration-console&family=zurich&ft:locale=en-US)**

Introduced Administration console to enable one-stop configuration for all Unified Security Exposure Management applications, including assignment rules, classification rules, and remediation targets. It provides consistent workflows across Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance applications.

-   **[Centralised Approval Experience via Employee Service Center](https://servicenow-staging.fluidtopics.net/access?context=employee-center-vr-overview&family=zurich&ft:locale=en-US)**

The Employee Service Center ESC now provides a standardized approval experience for Business Unit Heads, Service Owners, and IT Heads who may not regularly access the USEM platform. This enhancement ensures that vulnerability-related approvals can be managed from a single, central location, improving efficiency and transparency.

-   **[Configure approval workflow with unified Approval Rules](https://servicenow-staging.fluidtopics.net/access?context=sem-approval-rules-overiew&family=zurich&ft:locale=en-US)**

The Approval Rules now provide a standardized way to configure approval workflows across multiple findings and remediation task tables in Security Exposure Management. Administrators can now define approval conditions, select applicable tables, and configure multi‑level approvers through a single, unified interface.

-   **[Cloud Exposure view](https://servicenow-staging.fluidtopics.net/access?context=vr-cloud-exposure-view-db&family=zurich&ft:locale=en-US)**

View and act on all your cloud-related security findings from multiple vendors across your cloud environments with the Cloud Exposure View supported by USEM. The Cloud Exposure View provides a single location for your cloud security teams to monitor your cloud security posture.

-   **[Monitor integrations](https://servicenow-staging.fluidtopics.net/access?context=integrating-usem&family=zurich&ft:locale=en-US)**

USEM introduces integration monitoring capabilities within the Security Exposure Management Workspace Administration console. Administrators can now view and troubleshoot integration run statuses for installed third-party applications, ensuring better visibility and operational health.

-   **[Generate insights to prioritize findings](https://servicenow-staging.fluidtopics.net/access?context=sem-insights-skill&family=zurich&ft:locale=en-US)**

SEM Workspace uses Now Assist to bring generative AI to your dashboard. This capability helps you focus on critical risks and make informed decisions faster, improving overall security outcomes. It provides:

    -   Contextual summaries to quickly understand your security posture
    -   Actionable recommendations to address prioritized risks
-   **[Create custom widgets in the Visualization Library](https://servicenow-staging.fluidtopics.net/access?context=sem-create-widget&family=zurich&ft:locale=en-US)**

Create and manage custom widgets in the finding view of the SEM workspace to visualize findings data that align with your organization’s reporting needs. The Visualization Library lets you define widget attributes such as chart type, visualization group, and data filters, enabling you to build dashboards that highlight the insights most relevant to your teams. This flexibility helps you focus on meaningful security metrics and make data-driven decisions.

-   **[Improved remediation target date handling](https://servicenow-staging.fluidtopics.net/access?context=sem-recalculate-rt-date&family=zurich&ft:locale=en-US)**

Remediation target \(RT\) dates now dynamically recalculate when a finding’s risk rating changes. When enabled, the system recalculates the SLA from the most recent risk rating update date, preventing RT dates from being set in the past and ensuring accurate SLA tracking.

-   **[Exception management configuration](https://servicenow-staging.fluidtopics.net/access?context=sem-configure-exp-mngmt-vr&family=zurich&ft:locale=en-US)**
    -   Manual and automated exception request and approval workflow: Flexible, customizable workflows streamline submission, review, and approval of exception requests.
    -   Comprehensive exception tracking and audit trails: Detailed records of approvals, justifications, and timelines support compliance efforts and simplify regulatory reporting.
-   **Consistent remediation task management with [remediation views](https://servicenow-staging.fluidtopics.net/access?context=sem-workspaces-ui-remediation-module&family=zurich&ft:locale=en-US) and [centralized findings configuration](https://servicenow-staging.fluidtopics.net/access?context=sem-configure-rules-manage-findings&family=zurich&ft:locale=en-US)**

Unified task management: Supports both manual task creation and automated rule-based task generation across all Unified Security Exposure Management applications.

Centralized rule definition: Enables efficient management of tasks across Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance applications.

-   **[Advanced risk management](https://servicenow-staging.fluidtopics.net/access?context=sem-vuln-calc-define-risk-rule-fields&family=zurich&ft:locale=en-US)**

Risk calculators: Introduced for all Unified Security Exposure Management applications, enabling definition of risk rules based on multiple factors and calculation mechanisms.

Risk rollup calculators: Aggregate scores from findings to higher-level entities, ensuring consistent risk scoring across applications.

-   **[Generate Recommendation](https://servicenow-staging.fluidtopics.net/access?context=sem-approval-recommendation-skill&family=zurich&ft:locale=en-US)**

AI-powered recommendations for Exception and False Positive requests: Provides an on-demand recommendation to approve or reject a request using the Now Assist skill framework to analyze contextual data such as vulnerability details, risk factors, exploit availability, and related indicators. The recommendations are accessible directly from the Exception Change Approval record in the Security Exposure Management Workspace, enabling approvers to make faster, more consistent decisions while reducing the manual analysis effort.

-   **Exception Rule &amp; Change Approval Enhancements**
    -   [Change Approval Creation for Exception Rule submission](https://servicenow-staging.fluidtopics.net/access?context=sem-exception-rules-overview&family=zurich&ft:locale=en-US): Previously, Change Approval \(CA\) was created only for a few types of exception requests. Now, the Change Approval\(CA\) is also created during exception rule submission. This enhancement verifies consistency across exception workflows and improves traceability.
    -   [Vulnerability Intelligence Tile on Change Approval Record](https://servicenow-staging.fluidtopics.net/access?context=sem-configure-approval-view&family=zurich&ft:locale=en-US): The Vulnerability Intelligence Tile is added to change approval records, displaying vulnerability intelligence such as CISA KEV information, Known ransomware indicators, and EPSS percentile. This tile is visible only when the Intelligence and App-Vuln NVD plugins are installed. This enhancement provides approvers with the critical threat context for informed decision-making.
    -   [Summary Tiles on Change Approval Record](https://servicenow-staging.fluidtopics.net/access?context=sem-configure-approval-view&family=zurich&ft:locale=en-US): The Impact Tile is added in the overview tab of the Change Approval record to provide approvers with the visibility of the impacted count information such as, Impacted CIs, Total Findings, and Total Vulnerabilities on the Change Approval for a Remediation Task. This enhancement improves visibility of potential impact during approval or rejection of requests.
    -   [Application-Based Filtering on Approvals View](https://servicenow-staging.fluidtopics.net/access?context=sem-configure-approval-view&family=zurich&ft:locale=en-US): Added filtering capability on the Approvals view by application type such as: Application vulnerabilities \(AVR\), Container vulnerabilities \(CVR\), Infra Vulnerabilities \(VR\), and Misconfigurations \(CC\). This capability enables approvers to quickly drill down and manage approvals by category.
    -   [Reapply Assignment Rules for Deferred and Manually Assigned Items](https://servicenow-staging.fluidtopics.net/access?context=sem-reapply-assignment-rules&family=zurich&ft:locale=en-US): Introduced the ability to reapply assignment rules for Deferred items and Manually assigned items. This enhancement provides the flexibility to reassign items through the Re-evaluate action in the list view.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Unified Security Exposure Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Unified Security Exposure Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Unified Security Exposure Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Unified Security Exposure Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Unified Security Exposure Management is a ServiceNow AI Platform feature that is available with activation of the Security Exposure Management \(com.snc.security\_support.core\). For details, see [Install Unified Security Exposure Management](https://servicenow-staging.fluidtopics.net/access?context=sem-install-and-configure&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Unified Security Exposure Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Unified Security Exposure Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Unified Security Exposure Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Unified Security Exposure Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Unified Security Exposure Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   Experience a standardized data model and modular workflows for Vulnerability Response applications with Unified Security Exposure Management. This transformation and architectural design ensures consistent features across all modules, simplifies configuration, and enables flexible, role-based experiences. The modular approach allows faster updates and seamless integration, creating a scalable and future-ready platform.
-   Manage security exposures with Findings and Remediation views with a centralized platform in the Security Exposure Management Workspace.
-   Configure all USEM apps, including rules, email templates, email notifications, and severity mapping for integrations with the Administration console.
-   Enhanced exception management: Streamlined exception request and approval workflows with comprehensive tracking and audit trails.
-   Use generative AI with features in the SEM workspace that are included with the Now Assist for Vulnerability Response application. See the [Now Assist for Security Incident Response \(SIR\) release notes](https://servicenow-staging.fluidtopics.net/access?context=secops-now-assist-security-operations-rn&family=zurich&ft:locale=en-US) for more information.

 See [Unified Security Exposure Management](https://servicenow-staging.fluidtopics.net/access?context=unified-security-exposure-management-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

