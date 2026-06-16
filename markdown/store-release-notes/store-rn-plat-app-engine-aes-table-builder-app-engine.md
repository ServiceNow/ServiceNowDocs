---
title: Table Builder for App Engine release notes
description: Version history for the Table Builder for App Engine application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-app-engine-aes-table-builder-app-engine.html
release: store
topic_type: reference
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ServiceNow AI Platform App Engine release notes, ServiceNow Store release notes]
---

# Table Builder for App Engine release notes

Version history for the Table Builder for App Engine application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 24.0.1 - August 2023**
    -   New: Preferred Reference Tables: When configuring Reference field types, preferred reference tables are grouped and displayed first in the list of options for the field to make it easier to choose commonly-selected reference tables.
    -   Changed: Theming colors in the UI have been updated in Table Builder. Placeholder text was added for empty records in data views to clarify which fields do not contain data. Hover text was added for records that cannot be edited in data views. When you update data in a field record, a popup will notify you that the record has been updated
    -   Fixed: Column headers stay in a pinned position when adding roles and scrolling within Table Builder.
-   **Version 23.1.1 - May 2023**
    -   New:
        -   Added Spreadsheet view a new way to see and interact with your data
            -   Add and edit new datarecords
            -   Filter and sort your datarecords
            -   Added the ability to add/update/deletecolumns and tablerecords
            -   Pin columns
            -   Rearrange columns via drag anddrop
            -   Set column visibility \(hide and unhide\)
        -   Add Schema View functionality:
            -   View your base table and extended relationships up to N-1.
            -   Expand and collapse table nodes
            -   Filter, group and sort your fields globally
            -   View a guidance legend
            -   Use granular, node-level filtering, grouping, and sorting of fields
            -   Open your records within a node
    -   Changed: Spreadsheet view will now be the default view when users create a table.
    -   Removed: Redundant search field in Schema View
-   **Version 23.0.3 - February 2023**
    -   New:
        -   Schema view allows visualization of data relationships for tables in the application.
        -   Table recommendations are now available during table extension.
        -   Data mapping is available when extending a table from a spreadsheet to allow users to select desired data mapping fields or add additional fields before importing spreadsheet data.
        -   User guide was added to PDF extractor to educate users on navigating this interface.
    -   Changed:
        -   The Table tab has been renamed to the Data tab to encompass broader actions under this tab. It now contains Fields and Schema views.
        -   List Field Type support added to PDF extractor to allow the configuration of fields linked to records in a selected reference field.
    -   Fixed: Added multi-select capabilities to reference table popup.
-   **Version 22.1.1 - November 2022**

    New: The PDF Extractor is an interactive, no-code tool that enables users to create a table by selecting fields on a PDF and extracting them for use in the table. It's integrated with Table Builder for App Engine and enables users to easily upload and convert PDFs to tables in custom applications.

-   **Version 22.0.0 - August 2022**
    -   Table Builder for App Engine application is a modern, centralized way to create tables, forms, display logic, and flows. This premium version of Table Builder for App Engine is available only to App Engine v2 licensed customers.
    -   With a modern UI and centralized functionality, developers can perform tasks such as creating new fields on a table, dragging and dropping fields from referenced tables onto a form, configuring field metadata \(such as adding choices to a field\), adding display logic to a form, and building flows that run when records on a table are created and updated tasks that previously required developers to navigate to multiple different builders in the ServiceNow platform all in one place.
    -   Table Builder for App Engine is the premium version of Table Builder \(previously AES Table Builder\) for App Engine v2 licensed customers.

