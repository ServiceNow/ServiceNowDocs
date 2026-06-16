---
title: Vulnerability Response Integration with Tenable release notes
description: Version history for the Security Operations Vulnerability Response Integration with Tenable on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-integration-with-tenable.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 12
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration with Tenable release notes

Version history for the Security Operations Vulnerability Response Integration with Tenable on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.4.1 - June 2026 \(USEM\)**
    -   Fixed:
        -   Resolved an issue where Tenable vulnerability imports failed when the import\_size value exceeded the maximum integer limit, resulting in overflow errors for large payloads. The field is now stored as a decimal value, allowing imports of any size to complete successfully.
        -   Resolved an issue where detection key-change reconciliation produced non-deterministic results when multiple detections shared the same first\_found timestamp, causing previously fixed detections to intermittently revert to an open state. Detection state handling is now stable across scans, and reconciliation consistently selects the correct record.
-   **Version 30.3.3 - April 2026 \(USEM\)**
    -   New:
        -   The Tenable.io Compliance Results integration is now split into separate Open and Fixed integrations, significantly reducing ingestion time for large environments.
        -   You can now configure which identifier serves as the unique key for Tenable compliance tests, preventing test results from being unintentionally overwritten.
        -   Integration runs can now be split by severity levels \(Critical, High, Medium, Low\), for payload management and scalability for large data imports.
    -   Changed: Improved column sizing for JSON-based integrations to better accommodate data field lengths.
    -   Fixed:
        -   An issue where priority values from Tenable cloud findings \(Cloud security posture management \(CSPM\)\) were not imported into ServiceNow, causing inaccurate risk score calculations.
        -   Severity mapping for Tenable Web Application Scanning \(WAS\) integration and removed unnecessary setup assistant configuration.
        -   A failure in the Tenable.cs Cloud Container Asset integration caused by a backward-incompatible API change.The "Agent Exists" field which was incorrectly set to true for all discovered items from Tenable Security Center, even when the value was not provided.
    -   Removed:
        -   3DES algorithm-based data from out-of-box records for improved security.
        -   Hardcoded colors from integration run reports for better theme consistency.
-   **Version 6.1.3 - April 2026**
    -   New:
        -   The Tenable.io Compliance Results integration is now split into separate Open and Fixed integrations, significantly reducing ingestion time for large environments.
        -   Customers can now configure which identifier serves as the unique key for Tenable compliance tests, preventing test results from being unintentionally overwritten.
        -   Integration runs can now be split by severity levels \(Critical, High, Medium, Low\), for payload management and scalability for large data imports.
    -   Changed: Improved column sizing for JSON-based integrations to better accommodate data field lengths.
    -   Fixed:
        -   An issue where priority values from Tenable cloud findings \(Cloud security posture management \(CSPM\)\) were not imported into ServiceNow, causing inaccurate risk score calculations.
        -   Severity mapping for Tenable Web Application Scanning \(WAS\) integration and removed unnecessary setup assistant configuration.
        -   A failure in the Tenable.cs Cloud Container Asset integration caused by a backward-incompatible API change.
        -   The "Agent Exists" field which was incorrectly set to true for all discovered items from Tenable Security Center, even when the value was not provided.
    -   Removed:
        -   3DES algorithm-based data from out-of-box records for improved security.
        -   Hardcoded colors from integration run reports for better theme consistency.
-   **Version 30.2.1 - February 2026 \(USEM\)**

    Fixed: An issue where the Tenable Web Application Scanning \(WAS\) integration failed due to incorrect ECMAScript configuration settings. Vulnerability data now imports successfully and application vulnerable items \(AVITs\) are created as expected.

-   **Version 6.0.1 - February 2026**

    Fixed: An issue where the Tenable Web Application Scanning \(WAS\) integration failed due to incorrect ECMAScript configuration settings. Vulnerability data now imports successfully and application vulnerable items \(AVITs\) are created as expected.

