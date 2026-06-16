---
title: UI Components for Customer Portals release notes
description: Version history for the CSM UI Components for Customer Portals application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-csm-ui-components-cust-portals.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Customer Service Management release notes, ServiceNow Store release notes]
---

# UI Components for Customer Portals release notes

Version history for the CSM UI Components for Customer Portals application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.1.1 - June 2026**
    -   New Feature Enhancement and some defect fixes.
    -   This update includes several new features designed to improve user experience, along with critical defect resolutions to ensure system stability and performance. Specific enhancements focus on optimizing workflow efficiency and addressing reported issues from previous releases.
-   **Version 4.0.0 - February 2026**
    -   New:
        -   Role‑Based and Guest Views: Use the new role\_based\_views and guest\_view options to define different views for different user roles and for unauthenticated users. This removes the dependency on a single static view.
        -   Automatic URL Parameter Passing: URL parameters are now automatically passed into scripts invoked from Data List instance options, allowing admins to build richer, multi‑parameter conditions without extra setup.
        -   Script‑Based View Selection: Use the Data List Condition Script option to choose a view dynamically. Scripts can evaluate URL parameters and other context to determine the most appropriate view at runtime.
        -   Configurable Default Sorting: Define initial sorting behavior using the new sort\_by and sort\_order options so users see a meaningful default order when the list loads.
    -   Fixed: Defect fixes
-   **Version 3.9.3 - December 2025**

    Fixed: Bug fixes.

-   **Version 3.8.1 - October 2025**

    Bug fixes.

-   **Version 3.8.0 - August 2025**

    Bug fixes.

-   **Version 3.7.2 - June 2025**

    Bug fixes.

-   **Version 3.7.0 - May 2025**

    Bug Fixes.

-   **Version 3.6.0 - February 2025**

    New: Added pages with configurable widgets such as FAQ, Browse Taxonomy.

-   **Version 3.5.6 - December 2024**

    Bug fixes.

-   **Version 3.5.0 - August 2024**

    Fixed UI issues in configurable portal widgets.

-   **Version 3.4.1 - May 2024**
    -   Changed:
        -   Improvements to the Portal Data List widget:
            -   Dynamic list: Displays records dynamically based on the configuration provided in the URL parameters \(instead of instance options\). It avoids the need to create duplicate list pages. Now an administrator can use a common page to display records from any table by passing the following URL parameters: table, filter, sort order, view, target view page.
            -   Related list: Displays records related to an entity on the record view page. The data list is configured to identify the entity provided in the URL and accordingly filter the records.
            -   Dynamically selected category: Displays only one of many categories configured on the data list widget, based on the category provided in URL parameters.
            -   Introduced new labels for all the Data List JSON elements.
        -   Improvement to the Portal Object widget:
            -   Added support to edit the object record directly from the widget, if you've the Edit access.
            -   Capability to display information based on the portal page URL when the ID is provided in both portal page URL and instance options.
            -   Displays "-" on the widget for all the labels with empty values.
    -   Bug fixes.
-   **Version 3.3.1 - April 2024**

    Bug fixes.

-   **Version 3.3.0 - February 2024**
    -   New:
        -   Added the Portal Object widget that displays quick actions and key information of a record from the various tables such as product, household, asset, case, account address and more.
        -   Added the Portal Taxonomy Topic widget that displays the first-level taxonomy topics as cards on the widget. It displays articles and catalog items when the topic is accessed on the widget.
    -   Changed:
        -   Added capability to display cart, wish list, guided tour, and scripted list such as notification, approval, and survey on the header of your portal.
        -   Enabled mobile support for the Portal Mega Menu widget.
    -   Minor fixes.
-   **Version 3.2.1 - January 2024**

    Minor fixes.

-   **Version 3.2.0 - November 2023**
    -   New:
        -   Added Browse Taxonomy widget support to enable navigation to different knowledge articles and catalog items.
    -   Fixed:
        -   Fixes
-   **Version 3.1.1 - September 2023**

    The ServiceNow UI Components for Customer Portals application improves the Service Portal experience for customer service portals by providing a library of configurable components that offer better reusability, performance, and upgrade scalability. These new components can replace your existing portal widgets in the customer portals.


