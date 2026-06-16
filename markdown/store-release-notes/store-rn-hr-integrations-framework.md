---
title: HR Service Delivery Integrations Framework release notes
description: Version history for the HR Service Delivery Integrations Framework on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-integrations-framework.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# HR Service Delivery Integrations Framework release notes

Version history for the HR Service Delivery Integrations Framework on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.9.2 - June 2026**
    -   Changed: Access control lists \(ACLs\) have been updated to align with current platform security standards.
    -   Fixed: The sn\_hr\_integr\_fw.admin role hierarchy did not resolve as expected due to incorrect role containment.
-   **Version 3.3.4 - November 2021**

    Fixed: Fix for User fields not updated with empty value

-   **Version 3.3.2 - October 2021**
    -   Changed:
        -   Change of the primary field type to Boolean from String
        -   Changing Employee number as coalesce field in HR profile during transform map
        -   Remove assignment ID in "Enterprise Service Management Integrations Framework" application.
        -   Remove work\_phone,work\_mobile, work\_email from jobs staging table
    -   Fixed:
        -   Fixes for Probation period, Country, position code and Notice period not getting populated
        -   Fix for Vendor and Vendor Prefix information missing in "Enterprise Service Management Integrations Framework" application.
        -   Fix for Fields in target table getting cleared during mapping and empty field being ignored during mapping
        -   Fix for mapping of Work Mobile phone not mapped to mobile phone of User
-   **Version 3.3.1 - July 2021**

    New: For HR Service Delivery customers, added commonly used staging tables and transform maps.

-   **Version 3.2.0 - May 2021**
    -   New: Added External Interface to push modified records from ServiceNow to third-party systems.
    -   Changed: The application name has been changed from HR Service Delivery Integrations Framework to Enterprise Service Management Integrations Framework.
-   **Version 2.0.1 - December 2020**
    -   New: Added support to show to-dos in the Now Mobile application.
    -   Fixed: The time window in which modified records are fetched is made uniform for all the services.
    -   Changed: The services will be run in the order specified. Earlier, the order was honored only while transforming records.
-   **Version 1.0.2 - October 2020**
    -   The HR Service Delivery Integration Framework helps users rapidly connect HR Service Delivery with other critical systems and third-party applications. This framework provides a common set of tables, widgets, and APIs, that users can use to build integrations quickly.

    -   Common use cases include pulling employee profile information and to-dos between ServiceNow HR Service Delivery and other third-party applications.
    -   **Note:** Please be sure to check the **Systems Requirements** field for which integrations require this framework.


