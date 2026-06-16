---
title: Security Exposure Management Workspace release notes
description: Version history for the ServiceNow Security Exposure Management Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-security-exposure-mgmt-ws.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Security Operations Shared apps for release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Exposure Management Workspace release notes

Version history for the ServiceNow® Security Exposure Management Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 30.5.1 - June 2026**
    -   New:
        -   Added an Overview tab for Solutions, Configuration Items, and Remediation Effort records in the Security Exposure Management \(SEM\) Workspace.
        -   Added color coding for risk rating and remediation status to make prioritization faster and easier to assess at a glance.
        -   Added context-based filtering that automatically hides list records and filters not relevant to the current view.
        -   Added the ability for an IT Remediation Owner to manually create a Remediation Task directly from the list view in the SEM Workspace.
    -   Fixed:
        -   Resolved an issue where the Cloud Exposure View page in the SEM Workspace remained stuck on "Loading…" and never rendered.
        -   Improved performance of the unified dashboard by removing redundant queries against findings and feature configuration data.
        -   Added missing accessibility labels for buttons and dropdowns on the SEM Workspace homepage.
        -   Fixed an issue where the page title disappeared when the same dashboard was reselected on the SEM Workspace home page.
        -   Fixed an issue where findings with "Low" and "None" severity were not displaying correctly in the Cloud Workspace.
-   **Version 30.3.1 - April 2026**
    -   New: Create remediation tasks directly from the Remediation Overview page for all finding types including vulnerabilities, application, cloud, and compliance without leaving the Security Exposure Management workspace.
    -   Fixed:
        -   Vulnerability managers and analysts can once again add and remove widgets on out-of-the-box dashboards in the SEM workspace.
        -   Finding counts in charts and widgets now display as whole numbers, without unnecessary decimal values.
        -   Widget sizes no longer expand uncontrollably when filters are changed, preventing counts and labels from overflowing.
        -   Cloud security widget counts now update correctly when a filter is applied and then cleared.
        -   A scroll bar is now properly visible in the findings drill-down list, making it easier to navigate large result sets.
        -   The "Findings by Source" widget on the All Active Findings page now displays data correctly.
        -   Findings and remediation owner views now support custom findings configurations, removing a dependency on hardcoded references.
        -   Display and data rendering issues across multiple views in the Cloud Security workspace have been resolved.
        -   Chart and color-coding display issues in the SEM workspace under the Japanese locale have been resolved.
    -   Changed: Ingestion performance in the Security Exposure workspace has been improved by reducing redundant processing during data loads.
-   **Version 30.2.2 - January 2026**
    -   **Note:** This app version is intended for Unified Security Exposure Management \(USEM\), a significant architectural upgrade to the Vulnerability Response applications. If you are currently using Vulnerability Response and upgrading to USEM for the first time, you must use the Migration assistant for Unified Security Exposure Management to ensure a safe and successful upgrade. If you do not intend to upgrade to USEM, please select a version below 30.x when installing or upgrading.

    -   The Security Exposure Management Workspace application delivers a single, comprehensive Security Exposure Management \(SEM\) Workspace tailored to each security role—Vulnerability Admins, Vulnerability Analysts, Remediation Owners, and Approvers.
    -   Vulnerability Analysts benefit from the Findings View, which provides comprehensive visibility across all exposure types, along with powerful dashboard creation and configuration capabilities. Remediation Owners can work flexibly byRemediation Tasks, Findings, or Assets, with prioritisation tools to focus on the most critical issues.
    -   The Admin Console centralises configuration and administration for all USEM applications, eliminating the need to navigate multiple modules and ensuring consistent settings across the environment.

**Parent Topic:**[ServiceNow Store - Security Operations Shared apps for release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-shared.md)

