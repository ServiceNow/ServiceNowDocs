---
title: Vault Console release notes
description: Version history for the Vault Console application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-plat-sec-rn-vault-console.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - ServiceNow AI Platform Security version history release notes, ServiceNow Store version history release notes]
---

# Vault Console release notes

Version history for the Vault Console application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.0 - September 2026**
    -   New:
        -   Insights, an AI-generated summary of your data security posture, at the top of the Vault Console home page, covering data discovery, classification, and data protection, with a recommended next step for each area
        -   Code signing activity metrics in Vault Console, tracking create, update, and delete operations on code signing enabled records over the past week, and showing which tables hold the most such records
        -   Log Export Service export monitoring widget, showing total data exported over the past six months, the topics that export the most data, and the data exported by each topic so far in the current month
        -   ServiceNow Vault in Admin Home. Instances with a ServiceNow Vault entitlement show a ServiceNow Vault tile, where an administrator can install Vault Suite and then open Vault Console from the Configuration Console
        -   Default step-up authentication policies for Zero Trust Access, applied automatically when you install Zero Trust Access with ServiceNow Vault, and reviewable at any time from Vault Console
        -   Email notification when ServiceNow Vault onboarding completes on your instance
    -   Changed: Default policies provisioned for field encryption, data privacy, Zero Trust Access, and Log Export Service are now prefixed with Vault by Default, so you can distinguish policies that ServiceNow provisioned from policies your organization created
-   **Version 2.2.9 - August 2026**
    -   The security\_admin role has been removed from the roles required to elevate to and administer Vault Console. All administrative tasks including that of viewing tools metrics across the dashboard is now available to the sn\_vault\_console.vault\_console\_admin. This change was made to conform with the principle of least privilege, ensuring administrators only elevate to roles they actually need.
    -   UI fixes to ensure interface elements are displayed according to entitlement settings.
-   **Version 2.1.0 - June 2026**

    This release advances Vault Console’s AI‑driven data protection by combining automatic classification and protection of custom applications and tables with continuous AI insights that surface sensitive data appearing in non‑protected channels. Together, these capabilities help customers proactively discover and secure sensitive data—including custom-built workloads—while maintaining development agility and system performance. AI-assisted workflows reduce manual effort by recommending classifications and protections, while integrated monitoring highlights potential data leakage risks in real time, all within a unified, enterprise-ready Vault experience with role-based controls, auditability, and licensing governance.

-   **Version 1.1.1 - May 2026**
    -   Manage and monitor cloud encryption metrics.
    -   Explore more detail for each metric in Vault console with View more data links.
    -   Get AI guidance with the Ask Now Assist panel in Vault console.
-   **Version 2.0.0 - March 2026**

    This release advances Vault Console’s AI‑driven data protection by combining automatic classification and protection of custom applications and tables with continuous AI insights that surface sensitive data appearing in non‑protected channels. Together, these capabilities help customers proactively discover and secure sensitive data—including custom-built workloads—while maintaining development agility and system performance. AI-assisted workflows reduce manual effort by recommending classifications and protections, while integrated monitoring highlights potential data leakage risks in real time, all within a unified, enterprise-ready Vault experience with role-based controls, auditability, and licensing governance.

-   **Version 1.1.0 - December 2025**
    -   New:
        -   Manage and monitor cloud encryption metrics.
        -   Explore more detail for each metric in Vault console with View more data links.
        -   Get AI guidance with the Ask Now Assist panel in Vault console.
-   **Version 1.0.0 - August 2025**
    -   Vault Console is an application that seamlessly integrates and automatically installs all plugins included in the ServiceNow Vault subscription.
    -   It empowers organizations to efficiently auto-classify sensitive data within workflows, such as Financial Services Operations \(FSO\) and Customer Service Management \(CSM\).

**Parent Topic:**[ServiceNow Store - ServiceNow AI Platform Security version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-sec.md)

