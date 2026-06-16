---
title: CMDB and CSDM Data Foundations Dashboards release notes
description: Version history for the ServiceNow AI Platform capabilities CMDB and CSDM Data Foundations Dashboards on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-csdm-data-foundations-dashboards.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# CMDB and CSDM Data Foundations Dashboards release notes

Version history for the ServiceNow AI Platform capabilities CMDB and CSDM Data Foundations Dashboards on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.3.0 - June 2026**

    Fixed: Minor security enhancements

-   **Version 4.2.0 - December 2025**
    -   Changed:
        -   Enhanced custom service table records metric performance to use the latest batching strategy.
        -   Enhanced Hardware missing serial number metric performance to use the latest batching strategy. Also, changed corresponding PA metric to query pre-calculated score instead of doing live querying. Note that clicking on corresponding PA cards redirects to the UI16 list with same query condition of bad records. Original PA detail pages aren't available anymore.
    -   Fixed:
        -   Fixed unnecessary log requests which took too much storage space.
        -   Fixed Service Offering indicator source unmatched description vs. condition.
        -   Fixed batch job upgrade which sometimes caused duplicate score results issue.
-   **Version 4.1.2 - May 2025**
    -   Fixed:
        -   Performance fixes for Orphaned relationships and Information Objects related metrics.
        -   Tool tip text correction and assorted minor bug fixes
-   **Version 4.1.1 - February 2025**
    -   Fixed:
        -   Performance improvement for "CIs with Relationships to Parent and Child" metric
        -   Minor bug fixes
-   **Version 4.1.0 - November 2024**

    New: Report showing CIs where Operational Status and Lifecycle Stage differ.

-   **Version 4.0.3 - September 2024**
    -   Changed: The dashboards have been migrated to the latest UI for ServiceNow.
    -   Fixed: An aggregate limit with value zero now correctly calculates a health score.
-   **Version 2.6.1 - September 2024**

    Fixed: Defects fixed related to the Aggregate limit configurable fields which can improve performance in large CMDBs.

-   **Version 4.0.2 - August 2024**

    Changed: Overhaul of UI to move the CMDB and CSDM Data Foundations Dashboards to the ServiceNow Next Experience.

-   **Version 2.6.0 - August 2024**

    Two fixes related to performance tuning done in the previous version.

-   **Version 2.3.5 - May 2024**
    -   Changed:
        -   The following metrics on the CMDB dashboard have been improved for performance:
            -   CIs with Relationships to Parent and Child
            -   CIs Processed via IRE
            -   Hardware CIs with Serial Numbers
        -   The following metrics on the CSDM dashboard have been improved for performance:
            -   Application Services with 'Consumes::Consumed By' Relationships to Business Applications
            -   Application Services with Business Application Relationships
            -   Business Application with Application Service Relationships
        -   To improve performance, the following performance analytic widgets on the Data Management Practices tab will now only display a count of records rather than all record details:
            -   CIs with Relationship to Parent and Child
            -   CIs Processed via IRE
-   **Version 2.2.3 - December 2023**
    -   Fixed:
        -   In CSDM Data Foundations dashboard, Crawl tab, fixed the logical error in the script to calculate "Application Services with 'Consumes::Consumed by' Relation to Business Application"
        -   In CSDM Data Foundations dashboard, Walk tab, for "Technical service offering without support or change group", removed an irrelevant condition from the filter.
        -   In CMDB Data Foundations dashboard, "Services Without Owners" metric has been updated to only calculate operational services.
        -   The query behind "CIs with relationships to Parent and child" have been enabled with read replica rerouting.
-   **Version 2.2.1**
    -   New
    -   Changed
        -   Manage performance of the CSDM and the CMDB Data Foundations Dashboards by deactivating CMDB or CSDM metrics that you don't need. Settings that deactivate metrics are preserved during upgrades.
    -   Removed
        -   The following two metrics are no longer available in the CSDM Data Foundations dashboard, under the Fly tab:
            -   Information Objects Missing an App Service Relationship
            -   Catalog Request Items Related to Service Offerings
