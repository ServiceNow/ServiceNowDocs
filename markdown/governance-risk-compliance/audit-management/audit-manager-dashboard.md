---
title: Audit Manager Performance Analytics dashboard
description: The Audit Manager dashboard provides the current view of audit engagements and related audit activities. Users with the sn\_audit.manager role can view this dashboard. This Audit Manager dashboard is part of the Advanced GRC dashboard.
locale: en-US
release: xanadu
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Analytics and Reporting Solutions for Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# Audit Manager Performance Analytics dashboard

The Audit Manager dashboard provides the current view of audit engagements and related audit activities. Users with the sn\_audit.manager role can view this dashboard. This Audit Manager dashboard is part of the Advanced GRC dashboard.

## Audit Manager dashboard

**Important:** Starting with version 18.1.5 of the Audit Management application the Audit Manager dashboard is available in the Next Experience UI Framework.

If you are on Vancouver or Washington DC, you can view the dashboard in the Next Experience UI Framework.

![A short video featuring the different tabs in the Audit Manager dashboard.](../image/audit-manager-db-washingtondc.gif)

**Note:** For detailed reports on the audit activities, see the following tables.

To open the dashboard in the Next Experience UI Framework, navigate to **All** &gt; **Audit** &gt; **Analytics Audit Manager Dashboard**.

The Audit Manager dashboard provides detailed reports that capture audit activities, for example:

-   Overview of various open and closed engagements
-   Overview of audit tasks and control test status
-   Overview of audit issues and control test failures
-   Active remediation tasks
-   Closed audits
-   Data quality of audits

This dashboard provides useful answers to the following questions:

-   What are the open, past due, closed, and upcoming audits? What is the audit engagement date range? Who are the audit tasks assigned to?
-   What are the key audit engagements? Are the engagement results adequate or satisfactory?
-   What are the various audit tasks? What is the percentage of task completion?
-   How many tests are completed over given time?
-   Are the issues and remediation tasks completed on time?

Users with the sn\_audit.manager role can view and adjust a report chart by grouping or stacking data. To group and stack audits and their activities, use common filters such as State, Assigned to, Result, and Name.

Various interactive filters are provided to further refine reports. For example, use the Assigned to filter to view the audits assigned to Abel Tuter.

The **Overview** tab provides a color-coded bar chart report. It displays the latest view of the audit engagements and audit activities such as audit tasks, issues, and remediation tasks. You can further drill down in the individual reports.

Use the following interactive filters to filter data on the **Overview** tab reports:

-   Assigned to
-   Audit Engagement Date

The **Audit Engagements** tab provides an overview of the audit engagements and displays the following reports.

|Reports|Description|
|-------|-----------|
|Open Audits|Number of audit engagements which are open|
|Past Due Audits|Past due audits over time|
|Upcoming Audits|Monthly count for the upcoming audit engagements|
|Started Audits|Monthly count for the audit engagements that have been started|
|Closed Audits|Closed audit engagements|

Use the following interactive filters to filter data on the **Audit Engagements** tab reports:

-   Assigned to
-   Audit Engagement Date

The **Task Management** tab provides an overview of the audit tasks and displays the following reports.

|Reports|Description|
|-------|-----------|
|Active Tasks|Number of active tasks|
|Past Due Tasks|Past due tasks|
|Tasks Due This Week|Tasks that are due in a given week|
|Upcoming Audit Tasks|Upcoming audit tasks|
|Tasks Completed On-Time|Number of tasks completed by the users on time|
|Tasks Completed After Planned End date|Tasks that are completed after the planned end date|
|Tasks Completed|Number of tasks completed over time|

Use the following interactive filters to filter data on the **Task Management** tab reports:

-   Assigned to
-   Audit Engagement Date
-   Task Type

    The example task types are interviews, walkthroughs, activities, and control tests.


The **Control Testing** tab provides detailed information on control tests. On further drill down, you can view detailed information about the control tests. This tab displays the following reports.

|Reports|Description|
|-------|-----------|
|Active Tests|Number of active tests|
|Past Due Tests|Number of past due tests|
|Tests Due This Week|Tests that are due in a given week|
|Upcoming Tests|Upcoming control tests|
|Tests Completed On-Time|Number of tests completed on time|
|Tests Completed After Planned End date|Tests that are completed after the planned end date|
|Open Tests by Week|Tests that are open in a given week|
|Tests Completed by Month|Number of tests completed in a month|

