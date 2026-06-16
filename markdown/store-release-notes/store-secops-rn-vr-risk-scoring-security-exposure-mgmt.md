---
title: Risk Scoring for Security Exposure Management release notes
description: Version history for the ServiceNow Risk Scoring for Security Exposure Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-risk-scoring-security-exposure-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Risk Scoring for Security Exposure Management release notes

Version history for the ServiceNow® Risk Scoring for Security Exposure Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 30.1.5 - June 2026**

    Fixed: Resolved an issue where remediation tasks were not assigned the correct risk rating based on the configured weights. Risk ratings on the Vulnerability table now accurately reflect the configured weight settings.

-   **Version 30.1.4 - March 2026**

    Fixed: Moved the Run Severity Calculator background job and related scripts to the Vulnerability Response application, removing the Security Support Common dependency from Risk Scoring in the Security Exposure Management application.

-   **Version 30.1.3 - January 2026**
    -   **Note:** This app version is intended for Unified Security Exposure Management \(USEM\), a significant architectural upgrade to the Vulnerability Response applications. If you are currently using Vulnerability Response and upgrading to USEM for the first time, you must use the Migration assistant for Unified Security Exposure Management to ensure a safe and successful upgrade. If you do not intend to upgrade to USEM, please select a version below 30.x when installing or upgrading.

    -   The Risk Scoring for Security Exposure Management application delivers unified risk scoring capabilities across all Unified Security Exposure Management \(USEM\) applications.
    -   Administrators can define Risk Calculators and Risk Rules in the Security Exposure Management \(SEM\) Workspace to consistently evaluate exposure findings based on configurable factors. Risk scoring can be configured across infrastructure, application, container, and configuration compliance findings to ensure consistent prioritisation.
    -   With Risk Rollup Calculators, scores can be aggregated from individual findings to higher-level entities, such as Remediation Tasks, Assets, Vulnerability Items, and Configuration Tests, providing teams with a clear view of risk at every level.

**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

