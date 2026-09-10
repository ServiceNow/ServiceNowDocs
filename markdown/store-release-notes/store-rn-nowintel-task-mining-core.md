---
title: Task Mining Core release notes
description: Version history for the Task Mining Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-nowintel-task-mining-core.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Platform Analytics version history release notes, ServiceNow Store version history release notes]
---

# Task Mining Core release notes

Version history for the Task Mining Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.2.23 - September 2026**
    -   Changed: The activity categorization experience is redesigned to make it faster and more intuitive to review event data and build categorization rules.
        -   Search, sort, and filter user activity data directly in MAX view.
        -   Build rules with a guided condition builder instead of writing rule logic.
        -   See how your events are distributed across the rules you defined at a glance.
-   **Version 4.1.8 - August 2026**

    Included the fixes for Otto re-branding, as well as Report View ACL-related fixes. No features included.

-   **Version 4.1.7 - July 2026**

    New: Screenshot capture for user-initiated tasks in Task Mining Continuous and Targeted modes.

-   **Version 4.1.3 - June 2026**

    Task Mining workstation users now capture both steps and desktop actions automation properties \(screen recordings\) in a single recording session, instead of recording the same process twice. When a task mining analyst submits an automation request, the recording is delivered to the automation team with all UI properties needed to build desktop actions.

-   **Version 3.2.3 - May 2026**

    What is changed: Fixed a back port record, BAK0110748, to incorporate the Automation Center changes

-   **Version 3.2.2 - March 2026**
    -   New:
        -   Introduced Task Mining project creation from Process Mining Workspace - Analysts can create a prefilled Task Mining project from the Analyst Workbench by selecting a process flow node or Improvement opportunity.
        -   Introduced Guided Project Setup Flow - New step-by-step experience for creating and editing Task Mining projects with structured navigation, validation, and ordered configuration steps.
        -   Introduced Recording Type Configuration - Project-level control over recording mode: Continuous \(default\) and Targeted \(manual start/stop\).
        -   Introduced UI object-level data capture - Captures detailed UI interaction data \(e.g., button clicks, field entries\) from supported applications, improving Task timeline analysis.
        -   Introduced Unified Project Page - Centralized view with at-a-glance project details, analyses, status, contextual actions, and notification banners.
        -   Introduced Task timeline analysis - Detailed, editable view of collected task activities serving as the basis for task improvement actions.
        -   Introduced task improvement actions and automation request - Analysts can initiate an automation request directly from a Task timeline analysis.
    -   Changed:
        -   Improved Stacked Bar Chart - Updated with precise visualizations, drill-down capabilities, and context-aware tooltips.
        -   Updated Over Midnight Activities Handling - 'Lock' or 'Private' activities over 2 hours past midnight are now classified as 'Off', improving work/non-work time accuracy.
-   **Version 3.1.9 - December 2025**
    -   New: Introduced a configurable date range \(7 days by default\) for data aggregation on the Categorization page to allow power users to reduce data volume in order to prevent browser request failures with large datasets.
    -   Changed: Updated link to macOS agent to ensure users have access to the latest version.
    -   Fixed:
        -   Fixed issue where the business rule to view project lists was incorrectly applying to Sys Admin instead of Task Mining Admin role. Now, only users with the Task Mining Admin role can see all projects.
        -   Fixed issue where Task Mining entries appeared in the All menu for users without TM roles.
        -   Fixed issue where mining jobs completed without errors but failed to identify task instances due to environment-specific configuration.
-   **Version 3.1.7 - September 2025**

    Task Mining helps analysts and process owners understand everyday processes that drive business outcomes, identify inefficiencies in external activities and internal tasks, and make data-driven decisions to improve productivity. Gain insights into the effectiveness and specifics of how time is spent by workstation users with an analysis of how workstation users engage with processes. Continuous process optimization should be accessible to every organization, empowering them to operate smarter, faster, and with more transparency. Task Mining achieves this through its market-leading capability to gather structured data.


**Parent Topic:**[ServiceNow Store - Platform Analytics version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-air.md)

