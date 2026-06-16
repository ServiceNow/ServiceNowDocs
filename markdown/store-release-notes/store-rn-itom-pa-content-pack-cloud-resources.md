---
title: Performance Analytics Content Pack for Cloud Resources release notes
description: Version history for the IT Operations Management Performance Analytics Content Pack for Cloud Resources application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-pa-content-pack-cloud-resources.html
release: store
topic_type: reference
last_updated: "2026-01-20"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Performance Analytics Content Pack for Cloud Resources release notes

Version history for the IT Operations Management Performance Analytics Content Pack for Cloud Resources application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.5.1 - January 2026**
    -   Optimized performance and timeout issues in scheduled population jobs by optimizing queries and correcting provider logic.
    -   Improved job execution reliability by preventing older records from being reprocessed after timeouts.
    -   Optimized ITOM job conditions to avoid full table scans and enhanced auto-flush handling by applying safe default retention values.
-   **Version 1.5.0 - November 2024**

    Changed: Applied security fixes and updates.

-   **Version 1.4.2 - August 2024**

    Removed: Cloud Resources dashboard has been deprecated.

-   **Version 1.4.1 - May 2024**

    Fixed: A minor issue.

-   **Version 1.4.0 - November 2023**
    -   Changed: Improved query performance and made the scheduled job run faster to resolve the following issue "CloudResourceDashboardUtil jobs keeps timing out".
    -   Fixed:
        -   Fixed the issue "Cloud Resources Dashboard Shows CI's multiple times for VMware ESX and VM".
        -   Fixed the issue "Regions for cloud service accounts not showing correctly".
-   **Version 1.3.5 - May 2023**
    -   Fixed:
        -   Bug fixes
        -   Memory performance improvement
        -   Added fix script to truncate all the analytic tables including child analytic tables.
-   **Version 1.3.0 - February 2023**

    New: This release is built to support all analytics use-cases for the Cloud Operations Workspace 1.4 app and must be used only with the Cloud Operations Workspace app.

-   **Version 1.2.2 - July 2022**

    Fixed: Performance improvements for scheduled jobs and report rendering

-   **Version 1.2.1 - May 2022**
    -   New: Support for Google cloud in analytics tables
    -   Changed: Recommended to be used with Cloud Operations Workspace \(San Diego\)
-   **Version 1.1.0 - December 2021**

    New: Quality and scale improvements

-   **Version 1.0.5 - November 2020**

    The Performance Analytics Content Pack for Cloud Resources application \(also called Cloud Resource Dashboards\) provides overview visualization of growth trends and inventory counts for cloud resources. With this application, cloud admins can keep track of increases and falls in their cloud configuration items and check on discovery errors \(if any\). The dashboard filters for each cloud also allow for granular tracking of the CI counts for easy reporting and classification.


