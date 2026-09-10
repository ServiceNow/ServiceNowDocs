---
title: Analyze conversion funnel results
description: Review the results of a conversion funnel to review how users move through each step, where they drop off, and how the journey has changed compared with a previous period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/usage-insights/analyse-conversion-funnel-results.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 2
breadcrumb: [Conversion funnels, Using Usage Insights, Usage Insights, Platform Analytics]
---

# Analyze conversion funnel results

Review the results of a conversion funnel to review how users move through each step, where they drop off, and how the journey has changed compared with a previous period.

## Before you begin

Role required: none

A configured conversion funnel.

## About this task

The results view reports the funnel from two perspectives, which you can switch between at the top of the page. The global filters remain available in both.

-   **Session based**

    Counts the users who completed the steps within a single session. The transition times are typically short in this case. This choice will help determine various user actions like visiting the homepage, starting a search, and reading a knowledge article or even placing a laptop order, all in one session.

-   **User based**

    Counts users who completed the steps across any number of sessions, so transition times reflect longer real-world spans, such as days rather than minutes. Use this perspective to measure overall task completion and longer adoption journeys. This choice will help determine the total number of users completing a specific action like completing a training within a given timeline.


**Tip:** Choose **Session based** to determine unique session details vs. **User based** to determine users

details.

## Procedure

1.  Open the funnel that you want to analyze.

2.  At the top of the results view, select either the session-based or the user-based scope.

3.  Review the headline metrics.

    -   **Completion rate**

        The proportion of users who entered the funnel and reached the final step.

    -   **Average time**

        The average time taken to complete the funnel.

    -   **Total users entered**

        The number of users who reached the first step.

    -   **Total users completed**

        The number of users who reached the final step.

4.  Review the **Completion rate** trend analysis chart to see how the completion rate has moved over the selected date range.

    **Note:** When the funnel includes chat events, the completion rate trend can be read as a deflection trend.

5.  Review the funnel diagram beneath the chart.

    The diagram shows each step, the percentage and number of users who reached it, and the time taken to move between steps, which identifies where users drop off.

6.  To evaluate change over time, enable **Show previous period comparison**.

    Each metric shows its change compared with the previous period. A **Step Comparison** table reports engaged users, engaged sessions, and conversion time for the current and previous periods side by side.

7.  Apply the global filters to segment the results.


## Result

The results view reports how many users completed the journey, where they dropped off, and how those figures compare with the previous period.

**Parent Topic:**[Funnel reports in Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/funnel-reports-uxa.md)

