---
title: Qualys Integration for Security Operations release notes
description: Version history for the Qualys Integration for Security Operations on the ServiceNow Store .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-qualys-integration.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 13
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Qualys Integration for Security Operations release notes

Version history for the Qualys Integration for Security Operations on the ServiceNow Store .

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.6.0 - June 2026 \(USEM\)**
    -   Changed: Optimized the default Qualys Cloud Platform integration settings by reducing the host truncation limit from 500 to 300 for greater stability, and increasing the KnowledgeBase backfill limit from 100 to 300 for faster processing.
    -   Fixed:
        -   Removed the deprecated API endpoint from the Qualys integration for Security Operations. The integration now uses only supported API endpoints.
        -   Security fixes.
-   **Version 12.22.3 - June 2026**

    Fixed: Removed the deprecated API endpoint from the Qualys integration for Security Operations. The integration now uses only supported API endpoints.

-   **Version 30.3.1 - April 2026 \(USEM\)**
    -   Changed:
        -   Updated the QVS–CVDB API integration to prevent incorrect creation of Qualys IDs in the Common Vulnerability Database \(CVDB\) table.
        -   Added CVDB configuration support to the Qualys integration setup page, enabling administrators to manage Common Vulnerability Database settings directly.
        -   Removed the unused MITRE details parameter from the Qualys Vulnerability Detection host detection integration to streamline data ingestion.
        -   Extended CVSS v4 score mappings in the Qualys KnowledgeBase and KnowledgeBase Backfill integrations to support additional scoring attributes, ensuring more complete CVSS v4 data for accurate risk prioritization.
        -   Updated the Qualys setup page to use the latest REST messages, REST functions, and HTTP parameters, improving compatibility with the current Qualys API.
        -   Added support for configuring the vulnerability detection source in the Qualys Vulnerability Detection integration, allowing administrators to control how scan data is sourced during imports.
        -   Added a new Comprehensive PCRS integration that consolidates Policy Compliance Reporting Service host data and test results into a single integration, providing a unified view of compliance posture.
        -   Updated the Qualys PC Policies and PC Policies Detail integrations to align with the latest Qualys Policy Compliance API, ensuring policy configuration data is imported accurately and completely.
        -   Updated the Qualys PC Controls integration to support recent Qualys API changes and improve control-level data imports.
        -   Updated the Qualys Host List integration to align with the latest Qualys API and ensure complete host asset data import.
        -   Updated Integration Run Reports to use theme-aware colors instead of hardcoded values for improved UI consistency.
    -   Fixed:
        -   Fixed Qualys KnowledgeBase import to correctly remove CVE-to-QID associations when the scanner source no longer reports that relationship, preventing stale mappings.
        -   Resolved multiple issues in the Qualys Vulnerability Score \(QVS\) integration that caused import processing errors and prevented QVS scores from appearing correctly on vulnerability records.
-   **Version 12.21.1 - April 2026**
    -   Changed:
        -   Removed the unused MITRE details parameter from the Qualys Vulnerability Detection host detection integration to streamline data ingestion.
        -   Extended CVSS v4 score mappings in the Qualys KnowledgeBase and KnowledgeBase Backfill integrations to support additional scoring attributes, ensuring more complete CVSS v4 data for accurate risk prioritization.
        -   Updated the Qualys setup page to use the latest REST messages, REST functions, and HTTP parameters, improving compatibility with the current Qualys API.
        -   Added support for configuring the vulnerability detection source in the Qualys Vulnerability Detection integration, allowing administrators to control how scan data is sourced during imports.
        -   Added a new Comprehensive PCRS integration that consolidates Policy Compliance Reporting Service host data and test results into a single integration, providing a unified view of compliance posture.
        -   Updated the Qualys PC Policies and PC Policies Detail integrations to align with the latest Qualys Policy Compliance API, ensuring policy configuration data is imported accurately and completely.
        -   Updated the Qualys PC Controls integration to support recent Qualys API changes and improve control-level data imports.
    -   Fixed:
        -   Fixed Qualys KnowledgeBase import to correctly remove CVE-to-QID associations when the scanner source no longer reports that relationship, preventing stale mappings.
        -   Resolved multiple issues in the Qualys Vulnerability Score \(QVS\) integration that caused import processing errors and prevented QVS scores from appearing correctly on vulnerability records.
