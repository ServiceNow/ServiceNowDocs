---
title: Integration Commons for CMDB release notes
description: Version history for the ServiceNow AI Platform capabilities Integration Commons for CMDB on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-integration-commons.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Integration Commons for CMDB release notes

Version history for the ServiceNow AI Platform capabilities Integration Commons for CMDB on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.25.0 - June 2026**
    -   New: Introduced a reusable extension point \(sn\_cmdb\_int\_util.ADMPayloadEnrichment\) for the data enrichment of process and Application CIs. This enables the population of additional attributes required for identification and reconciliation of child Application classes by Service Graph Connectors.
    -   Fixed: Updated 33 wildcard Query ACL security attributes fromUserIsAuthenticatedAndHasRightsToRead \(SAC\) toHasRightsToReadAllDataIsTrue \(SAB\). Table-level ACLs remain unchanged.
-   **Version 2.23.1 - April 2026**
    -   Fixed:
        -   Fixed the issue that caused non-concurrent import sets to be linked to incorrect or missing CMDB Integration Execution records.
        -   Fixed the issue that caused the SGC connection processing state to remain in Pending after a successful import set run due to missing execution records for transform map-based integrations.
        -   Fixed the issue where filtering Service Graph Connection records failed with a query range error.
-   **Version 2.23.0 - March 2026**
    -   Changed:
        -   Optimized the Record Removal API for better performance and added a filter to include only recent records for soft deletion.
        -   Implemented ACL fixes and minor enhancements.
-   **Version 2.22.1 - February 2026**

    Fixed: Test connection issue: The Test connection flow fails when the SGC Central plugin isn't installed due to the sgc\_centralAPI call for last\_check\_on. Added a safe check to prevent impact on connectors when SGC Central is not a required dependency.

-   **Version 2.22.0 - December 2025**
    -   New:
        -   Added support for import set run status at the connection level.
        -   Added logic to create a relationship between VM and server when both are discovered by different discovery sources.
    -   Fixed: Import set logs are linked to the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error table.
-   **Version 2.21.0 - September 2025**
    -   New:
        -   Removed the dependency on getSession\(\) to show the current execution of integrations.
        -   Added the Create Managed API Product Model RTE operation to create a new product model or retrieve an existing product model based on the name of an API CI record.
    -   Fixed:
        -   Mapped the import set to correct execution records when multiple data sources are running concurrently.
        -   Fixed the application scope for CEX records.
        -   Fixed the record removal function for the connectors where sourceFeed is not hardcoded.
        -   Linked import logs to the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error table.
-   **Version 2.20.0 - July 2025**
    -   New: Updated queries to support the SGC Central use case.
    -   Fixed:
        -   Fixed ORA-00904 error while accessing the CMDB Workspace.
        -   Fixed the display value for "Robust Transform Engine Entity Operation Type" BR.
        -   Improved performance for the Record Removal API.
        -   Fixed the SG-Intune OS field unexpected capitalization issue.
        -   Fixed the flow context to associate with the correct application scope.
-   **Version 2.19.0 - May 2025**

    New: Created common classes for processing command executions such as the Send and Run commands for the SGC for AWS and SGC for Azure.

-   **Version 2.18.0 - March 2025**

    New: Added support for air gap solution.

-   **Version 2.17.0 - February 2025**
    -   New:
        -   Added new APIs to access the sn\_cmdb\_int\_util\_execution\_diagnosis table.
        -   Added support for the Cleanse Firmware Version transform in ETL.
        -   Added null check to CI Lookup Operation.
    -   Fixed:
        -   Corrected the date timestamp for Start Time, Import Start Time, and Import End Time in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution table.
        -   Corrected the loading state in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution table when Import Sets are in cancelled state.
-   **Version 2.16.0 - December 2024**
    -   Fixed:
        -   Updated the logic to trigger the Set the session context business rule in specific scenarios.
        -   Corrected the Imported Rows with Errors widget on the CMDB Integrations Dashboard to aggregate by sum of the Count column values.
        -   Enhanced the CMDB Integration Errors widget on the CMDB Integrations Dashboard by implementing cleanup logic for orphan records in the CMDB Integration Execution Error \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error\] and CMDB Integration Execution Audit \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_audit\] tables.
-   **Version 2.15.1 - November 2024**

    New: API now exposed to allow updates to common system properties.

-   **Version 2.14.2 - August 2024**
    -   New: Added a feature for computing partition size for the parallel loading framework in Service Graph Connectors.
    -   Fixed:
        -   Changed the install status of an application to retired when the application was removed or deleted from the source.
        -   Updated the install status of retired applications back to installed when the applications reappear in the import set.
        -   Removed the mandatory check for the connection alias field in common connection framework \(ccf\).
