---
title: Vulnerability Response Integration with NVD release notes
description: Version history for the Vulnerability Response Integration with NVD on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-nvd.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration with NVD release notes

Version history for the Vulnerability Response Integration with NVD on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.3.1 - June 2026**
    -   Changed:
        -   Admin console UI changes.
        -   Migrated query access control definitions in National Vulnerability Database \(NVD\) to the standard product codebase, ensuring consistent access control enforcement.
-   **Version 30.3.0 - April 2026 \(USEM\)**
    -   Fixed: The Common Vulnerability Scoring System \(CVSS\) V4 score mapping to align with the latest NVD API response structure.
    -   Changed: Added the no\_audit\_delete attribute to the NVD CPE key \[sn\_vul\_nvd\_cpe\_key\] table.
-   **Version 1.7.4 - April 2026**
    -   Fixed: The Common Vulnerability Scoring System \(CVSS\) V4 score mapping to align with the latest NVD API response structure.
    -   Changed: Added the no\_audit\_delete attribute to the NVD CPE key \[sn\_vul\_nvd\_cpe\_key\] table.
-   **Version 1.7.1 - August 2025**

    New: Create assessments without explicitly creating CPEs using the Version Range information that the National Vulnerability Database \(NVD\) provides.

-   **Version 1.6.1 - May 2025**

    Changed: The 'Source' column in the reference table and the CPE field should be populated with 'NVD'. If any changes occur, only the CPE and references marked with the source 'NVD' should be deleted.

-   **Version 1.5.3 - December 2024**

    Minor fixes for this release.

-   **Version 1.5.1 - November 2024**

    New: The National Vulnerability Database \(NVD\) now includes entries for the Common Vulnerability Scoring System \(CVSS\) score 4.0 values.

-   **Version 1.4.5 - May 2024**

    Fixed: The NVD integration has been fixed to utilize the secondary CVSS score when primary CVSS score is unavailable.

-   **Version 1.4.3 - February 2024**

    Changed: CVSS3.0 will be considered for processing if CVSS3.1 is not present in the NVD response.

-   **Version 1.4.2 - November 2023**

    Fixed: Updated unmapped integration to use the cpesearch Rest Endpoint API so that the number of API calls are reduced to NVD for associating software with NVD entry if the NVD entry exists.

-   **Version 1.3.3 - August 2023 \(Vancouver\)**
    -   New:
        -   Created the following integrations to use NVD API 2.0 version.
        -   NIST National Vulnerability Database Integration - API \(CPE only\). This integration fetches CPEs.
        -   NIST National Vulnerability Database Integration - API \(Unmapped CPE\). This integration maps CPEs with the CVEs.
    -   Changed: Deprecated existing integration i.e NIST National Vulnerability Database Integration - API \(CVE and CPE\).
-   **Version 1.2.0 - May 2022**

    New: Added support for using API keys for calling NVD endpoints.


-   **Version 1.1.0 - October 2021**
    -   Changed:
        -   Modifications to support changes to the CPE APIs done by NIST. These changes restrict CPE APIs by limiting date ranges to 120 days.
        -   When you enter a start or end date for the optional parameters, you need to provide both the start and end dates.
-   **Version 1.0.3 - June 2021**

    Fixed: The "source" attribute is populated in the Third-party entry table for NVD records. Vulnerable Software records from NVD are available as expected.

-   **Version 1.0.0 - February 2021**
    -   New:
        -   Initial release.
        -   Two NVD integrations that import the CVEs and CPEs information from the NIST National Vulnerability Database \(NVD\).

