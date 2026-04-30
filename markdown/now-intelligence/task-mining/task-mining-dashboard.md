---
title: Task Mining analysis
description: Project analyses enable you to gain insights from your categorized data.
locale: en-US
release: yokohama
product: Task Mining
classification: task-mining
topic_type: concept
last_updated: "2024-10-14"
reading_time_minutes: 3
breadcrumb: [Explore, Task Mining, Platform Analytics]
---

# Task Mining analysis

Project analyses enable you to gain insights from your categorized data.

You can access two types of analyses for Task Mining projects: Overall activity and Task activity.

-   The Overall activity analysis provides a complete, layered overview of all categorized applications used by workstation users.
-   The Task activity analysis shows time spent and frequency of activities and applications used during scoped task, such as resolving incidents. Workstation user actions must be grouped as a task that can be logged to provide data for a Task activity analysis. For more information about defining tasks, see [Define user actions for task logging](../task/mine-data.md).

For both analysis types, view when and from whom data is collected in the top section of the analysis. Use the drop-down selectors to adjust the time, categories, activities, and users that are shown in the charts.

## Overall activity analysis

The overall activity analysis provides a layered view of user activities. View data by activity categories, applications, and users to analyze usage trends and user engagement at different levels of detail.

The overall activity analysis includes the Average daily usage and Average daily usage per user charts.

-   Average daily usage - This treemap chart shows project data according to the categorization rules set up by the Task Mining power user. View details such as the number of views percentage of total time, number of active workstation users, and average daily usage by hovering over a tile.

-   Average daily usage per user - The stacked bar chart shows project data broken down by workstation users.

    -   See workstation user data according to application categories, applications, or activities by changing the view.
    -   View detailed information on the categories, applications, or activities by changing the view and hovering over a column bar.

![Screenshot showing an overall activity analysis in Task Mining.](../image/task-mining-overall-activity-dashboard.png)

## Task activity analysis

The task activity analysis shows the time spent and frequency of task-related activities within tasks that are defined to provide data for the Task activity analysis. In the task activity analysis you can view the number of tasks in the project and the average task duration in addition to when and from whom data is collected in the top section of the analysis.

View the data by tasks, categories, applications, and users to analyze task execution details at multiple levels. Use the drop-down selector to adjust the tasks that are shown in the charts as well as time, categories, activities, and users.

The task activity analysis includes the Average usage per task and Average usage per task per user charts.

-   Average usage per task - This treemap chart shows project data according to the categorization rules set up by the Task Mining power user. View details such as the number of views percentage of total time, number of active workstation users, and average daily usage by hovering over a tile.

-   Average usage per task per user - The stacked bar chart shows project data broken down by workstation users.

    -   See workstation user data according to application categories, applications, or activities by changing the view.
    -   View detailed information on the categories, applications, or activities by changing the view and hovering over a column bar.

![Screenshot showing a task activity analysis in Task Mining.](../image/task-mining-task-activity.png)

Selecting the **View across task timeline** link displays the Applications categories across task timeline chart, which shows how applications are being used by the selected workstation users. This chart is accessible only from the Task activity analysis.

The stacked column bar chart divides the task length into percentages. For example, if the task takes 200 minutes, the first section shows 20 minutes of activity.

![Screenshot showing the Applications categories across task timeline chart in the Task Mining task activities analysis.](../image/task-mining-task-timeline.png)

