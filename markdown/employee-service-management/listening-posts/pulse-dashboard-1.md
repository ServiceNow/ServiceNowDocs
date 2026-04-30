---
title: Reporting capabilities for Listening Posts
description: Visualize survey metrics to understand overall employee experience. Identify problem areas by drilling down to survey questions with lower scores.
locale: en-US
release: yokohama
product: Listening Posts
classification: listening-posts
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Listening Posts, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Reporting capabilities for Listening Posts

Visualize survey metrics to understand overall employee experience. Identify problem areas by drilling down to survey questions with lower scores.

## Before you begin

Role required: sn\_lp.dashboard\_view

## About this task

-   Gain insights based on location, department, and other parameters.
-   View average scores, trends, response rates, and summary of user responses for surveys under a theme.
-   Identify problem areas by drilling down to survey questions with lower scores.

## Procedure

1.  Navigate to **Listening Posts** &gt; **Pulse Dashboard**.

2.  In the Global filters section, you can perform the following tasks:

    1.  In the **Theme** field, select a theme for which you want to view user responses.
    2.  In the **Surveys** field, select the survey in the theme for want to view user responses.
    3.  In the **Start Date** field, specify the date from which you want to view the data of pulse surveys.

        **Note:** For a survey under the theme type **Group Pulse**, **Start Date** corresponds to the start date of pulse survey. For a survey under the theme type **Employee Lifecycle**, **Start Date** corresponds to the date starting which instances are created.

    4.  In the **End Date** field, specify the date until which you want to view the data of pulse surveys.

        **Note:** For a survey under the theme type **Group Pulse**, **End Date** corresponds to the surveys whose start date falls before the selected end date. For a survey under the theme type **Employee Lifecycle**,**End Date** corresponds to date until which the instances are created.

    5.  To enable canceled surveys in reporting, select **Include canceled surveys**.
3.  In the **Overall Score** section, view the aggregate scores of all surveys under a given theme.

4.  In the **Overall Summary** tab, you can perform the following tasks:

    1.  In **Viewable Score**, view the aggregated user response scores to which you have access.
    2.  View the average aggregate scores broken down by user demographics. For example, view Average scores by Country, Average scores by Department, Average scores by Title , Average Score by HR Task Type and Average Score by HR Service.

        **Note:**

        -   The Average Score by HR Task Type and Average Score by HR Service reports appear only when you select **HR task** in the Task type filter. **HR task** in Task type filter functions when a survey uses feedback initiators to trigger a pulse survey, post completion of an HR task only.
        -   To select the HR Task in Task type filter, you must have the case\_reader role.
    3.  Drill down to the data of any department or country by applying filters in the Filters section.
5.  In the**Trend History** tab, view the average scores trending \(quarterly/yearly\) for a survey selected under a theme.

6.  In the **Response Details** tab, view the response rates and average scores for all pulse surveys under a theme.