-   **Version 30.3.0 - March 2026 \(USEM\)**
    -   Changed:
        -   Upgraded Qualys Integration to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations.
        -   The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data.
        -   Use the new posture\_api\_version integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.
    -   Fixed:
        -   Qualys PC Results and Qualys Comprehensive PC Results now use separate REST messages, with previously hardcoded values moved into the REST messages. This gives you greater granularity with REST parameters.
        -   The qvs\_score field in the Third-party entry table now supports QVS score population for all vulnerability types.
        -   Qualys QVS Score Integration now supports delta ingestion with pagination. Integration run records display processing statistics such as total imported, created, updated, and ignored records. This update also improves error handling, scalability, and multi-instance support.
        -   The description text for the "max\_backfill\_qid" integration instance parameter has been clarified.
-   **Version 12.21.0 - March 2026**
    -   Changed:
        -   Upgraded Qualys Integration to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations.
        -   The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data.
        -   Use the new posture\_api\_version integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.
    -   Fixed:
        -   Qualys PC Results and Qualys Comprehensive PC Results now use separate REST messages, with previously hardcoded values moved into the REST messages. This gives you greater granularity with REST parameters.
        -   The qvs\_score field in the Third-party entry table now supports QVS score population for all vulnerability types.
        -   Qualys QVS Score Integration now supports delta ingestion with pagination. Integration run records display processing statistics such as total imported, created, updated, and ignored records. This update also improves error handling, scalability, and multi-instance support.
        -   The description text for the "max\_backfill\_qid" integration instance parameter has been clarified.
-   **Version 12.20.0 - January 2026**

    Changed: Detection creation now supports cmdb\_ci as the uniqueness attribute instead of asset\_id, providing greater flexibility in detection handling.

-   **Version 30.2.0 - January 2026 \(USEM\)**

    New: Test results can now be split based on the database instance for more granular tracking and remediation.

-   **Version 12.19.6 - December 2025**

    Fixed: Store application upgrades no longer recreate data source mappings.

-   **Version 12.18.3 - October 2025**
    -   Fixed:
        -   Updated the QVS integration to use a dynamic URL instead of a hardcoded one.
        -   Resolved an issue where the Source Instance field was populating as empty.
-   **Version 12.18.2 - September 2025**

    Fixed: The Resource ID Lookup rule in Qualys integrations has been updated to ensure accurate assignment of newly discovered items to their respective CI classes.

-   **Version 12.18.0 - August 2025**

    Changed: Updated the Qualys Host Detection Integration to parse the proof information from the new attributes in the API response \(current: INSTANCE\_INFO, upcoming: INFO\) for accurate remediation. Created a new Qualys Vulnerability Scores \(QVS\) Integration which provides additional context by providing visibility to Qualys-specific risk context in CVEs by importing QVS scores.

-   **Version 12.17.1 - May 2025**

    Changed: Qualys PCRS integrations are updated to use 2.0 API.

-   **Version 12.16.3 - February 2025**

    Fixed: Minor fixes for this release.

-   **Version 12.15.3 - November 2024**

    New: Qualys Test Group/Policy reference from Test Result and Test: Enabling the 'sn\_vulc.add\_policy\_as\_key' system property populates the Test Group/Policy on a Test/Control and the Test Group can be referenced from a Test Result by dot-walking to the Test. For additional guidance and prerequisites, see Qualys integration with Configuration Compliance and KB1644268 KB article.

-   **Version 12.14.2 - August 2024**
    -   New: You can enable or disable the import of test results for a Qualys test group in the Vulnerability Manager Workspace.
    -   Changed:
        -   Auditing is disabled on the Ticket number, Assignee name, Assignee email, Qualys severity fields.
        -   Renamed the Mark Deprecated button on a Test Group form to Disable Imports.
-   **Version 12.13.0 - June 2024**

    New: The execution of Integration Run of Qualys Host Detection and Qualys Comprehensive Host Detection Integration also accounts for the number of detections excluded with the application of exclusion rules.

