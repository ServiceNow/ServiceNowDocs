---
title: SharePoint Online Search Connector release notes
description: Version history for the HR SharePoint Online Search Connector application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-sharepoint-online-search-connector.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# SharePoint Online Search Connector release notes

Version history for the HR SharePoint Online Search Connector application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.1.2 - November 2024**

    No new improvements.

-   **Version 6.0.2 - August 2024**
    -   Granular Site Access Control New Sites. Selected permission is added for administrators to grant selective access to individual sites.
    -   Microsoft 365 Group Support SharePoint Online Search Connector now reads users and their permissions from Microsoft 365 groups, eliminating the need for managing site permissions manually with SharePoint groups.
    -   Other: SharePoint Online Search Connector now supports everyone except external users, enabling end-users to access information from company-wide sites.
-   **Version 5.0.10 - May 2024**

    No new feature was delivered in May '24.

-   **Version 5.0.2 - February 2024**
    -   Flexible Permission: Option to setup SharePoint connector with read only or full control permission to SharePoint.
    -   Selective Indexing: Administrators now have the option to exclude specific sites from being indexed.
    -   Index Published Versions: Option to index only the published versions of documents.
-   **Version 3.1.3 - October 2023**

    Release v3.1.3, which includes two important fixes as below:

    -   SharePoint search connector file permissions not working for site collection sites/&lt;siteName&gt;
        -   Previously, search used to work only for root sites due to incorrect handling of file permissions for site collection sites/&lt;siteName&gt;. We have fixed this issue, and now SharePoint search is functioning as expected for all site collection sites and honoring the file permissions defined in SharePoint accurately.
    -   Users directly added to file permission in SharePoint are not able to search files in Employee Center portal.
        -   Users who were directly added to file permissions in SharePoint were unable to search for files in Employee Center. As part of this fix, users who have been added to file permissions in SharePoint can now successfully search for files in the EC portal without any issues.
-   **Version 3.1.2 - May 2023**

    Fixed: Bug fixes.

-   **Version 3.0.1 - February 2023**

    Changed: Improved setup process as well as performance and scalability of indexing.

-   **Version 2.0.2 - November 2022**

    SharePoint Online Search Connector allows your employees to search and discover content from ServiceNow. You can index content from multiple sites, enabling employees to find the right answers through Employee Service Center, Now Mobile, and Virtual Agent.

-   **Version 1.0.1 - February 2021**
    -   New:
        -   Search internal public SharePoint sites, pages, and files.
        -   Select multiple public SharePoint sites for indexing.
        -   Integrate with AI Search engine.
        -   Support Public SharePoint Content that is available to all employees.
        -   Enable support across multiple channels: Employee Service Center, Service Portal, Now Mobile app, and Virtual Agent.

