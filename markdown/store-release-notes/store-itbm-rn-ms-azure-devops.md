---
title: Microsoft Azure DevOps integration for Agile Development release notes
description: Version history for the Microsoft Azure DevOps integration for Agile Development on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-ms-azure-devops.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Microsoft Azure DevOps integration for Agile Development release notes

Version history for the Microsoft Azure DevOps integration for Agile Development on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.7.1 - March 2026**

    Fixed an issue where the default Area Path was not automatically populated when a team was selected during work item creation. The Area Path now correctly defaults based on the selected team's configuration.

-   **Version 1.7.0 - December 2025**

    Performance improvements.

-   **Version 1.6.2 - August 2025**

    Fixed: Issues with duplicate work notes generated in SPM, when linking related items to a story in Azure DevOps and commenting in parallel.

-   **Version 1.6.1 - June 2025**
    -   Fixed:
        -   Addressed an out-of-order update issue occurring during rapid consecutive updates to the same record.
        -   Resolved an image synchronization problem when attaching images to HTML fields.
-   **Version 1.6.0 - November 2024**
    -   New: Support for OAuth authentication protocol for integration between Azure DevOps and Agile Development 2.0
    -   Fixed: Fixed issue with Azure DevOps integration when Area Path is updated in ADO for an AzureDevOps work item
-   **Version 1.5.5 - September 2024**

    Bug fixes.

-   **Version 1.5.4 - May 2024**

    Minor fixes related to features like bulk import and real time sync.

-   **Version 1.5.3 - February 2024**

    Minor bug fixes for issues around import, export and mapping.

-   **Version 1.5.2 - May 2023**
    -   Following issues have been fixed:
        -   Creation of duplicate records
        -   Clearing sprint field when sync\_sprint field is disabled
        -   Clearing Description and Acceptence criteria fields on the ADO.
-   **Version 1.5.1 - February 2022**

    Fixed: Bug fixes.

-   **Version 1.5.0 - June 2021**
    -   Changed:
        -   Support for multi-select fields in Azure integration.
        -   Improved troubleshooting and updated log details.
-   **Version 1.4.2 - April 2021**
    -   New:
        -   Agile Release Train field does not appear in Azure DevOps Projects when mapping exists for tables extending SAFe Story
        -   Duplicate External IDs are created when work items are converted from one type to another in Azure DevOps
-   **Version 1.4.1 - March 2021**
    -   New:
        -   Support for synchronization of SAFe Sprints with Microsoft Azure DevOps
        -   Native support for export of SAFe entities \(SAFe Story, SAFe Feature and SAFe Epic\)
        -   Support for following additional field types in field mapping
            -   Date Time
            -   Reference Field
        -   Support for two-way sync of Assignee field
        -   Support for two-way sync of Work Notes
-   **Version 1.3.0 - July 2020**
    -   New: Process-level mappings: Table, field, and workflow state mapping are supported for Azure DevOps projects of default and custom process types.
    -   Changed: Instance-level mapping: Map configuration for Azure DevOps projects is no longer generated at the instance level.
    -   Fixed: Minor bugs
-   **Version 1.2.1 - May 2020**

    Fixed: Performance bug fixes.

-   **Version 1.1.0 - April 2020**
    -   New: Support for Iterations
    -   Fixed: Bug fixes
-   **Version 1.0.0 - February 2020**

    Integrate Microsoft Azure DevOps Boards with ServiceNow Agile Development to enable bidirectional synchronization of records between the two applications.


