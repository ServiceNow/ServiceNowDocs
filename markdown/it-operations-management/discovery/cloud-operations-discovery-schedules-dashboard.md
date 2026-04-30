---
title: Cloud Discovery schedules dashboard in Cloud Discovery Workspace
description: The Cloud Discovery schedules dashboard displays information about the selected discovery run.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 2
breadcrumb: [Discovery monitoring and issue resolution, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Cloud Discovery schedules dashboard in Cloud Discovery Workspace

The Cloud Discovery schedules dashboard displays information about the selected discovery run.

**Important:** Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## Required ServiceNow AI Platform roles

sn\_cloud\_ops\_ws.cloud\_ops\_admin

## Access the Cloud Discovery schedules dashboard

To open the dashboard, navigate to **Cloud Discovery Workspace** &gt; **Cloud Discovery** &gt; **Schedules**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

<table id="table_ydx_q53_jsb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

sn\_cloud\_ops\_ws.cloud\_ops\_admin

</td><td>

-   View the resource count from the recent discovery runs.
-   View the time taken for the recent discovery runs.
-   View the list of newly discovered CIs
-   View the list of CIs missing from the previous discovery run.
-   View the count of CIs discovered during the selected discovery run.
-   View the count of discovery errors that occurred during the selected discovery run.

</td></tr></tbody>
</table>## Indicators

-   **Total Resources**

    The indicator displays the total count of Configuration Items \(CI\) discovered during the selected discovery run.

-   **Newly discovered**

    The indicator displays the count of new CIs discovered during the selected discovery run.

-   **Absent from last**

    The indicator displays the count of CIs missing during the selected discovery run. That is, CIs were discovered during the previous discovery run, but are missing during the selected discovery run.

-   **Errors**

    The indicator displays the count of discovery errors that occurred during the selected discovery run.

-   **Duration**

    The indicator displays the time taken to complete the selected discovery run.


**Note:** Cloud Discovery calculates the **Newly discovered** and **Absent from last** indicators only for the pattern-based discoveries.

## Reports

<table id="table_d2x_q53_jsb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resource counts from recent discovery runs

</td><td>

Bar chart![Bar chart.](../../../use/reporting/image/icon-bar-report-p.png)

</td><td>

discovery\_cloud\_results

</td><td>

This report displays the count of CIs discovered during the last 10 runs of the selected discovery schedule.

</td></tr><tr><td>

Time taken for recent discovery runs

</td><td>

Bar chart![Bar chart.](../../../use/reporting/image/icon-bar-report-p.png)

</td><td>

discovery\_status

</td><td>

This report displays the time taken to complete the last 10 runs of the selected discovery schedule.This report covers both completed as well as canceled discovery runs.

</td></tr></tbody>
</table>## Filters

<table id="table_f2x_q53_jsb"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schedules filter

</td><td>

Choice-based filter

</td><td>

By default, the list shows all the Cloud Discovery schedules in alphabetical order, regardless of their current running status. Use the schedule filter to filter the Cloud Discovery schedules. You can filter the schedules by cloud provider, schedule name, or both. You can also sort the filtered list by any one of the following criteria:-   **Alphabetically**: Sort the schedule names alphabetically.
-   **Errors**: Sort by the count of errors encountered during the discovery.
-   **Discovery in progress**: Sort by status of the discovery.

 After filtering the schedule, select the discovery run from the Report drop-down list to visualize its data in the schedules dashboard displayed on the **Results** tab.

 **Note:**

Only the last 10 discovery runs appear in the Report drop-down list.

</td></tr></tbody>
</table>