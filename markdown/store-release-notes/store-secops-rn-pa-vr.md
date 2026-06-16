---
title: Performance Analytics for Vulnerability Response release notes
description: Version history for the Security Operations Performance Analytics for Vulnerability Response on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-pa-vr.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Performance Analytics for Vulnerability Response release notes

Version history for the Security Operations Performance Analytics for Vulnerability Response on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.2.1 - June 2026 \(USEM\)**
    -   New: Added localization support for Performance Analytics dashboard chart titles.
    -   Changed: Improved protection and validation for read-only Performance Analytics fields to strengthen security compliance and improve maintainability.
    -   Fixed: Fixed an issue in read-only field validation that could cause incorrect row indexing during processing.
-   **Version 12.17.0 - June 2026**

    Fixed: Resolved an issue where Performance Analytics dashboard chart titles and filter labels were not translated correctly for non-English languages. Localized text now renders properly across dashboard visualizations and filter components.

-   **Version 30.1.1 - April 2026 \(USEM\)**

    Fixed: An error where installing the Vulnerability Analytics plugin caused Performance Analytics indicators to fail due to a missing "Remediation Target Status \(Closed\)" breakdown.

-   **Version 12.16.2 - April 2026**

    Fixed: An error where installing the Vulnerability Analytics plugin caused Performance Analytics indicators to fail due to a missing "Remediation Target Status \(Closed\)" breakdown.

-   **Version 12.16.1 - December 2025**

    Fixed: Enhanced the application's Access Control List \(ACL\) security for the application by removing admin override checks from multiple ACLs.

-   **Version 12.16.0 - August 2025**

    Fixed: Localization improvements for the CISO dashboard.

-   **Version 12.15.9 - May 2025**

    Minor fixes for this release.

-   **Version 12.15.4 - November 2024**

    Changed: Age-based Performance Analytics \(PA\) reports have been updated to include support for configurable age calculation.

-   **Version 12.14.1 - August 2024**

    Fixed: Translations of titles and labels in the dashboards of Vulnerability Manager workspaces.

-   **Version 12.13.5 - June 2024**
    -   Removed: Deprecated the following dashboards:
        -   Application Vulnerability Management
        -   Vulnerability Management \(PA\)
        -   My Application Vulnerabilities
        -   Container Vulnerability Management
        -   CISO Dashboard
-   **Version 12.13.4 - May 2024**

    Minor fixes for this release.

-   **Version 12.12.2 - February 2024**
    -   New: Added updates to the jobs and indicators to support the Cybersecurity Executive Dashboard.
    -   Fixed:
        -   The rendering issue in the Application Vulnerabilities dashboard for app-sec-manager and security champion role.
        -   Performance issues for the PA jobs.
-   **Version 12.10.3 - January 2024**

    New: Created and updated the PA indicators to support benchmarking metrics.

-   **Version 12.10.2 - November 2023**

    Fixed: Minor fixes for this release.

-   **Version 12.9.3 - August 2023 \(Vancouver\)**

    New:

    -   The following dashboards are now available in the Next Experience UI:
        -   Container Vulnerability Management Overview
        -   Vulnerability Management \(PA\)
        -   CISO Dashboard
        -   Application Vulnerability Management
-   **Version 12.8.1 - May 2023**

    Fixed: The scheduled job ""Update Vulnerable Item CI Class"" is no longer consuming high database CPU or load.

-   **Version 12.6.1 - February 2023**

    Fixed: The overview module for the Application Vulnerability Response dashboard displays as expected.

-   **Version 12.5.0 - November 2022**

    Minor fixes for this release.

-   **Version 12.4.3 - August 2022**

    New: The report\_view access control lists \(ACLs\) that govern who can see reports in dashboards and elsewhere are enabled by default in the Tokyo release.

-   **Version 12.4.1 - March 2022**

    New: The Overview tab on Vulnerability Management \(PA\) dashboard and the Remediation tab of the CISO dashboard display patch update data if the Patch Orchestration application and a supported patch vendor integration are installed.

-   **Version 12.3.0 - February 2022**

    No new features or updates are included with this version. This version ensures that features from the last release are compatible with the San Diego family release.

-   **Version 12.1.0 - October 2021**
    -   New: Reports that support the Penetration Testing assessment
    -   Changed: Replaced assignment group-related reports with a standard report for performance improvement in the Vulnerability Management Performance Analytics \(PA\) Dashboard. You have the option to add any reports back to the dashboard at any time.
-   **Version 12.0.6 - June 2021**
    -   Fixed:
        -   The Top 10 exploits are now populated as expected.
        -   Translation issue with "Countries with Most Vulnerabilities" widget.
        -   Missing demo data for the "Top 10 Assignment Groups with Lowest Remediation Target Adherence" widget.
-   **Version 12.0.4 - February 2021**
    -   New:
        -   CISO dashboard: The dashboard helps executives understand the efficacy of their vulnerability management programs. The dashboard provides Key Performance Metrics \(KPIs\), areas that have the highest risk, and reports along with recommendations for lowering risk.
        -   Define Service classifications for Performance Analytics: Configure the kinds of service CIs to include in the business service scorecard reports in the Performance Analytics dashboards.
        -   Filter the Application Vulnerability Response PA Dashboard reports based on key attributes.
        -   Security Champion dashboard, My Application Vulnerabilities, in Application Vulnerability Response.
-   **Version 11.0.0 - October 2020**

    New: Visually display all of your application vulnerable item activity with reports organized by tabs on the dashboard.

-   **Version 10.3.1 - June 2020**

    New: Recertified for version 10.3.1

-   **Version 10.0.3 - March 2020**
    -   New:
        -   Recertified for Orlando.
        -   Added a preconfigured method of reporting that permits you to view data on certain reports in real time.
        -   Added a Distinct Vulnerabilities indicator that determines how many third-party vulnerabilities have at least one corresponding VI.
    -   Changed:
        -   Improved speed and memory consumption of PA data collection jobs.
        -   Increased the preconfigured limits on all indicator sources, including active VIs, vulnerable CIs, and assignment groups.
        -   Adjusted Collect Records settings and second-level breakdowns for improved performance.
-   **Version 9.0.1 - November 2019**

    New: Certified for New York.

-   **Version 8.0.10 - June 2019**

    Refer to [Vulnerability Response release notes](https://www.servicenow.com/docs/bundle/madrid-release-notes/page/release-notes/security-operations/secops-vuln-resp-rn.html) for product changes and updates in the Madrid release.


