---
title: Strategic Spend Tracking for PPM release notes
description: Version history for the IT Business Management Strategic Spend Tracking for PPM on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-strategic-spend-tracking.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Strategic Spend Tracking for PPM release notes

Version history for the IT Business Management Strategic Spend Tracking for PPM on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.3.0 - June 2026**
    -   New:
        -   Non-Glide Query Access Controls
            -   Added query-level access control lists \(ACLs\) for areas not previously covered by automated tooling. These ACLs address blind query vulnerabilities across the ServiceNow platform and are now embedded directly in source code for each affected application.
            -   After installing or upgrading affected applications, query access controls are automatically restored without requiring a manual security audit. ACL definitions are now discoverable in source code, improving maintainability and forward compatibility.
-   **Version 1.2.0 - December 2025**

    Changed: Users with the pps\_admin role can now update system properties related to Strategic Spend Tracking.

-   **Version 1.1.0 - May 2024**

    Changed: The old dashboard has been migrated to the Next Generation dashboard. A new module Analytics has been added under the application module "Strategic Spend Tracking for PPM" that redirects to the next experience dashboard.

-   **Version 1.0.2 - February 2023**

    Fixed:

    -   Supported translations and also optimized the application to improve the build, test and provisioning time.
    -   Added report view ACLs for "Strategy Allocation Breakdown" and "Goal Allocation Breakdown" tables. This allows users who have access to those tables, to see only aggregate data from those tables.
-   **Version 1.0.1 - July 2020**
    -   Fixed:
        -   Missing navigation link to Strategic Spend Dashboard
        -   Changing of the Project and Demand Default view scope
        -   Missing recalculation option for inactive projects and demands
-   **Version 1.0.0 - May 2020**
    -   Enables you to align your projects and demands with organizational strategies and goals. You can allocate a percentage of the demand or project’s total cost and benefits towards achievement of one or multiple strategies and goals.
    -   This information gets shown through a dashboard enabling you to visualize your projects, which are aligned to organizational strategies and goals, your planned and actual spend and also potential benefits you will realize through these projects. Additionally, you can also drill into a specific strategy or goal and visualize planned and actual spend along with the potential benefit.

**Parent Topic:**[ServiceNow Store - Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itbm-highlight.md)

