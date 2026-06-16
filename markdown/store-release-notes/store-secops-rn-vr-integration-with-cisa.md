---
title: Vulnerability Response Integration with CISA release notes
description: Version history for the Security Operations Vulnerability Response Integration with CISA application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-integration-with-cisa.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration with CISA release notes

Version history for the Security Operations Vulnerability Response Integration with CISA application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.7.0 - June 2026 \(USEM\)**

    Changed: Migrated query access control definitions in Vulnerability Intelligence to the standard product codebase, ensuring consistent access control enforcement.

-   **Version 30.2.1 - April 2026 \(USEM\)**
    -   New: Added support for Exploit Prediction Scoring System \(EPSS\) and Known Exploited Vulnerabilities \(KEV\) data sources to improve vulnerability data enrichment.
    -   Changed:
        -   Exploit Prediction Scoring System \(EPSS\) API processing now uses the Common Vulnerability Data \(CVD\) utility for more reliable record creation and updates.
        -   Vulnerability entry fields are now managed centrally, removing the need for local overrides.
        -   The CISA transform script now validates import queue entries before processing.
-   **Version 1.5.1 - August 2025**

    Fixed: Resolved an issue where the Exploit Prediction Scoring System \(EPSS\) integration was not calculating or retrieving correct delta values between scoring updates. Delta calculations during data synchronization are considering changes between current and previous EPSS scores.

-   **Version 1.5.0 - November 2024**

    Fixed: Minor fixes for this release.

-   **Version 1.4.1 - February 2024**

    Changed: Combined and converted 4 single score tiles to a pie chart for host vulnerable items, which are external facing by risk rating.

-   **Version 1.3.1 - December 2023**

    The Vulnerability Response integration with the CISA Known Exploited Vulnerabilities \(KEVs\) catalog ingests data to help you effectively prioritize and remediate these vulnerabilities.

-   **Version 1.2.4 - August 2023 \(Vancouver\)**

    Changed: Made dictionary changes by moving the due\_date and cisa\_exists columns to NVD scope.

-   **Version 1.2.1 - March 2023**
    -   Changed:
        -   "CISA Exists" column label on sn\_vul\_entry has been changed to "CISA KEV \(BOD 22-01\)".
        -   Whenever the value in "CISA KEV \(BOD 22-01\)" changes, the vulnerability entry is flagged for recalculating the risk score on its associated VITs.
-   **Version 1.2.0 - February 2023**
    -   Changed:
        -   "CISA Exists" column label on sn\_vul\_entry has been changed to "CISA KEV \(BOD 22-01\)".
        -   Whenever the value in "CISA KEV \(BOD 22-01\)" changes, the vulnerability entry is flagged for recalculating the risk score on its associated VITs.
-   **Version 1.0.0 - August 2022**

    The Vulnerability Response integration with the CISA Known Exploited Vulnerabilities \(KEVs\) catalog ingests data to help you effectively prioritize and remediate these vulnerabilities.


