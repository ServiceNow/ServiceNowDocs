---
title: Analyze a dashboard in Service Observability
description: Use the analyze Service Observability dashboard skill to view an analysis of a single Service Observability dashboard.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Generative AI for IT Operations Management, Generative AI for ITOM, Service Observability dashboard analysis, Now Assist panel]
breadcrumb: [Use generative AI, Now Assist for ITOM, IT Operations Management]
---

# Analyze a dashboard in Service Observability

Use the analyze Service Observability dashboard skill to view an analysis of a single Service Observability dashboard.

## About this task

The analyze Service Observability dashboard skill uses generative AI to summarize a single Service Observability dashboard, including calling out insights found in the charts. This summary helps operators quickly orient to and understand a particular dashboard.

When you ask the skill to analyze a dashboard, it generates an optimized version of the Service Observability charts on the dashboard and then analyzes the data, taking the time period shown into account. It then reports any insights it finds.

![The skill found two insights on the Service dashboard](../image/so_NADashboard.png)

The skill's results remain available for an hour and don't automatically refresh. You need to rerun the skill to view a new analysis.

Note the following:

-   The analysis captures the time range as reflected by the user's set time zone. When sharing analysis data across time zones, be aware that the analysis time period always reflects the time zone originally captured and may not be in sync with your time zone settings.
-   The analysis doesn't weigh insights with regards to possible impact to an alert, incident, or overall dashboard health.
-   The skill has a maximum number of 50 images that can be analyzed.

## Before you begin

You need to manually activate this skill before it can be used. See [Activate the analyze Service Observability dashboard skill](../task/activate-the-analyze-service-observability-dashboard-skill.md) for more information.

Role required: admin, operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** and then navigate to a service record.

    You can access a service record from these pages in the SOW:

    -   **Services** list: Choose a service from the list.
    -   **Service dashboard**: Choose a service in the dashboard and select **Service Details**.
    -   **List**: Navigate to **Application Services** &gt; **Services** and select a service.
    -   **Express list** alert: Select a service from the **Impacted services** column.
    The Service Details page opens and the Overview tab is displayed.

    If charts are displaying error messages, see [Chart error states](../../service-observability/reference/chart-error-states.md).

2.  To the right of the dashboard name, select **Analyze dashboard**.

    The skill analyzes the data in Service Observability charts, looking for insights in the data that happened within the currently selected time period. Once complete, a badge displays one of the following:

    -   **Analysis**: The skill didn't find any insights, but will display a summary of the dashboard.
    -   **Insights**: A count of insights found is shown.
    -   **Analysis unavailable**: The skill wasn't able to run an analysis.
    **Note:** Because the skill only analyzes the data in the time period captured by the screen shot, it may produce more accurate results if you lengthen the time period before analyzing. Note that longer time periods result in longer response time. For best results, use time periods less than 48 hours.

3.  Select the info icon next to the badge to review the analysis and possible insights.

    The analysis tells you where it found the insights and the next steps you can take to determine the source of the insights.

    The analysis badge remains on the page for 60 minutes, after which the button resets so you can run a new analysis. After five minutes of running or if you change the time period, the analysis shows you a warning that it's out of date. Select the refresh icon to rerun it.

    **Note:** Select the **Copy** icon to copy the analysis, for example to paste it into work notes for an incident or alert.


**Parent Topic:**[Use generative AI in Now Assist for ITOM](now-assist-itom-use.md)

