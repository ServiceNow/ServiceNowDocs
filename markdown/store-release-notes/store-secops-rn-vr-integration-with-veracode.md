---
title: Vulnerability Response Integration with Veracode release notes
description: Version history for the Vulnerability Response Integration with Veracode on the ServiceNow Store .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-integration-with-veracode.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration with Veracode release notes

Version history for the Vulnerability Response Integration with Veracode on the ServiceNow Store .

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.1.3 - June 2026 \(USEM\)**
    -   The following enhancements and changes support internal security directives:Dictionary fields on sn\_vul\_app\_release and sn\_vul\_veracode\_link\_projects are now read-only. A one-time fix script applies the option to existing fields.
        -   Fix script renamed to a per-plugin name to prevent update set conflicts with other Vulnerability Response plugins.
        -   Translation packaging updated to match the platform-wide convention. Locales include but are not limited to: Arabic, Portuguese, Chinese, Czech, Dutch, Finnish, French, and French-Canadian.
-   **Version 30.1.2 - April 2026 \(USEM\)**
    -   Fixed:
        -   Enhanced SCA findings processing with validation to skip null/empty CVE IDs and create custom vulnerability entries for non-CVE identifiers.
        -   The default Auto-Close Rule included with the application "Close findings associated to deleted scans", where an invalid column
    -   Changed: Added automatic CVSS v2/v3 score and vector population.
-   **Version 4.7.5 - April 2026**
    -   Fixed:
        -   Enhanced SCA findings processing with validation to skip null/empty CVE IDs and create custom vulnerability entries for non-CVE identifiers.
        -   The default Auto-Close Rule included with the application "Close findings associated to deleted scans", where an invalid column scan\_deletion\_date was referenced in the condition. The rule has been updated by replacing scan\_deletion\_date with source\_scan\_deletion\_date.
    -   Changed: Added automatic CVSS v2/v3 score and vector population.
-   **Version 4.7.3 - December 2025**
    -   Fixed:
        -   Fixed a naming inconsistency in the Veracode Reporting API processing logic.
        -   Fixed region-based validation for Veracode configuration to ensure credential validation work correctly across all supported regions.
        -   Fixed the scan deletion tracking logic to use source-based deletion date
-   **Version 4.7.1 - August 2025**
    -   New: Added the required mapping from Veracode to AVITs for displaying the 'fixable' status of findings
    -   Fixed: As part of this bug, fixed the workflow to deactivate the Discovered Applications that are no longer present in the Application List from Veracode.
-   **Version 4.6.2 - March 2025**
    -   Fixed:
        -   The 'Policy compliance state' column is added to the Application Vulnerability Scan Summaries table.
        -   The Veracode Deleted Scans API integration imports data about scans that are deleted from Veracode into your ServiceNow AI Platform instance.
        -   Linked projects that are added or removed from Veracode are updated on the Linked Projects \[sn\_vul\_veracode\_link\_projects\] table in your ServiceNow AI Platform instance.
-   **Version 2.12.2 - February 2025**
    -   Changed: You can now see the precise date and time when a container vulnerable item \(CVIT\) was first discovered, last opened, resolved, and last found, ensuring clarity and accounting for different time zones.
    -   Fixed: The UI actions and validations in the CVIT form now align consistently with the current state.
-   **Version 4.5.1 - November 2024**
    -   Fixed:
        -   Fix provided for data mismatch for scan updates to Software Composition Analysis \(SCA\) findings.
        -   Error handling fix to address retry and skip errors specifically for the Veracode Link Projects and Veracode SBOM Integrations. To support deleted applications for these two integrations, users can choose to skip 403 and 404 errors and retry 50x errors.
    -   Changed:
        -   You can select the scan that takes precedence for the final updates for SCA findings data imported from Veracode. On the Veracode configuration page, Default' is the set value until you change it. You must select the 'Include SCA findings' check box and choose one from the list:
            -   Agent - the agent scan results make the final updates to SCA findings
            -   Upload - the upload scan results make the final updates to SCA findings
            -   Default - the last scan processed, either the agent or upload scan, makes the final updates to SCA findings
    -   Note: If you do not select the 'Include SCA findings' check box on the configuration page, the scan you selected from the list is not used, and the last scan that is processed makes the final updates.
    -   Support for Veracode's adding and deleting of applications imported from the ServiceNow AI Platform.
    -   Set the value for the \[sn-vul-veracode.app-mark-unseen-apps-inactive\] system property to 'true' to prevent errors if the Platform requests applications already deleted by Veracode. If this property is set to 'true' \(activated\), the successful import of the Application List Integration marks any unseen applications in the Platform as 'inactive'.