-   **Version 6.0.0 - January 2026**
    -   New:
        -   Database instance test result splitting provides improved isolation and traceability of scan outcomes.
        -   Introduced Tenable Web App Scanning \(WAS\) integration for Application Vulnerability Response including Setup Assistant improvements and expanded configuration options for Tenable connectivity.
    -   Changed: Proof‑based split detection now generates distinct detections and vulnerable items \(VITs\) for each unique proof, enabling granular tracking and remediation.
-   **Version 30.2.0 - January 2026 \(USEM\)**
    -   New:
        -   Database instance test result splitting provides improved isolation and traceability of scan outcomes.
        -   Introduced Tenable Web App Scanning \(WAS\) integration for Application Vulnerability Response including Setup Assistant improvements and expanded configuration options for Tenable connectivity.
    -   Changed: Proof‑based split detection now generates distinct detections and vulnerable items \(VITs\) for each unique proof, enabling granular tracking and remediation.
-   **Version 5.2.1 - December 2025**
    -   New:
        -   Advanced vulnerability risk data from Tenable: Support for the latest and most comprehensive risk scoring methods from Tenable.io for both open and fixed vulnerabilities, as well as plugin Integrations. This includes:
            -   Vulnerability Priority Rating v2 \(VPRv2\): Tenable's updated system for prioritizing vulnerabilities.
            -   Exploit Prediction Scoring System \(EPSS\): A new metric that estimates the likelihood of a vulnerability being exploited in the wild.
            -   Common Vulnerability Scoring System v4 \(CVSSv4\): The newest industry standard for assessing vulnerability severity.
        -   Dedicated storage for Tenable data:
            -   Introduced a new table: sn\_vul\_tenable\_tpe\_attributes to store detailed metadata from Tenable \(VPRv2, EPSS, plugin-related information\).
            -   Added new columns: vprv1\_risk\_score and vprv2\_risk\_score to the Third-party Entry \(TPE\) table.
            -   Added a reference column: tenable\_tpe\_attributes\_entry in the sn\_vul\_entry table to link to the new attribute data.
        -   Flexible REST message filtering: You can now add specific filter parameters directly within the "Content" field of REST messages.
        -   Automated asset decommissioning: Added support to automatically detect assets marked with Tenable's deleted\_at attribute and decommission them in our system when shut down or deleted in Tenable.
        -   Prioritization of VPRv2 for Risk Scoring: A new business rule, "Update Source Risk Score and Rating," has been implemented. If VPRv2 data is available for a vulnerability, it will now be used as the primary "Source Risk Score," overriding the older VPRv1 score.
    -   Changed: Updated Tenable.io / .cs / .sc source risk score handling: Changes have been made to how source risk scores are handled across various Tenable products.
-   **Version 5.1.1 - September 2025**

    Fixed: The Resource ID Lookup rule in Tenable integrations has been updated to ensure accurate assignment of newly discovered items to their respective CI classes.

-   **Version 5.1.0 - August 2025**

    Fixed: Integration runs are now allowed from newly created Tenable.cs integrations from the Setup Assistant. After the integration is run, the source will point to the parent integration instance.

-   **Version 5.0.3 - May 2025**
    -   New:
        -   The Vulnerability Response Integration with Tenable application now supports data ingestion from Tenable.cs, enabling you to bring in cloud and container vulnerabilities directly into ServiceNow. This integration improves the ability to prioritize and remediate vulnerabilities identified in Tenable cloud resources and container images.
    -   Fixed:
        -   Introduced a new instance parameter for page size.
        -   Correctly mapped Tenable.io serial number to the attribute.
        -   Test results received from Tenable with empty "check\_name" caused display\_name issue, which is fixed.
        -   Error handling is done for page limit exceed scenario.
        -   Skip updating Plugin family id for Tenable.io.
-   **Version 4.1.1 - February 2025**
    -   New:
        -   Added the Tenable CVSS 3.0 mapping to the Vulnerability column.
        -   The source payload data in Discovered Items will now contain the serial number.
