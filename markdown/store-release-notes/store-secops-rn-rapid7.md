---
title: Rapid7 Integration for Security Operations release notes
description: Version history for the Rapid7 Integration for Security Operations on the ServiceNow Store .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-rapid7.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 8
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Rapid7 Integration for Security Operations release notes

Version history for the Rapid7 Integration for Security Operations on the ServiceNow Store .

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.3.2 - June 2026 \(USEM\)**

    Changed: Improved access control reliability and maintainability in Vulnerability Intelligence.

-   **Version 13.17.3 - June 2026 \(USEM\)**

    Fixed: Fixed an issue where the solution and solution summary fields on detection records were not updated after the initial creation.

-   **Version 30.3.0 - April 2026 \(USEM\)**

    Fixed: Resolved an issue where the Rapid7 scan engine lookup could fail with an error when scan engine parameters were not available for a source instance.

-   **Version 30.3.1 - April 2026 \(USEM\)**

    Fixed: Resolved an issue where Rapid7 scan engine lookup failed when scan engine parameters were unavailable for a source instance.

-   **Version 13.17.0 - January 2026**

    Changed: Detection creation now supports cmdb\_ci as the uniqueness attribute instead of asset\_id, providing greater flexibility in detection handling.

-   **Version 30.2.0 - January 2026 \(USEM\)**

    Changed: Detection creation now supports cmdb\_ci as the uniqueness attribute instead of asset\_id, providing greater flexibility in detection handling.

-   **Version 13.16.4 - December 2025**

    Fixed: Resolved an issue where new vulnerabilities from Rapid7 with multiple UUID values were not consistently parsed into ServiceNow, resulting in only a single UUID being captured. All UUID values are now parsed correctly.

-   **Version 13.15.1 - May 2025**

    Fixed: The Rapid7 Resolution integration timing out due to exclusion rules lacking a sys\_id has been resolved.

-   **Version 13.14.0 - November 2024**

    Fixed: Minor fixes for this release.

-   **Version 13.13.0 - June 2024**

    New: The execution of the Rapid7 Vulnerable Item Integration also accounts for the number of detections excluded with the application of exclusion rules.

-   **Version 13.12.5 - June 2024**

    Fixed: Minor fixes included in this release.

-   **Version 13.12.2 - May 2024**
    -   Changed:
        -   Solutions created by Rapid7 Integrations are no longer queued for processing. Instead, update\_status flag on solutions is marked as true when remediation status metrics need to be updated.
        -   Rapid7 Integration instance is populated on the solutions created by Rapid7.
        -   If the newly introduced "vuln\_comp" integration instance parameter is set to true, Rapid7 third-party vulnerabilities integration pulls all the vulnerabilities every Sunday.
-   **Version 13.11.2 - March 2024**
    -   Fixed:
        -   For the solutions created by Rapid7, the value populates as Scanner in the Category field.
        -   Solutions will now be created from Rapid7 InsightVM using the solution\_id sent by the scanner. This functionality will persist even if any of thesolution\_summary, solution\_fix, orsolution\_type fields are empty.
-   **Version 13.11.1 - February 2024**
    -   Changed: Provision to pass engine IDs for Rapid7 rescan.
    -   Fixed:
        -   The source\_risk\_score field of the vulnerable items gets updated during the Rapid7 integration run.
        -   The site name is not truncated when we run the rapid7 site integration if the character size is more than 40.
-   **Version 13.10.1 - November 2023**
    -   Changed:
        -   Revised CI Lookup rules to validate all CI lookup rules for cloud assets reported by Rapid7.
        -   A system property is created to set the CI class for unmatched cloud assets. This allows users to set unclassed hardware for unmatched cloud assets.
    -   These changes will help to ensure that all cloud assets are properly tracked and managed, which is essential for maintaining a secure and compliant cloud environment.
-   **Version 13.9.1 - September 2023**

    New: Starting with V13.9, vulnerability solutions are ingested with the Rapid7 Data Warehouse Integration and associated with vulnerable items.

-   **Version 13.8.2 - August 2023**

    New:

    -   The Rapid7 integration run status dashboard will be displayed in the next generation experience.
    -   Added NIC to the Detection Key for more granularity \(Applicable only for Rapid7 IVM\).
    -   Added a new integration instance parameter for the Rapid7 InsightVM to close the stale detections that are no longer coming through the Rapid7 API for the assets scanned and retrieved through the Rapid7 API via rapid7 comprehensive integration.
    -   Added a new integration instance parameter to set the buffer time for comprehensive integration.
    -   Rescan API requests will fetch the additional details.
-   **Version 13.7.4 - June 2023**

    Fixed: On Discovered items, the CREDENTIAL\_ASSESSMENTS field in the source\_data column now contains all the credentials without any duplicates.

-   **Version 13.7.2 - May 2023**
    -   Fixed:
        -   Earlier, CIs were being continuously removed and associated again based on lookup rules or IRE for cloud discovered items. This issue has now been fixed.
        -   Empty records are no longer being created in the Solution Mapping table for the Rapid7 solution and third-party entries.
-   **Version 13.6.1 - February 2023**
    -   New: A CI Lookup Rule "Cloud Resource ID" has been introduced to match the Cloud CIs based on Cloud Metadata.
    -   Changed:
        -   "Rapid7 Asset List - API" integration now processes the Cloud resource ID information and stores it on the Discovered Item.
        -   The existing default CI lookup rules are modified to include Asset Category not equals Cloud in the condition.
-   **Version 13.5.3 - November 2022**

    New: Proof is supported in the VI key for selected vulnerabilities.

