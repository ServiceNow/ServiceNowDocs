---
title: Event Management Core release notes
description: Version history for the Event Management Core on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-event-management-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Event Management Core release notes

Version history for the Event Management Core on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 23.16.0 - June 2026**

    Changed: Enhancements to support Proactive grouping recommendations

-   **Version 23.15.10 - May 2026**

    New: Improve regex error message

-   **Version 23.14.3 - March 2026**
    -   New:
        -   Enhanced grouping experience in Alert Automation:
            -   Additional grouping criteria: Related log properties \(HLA\) and Impacted service instance
            -   Advanced Options: Minimum threshold, seed alert option
-   **Version 23.14.1 - January 2026**

    Fixed: Removing admin ACL from sn\_em\_ai\_alert\_resolution table.

-   **Version 23.13.0 - December 2025**

    Fixed: Fixing performance issues in the \[sn\_em\_ai\_changed\_service\] table.

-   **Version 23.12.2 - August 2025**
    -   New: New tables and scheduled jobs to calculate AIOps Dashboards indicators
    -   Fixed:
        -   Mute alert not working for HLA alerts
        -   Alert tags are removed when ACK of closing alerts in the Express List
-   **Version 23.6.2 - May 2025**
    -   Changed:
        -   HLA alerts will no longer include ReadOnly alerts or multiple events.
        -   The new HLA alert model generates a single alert per service, simplifying visualization and improving the operator experience by reducing unnecessary complexity.
-   **Version 23.4.7 - February 2025**
    -   New: Support new role for team operator \(evt\_team\_operator\) that allows adding new Alert Automations, and getting segregated views in the Service Operations Workspace.
    -   Changed:
        -   Adding additional CI fields on the Express List
        -   Modifying Event Management menu items
    -   Fixed: Minor fixes
-   **Version 23.4.5 - December 2024**

    No updates.

-   **Version 23.4.3 - November 2024**

    No updates.

-   **Version 23.3.1 - August 2024**

    Fixed: Fix ACLs on various tables.

-   **Version 23.2.1 - June 2024**

    New: Add support for team-based alert clustering definition.

-   **Version 23.1.2 - March 2024**

    Fixed: Fixing installation dependency.

-   **Version 23.1.1 - March 2024**
    -   Changed: Adding preconfigured alert tags for common attributes.
    -   Fixed:
        -   Handle exception in EvtMgmtAlertCrawler and EMLicensingUtilWrapper - cross-scope privileges are missing
        -   Missing OOB \`report\_view\` ACLs for "sn\_em\_ai\_agg\_alert\_queue, sn\_em\_ai\_alert\_cis, sn\_em\_ai\_alert\_services, sn\_em\_ai\_alert\_tags" tables
        -   The alert screen shows the wrong description for the custom alert.
-   **Version 22.3.4 - November 2023**
    -   New:
        -   Supporting tables for the Express List
        -   New job to sync the supporting table data to the express list
-   **Version 22.1.2 - August 2023**
    -   New: Add a new Tag Cluster overview screen to the alert form in Service Operations Workspace \(starting in Vancouver\).
    -   Changed: Adding new alert tags for HLA alerts.
    -   Fixed: Fixing translation files.
-   **Version 22.0.2 - May 2023**

    Fixed: Fixing highlighted text for pattern metric.

-   **Version 21.1.3 - February 2023**
    -   Fixed:
        -   Remove the Alert Intelligence link for new installations
        -   Fix the mute alert action
        -   Add/remove alerts to a group is missing when the language is changed
-   **Version 19.7.8 - November 2022**
    -   Fixed:
        -   Impacted services and offerings count is incorrect
        -   Alert actions tab appears stuck while loading
        -   Alert actions tab repeatedly refreshes when the action is in error state
-   **Version 19.6.13 - August 2022**
    -   New:
        -   New API to retrieve related Service Offerings of an alert and retrieve the business/technical service portfolio
        -   Support 'Raise' ML feedback for Health Log Analytics alerts
    -   Changed: Remove group icon from Alert header
    -   Fixed:
        -   The dynamic CI service form missing alerts related list
        -   Metric name field is missing from alert details
        -   Fixing anomaly card text
-   **Version 19.5.7 - May 2022**
    -   New:
        -   Foundations and APIs for Service Operations Workspace
        -   New API to retrieve associated Service Offerings
-   **Version 19.4.7 - December 2021**
    -   Fixed:
        -   Handling error 500 in metric explorer screen
        -   Fixed values in custom anomaly alert card
        -   Fixed privileges when calling Clotho
        -   Alert overview details card
        -   Updated Domain field in the Alert Extra Data table
        -   Alerts now showing for the Dynamic CI Group service
-   **Version 19.3.8 - July 2021**
    -   New: Adding domain for log analytics alerts Add support for binding based on FQDN for log analytics alerts
    -   Fixed: Tune metric types visualization for log analytics alerts Fix log analytics groups binding to a CI Inadequate ACL for "points\_to\_alert" table
-   **Version 19.2.8 - March 2021**
    -   Changed: Improve KB to alert matching logic
    -   Fixed:
        -   Overview tab for manual and rule-based groups
        -   Styling fixes to cards in the overview tab
        -   Fixing links from overview tab to surrounding log card, probable root cause card and identified issues card
        -   Fixing alert feedback modal texts
        -   Alert layout for CI-less alerts
        -   Alert creation time for log analytics alert
        -   Fixing Alert reopen error
        -   Validate ACL for 'EvtMgmtProcessFeedback' Script
-   **Version 19.1.3 - January 2021**
    -   New:
        -   The Event Management Core app enables you to track and monitor alerts in the ServiceNow Agent Workspace. It allows operators to navigate and drill down to Alerts and Alert Groups. Workspace lists are there to help the user to view the top priority alerts considering the Alert priority calculation.
        -   The Alert Overview tab summarizes the most significant information about the alert and its impact on the application services. The actions side bar enables the user to execute remediation subflows and launch related app directly from the alert form.

**Parent Topic:**[ServiceNow Store - ITOM AIOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-ai-ops-landing.md)

