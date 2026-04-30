---
title: Analytics Project manager
description: The Analytics Project manager provides the project managers with quick reports of time card exceptions, and category wise time reported for their projects. The dashboard displays time card reports only for the projects managed by a project manager.
locale: en-US
release: zurich
product: Time Card Management
classification: time-card-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Analytics Project manager

The Analytics Project manager provides the project managers with quick reports of time card exceptions, and category wise time reported for their projects. The dashboard displays time card reports only for the projects managed by a project manager.

**Important:** Starting with Xanadu release, **Project Manager Dashboard** is renamed to **Analytics Project manager** for new customers.

The dashboard can be activated using the Performance Analytics - Content Pack - Project Portfolio Suite Dashboards plugin \(com.snc.pps\_dashboards\). You require Performance Analytics license to use this dashboard.

The reports in the dashboard are filtered based on **Project**, and **Date** selected.

The Analytics Project manager consists of these components:

## Project time card exception count

It displays the total count of entries in **Project time card exceptions** report.

![Screenshot for Project Time Card Exception Count section](../image/ProjectTimeCardExceptionCount.png "Project time card exception count")

## Project time card exceptions report

The Project time card exceptions report lists the users who did not submit their time cards, and the time cards which are not yet approved for the selected project and time range. The exception report is generated for the users who are assigned to a task in progress, or hard allocated to the project/task in that time range. The report displays the following data:

-   **User**: The time card user assigned to the selected project, or hard allocated to the resource plan associated with the project. If there are more than one time cards for a user in a given date range which are not submitted or require approval, then multiple entries are listed for the user.
-   **Week starts on**: Starting date of the time card week in the selected time range.
-   **State**: State of the time card. Time card entries with state as **Not Submitted** are also listed if a time card is not created for the week.

The report is generated from the project\_timecard\_exception table. It requires the schedule job **Project Time Card Exceptions** to be running to get the up-to-date information.

![Screenshot for Project Time Card Exceptions report](../image/ProjectTimeCardExceptions.png "Project time card exceptions report")

## Total approved hours for project\(s\)

It displays the total approved hours in all project categories displayed in **Time by Project Time Category** report.

![Screenshot for total approved hours for selected projects](../image/ProjectDashboardTotalHours.png "Total approved hours for projects")

## Time by Project Time Category report

The bar chart report displays the time approved against each project category for the users allocated to the selected project.

![Screenshot for Time by Project Time Category report](../image/TimeByProjectTimeCategory.png "Time by Project Time Category report")

-   **[Use the Analytics Project manager](../task/use-project-manager-dashboard.md)**  
The Analytics Project manager shows the time card reports for the selected projects.

**Parent Topic:**[Time Card Management](time-card-management.md)