-   **Version 3.13.3 - November 2024**

    New: Split Detection: Vulnerability Managers can now configure the split of detections from Tenable using plugin ID, enabling them to specify the delimiter for each plugin ID to parse the proof. This enhancement results in the creation of multiple vulnerable items for each proof. By default, the configuration to enable split detection by proof is disabled.

-   **Version 3.12.1 - August 2024**

    New: In the Tests table, the test group associated with a test is populated for the Tenable.io Integration.

-   **Version 3.11.0 - June 2024**

    New: For the Tenable.io and Tenable.sc integrations, execution of the Integration Run of Tenable Vulnerabilities integration also accounts for the number of detections excluded with the application of exclusion rules.

-   **Version 3.10.2 - May 2024**

    Changed: If the newly introduced 'vuln\_comp' integration instance parameter is set to true, the Tenable.io and Tenable.sc integrations pull all the vulnerabilities every Sunday.

-   **Version 3.9.1 - February 2024**
    -   Changed: The Tenable.io integrations can now be configured to run from Standard user role onwards.
    -   Fixed: In the Tenable scan record, the source table field value populates with the source table name.
-   **Version 3.8.1 - November 2023**
    -   Changed:
        -   The has\_agent field will be populated on the discovered item for tenable.sc assets if asset has agent installed on it.
        -   The UUID value will now be populated on the source\_data so that the customer can use the sn\_sec\_cmn\_src\_cmdb\_map to map to cmdb column if required.
-   **Version 3.7.2 - August 2023 \(Vancouver\)**
    -   New: The Tenable Integration run status dashboard is now available in the Next Experience UI.
    -   Fixed:
        -   The Tenable.io scan credential integration supports pagination now.
        -   On running the Tenable Configuration Compliance integrations, the Last Pass field is populated on the test results.
-   **Version 3.6.4 - July 2023**

    Fixed: Tenable asset unique ID is generated properly in ServiceNow in case there is an additional key added in uniqueness on the tenable side.

-   **Version 3.6.3 - June 2023**

    Fixed: Earlier, if the Vulnerability Response application was upgraded after installing the Tenable plugin, plugins with severity 'Medium' were ingested with the severity 'None' in ServiceNow. This issue can be fixed using the fix script provided to correct the existing plugins. Starting from Tenable v3.6.3, all the plugins ingest data with the correct severity. As a result, the risk score for vulnerable items associated with those updated plugins will be recalculated.

-   **Version 3.6.2 - May 2023**

    Fixed: Earlier, CIs were being continuously removed and associated again based on lookup rules or IRE for cloud discovered items. This issue has now been fixed.

-   **Version 3.5.1 - February 2023**
    -   New:
        -   A CI Lookup Rule "Cloud Resource ID" has been introduced to match the Cloud CIs based on Cloud Metadata.
        -   You can choose to configure the REST integration to bring in Asset Exposure Score and Asset Criticality Score on Discovered Items.
    -   Changed:
        -   Assets integration now processes the Cloud Metadata information and stores it on the Discovered Item.
        -   The existing default CI lookup rules have been modified to include Asset Category Not Equals Cloud in the condition.
        -   Both the Tenable.io Vulnerabilities integrations \(Open/Closed\) now use the parameter "indexed\_at" instead of last\_found/last\_fixed to import the delta from the last successful integration run.
-   **Version 3.4.1 - November 2022**

    Fixed: Minor fixes for this release.

-   **Version 3.3.2 - August 2022**
    -   New:
        -   You can initiate Tenable rescans without selecting credentials.
        -   From your ServiceNow AI Platform instance, without coding or adding additional queries, further refine your imported vulnerability data with parameters that are provided by the Tenable.io scanner. The following Tenable.io integrations support filtering by providing JSON content in the request body.
            -   Tenable.io Assets Integration
            -   Tenable.io Fixed Vulnerabilities Integration
            -   Tenable.io Open Vulnerabilities Integration
        -   The report\_view access control lists \(ACLs\) that govern who can see reports in dashboards and elsewhere are enabled by default in the Tokyo release.
        -   With changes to the integration runs, you can view the following information for the vulnerability integration runs:
            -   Total chunks: Total number of chunks generated by the Tenable product.
            -   Available chunks: The number of chunks available for download to your ServiceNow AI Platform.
    -   Fixed: Saving the selected query filter in an integration instance works as expected.