-   **Version 4.4.2 - October 2024**
    -   Fix provided for data mismatch for scan updates to Software composition analysis \(SCA\) findings.
    -   You can select the scan that takes precedence for the final updates for SCA findings data imported from Veracode. On the Veracode configuration page, ‘Default’ is the set value until you change it. You must select the Include SCA findings check box and choose one from the list:
        -   Agent – the agent scan results make the final updates to SCA findings
        -   Upload – the upload scan results make the final updates to SCA findings
        -   Default – the last scan processed, either the agent or upload scan, makes the final updates to SCA findings
    -   Note: If you do not select the Include SCA findings check box on the configuration page, the scan you selected from the list is not used, and the last scan that is processed makes the final updates.
    -   Support Veracode’s adding and deleting applications imported from the ServiceNow AI Platform.
        -   Set the value for the \[sn-vul-veracode.app-mark-unseen-apps-inactive\] system property to ‘true’ to prevent errors if the Platform requests applications already deleted by Veracode. If this property is set to ‘true’ \(activated\), the successful import of the Application List Integration marks any unseen applications in the Platform as ‘inactive’.
    -   Error handling fix to address retry and skip errors specifically for the Veracode Link Projects and Veracode SBOM Integrations. To support deleted applications for these two integrations, users can choose to skip 403 and 404 errors and retry 50x errors.
-   **Version 4.3.3 - August 2024**
    -   New:
        -   Improvements to the Veracode Vulnerability Integration Configuration page:
            -   API region and API timeout parameters are supported.
            -   If you have installed SBOM Response, you have the option to include vulnerabilities found by Veracode for the SBOM files you upload.
        -   Vericode' is mapped to the Source field for records in the Bill of Materials \[sn\_sbom\_doc\] table for the Veracode SBOM files that you upload.
    -   Fixed:
        -   Modifications to data mapping to support the following improvements:
            -   The Source resolved date and Last found fields are populated on application vulnerable items \(AVITs\).
            -   The filtering capability for the attributes of Source additional info persists the key-value pairs in a string field.
-   **Version 4.2.7 - June 2024**

    New: Auto close for application vulnerable items is supported for the Veracode integrations.

-   **Version 4.2.4 - May 2024**
    -   New:
        -   Select 'Get More Details' on Veracode application vulnerable items \(AVITs\) on the Application Vulnerable Item \(sn\_vul\_app\_vulnerable\_item\) table or from the list views in the Vulnerability Response Workspaces to update Veracode AVITs with the following information from Veracode:
            -   HTTP Source request and Source response details for DAST scans are displayed on theHTTP 'Request/Response'related list.
            -   Solution recommendations from Veracode are displayed on the 'Findings' related list.
            -   In the Vulnerability Response Workspaces, you can view HTTP Source request, Source response, and recommendations on the 'Details'tab.
            -   The Description column is supported on the Application Vulnerable Item \(sn\_vul\_app\_vulnerable\_item\) table.
        -   View details such as total processing times, average times for pre- and post-integration run processes, and reports on the integration run records.
-   **Version 4.1.11 - March 2024**

    Fixed: Business application references are resolved using discovered application data during Veracode Software Bill of Materials \(SBOM\) Integration runs and mapped to BOM entities as expected.

-   **Version 4.1.8 - February 2024**
    -   New:
        -   You can reapply your configuration item \(CI\) lookup rules to update existing CIs \(scanned applications and product models\).
        -   Manually create remediation tasks \(AVULs\) for application vulnerable items \(AVITs\) from remediation task records on the Group Configuration tab.
    -   Fixed:
        -   Enhancements to the application vulnerable item record \(AVIT\) enable you to view:
            -   Dependency and remediation effort information.
            -   Vulnerability values populated as expected.
-   **Version 4.1.6 - December 2023**

    Fixed: Records cannot be created in the Veracode Link Projects table manually. Run the Veracode Link projects Integration to fetch the data.