-   **Version 13.4.1 - August 2022**
    -   Fixed: If a parent scan or rescan is successfully completed, times out, or errors out, its child scans are also annotated as expected so their status matches the parent scan or rescan.
    -   New: From your ServiceNow AI Platform instance, without coding or adding additional queries, further refine your imported vulnerability data with parameters that are provided by the Rapid7 InsightVM scanner. The following integrations support filtering by providing JSON content in the request body:
        -   Rapid7 InsightVM Vulnerable item Integration API
        -   Rapid7 InsightVM Vulnerability Integration API
        -   Rapid7 InsightVM Asset List Integration API
-   **Version 13.3.6 - March 2022**
    -   New:
        -   If you subscribe to the license for Vulnerability Solution management application, then the solutions from Rapid7 are populated in the Vulnerability Solution management schema.
        -   With this change, the Rapid7 solutions are now available as preferred solutions on Rapid7 Third-party entry records and the Vulnerable items \(VIs\).
        -   If you do not have the subscription to the Vulnerability Solution management application, then the Rapid7 solutions work as-is.
-   **Version 13.2.0 - February 2022**

    No new features or updates are included with this version. This version ensures that features from the last release are compatible with the San Diego family release.

-   **Version 13.1.1 - October 2021**
    -   Fixed:
        -   After Rapid7 split its US servers into three regions \(United States - 1, United States - 2, and United States - 3\), support for all three servers has been enabled from the Rapid7 configuration page.
        -   A buffer has been added to the ‘Import since’ attribute to ensure that no Rapid7 third-party vulnerabilities are missed when the Rapid7 Vulnerability Integration - API is run daily.
        -   Ignored detection count was earlier reflecting an incorrect count. It has been fixed for the integration process and integration run records.
-   **Version 13.0.2 - June 2021**
    -   New: The rescan option permits remediation owners, analysts, and managers to initiate scans from vulnerability group, vulnerable item, third-party entry \(TPE\), and discovered item records in your Now Platform. Target the scan command from your instance on specific vulnerabilities or configuration items so that you can verify the remediation activity you performed has fixed specific vulnerabilities.
    -   Fixed:
        -   Removed the buffer time between comparison calculations for the Rapid7 InsightVM Vulnerable Item integration to avoid discrepancies in the states of the vulnerabilities.
        -   The Rapid7 Nexpose data warehouse Vulnerability Integration no longer hangs in the "Running" state when no information is returned from the SQL probe.
        -   The "source\_status" attribute is now set correctly on the detections for the Rapid7 InsightVM integration.
-   **Version 12.0.0 - February 2021**
    -   Changed:
        -   Rescans With the updated rescan functionality, initiate scans from the vulnerability group, vulnerability item, third-party entry \(TPE\), and discovered item records.
        -   After the scan completes, view the Qualys scan results on the vulnerability scan record, any vulnerable items that were updated by the scan, and details for any assets that were not reached during scans.
        -   Vulnerability managers can specify that rescans for resolved item are available within certain time windows or only can start at certain times.
-   **Version 11.2.1 - December 2020**

    Fixes.

-   **Version 11.1.0 - November 2020**
    -   New:
        -   Discovery source VR-Rapid7 is created and passed to IRE to create CIs.
        -   New Host Import maps are added for Unclassed Hardware.
        -   Two new CIs, Network Adaptor and IP Address, are created along with the Unclassed Hardware CI.
-   **Version 11.0.0 - October 2020**
    -   New: An optional condition builder has been added to the CI lookup rules that permits you to filter out specific assets in your IT environment. Create filter conditions using the attributes received from the Rapid7 host payload.
    -   Changed:
        -   To limit the number of vulnerable items and import data more efficiently from the Rapid7 InsightVM daily VI integration, when 'Last Assessed for Vulnerabilities' is specified, only scanned assets are imported.
        -   If you choose to close vulnerable items based on 'Assets last scanned' with the Auto-Close Stale vulnerable items module, a completed run from the Rapid7 comprehensive integrations is not required.
        -   Set the 'Run Separately' flag to 'true' to prevent other integrations with this flag also enabled from colliding during scheduled runs. This flag is enabled by default for the Vulnerable Item Integration and Comprehensive Vulnerable Item Integration for Rapid7 Data Warehouse, and the Vulnerable Item Integration - API and Comprehensive Vulnerable Item Integration - API for Rapid7 InsightVM.
-   **Version 10.3.5 - June 2020**
    -   New:
        -   Recertified for version 10.3.5
        -   Comprehensive Vulnerable Item Integration for Rapid7 Nexpose data warehouse. This integration is required for Rapid7 Nexpose data warehouse users who want to enable the Auto-Close Stale Vulnerable Items module.
        -   Comprehensive Vulnerable Item Integration - API for Rapid7 InsightVM. This integration is required for Rapid7 InsightVM users who want to enable the Auto-Close Stale Vulnerable Items module.
        -   For Rapid7 detections, an option is available on the Rapid7 configuration page in your instance to reopen resolved VIs based on age.
    -   Fixed: Vulnerable items set to 'Resolved' in your instance but not transitioned to 'Closed' -'Fixed' by the integration runs are reopened if they are detected during rescans.
-   **Version 10.0.1 - March 2020**
    -   New:
        -   An exponential backoff algorithm for improving the integration process
        -   Rapid7 Integration detections import to avoid de-duplication
        -   Retry for API failures such as timeouts
        -   Asset List Integration for Rapid7 Nexpose Data Warehouse
    -   Changes: Fixes
    -   Upgrade Note: Prior to upgrade to 10.0.1, ensure each of the CI Lookup Rules is Order values is unique. If there are CI Lookup Rules with the same Order value, they may not upgrade correctly. After upgrade, Rapid7 InsightVM lookup rules are assigned new Order values. Rapid7 Data Warehouse Order values remain the same. See KB0786526 for more information.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