-   **Version 3.2.3 - March 2022**
    -   New:
        -   The Tenable.sc Open Assets Integration imports information about open assets.
        -   For the Tenable.sc and Tenable.io products, if you choose API Authorization for authentication in the Setup Assistant, the access key is saved as a plain text string in your integration instances. The secret key remains encrypted. For existing customers, this changes applies after you upgrade to version 16.1 of the Vulnerability Response and version 3.2 of the Tenable Vulnerability Integration applications.
    -   Changed: To avoid creating duplicate discovered items with imported asset data, a new integration has been added to the Tenable.sc Assets Integration. The new integration, the Tenable.sc Open Assets integration, imports information about open assets. The Tenable.sc Fixed Assets Integration imports information about fixed assets.
-   **Version 3.0.5 - October 2021**
    -   New:
        -   Verify that your assets are in compliance with your policies and controls with imports from the Tenable.io product. The Tenable.io product in the Tenable Vulnerability Integration imports policies, controls \(test results\), and configuration tests for processing in the Configuration Compliance application.
        -   Initiate remediation scans for the vulnerabilities identified by Tenable.io from your ServiceNow AI Platform instance.
    -   Changed: Introduced a property to make the Tenable.sc API calls synchronously when using a MID server.
    -   Fixed:
        -   When the configuration items associated with discovered items have no data, vulnerable items are not created.
        -   Vulnerable items are closed as expected using the last\_fixed date instead of the last\_found date when running the Tenable.sc Closed Vulnerabilities integration.
        -   Compliance assessment data is imported as expected and not brought in as part of the Vulnerabilities Integration.
        -   The default URL is populated as expected when the integration instance record is created directly on the integration instance module.
        -   The status of the Tenable.io and Tenable.sc integrations is active as expected on the Vulnerability Integrations List. If both Tenable integrations are configured with their URLs and credentials in the Setup Assistant, both are active on the list. If only one integration is configured in Setup Assistant, Tenable.io, for example, only Tenable.io is active on the Vulnerability Integrations List.
-   **Version 2.2.3 - June 2021**
    -   New: The Backfill Vulnerabilities Integration for the Tenable.sc product imports any open and fixed vulnerabilities from the last seven days that might have been missed during an import.
    -   Changed:
        -   Starting with v14.0 of Vulnerability Response and v2.2 of the Tenable Vulnerability Integration, you have two options for your authentication with the Tenable.sc product: API Key Authentication and User authentication. With these authentication options, you can continue using your FIPS compliant solutions with v5.12 and earlier of the Tenable product.
        -   The Tenable query filter you select in the Setup Assistant also applies to the Tenable.sc Assets Integration. Only the assets with the vulnerabilities that match the conditions of the query filter are imported. For the Tenable.io assets integration, Last Scan Time is imported and updated only for assets that have vulnerabilities.
        -   An attribute on the integration instance now controls the configuration item lookup using IP Address for networks that having overlapping IPs.
-   **Version 2.1.1 - February 2021**
    -   Changed:
        -   The CI lookup rule
            -   With this change, identify the assets across your environment that have the same IP Addresses and update the associated CIs.
        -   Tenable.sc rescans
            -   Initiate a Tenable.sc rescan from discovered item records.
            -   View IP addresses for assets not accessed during the scan on Tenable Vulnerability Scan records.
-   **Version 2.0.4 - November 2020**

    The Vulnerability Response Integration with Tenable built by ServiceNow imports data from the Tenable.io and Tenable.sc products to help you prioritize and remediate vulnerabilities for your assets.


