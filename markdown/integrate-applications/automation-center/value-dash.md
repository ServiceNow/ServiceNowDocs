---
title: Automation Center Value dashboard
description: The Automation Center Value dashboard provides summary information about the states of goals and automations along with the actual and estimated cost and time saved for all active and future automations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/automation-center/value-dash.html
release: zurich
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Workspace, Explore, Automation Center, Workflow Data Fabric]
---

# Automation Center Value dashboard

The Automation Center Value dashboard provides summary information about the states of goals and automations along with the actual and estimated cost and time saved for all active and future automations.

All widgets under the following sections are available only if the you have the sn\_ac.automation\_technical\_user role:

-   Goals chart
-   Number of deployed automations under Active automations
-   Future automations

To access all other widgets in the Active automations section, you must associate a domain configuration with a data collection job. For more information see https://www.servicenow.com/docs/bundle/zurich-now-intelligence/page/use/performance-analytics/task/associate-domain-config-dc-job.html.

You can access the Value dashboard in either of two ways:

-   By navigating to **All** &gt; **Automation Center** &gt; **Automation Center Home** and then selecting the **Value** tab.
-   By navigating to **Workspaces** &gt; **Automation Center Workspace** &gt; **Value**.

## Goals chart

The Goals chart displays the summary of automation goals categorized by their state along with the estimated cost saved per year.

For information about automation goals, see [Create an automation goal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/create-automation-goal.md).

By default, the Goals chart provides details of all automation goals with associated active automation requests for the day you’re viewing the data.

Use the **Target date** drop-down list to view goals for a specific period. When you select the **Target date** filter, you can view the calendar of the current and the next month. Date filters are available for Custom range, Last 12 months, Last 6 months, and so on.

\[Omitted image "value-goal.png"\] Alt text: Goals chart

## Active automations

The Active automations chart displays data for active automations. You can filter the data by date, department, and automation. If no filter is set, the data is displayed for all the data.

<table id="table_yl4_p4m_c2c"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total cost saved

</td><td>

This chart displays the total cost saved for the selected date range, department, and automation.**Note:** Selecting the Total cost saved widget opens the Analytics Hub KPI Details widget in a new tab.

\[Omitted image "value-cost-saved.png"\] Alt text: Total cost saved

</td></tr><tr><td>

Total time saved

</td><td>

his chart displays the total time saved for the selected date range, department, and automation.**Note:** Selecting the Total time saved widget opens the Analytics Hub KPI Details widget in a new tab.

\[Omitted image "value-time-saved.png"\] Alt text: Total time saved

</td></tr><tr><td>

Number of deployed automations

</td><td>

This chart displays the total number of deployed automations for the selected date range, department, and automation. It also compares the data with the previous cycle. The previous cycle has the same duration as the current cycle. For example, if the current cycle is January 1, 2021, to March 31, 2021, the previous cycle would be October 1, 2020, to December 31, 2020.\[Omitted image "value-deploy-auto.png"\] Alt text: Number of deployed automations

</td></tr><tr><td>

Average process success rate

</td><td>

This chart displays the average process success rate for the selected date range, department, and automation. The success rate is calculated from the total executions within the selected date range that have the states Complete, Error, and canceled divided by the executions that completed with no errors. It also compares the data with the previous cycle. The previous cycle has the same duration as the current cycle. For example, if the current cycle is January 1, 2021, to March 31, 2021, then the previous cycle would be October 1, 2020, to December 31, 2020.\[Omitted image "value-average-process.png"\] Alt text: Average process success rate

</td></tr><tr><td>

Automation performance by sources

</td><td>

This chart displays automation performance by sources, such as ServiceNow RPA, flows, and other third-party automation vendors for the selected date range, department, and automation.**Note:** You can get data for a maximum of 20 sources.

\[Omitted image "value-sources.png"\] Alt text: Automation performance by sources

</td></tr><tr><td>

Total cost saved by department

</td><td>

This chart displays the cost savings per run per department for the selected date range.\[Omitted image "value-totalcost.png"\] Alt text: Cost savings by department

</td></tr><tr><td>

Total time saved by department

</td><td>

This chart displays the time savings per run per department for the selected date range.\[Omitted image "value-totaltime.png"\] Alt text: Total time saved by department

</td></tr></tbody>
</table>**Note:** A lag in the Performance Analytics data collection could cause a delay in the date that is displayed in the Analytics Hub.

## Future automations

The Future automations section displays the estimated cost savings and time savings of future requests per year.

Use the **Intake source** and **Goal** filters to limit your results to a specific intake source or goal.

\[Omitted image "value-fut-auto.png"\] Alt text: Future automations

**Parent Topic:**[Automation Center Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/automation-center/automation-center-workspace-ui.md)