-   **Version 12.12.2 - May 2024**

    Changed: If the newly introduced 'vuln\_comp' integration instance parameter is set to true, the Qualys Knowledge Base integration will pull all the vulnerabilities every Sunday.

-   **Version 12.11.2 - February 2024**

    Fixed: The Malware exists field populates in the Vulnerability which is imported from the Qulays Knowledge Base integration.

-   **Version 12.10.1 - November 2023**
    -   Changed:
        -   Revised CI Lookup rules to validate all the CI lookup rules for cloud assets reported by Qualys.
        -   A system property is created to set the CI class for unmatched cloud assets. This allows users to set unclassed hardware for unmatched cloud assets. These changes help to ensure that all cloud assets are properly tracked and managed, which is essential for maintaining a secure and compliant cloud environment.
-   **Version 12.9.2 - August 2023 \(Vancouver\)**
    -   New:
        -   The Integration run status report and Qualys overview dashboard is updated to the next generation experience.
        -   The Qualys PC Policies integration run fetches only Basic policy information during the integration run to avoid a huge payload.
        -   The last pass field will be populated on the test results when Qualys integration is triggered.
        -   The Extended Evidence and Cause of Failure are captured in the Actual values field when the integration is triggered.
        -   Introduced a new Qualys comprehensive integration to update the last seen of the test results with the last evaluation date for unhealthy test results.
    -   Changed:
        -   Rescan will be terminated if the Remediation Tasks contain more than 10K VITs.
        -   Introduced a new integration instance parameter, 'vm\_scan\_since' to fetch the assets based on 'vm\_scan\_since' parameter value when an Assets integration is triggered.
    -   Fixed: Earlier, the Qualys KB integration used to go in an infinite loop, when 'max\_delta\_days' is provided as '1'. After the fix, the Qualys KB integration works fine even if the 'max\_delta\_days' is provided as '1'.
-   **Version 12.8.6 - July 2023**

    Fixed: Capability to update all the Qualys TPE's via Qualys Knowledge Base \(Backfill\) integration.

-   **Version 12.8.4 - June 2023**
    -   Fixed:
        -   For Azure assets, the account\_id populates on the discovered item created from Qualys integration.
        -   The Qualys Knowledge Base integration has been updated to pull the data for past two days on a daily basis so that any updated data is not missed.
        -   Earlier, if there is a rescan integration run record in the queue, an integration run was not being created. This issue has been fixed. An integration run is created in the Ready state even if there is an integration run created for rescan which is in the Ready state.
-   **Version 12.8.2 - May 2023**
    -   Fixed:
        -   Earlier, CIs were being continuously removed and associated again based on lookup rules or IRE for cloud discovered items. This issue has now been fixed.
        -   The Qualys Policy Compliance Reporting Service \(PCRS\) integrationused to fail when there was no data to fetch. Now, the Qualys PCRS Integration is marked as complete if there is no data to fetch.
        -   Starting from 12.8.1 release, the Cloud resource ID data will be populated on Discovered Item by Qualys PCRS integration.
-   **Version 12.7.3 - March 2023**
    -   Fixed:
        -   For Qualys version 12.6, the Qualys Host Detection integration was updated to use the parameter "detection\_processed\_after" instead of "detection\_updated\_since" to retrieve the missing detections.
        -   However, using this parameter was retrieving more than the delta data, increasing the duration of the integration runs. To address this issue, the change has been reverted. Now, the "detection\_updated\_since" parameter is the default value. To use the parameter "detection\_processed\_after", set the value of the configuration 'Use Detection Processed After' to true.
-   **Version 12.7.1 - February 2023**
    -   New:
        -   A CI Lookup Rule "Cloud Resource ID" has been introduced to match the Cloud CIs based on Cloud Metadata.
        -   You can choose to configure the REST integration to bring in QDS on Detections.
        -   You can choose to configure the REST integration to bring in Asset Risk Score and Asset Criticality Score on Discovered Items.
    -   Changed:
        -   Host List integration now processes the Cloud Metadata information and stores it on the Discovered Item.
        -   The existing default CI lookup rules are modified to include Asset Category Not Equals Cloud in the condition.
        -   Qualys Host Detection integration now uses the parameter "detection\_processed\_after" instead of "detection\_updated\_since" to identify the delta since the last successful integration run.
