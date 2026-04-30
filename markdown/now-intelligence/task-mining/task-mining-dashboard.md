---
title: Task Mining analyses
description: Project analyses enable you to gain insights into user activities from your categorized data.
locale: en-US
release: zurich
product: Task Mining
classification: task-mining
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Explore, Task Mining, Platform Analytics]
---

# Task Mining analyses

Project analyses enable you to gain insights into user activities from your categorized data.

You can generate three types of analyses for Task Mining projects: Task activity, Overall activity, and Task timeline analysis.

-   The Task activity analysis shows time spent and frequency of activities and applications used during scoped task, such as resolving incidents. This analysis is based on workstation user actions grouped as tasks.
-   The Overall activity analysis provides a complete, layered overview of all categorized applications used by workstation users.
-   The Task timeline provides a detailed view of collected task activities with a sequential view of applications, windows, and user interactions. Use these task steps as the basis of your automation requests. This analysis is based on workstation user actions grouped as tasks.

Use the tabs to navigate between available analyses in your project.

## Task activity analysis

The Task activity analysis shows the time spent and frequency of task-related activities within tasks that are defined to provide data for this analysis. You can view the average task duration and when and from whom data is collected in the top section of the analysis, along with other project details. Workstation user actions must be grouped as a task that can be logged to provide data for a Task activity analysis. For more information about defining tasks, see [Define user actions for task logging](../task/mine-data.md).

View the data by date, categories, applications, users, and tasks to analyze task execution details at multiple levels. Use the drop-down selector to adjust the tasks that are shown in the charts as well as dates, categories, activities, and users.

The task activity analysis includes the Average time per category, Time by workstation user, and View across task timeline charts.

-   Average time per category - This treemap chart shows project data according to the categorization rules set up by the Task Mining power user. View details such as the number of views percentage of total time, number of active workstation users, and average daily usage by hovering over a tile. Select a tile to see category details and application details.

-   Time by workstation user - The stacked bar chart shows project data broken down by workstation users.

    -   See workstation user data according to category.
    -   Order the users by fastest or slowest task execution times by sorting the chart.
    -   View detailed information on the category for the user by hovering over a category on the column bar.
    -   Select a category to see application details per user.

![Screenshot showing a task activity analysis in Task Mining.](../image/task-mining-task-activity.png)

Selecting the **View across task timeline** link displays the Activities across task timeline chart, which shows how applications are being used by the selected workstation users. This chart is accessible only from the Task activity analysis.

The stacked column bar chart divides the task length into percentages. For example, if the task takes 200 minutes, the first section shows 20 minutes of activity. View detailed information on an activity by hovering over a column bar.

![Screenshot showing the Applications categories across task timeline chart in the Task Mining task activities analysis.](../image/task-mining-task-timeline.png)

## Overall activity analysis

The Overall activity analysis provides a layered view of user activities. You can view the average task duration and when and from whom data is collected in the top section of the analysis, along with other project details.

View data by the date, categories, applications, and users to analyze usage trends and user engagement at different levels of detail. Use the drop-down selectors to adjust the dates, categories, applications, and users that are shown in the charts.

The Overall activity analysis includes the Average time per category and Time by workstation user charts.

-   Average time per category - This treemap chart shows project data according to the categorization rules set up by the Task Mining power user. View details such as the number of views percentage of total time, number of active workstation users, and average daily usage by hovering over a tile. Select a tile to see category details and application details.

-   Time by workstation user - The stacked bar chart shows project data broken down by workstation users.

    -   See workstation user data according to category.
    -   Order the users by fastest or slowest task execution times by sorting the chart.
    -   View detailed information on the category for the user by hovering over a category on the column bar.
    -   Select a category to see application details per user.

![Screenshot showing an overall activity analysis in Task Mining.](../image/task-mining-overall-activity-dashboard.png)

## Task timeline analysis

The task timeline analysis provides a detailed view of collected task activities. These tasks are the bases for taking task improvement actions. Improvement actions include opening automation requests or sharing details of the task. Workstation user actions must be grouped as a task that can be logged to provide data for a Task timeline analysis. For more information about defining tasks, see [Define user actions for task logging](../task/mine-data.md).

You can view the average task duration and when and from whom data is collected in the top section of the analysis, along with other project details. The analysis shows who collected the tasks, duration, the number of steps and applications used, whether the task is user-defined or custom, automation request details, and date created. If an automation request has already been opened for the task, a link to the request is provided. You can only open one automation request per task. For more information about the prerequisites for initiating automation requests, see [Integration with Automation Center](integration-with-automation-center.md).

![Screenshot showing a task timeline analysis in Task Mining.](../image/tm-task-timeline-analysis.png)

Select a task to see details of the steps of the task. The task steps view shows the details of the task at the top. From this view, you can initiate automation requests or share a link to task details. For more information, see [Identify task improvement actions](../task/identify-improvement-opportunities.md).

