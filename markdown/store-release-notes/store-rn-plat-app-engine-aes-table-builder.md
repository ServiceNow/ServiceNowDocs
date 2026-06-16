---
title: Table Builder release notes
description: Version history for the Table Builder on the ServiceNow Store .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-app-engine-aes-table-builder.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - ServiceNow AI Platform App Engine release notes, ServiceNow Store release notes]
---

# Table Builder release notes

Version history for the Table Builder on the ServiceNow Store .

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.2.1 - June 2026**

    Changed: Maintenance release.  No customer facing changes.

-   **Version 29.1.1 - March 2026**

    Changed: Inline form configuration changes

-   **Version 28.2.1 - December 2025**
    -   Changed:
        -   Granular configuration admin roles
            -   Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.
-   **Version 28.1.1 - August 2025**

    Maintenance release.

-   **Version 26.3.2 - June 2025**

    Fixed: Addressed several cross-scope issues around save functionality and the override property.

-   **Version 27.2.2 - May 2025**
    -   New: Developer can type tablename.builder \(field view\) / tablename.view / tablename.flow / tablename.sheet in the SNS Search box or Application Navigator to launch Table Builder with the appropriate table opened.
    -   Changed: All table creation will require a role with ACL permissions in order to be created. Previously some of the paths to creation were inconsistently applying this pattern.
-   **Version 27.1.2 - February 2025**

    Maintenance update.

-   **Version 26.2.5 - November 2024**
    -   Fixed:
        -   Issue with adding a field from the field view in some scenarios
        -   Delegated Dev user create table issues from spreadsheet &amp; PDF
        -   Automapping for transform due to session scope issues
-   **Version 26.0.11 - October 2024**

    Bug fixes.

-   **Version 25.1.1 - May 2024**

    Fixed: RTE field created via App Engine Studio not working as expected.

-   **Version 25.0.3 - February 2024**
    -   New:
        -   Access Form Builder from the additional actions menu on any form on the ServiceNow AI Platform, and from the related links section of any table.
        -   Easy access to Form Builder from within UI Builder, via an edit form functionality.
    -   Changed: Table Builder for App Engine application has been combined with the Table Builder application, therefore features such as schema view, spreadsheet view, flows, and PDF extractor which were previously only available in Table Builder for App Engine are now fully available within Table Builder.
-   **Version 24.1.1 - November 2023**
    -   New:
        -   Added Form Builder link in the configure menu option of platform.
        -   Added Form builder link in the related links menu option of platform.
        -   Implemented builder flags to show/hide features in Table Builder .
        -   Added the ability to auto install Table Builder with Family True-up \(active in Washington Family\) .
    -   Changed:
        -   Improved Schema Builder loading time by 9 seconds by replacing multiple API calls with a single API call dedicated only to Schema View.
        -   Updated Standalone Form Builder to only load with the Form Builder Header and banner.
    -   Fixed: We now prevent Form Builder users from being able to edit a section in the application scope when the original form is in another scope when in Form Builder for platform.
    -   Removed: Removed one of the two create field buttons within the data import wizard.
-   **Version 24.0.2 - August 2023**
    -   New: Preferred Reference Tables: When configuring Reference field types, preferred reference tables are grouped and displayed first in the list of options for the field to make it easier to choose commonly-selected reference tables.
    -   Changed: Theming colors in the UI have been updated in Table Builder. Placeholder text was added for empty records in data views to clarify which fields do not contain data. Hover text was added for records that cannot be edited in data views. When you update data in a field record, a popup will notify you that the record has been updated
    -   Fixed: Column headers stay in a pinned position when adding roles and scrolling within Table Builder.
-   **Version 23.0.3 - February 2023**

    Changed: The Table tab has been renamed to the Data tab to encompass broader actions under this tab.

-   **Version 22.1.2 - November 2022**
    -   New:
        -   Search for field columns in a table by using the search bar in the Table tab.
        -   Access a filterable list of form views using the new navigation experience in the Forms tab additional actions list \(ellipsis menu\).
-   **Version 22.0.3 - August 2022**
    -   New: This application now displays as Table Builder in the ServiceNow Store instead of AES Table Builder.
    -   Changed: Make fields on a form inactive and prevent them from displaying in the available list of fields in the form editor. Inactive fields may be reactivated from the Table tab
-   **Version 21.1.2 - May 2022**
    -   New:
        -   New multiselect to add fields to Forms in bulk
        -   New configuration side panel in Table toggle for consistent field editing experience between Table and Form views. When switching between Table and Form views, field will remain in context of the side panel when present on the Form stage.
    -   Fixed:
        -   Fixed the ability to select a reference table when creating a list type field
        -   Fixed Reverse if False under advanced settings in policy setup to be enabled by default
-   **Version 21.0.3 - March 2022**
    -   New:
        -   Merged with the new Form Builder to create a single, integrated experience
        -   Updated "Type" to be mandatory and set "String" to be the default type when adding a new field
        -   Updated to display dictionary overrides
    -   Changed:
        -   Replaced the table\_builder.user role with the personalize\_dictionary role
        -   Changed Field Name to be read only after field creation to be consistent with Platform
    -   Fixed: Field name fixed to be read only after field creation to be consistent with Platform
-   **Version 19.0.4 - March 2021**

    New: Low code interface for building ServiceNow tables


**Parent Topic:**[ServiceNow Store - ServiceNow AI Platform App Engine release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-app-engine.md)

