---
title: Administration for Security Exposure Management release notes
description: Version history for the ServiceNow Administration for Security Exposure Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-admin-security-exposure-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Administration for Security Exposure Management release notes

Version history for the ServiceNow® Administration for Security Exposure Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 30.5.0 - June 2026**
    -   Fixed:
        1.  Resolved an issue where assignment rules could be created without completing all mandatory fields, ensuring validation is enforced during rule creation.
        2.  Resolved a duplicate key error caused by a script conflict that prevented records from being inserted.
        3.  Resolved an issue in Configuration Compliance where the time-to-remediate evaluation was not accounting for the configured TTR start date field when reapplying remediation target rules.
-   **Version 30.2.1 - April 2026**

    Minor enhancements.

-   **Version 30.1.5 - March 2026**

    Fixed: Moved "Run severity calculator after vuln entry promotion" scheduled job to Vulnerability Response application to remove Security Support Common dependency from Risk Scoring for Security Exposure Management application.

-   **Version 30.1.4 - January 2026**
    -   **Note:** This app version is intended for Unified Security Exposure Management \(USEM\), a significant architectural upgrade to the Vulnerability Response applications. If you are currently using Vulnerability Response and upgrading to USEM for the first time, you must use the Migration assistant for Unified Security Exposure Management to ensure a safe and successful upgrade. If you do not intend to upgrade to USEM, please select a version below 30.x when installing or upgrading.

    -   The Administration for Security Exposure Management application provides a unified administrative experience across all Unified Security Exposure Management \(USEM\) applications.
    -   It introduces the Admin Console within the Security Exposure Management \(SEM\) Workspace, enabling administrators to configure all SEM apps and monitor integrations from a single location.

**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

