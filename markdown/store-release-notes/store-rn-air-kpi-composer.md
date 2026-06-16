---
title: KPI Composer release notes
description: Version history for the Now Intelligence KPI Composer on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-air-kpi-composer.html
release: store
topic_type: reference
last_updated: "2022-02-03"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Platform Analytics release notes, ServiceNow Store release notes]
---

# KPI Composer release notes

Version history for the Now Intelligence KPI Composer on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.1.1 - February 2022**
    -   Fixed:
        -   Security issues
        -   Issues with the Next Experience UI
-   **Version 4.1.0 - December 2021**

    New: Import and export KPI Composer projects

-   **Version 4.0.0 - November 2021**

    New: You can now generate a task to create a Performance Analytics object for every KPI Composer artifact you define in a project. All tasks in a project are automatically assigned to the user group of your choice.

-   **Version 3.0.3 - August 2021**

    Fixed: KPI composer was triggering full table scans and ACL evaluations on all records in Knowledge \[kb\_knowledge\] and User \[sys\_user\] tables when no entity in a project had an attached knowledge article or user, respectively.

-   **Version 3.0.1 - June 2021**
    -   New:
        -   Dashboard Tab Templates: Design a dashboard tab and save it as a reusable template. Both the row layout and the canvases are saved in the template. You can then insert that tab into any dashboard, including those in other projects. You can modify a dashboard tab you have created from a template without affecting the template itself.
        -   Library elements: Save part of a KPI tree and reuse it in the Analysis tab of any project. You can select, edit, or delete these library elements. Library elements by default are only for their creator's use, but an administrator can make them individually available to all KPI Composer users.
-   **Version 2.1.2 - December 2020**
    -   New:
        -   Widget types: Reporting, Content Block, Interactive Filter, and Spotlight join original Performance Analytics.
        -   Report definitions: Specify the facts table or report source for a developer to build a report. Provide a report definition for any artifact associated with a Reporting widget. Joins original Performance Analytics indicator definitions.
    -   Changed:
        -   Elements renamed Artifacts, to prevent confusion with breakdown elements.
        -   Dashboard Design tab renamed Dashboard Visualizations.
        -   Indicator Definition tab renamed Data Definitions, because it now includes Report Definitions.
        -   Dashboard canvasses can contain multiple artifacts.
        -   To replace a widget on a canvas, you can drag another widget on top of it.
        -   Indicator definition forms show the details of the linked indicator, if one is specified.
        -   Definition forms have a field to give instructions to the developer.
        -   The positions of breakdown definitions and personas at the top of the Analysis and Dashboard Visualization tabs have been reversed.
    -   Fixed: The title of new widgets is blank instead of containing the widget position.
-   **Version 2.0.4 - February 2020**

    Fixed: Security improvements and minor bug fixes

-   **Version 2.0.3 - December 2019**

    KPI Composer ensures that your performance management strategy aligns with business goals and has support from executive sponsors. Using KPI Composer, you’ll visually define and connect organizational goals to critical success factors and specific process measurements before performing any technical configuration of Performance Analytics.


