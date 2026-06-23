---
title: Create a cohort
description: Create an analysis of users who complete a predetermined sequence of actions so you can track conversion rates at each step.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/now-intelligence/usage-insights/create-action-cohort.html
release: xanadu
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2024-11-13"
reading_time_minutes: 1
breadcrumb: [User Experience Analytics cohorts, Using User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Create a cohort

Create an analysis of users who complete a predetermined sequence of actions so you can track conversion rates at each step.

This video shows you how to create and use cohorts.

## Before you begin

Role required: Users with the analytics\_viewer, portal\_analytics\_viewer, mobile\_analytics\_viewer, core\_ui\_analytics\_viewer, now\_experience\_analytics\_viewer roles can create, edit and delete cohorts for the applications they have access to.

## About this task

## Procedure

1.  From the Dashboard, navigate to **Cohorts**, and click **Create Your First Cohort** or **New Cohort**.

2.  Enter a name for the relevant process you want to measure.\[Omitted image "new-cohort-wizard.png"\] Alt text: New cohort dialog.

3.  Select the timeframe for sessions you want to include.

<table id="choicetable_rqr_3zv_xjb"><thead><tr><th align="left" id="d66182e90">

Option

</th><th align="left" id="d66182e93">

Description

</th></tr></thead><tbody><tr><td id="d66182e99">

**Now**

</td><td>

The report begins collecting data from the second the report saves.

</td></tr><tr><td id="d66182e111">

**1 Week Ago**

</td><td>

Reports on data seven days prior to the current date. Includes data generated at 12AM GMT of the date.

</td></tr><tr><td id="d66182e123">

**1 Month Ago**

</td><td>

Reports on data 30 days prior to the current date. Includes data generated at 12AM GMT of the date.

</td></tr><tr><td id="d66182e135">

**3 Months Ago**

</td><td>

Reports on data 90 days prior to the current date. Includes data generated at 12AM GMT of the date.

</td></tr><tr><td id="d66182e148">

**Original Date**

</td><td>

This option is available when editing an existing report. Reports on data from the original date of the report.

</td></tr></tbody>
</table>4.  Click **Next**.

5.  Select the first action from the options that will define the cohort.

    Users who perform the defined action are grouped in the rows of the cohort.

6.  -   Visited a Screen
-   Triggered an Event
-   Performed an Action
-   Started any Session
-   Started their 1st Session
7.  Click **Match by properties** to select and enter a property value to match the action with.

8.  Select the second action that will define the cohort, and a screen, event, or action as applicable.

9.  Click **Finish**.


## What to do next

View the cohort to see how many of the users who performed the first defined action returned to perform the second action.

**Note:** If data shown in the cohort analysis is not final, a note indicates that retroactive data is still being processed. Refresh the screen to see the report with final data.

**Parent Topic:**[User Experience Analytics cohorts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/usage-insights/uxa-cohorts.md)

