---
title: Advanced Work Assignment dashboard for tasks
description: Enable managers to monitor Task \[task\] work items so that their agents can better support customer needs.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Platform Analytics Solutions for Advanced Work Assignment, Analytics &amp; Reporting Solutions, Reference, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Advanced Work Assignment dashboard for tasks

Enable managers to monitor Task \[task\] work items so that their agents can better support customer needs.

This dashboard is available in the Performance Analytics - Content Pack - Advanced Work Assignment plugin. For information on activating the content pack, see [Platform Analytics Solutions for Advanced Work Assignment](../../application-content-packs/concept/awa-content-pack.md).

![The dashboard displays indicators and reports to track agent tasks with customers](../../../administer/advanced-work-assignment/image/AWATasks-update.png "AWA dashboard for Tasks")

## End users and roles

|End user and goal|Required role|
|-----------------|-------------|
|AWA administrator: Configures Advanced Work Assignment to best fit the business needs of customer service.|awa\_admin|
|AWA manager: Identifies the areas of concern for routing and assignment of work items across service channels.|awa\_manager|
|Agent manager: Manages agents or agent groups. The agent manager needs to know what agents are working on in order to make sure customer needs are being met.|sn\_customerservice\_manager|
|Performance Analytics administrator: Ensures that business managers are making the best use of Performance Analytics solutions.|pa\_admin or pa\_viewer|

## Use case

This dashboard provides support managers with an overview of incoming work items and the availability of agents to handle them. Managers can monitor these daily trends to determine if adjustments should be made to the routing criteria, agent capacity values, and other settings that determine how work is pushed to agents.

## Indicators

Indicators define a performance measurement taken at regular intervals of a business service, an activity, or organizational behavior.

<table id="table_kbm_5wt_rhb"><thead><tr><th>

Indicator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New Work Items

</td><td>

Total number of task work items that were created today. The goal for this indicator is to minimize the amount of task work items that agents receive.

</td></tr><tr><td>

Accepted Work Items

</td><td>

Percentage of all task work items that agents have accepted.

</td></tr><tr><td>

Auto-Assigned Work Items

</td><td>

Percentage of all task work items that were automatically assigned.

</td></tr><tr><td>

Exceeding Target Work Items

</td><td>

Percentage of all interaction work items that have exceeded the target wait time.

</td></tr><tr><td>

Timed Out Work Items

</td><td>

Percentage of all interaction work items that timed out.

</td></tr><tr><td>

Rejected Work Items

</td><td>

Percentage of all interaction work items that agents have rejected.

</td></tr><tr><td>

Weekly Trends

</td><td>

Number of work items in each of the following states for the past week:-   New
-   Exceeding Target
-   Abandoned
-   Rejected
-   Timed Out
-   Auto-Assigned

</td></tr></tbody>
</table>## Breakdowns

To analyze data according to different categories, select a breakdown from the dashboard menu:

-   Service Channel
-   Queue

For more information on analyzing data with breakdowns, see [Using breakdowns on dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_SpecialDashboards.md).

## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Average Task Wait Time - Last Hour|Single Score![Single score report](../../../reuse/reporting/image/single-score.svg)|Average amount of time in the past hour that customers have spent waiting for an agent response.|

