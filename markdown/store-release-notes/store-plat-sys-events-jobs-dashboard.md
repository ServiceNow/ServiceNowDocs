---
title: System Events and Jobs Dashboard release notes
description: Version history for the System Events and Jobs Dashboard on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-plat-sys-events-jobs-dashboard.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Operations Shared apps for release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# System Events and Jobs Dashboard release notes

Version history for the System Events and Jobs Dashboard on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.1.5 - March 2026**
    -   Changed: "Job lateness" is now "Job wait time"
    -   New: Granular roles and permissions to control access to the dashboard information
    -   Fixed:
        -   An issue where charts in the Current Score and Trends sections failed to load on the System Events and Jobs Dashboard
        -   An issues where the Gear icon in the System Event Processing Health Checks section was non-functional, preventing users from configuring event processing alerts
        -   An issue where filtering by queue name or interval start/end times via the global filter did not update the Event Processor Statistics table
        -   An issue where the ux\_macroponentrequired an explicit adminrole check in addition to the granular admin role for proper access control
-   **Version 3.0.7 - January 2026**

    Fixed charts under the trends section and total error count under the current score section, which were not loading

-   **Version 2.0.5 - September 2024**
    -   Fixed: Fixed issue where Average Processing Time was not reporting accurate values consistently
    -   Removed: Minor UI update to remove unnecessary icon
-   **Version 2.0.4 - August 2024**
    -   New overall:
        -   Updated dashboard application design layout to support Next Experience UI
        -   Updated modules in Filter Navigator to improve navigating to the individual dashboards
            -   Dashboard is found under System Diagnostics
                -   System Events &amp; Jobs Dashboard
                    -   System Events
                    -   Scheduled Jobs
            -   added links to the dashboard application from:
                -   sys\_trigger
                -   sys\_scheduler\_job\_history
                -   scheduler\_job\_history\_node
                -   sysauto
    -   Added a feedback mechanism
    -   Scheduled Jobs dashboard page changes
    -   -   Added time range, job classification and priority filters to visualizations
-   Default time range set to 24 hours
-   Added stuck jobs and permanent error score cards
-   Updated visualizations to be at instance level
    -   System Events dashboard page changes
        -   Added processing framework jobs score card
-   **Version 1.1.3 - October 2023**

    Fixed: Scheduled jobs pending and running jobs count is displaying 0 when read-replica lag is observed.

-   **Version 1.1.1 - September 2023**
    -   Fixed:
        -   Event Processing Jobs behind schedule count is inaccurate when events process 0 job is disabled
        -   Job Classification Trends list views display empty row counts due to an invalid query
-   **Version 1.1.0 - August 2023**

    System Events and Jobs Dashboard is a brand new application available on Vancouver instances.