Use the following interactive filters to filter data on the **Control Testing** tab reports:

-   Assigned to
-   Audit Engagement Date
-   Operation Effectiveness
-   Design Effectiveness

The **Issues** tab provides an overview of all the issues that are created under audit and the issues that are generated due to control test failures. This tab displays the following reports.

|Reports|Description|
|-------|-----------|
|Active Issues|Number of active issues assigned to different users|
|Past Due Issues|Past due issues assigned to different users|
|Issues Awaiting response|Issues that are open and awaiting response|
|Issues Due This Week|Issues that are due in a given week|
|Upcoming Issues|Number of upcoming issues|
|Issues Completed Before Planned End date|Issues that are completed before the planned end date|
|Issues Completed After Planned End date|Issues that are completed after the planned end date|
|Issues Completed On-Time|Number of issues completed on time by the users|
|Issues Completed by Month|Number of issues completed in a month|

Use the following interactive filters to filter data on the **Issues** tab reports:

-   Assigned to
-   Audit Engagement Date
-   Issue Entity
-   Issue State
-   Issue Priority
-   Issue Response

The **Remediation** tab provides an overview of the remediation tasks created for the audit issues and displays the following reports.

|Reports|Description|
|-------|-----------|
|Active Remediation Tasks|Number of active remediation tasks|
|Past Due Planned Remediation|Number of past due remediation tasks|
|Remediation Tasks Due This Week|Remediation tasks that are due in a given week|
|Upcoming Remediation Tasks|Remediation tasks that are forthcoming|
|Remediation Tasks Completed Before Planned End date|Remediation tasks that are completed before the planned end date|
|Remediation Tasks Completed After Planned End date|Remediation tasks that are completed after the planned end date|
|Remediation Tasks Completed On-Time|Number of remediation tasks completed on time by the users|
|Remediation Tasks Issues Completed by Month|Number of remediation tasks completed in a month|

Use the following interactive filters to filter data on the **Remediation** tab reports:

-   Assigned to
-   Audit Engagement Date
-   Remediation Task Priority

The **Data Quality** tab provides the reports to validate whether the data for audits, audit issues, remediation tasks, and control tests is captured in a correct manner. This tab displays the following reports.

|Reports|Description|
|-------|-----------|
|Active Audits No Assignee|List of unassigned active audits|
|Audits Without Tasks|List of audits without tasks|
|Active Audits No Entity|List of active audits with no entities|
|Audit Task No Assignee|List of unassigned audit tasks|
|Operation Test No Result|List of operation tests with no results|
|Active Audits No Description|List of active audits with no description|
|Design Test No Result|List of design tests with no results|
|Issues No Description|List of issues with no description|
|Control Test No Assignee|List of unassigned control tests|
|Issues No Assignment Group|List of issues with no assignment group|
|Issues No Remediation Tasks|List of issues with no remediation tasks|
|Control Test No Test Plan|List of control tests with no test plans|
|Issues No assignee|List of unassigned issues|
|Issues No Recommendation|List of issues with no recommendation|
|Issues No Explanation|List of issues with no explanation|
|Remediation Task No Assignee|List of unassigned remediation tasks|
|Issues No item|List of issues with no items|
|Remediation Task No Issues|List of remediation tasks with no issues|

Use the Assigned to filter in the report to filter data on the **Data Quality** tab reports.

## Audit Manager dashboard in classic UI

**Important:** Starting with version 18.1.5 of the Audit Management application, the Audit Manager dashboard can be viewed in the Next Experience UI Framework.

To view the Audit Manager dashboard, activate the following GRC applications:

-   GRC Audit Management \(com.sn\_audit\)
-   GRC Advanced Dashboards \(com.sn\_grc\_pa\_advanced\)

To view the Audit Manager dashboard, navigate to **Audit** &gt; **Audit Manager Dashboard**. Log in with the sn\_audit.manager role to view reports.

![Audit Manager dashboard](../../../product/grc-audit/image/audit-manager-dashboard.png "Audit Manager dashboard")

**Related topics**  


[Advanced Governance, Risk, and Compliance Application Risk dashboard](../../../product/grc-common/concept/advanced-grc-dashboard.md)

