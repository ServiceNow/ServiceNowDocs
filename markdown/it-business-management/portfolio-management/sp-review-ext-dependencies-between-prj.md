---
title: Review external dependencies between projects
description: Review the external dependencies between projects in a portfolio to track projects that are dependant on each other more closely.
locale: en-US
release: xanadu
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create planning scenarios, Scenario Planning for PPM, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Review external dependencies between projects

Review the external dependencies between projects in a portfolio to track projects that are dependant on each other more closely.

## Before you begin

Role required: it\_portfolio\_manager

Open demands and projects in the timeline view of the Portfolio Planning Workbench.

## About this task

As a portfolio manager, you may want to know the projects which are dependent on each other so that these projects can be tracked more closely.

For example, project B is dependent on project A \(external soft dependency\) and you want to make sure that project A is executed on time so that the schedule of project B is not affected. The **Dependencies** column shows that there is an outgoing external dependency from project A and an incoming external dependency to project B. You can the use the incoming dependency to determine whether a delay in project A will affect project B.

## Procedure

1.  Click the show or hide columns in gantt icon \(![show or hide columns in gantt](../image/show_hide_columns.png)\) in the timeline view and add the **Dependencies** column if it is not visible.

    The number of incoming and outgoing external dependencies are displayed, if any.

2.  Click the external dependency in **Dependencies** column for the project.

3.  In the **Dependencies** pop-up dialog, click a tab to review the dependency:

    -   **Inbound tab**

        Tasks that have an incoming dependency from a project are listed.

    -   **Outbound tab**

        Tasks with an outgoing dependency to the project are listed.

    ![Dependencies example](../../project-management/image/ReviewExternalDependencies.png "Example of external dependencies between projects")

4.  Click the project number in a tab to open and review the linked project in the planning console view.


**Parent Topic:**[Create planning scenarios](create-scenarios.md)

