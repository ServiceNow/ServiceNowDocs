---
title: Automation Center Value dashboard
description: The Automation Center Value dashboard provides summary information about the states of goals and automations along with the actual and estimated cost and time saved for all active and future automations.
locale: en-US
release: xanadu
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Automation Center Workspace, Exploring Automation Center, Automation Center, Creating integrations with applications]
---

# Automation Center Value dashboard

The Automation Center Value dashboard provides summary information about the states of goals and automations along with the actual and estimated cost and time saved for all active and future automations.

You can access the Value dashboard in either of two ways:

-   By navigating to **All** &gt; **Automation Center** &gt; **Automation Center Home** and then selecting the **Value** tab.
-   By navigating to **Workspaces** &gt; **Automation Center Workspace** &gt; **Value**.

## Goals chart

The Goals chart displays the summary of automation goals categorized by their state along with the estimated cost saved per year.

For information about automation goals, see [Create an automation goal](../task/create-automation-goal.md).

By default, the Goals chart provides details of all automation goals with associated active automation requests for the day you’re viewing the data.

Use the **Target date** drop-down list to view goals for a specific period. When you select the **Target date** filter, you can view the calendar of the current and the next month. Date filters are available for Custom range, Last 12 months, Last 6 months, and so on.

## Active automations

The Active automations chart displays data for active automations. You can filter the data by date, department, and automation.

-   **Total cost saved**

    This chart displays the total cost saved for the selected date range, department, and automation.

    **Note:** Selecting the Total cost saved widget opens the Analytics Hub KPI Details widget in a new tab.

-   **Total time saved**

    This chart displays the total time saved for the selected date range, department, and automation.

    **Note:** Selecting the Total time saved widget opens the Analytics Hub KPI Details widget in a new tab.

-   **Number of deployed automations**

    This chart displays the total number of deployed automations for the selected date range, department, and automation. It also compares the data with the previous cycle. The previous cycle has the same duration as the current cycle. For example, if the current cycle is January 1, 2021, to March 31, 2021, the previous cycle would be October 1, 2020, to December 31, 2020.

-   **Average process success rate**

    This chart displays the average process success rate for the selected date range, department, and automation. The success rate is calculated from the total executions within the selected date range that have the states Complete, Error, and canceled divided by the executions that completed with no errors. It also compares the data with the previous cycle. The previous cycle has the same duration as the current cycle. For example, if the current cycle is January 1, 2021, to March 31, 2021, then the previous cycle would be October 1, 2020, to December 31, 2020.

-   **Automation performance by sources**

    This chart displays automation performance by sources, such as ServiceNow RPA, flows, and other third-party automation vendors for the selected date range, department, and automation.

    **Note:** You can get data for a maximum of 20 sources.

-   **Cost savings by department**

    This chart displays the cost savings per run per department for the selected date range.

-   **Time savings by department**

    This chart displays the time savings per run per department for the selected date range.


**Note:** A lag in the Performance Analytics data collection could cause a delay in the date that is displayed in the Analytics Hub.

## Future automations

The Future automations section displays the estimated cost savings and time savings of future requests per year.

Use the **Intake source** and **Goal** filters to limit your results to a specific intake source or goal.

**Parent Topic:**[Automation Center Workspace](automation-center-workspace-ui.md)