-   **Version 2.14.1 - June 2024**
    -   New:
        -   Added a transform map-based method utilizing the Remove Record Transform Map and the Integration Commons Remove Record \[sn\_cmdb\_int\_util\_remove\_record\] staging table for improving performance when removing records.
        -   Added a cleanup process for deleting older records in for the CMDB Integration Execution Error \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error\] table.
    -   Fixed:
    -   -   Fixed issue when populating Target sys id column value by adding a new column Target Table in the CMDB Integration Execution Error \[sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error\] table.
-   Fixed slow query performance issue when evaluating import log errors against non-CMDB Integration errors using the Create Execution Import Error business rule.
-   Fixed the CMDBIntegrationExecutionRollup script include to check that a valid record is passed in before attempting to update fields.
-   **Version 2.14.0 - May 2024**
    -   Fixed:
        -   Fixed the handling of admMetadata to handle per computer
        -   Fixed 'cleanseIpAddress' function to validate IP addresses with leading zero
        -   Fixed memory issues for software removal in RecordRemoval script
        -   Business rule 'Update CMDB Integration Execution State' was not handling cancelled state
        -   Added related link in common connection framework to test all the connections at once
    -   Removed: Related files of the CMDB Integrations Dashboard.
-   **Version 2.12.0 - February 2024**
    -   New:
        -   Clone Data Source Table access has been updated to execute cache script steps when access is not granted
        -   Added API to edit legacy connections in SGC Central
        -   Added ability to display knowledge articles in the Now Support knowledge base for all connector issues and to direct users to that knowledge base using the Service Graph Connector Support Tools application
-   **Version 2.11.1 - October 2023**

    New: Added an additional parameter "CI Class" in the Cleanse Hardware Model with Model Number operation to support the Enterprise Asset Management classes.

-   **Version 2.11.0 - September 2023**
    -   New:
        -   Updated the data dictionary for missing sections of the model
        -   Updated the hardware cleansing operation to take a model number also as an input
-   **Version 2.10.0 - June 2023**

    Fixed: Added support for a parameter associated with any discovered software applications that were deleted later in an application.

-   **Version 2.9.2 - March 2023**
    -   New:
        -   Mappings coverage tool - Show the mapping covered by ATF tests in a connector.
        -   Add common connection table framework
        -   Add common operation to lookup a CI via source native key
        -   Migrated common ADM code in Integration commons
        -   Software Removal - Create a common API to remove/update records based on the last\_scan on sys\_object\_source
-   **Version 2.8.1 - February 2023**

    Fixed: Fixed report\_view ACLs for platform tables owned by Service Graph.

-   **Version 2.8.0 - May 2022**
    -   New: Added top-level Service Graph Connector module in left-navigation menu in preparation for Service Graph Connectors to move under it.
    -   Changed: Updated Data Dictionary
    -   Fixed:
        -   Cleanse Serial Number now removes invalid values
        -   Inactive users no longer selected for assigned\_to column in the CMDB
        -   Added check for empty userid or emails when looking up users
-   **Version 2.7.0 - December 2021**

    New: Added support for nested data in ATF tests.

-   **Version 2.6.3 - September 2021**

    New: Integration with Apple iTunes Search API for getting high-fidelity publisher and software title information.

-   **Version 2.5.0 - December 2020**
    -   Fixed:
        -   Duplicate manufacturer and model created when manufacturer name is greater than core\_company.name max length.
        -   CMDB Integration Dashboard - Test load 20 records creates a permanent record in the 'Loaded' state so the dashboard always shows it running.
        -   Additional performance improvements.
-   **Version 2.4.1 - September 2020**

    Fixed: Miscellaneous fixes.

-   **Version 2.3.1 - August 2020**
    -   New:
        -   Cleanse Software Instance Name transform
        -   Cleanse Serial Number transform
        -   Implemented content for class-mapping recommendation engine \(in limited preview\)
-   **Version 2.2.0 - June 2020**
    -   New:
        -   Added a transform, Extract and Scale by Units, to extract unit of measure from the data and normalize it to the required unit for that field
        -   Performance improvements
    -   Fixed: The CMDB Integration Dashboard now only displays information CMDB executions.
-   **Version 2.1.1 - May 2020**
    -   The Integration Commons for CMDB scoped application contains a collection of utility functions. These functions provide a common methodology for the processing of key CMDB attributes and is available to all CMDB certified integrations. Using the transforms provided in Integration Commons for CMDB, helps:
        -   Avoid repeating the implementation of frequently-used processing tasks for CMDB attributes.
        -   Reduce variation across different integrations.
    -   Integration Commons also includes the CMDB Integrations Dashboard, which shows rolled up errors and progress details.

**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

