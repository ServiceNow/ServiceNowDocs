---
title: Create a cohort
description: Define the predetermined sequence of actions a group of users complete so you can track conversion rates at each step.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/usage-insights/create-action-cohort.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cohort analysis, Using Usage Insights, Usage Insights, Platform Analytics]
---

# Create a cohort

Define the predetermined sequence of actions a group of users complete so you can track conversion rates at each step.

## Before you begin

Role required: analytics\_viewer, portal\_analytics\_viewer, mobile\_analytics\_viewer, core\_ui\_analytics\_viewer, or now\_experience\_analytics\_viewer.

## About this task

## Procedure

1.  Navigate to **Platform Analytics** &gt; **Usage Insights**.

2.  From the Applications list, select the application to create a cohort for.

3.  Select **Analysis** &gt; **Cohort Analysis**.

4.  Select the **Create new cohort** button \(\[Omitted image "uxa-create-cohort-button.png"\] Alt text:\).

5.  Enter a name and a description for the process you want to measure.

6.  Select two step types and their values and select **Add**.

    The step types are:

    -   **Visited a Screen**
    -   **Triggered an Event**
    -   **Performed an Action**
    -   **Started any Session**
    -   **Started their first Session**
    The actions are dependent on the step type.

    \[Omitted image "uxa-create-cohort-wizard.png"\] Alt text: Create cohort wizard

7.  Select **Save**.


## What to do next

View the cohort to see how many users who complete the first defined action also complete the second action. When you view the cohort, you can filter on **Aggregation**, **Date range**, **User type**, and **Country**, and add filters as necessary.

\[Omitted image "uxa-cohort-ex.png"\] Alt text: UXA cohort example, aggregated daily with a range of 7 days

**Note:**

1.  If data shown in the cohort analysis is not final, a note indicates that retroactive data is still being processed. Refresh the screen to see the report with final data.
2.  Users with the required roles can create, edit and delete cohorts for the applications they have access to.

**Parent Topic:**[Cohort analysis in Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/usage-insights/uxa-cohorts.md)