-   **Version 12.6.3 - November 2022**
    -   New:
        -   Two new Qualys Integrations for importing test results with new sets of Qualys APIs: Qualys PCRS Policy Host Integration and Qualys PCRS Test Results Integration.
        -   The Qualys PC Results Integration is marked inactive if the two new integrations are activated.
    -   Fixed: Existing policies are marked inactive if they are not imported with the Qualys PC policy integration.
-   **Version 12.5.2 - August 2022**
    -   New: A new parameter, include\_only\_confirmed, allows you to filter only for vulnerabilities of the type, confirmed. Activate this parameter from the integration instance parameters. It is inactive by default. From your ServiceNow AI Platform instance, without coding or adding additional queries, further refine your imported vulnerability data for all the Qualys integrations with query parameters that are supported by Qualys.
    -   Fixed: Values for Qualys metadata fields are displayed as expected. Rollup of kernal field values to VITs from associated detections occurs as expected.
-   **Version 12.4.1 - March 2022**

    Fixed: An inactive policy was causing the vulnerability integration to fail. This issue has been fixed. Now, these policy details and test results will not be fetched for the inactive policies, ensuring that the integration does not fail.

-   **Version 12.3.0 - February 2022**

    No new features or updates are included with this version. This version ensures that features from the last release are compatible with the San Diego family release.

-   **Version 12.2.2 - October 2021**
    -   New:
        -   Added support to import additional metadata for detections. This helps in filtering the Linux vulnerabilities based on the impact on kernel, service or configuration.
        -   Qualys Host Detection Comprehensive Integration retrieves host and vulnerability data from Qualys. The output of this integration is vulnerable items. This integration imports vulnerabilities in all the states - New, Fixed, Active, and Reopened. By default, this integration is inactive and runs weekly.
    -   Changed: Changed the existing Qualys Host Detection Integration to bring in only new and closed detections. This change is done to improve the daily integration performance.
-   **Version 12.1.1 - June 2021**
    -   New: With the configuration item lookup rule change, identify the assets across your environment that have the same IP Addresses and update the associated CIs.
    -   Fixed:
        -   Remediation owners have permission to view appliance and profile option information related to the Qualys scanner.
        -   Initiating a rescan no longer returns, "Error code: 1901".
        -   Upgrades no longer disable the Qualys records.
-   **Version 12.0.0 - February 2021**
    -   Changed:
        -   Rescans
            -   With the updated rescan functionality, initiate scans from the vulnerability group, vulnerability item, third-party entry \(TPE\), and discovered item records.
            -   After the scan completes, view the Qualys scan results on the vulnerability scan record, any vulnerable items that were updated by the scan, and details for any assets that were not reached during scans.
            -   Vulnerability managers can specify that rescans for resolved item are available within certain time windows or only can start at certain times.
-   **Version 11.1.0 - November 2020**
    -   New:
        -   New Host Import maps are added for Unclassed Hardware.
        -   Discovery source VR-Qualys is created and passed to IRE to create CIs.
-   **Version 11.0.0 - October 2020**

    New: An optional condition builder has been added to the CI lookup rules that permits you to filter out specific assets in your IT environment. Create filter conditions using the attributes received from the Qualys host payload.

-   **Version 10.3.3 - June 2020**
    -   New: Recertified for version 10.3.3.
    -   Changed: Imported Qualys host tags are ingested using the Qualys Asset List Integration and processed using the common tags framework.
    -   Fixed: For detections, if a scanner continues to find VIs set to 'Resolved' but not transitioned to 'Closed' - 'Fixed' by subsequent scans, these VIs transition back to 'Open' if the last found date is later than the resolved date.
-   **Version 10.0.1 - March 2020**
    -   New:
        -   Improved Error Handling and State Management
        -   Retry for API failures such as timeouts
        -   Fixes

