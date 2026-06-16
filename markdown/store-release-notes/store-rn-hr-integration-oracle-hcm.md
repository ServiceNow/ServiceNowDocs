---
title: HR Service Delivery Integration with Oracle HCM release notes
description: Version history for the HR Service Delivery Integration with Oracle HCM on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-integration-oracle-hcm.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# HR Service Delivery Integration with Oracle HCM release notes

Version history for the HR Service Delivery Integration with Oracle HCM on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.0.11 - March 2026**

    Pulls employee profile information, such as job, department, and location, from Oracle Cloud HCM to ServiceNow on a scheduled basis.

-   **Version 1.0.10 - November 2024**

    Minor bug fixes.

-   **Version 1.0.9 - February 2024**

    Minor fixes.

-   **Version 1.0.7 - July 2023**
    -   This patch version has been certified with Oracle HCM Cloud Spoke 3.3.0.
-   **Version 1.0.6 - November 2022**

    Minor optimization and refactoring

-   **Version 1.0.5 - April 2022**
    -   Fixed:
        -   Changing the name from employee number to employee id in jobs
        -   Fix for employment start date not being populated correctly
        -   For future rehire the profile remains active even if it is terminated
-   **Version 1.0.4 - February 2022**

    Fixed: In subflow "Get Updated Workers", records per page input parameter i.e. "Look up Atom Feeds Employees Update Stream" was missing

-   **Version 1.0.3 - November 2021**
    -   Fixed:
        -   Fixes for few fields are not updated with Delta pull/load
        -   Fix for full load pulling deactivate users
        -   Fix for new hire scenario
        -   Fix for department, employment type and few other fields are not updating in delta load
        -   Fix for User fields not updated with empty values
-   **Version 1.0.2 - October 2021**
    -   Fixed:
        -   Fix for Probation period, Country, position code and Notice period not getting populated at profile level
        -   Fix Vendor and Vendor Prefix information missing in "HR Service Delivery Integration with Oracle HCM" application
        -   Remove population of Work Email in jobs
        -   Add new property workers\_query in "Get All workers" Flow
        -   Fix for multiple primary jobs getting created in full pull
        -   Fix for Position Service is not working
        -   Disable Delta pull of Workers and jobs
        -   Fix for department not populating any value in HR Profile form during full load for the first time
        -   Fix for Personal email getting replaced by work email in Delta pull
        -   Fix for RCA issues with fresh installation of Oracle HCM Fix for storing primary email &amp; primary phones
-   **Version 1.0.1 - July 2021**

    New: Pull worker profile, job profile, department and location information from Oracle Cloud HCM to ServiceNow on a scheduled basis.


**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)