-   **Version 4.1.3 - November 2023**

    New:

    -   New:
        -   A filter parameter on the configuration page enables you to list only records that match the severity values provided by Veracode. You can add multiple severity values to the filter.
        -   Buffer time is a configurable parameter with the sn\_vul\_veracode.import\_starttime\_buffer system property. The buffer, in hours, is subtracted from Start Time \(delta\_start\_time\). The scanner gets results at the new derived delta start time.
        -   TheManage exceptions in ServiceNowandManage false positivesin ServiceNowoptions on the Veracode configuration page can help you triage your imported application vulnerabilities with ServiceNow workflows. These options are activated by default.
            -   Manage exceptions in ServiceNowtriages application vulnerable items \(AVI\) with the ServiceNow Exception management workflow.AVIs transition toOpen, and you request exceptions from AVI records. Deactivate the option to preserve the Source states on AVIs imported from Veracode.
            -   Manage false positives in ServiceNowtriages false positives with the ServiceNow False positive workflow.AVIs transition toOpen, and you request false positives from AVI records. Deactivate the option to preserve the Source states on AVIs imported from Veracode.
    -   Changed: More supported combinations for state mapping enable the system to map scanner imports to their associated states in your instance based on your triage settings for Manage exceptions in ServiceNow and manage false positives in ServiceNow.
    -   Fixed: Fields for the data of the source for an AVI ID, along with the combination of the Application ID, Componet ID, and CVE ID are populated in fields as expected. Data is stored for Linked SCA projects and source exploit scores.
-   **Version 4.0.4 - September 2023**

    Fixed: The Veracode reporting API supports requests for six months. The Vulnerable Item Integration imports data for the 'Import since' date for a six month window as expected.

-   **Version 4.0.3 - August 2023**

    New:

    -   The following integrations were added to import data via a JSON REST API: Veracode Application List, Veracode Scan Summary, Application Vulnerable Item. The versions of these integrations that used an XML-based API are deprecated.
    -   The Veracode Categories Integration imports 'Category' data.
    -   Veracode integrations support imports of Software Composition Analysis \(SCA\) vulnerabilities.
    -   Veracode manual penetration testing results imports are supported. These test results are manual findings from Veracode that you configure for import in the integration instance. They are not linked to the test assessments that you request in Application Vulnerabilty Response.
    -   The Veracode CWE Integration imports threat information and remediation recommendations for Veracode vulnerabilities. Your vulnerability data are not duplicated if you have this integration activated and the CWE Comprehensive Integration activated in Vulnerability Response.
    -   The Veracode Software Bill of Material \(SBOM\) Integration imports of SBOMs from Veracode in CycloneDX JSON fomat. You must install the SBOM applications that are available in the ServicNow Store to parse and view SBOM data.
    -   The Veracode DevOps Integration permits users with the DevOps Change Velocity license to view third-party scan summaries from Security Operations in DevOps. This integration is listed in the Vulnerability Integrations \[sn\_vul\_integration\_list\] table, but there is no impact to Application Vulnerability Reponse.
    -   You can configure the following parameters on the Integration Instance Parameters tab:
        -   Import manual - import manual penetration testing results from Veracode.
        -   import\_sca - import SCA vulnerabilities.
        -   Status - import records in 'Open' or 'Closed' states. If you leave this field blank, you import records for both states.
        -   policy\_sandbox - enter 'policy' or 'sandbox' to import results from your test environments.
        -   policy\_rule\_passed - import records that have passed a policy rule \(true\).
    -   On the Application Vulnerability Scan Summaries \[sn\_vul\_app\_vul\_scan\_summary\] table, use the configuration icon \(gear\) to view data for new columns.
-   **Version 3.5.0 - February 2023**

    Fixed: The pagination issues related to the Veracode Application List JSON Integration have been fixed.

-   **Version 3.4.0 - November 2022**
    -   New: Introduced a new integration, Veracode Application List Json Integration, that provides support for delta ingestion.
    -   Changed: You can now bring application vulnerabilities and scan summary from only those applications which are scanned from the last import since date.
-   **Version 3.3.0 - March 2022**

    New: Added the option to perform triaging within ServiceNow. Enable this option to request exceptions or mark AVIs as false positives. Use the new state mapping logic for AVIs.

-   **Version 3.2.0 - February 2022**

    No new features or updates are included with this version. This version ensures that features from the last release are compatible with the San Diego family release.

-   **Version 3.1.0 - October 2021**

    Updated version number for dependency applications.

-   **Version 3.0.1 - June 2021**

    New: Ingest SAST findings to detect security risks in your applications and help you remediate these vulnerabilities.

-   **Version 2.0.0 - February 2021**

    New: Additional fields as SDLC Status, Vulnerability Summary, Vulnerability Explanation, and Recommendation, imported and mapped to display on Application Vulnerable Item form.

-   **Version 1.0.1 - December 2020**

    Fixes.

-   **Version 1.0.0 - October 2020**
    -   New:
        -   Initial release of Vulnerability Response Integration with Veracode
        -   Supports Dynamic Application Security Testing \(DAST\)