-   **Version 2.1.0 - February 2023**
    -   New: The CSDM and CMDB Data Foundations Dashboards Version 2.x is a major new release that contains 11 new CMDB health indicators, new remediation playbooks for those metrics, as well as new drill-down Performance Analytics \(PA\) widgets for almost all indicators in the CMDB Data Foundations Dashboard.
    -   Changed: The CMDB indicators are now grouped by function and purpose under 4 tabs, such as the Customization or ITSM Processes tab.
    -   Fixed: v2.1 Fixes ACL Issue
-   **Version 2.0.0 - August 2022**
    -   The CSDM and CMDB Data Foundations Dashboards Version 2.0 is a major new release that contains 11 new CMDB health indicators, new remediation playbooks for those metrics, as well as new drill-down Performance Analytics \(PA\) widgets for almost all indicators in the CMDB Data Foundations Dashboard.
    -   The CMDB indicators are now grouped by function and purpose under 4 tabs, such as the Customization or ITSM Processes tab.
-   **Version 1.4.0 - November 2021**

    Fixed: Custom status values now retrieved correctly

-   **Version 1.3.0 - March 2021**
    -   New:
        -   Configuration Item Status Values - New indicator on Foundation tab of CSDM Data Foundations with related report. Identifies when custom values exist in Status attributes within the CMDB.
        -   Technical Service Offerings with Support Group or Change Group - New indicator on Walk tab of CSDM Data Foundations with related PA report. Identifies when Technical Service Offerings do not have Support Group \(support\_group\) or Change Group \(assignment\_group\) populated.
        -   Dynamic CI Groups with CMDB Group - New indicator on Walk tab of CSDM Data Foundations with related PA report. Identifies when a Dynamic CI Group does not have the CSDM Group populated.
    -   Fixed: Vendor tables are no longer counted as custom tablesIndicator results for the same metric are removed when more than 1 exist
-   **Version 1.2.0 - December 2020**
    -   New:
        -   Reports have been migrated to Performance Analytics \(PA\) reports with history over time and current CI lists to drill down to the affected Cis’ \(PA licensing not required\)
        -   CSDM 3.0 alignment with new CSDM Data Foundations Dashboard tab for Foundations domain with related indicators and PA reports
    -   Changed:
        -   CMDB Data Foundation Dashboard
            -   Reports have been arranged in the order of weight and importance from left to right
            -   For CIs with Serial Numbers and Active CIs Updated in Last 90 days - added a threshold, so that If the percentage of compliant CIs is less than that threshold, then the result displayed for the indicator is set to 0
            -   For CIs Processed via IRE: Changed calculation: Sys\_id is IN \(target\_sys\_id FROM sys\_object\_source table\)
            -   For Handled Duplicate CIs changed calculation: duplicate\_of in not empty
            -   Name of CIs with Name Populated changed to CIs With Names
            -   Name of CIs with Serial Numbers changed to Hardware CIs with Serial Numbers
            -   Moved CIs Processed via IRE from CMDB Data Foundation tab to CMDB Insights tab and removed related report
            -   Moved CIs with Names from CMDB Insights tab to CMDB Data Foundation tab and created related PA report
        -   CSDM Data Foundations Dashboard
            -   Reports have been arranged in the order of weight and importance from left to right
    -   Fixed:
        -   Performance of CIs Processed via IRE \(removed report\)
        -   Calculations of CIs with Serial Number and Active CIs updated in last 90 days
    -   Removed: Reports \(replaced with PA reports\)
-   **Version 1.1.0 - October 2020**
    -   New: Created new CSDM report for Custom Business Services table count
    -   Changed:
        -   Updated logic for 'Unhandled Duplicate CIs'
        -   Updated logic for 'Active CIs not updated in 90 days' \(was 'Active CIs not updated in 60 days'\)
    -   Fixed: 'CMDB Attributes on the Right Level' and 'Use of Custom Attributes' metric calculations
-   **Version 1.0.2 - August 2020**

    The CMDB and CSDM Data Foundations Dashboards is a new store app that contains dashboards which provide insights into key indicators of your CMDB and Common Service Data Model \(CMDB\). This app provides recommendations to ensure that the CMDB and CSDM are properly configured for optimal usage and to mitigate any potential risks.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

