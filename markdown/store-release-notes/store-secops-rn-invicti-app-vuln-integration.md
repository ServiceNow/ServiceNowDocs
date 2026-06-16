---
title: Invicti Application Vulnerability Integration release notes
description: Version history for the Invicti Application Vulnerability Integration application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-invicti-app-vuln-integration.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Invicti Application Vulnerability Integration release notes

Version history for the Invicti Application Vulnerability Integration application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.1.3 - April 2026 \(USEM\)**
    -   Fixed:
        -   Fixed Invicti Configuration Page cross-scope credentials saving issue. You'll now receive a warning when opening Invicti configurations page from a scope different than the one associated with the Invicti account. This ensures scope alignment before accessing sensitive configuration data. Additionally, an error displays if you attempt to save credentials from a mismatched scope, preventing potential security misconfigurations.
        -   Fixed warning messages in Invicti Application Vulnerable Item Integration caused by populating a threat field that does not exist in the Application Vulnerable Item table.
-   **Version 1.2.1 - November 2024**

    Changed: Improvements to support a date format that you can specify from the Invicti configuration screen in your ServiceNow AI Platform instance.

-   **Version 1.1.1 - May 2024**

    Changed: View details such as total processing times, average times for pre- and post-integration run processes, and reports on the integration run records.

-   **Version 1.0.2 - February 2024**

    Vulnerability Response Integration with Invicti imports applications and application vulnerabilities using Application Vulnerability Response. Application Vulnerability Response is a feature in Vulnerability Response that helps you prioritize and remediate application vulnerabilities.


