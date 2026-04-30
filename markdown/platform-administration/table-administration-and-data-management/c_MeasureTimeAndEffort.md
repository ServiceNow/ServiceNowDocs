---
title: Measure time and effort
description: The Planned Task \[planned\_task\] table provides standard fields for tracking duration and effort.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Extending the Task table with Planned tasks, Working with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Measure time and effort

The Planned Task \[planned\_task\] table provides standard fields for tracking duration and effort.

Duration measures the time from start to end date. Effort measures the hours of work exerted on the project.

Duration

-   Planned duration: The projected length of time for the planned task.
-   Actual duration: The actual length of time so far for the planned task.
-   Remaining duration: The Planned duration minus the Actual duration, which represents the projected length of time left.

Effort

-   Planned effort: The projected amount of time that will be spent on the planned task.
-   Actual effort: The actual amount of time that has already been spent on the planned task.
-   Remaining effort: The Planned effort minus the Actual effort, which represents the amount of project work left.
-   Percent complete: For the parent task, the percent complete field is not editable and is rolled up from the percent completion of child tasks using the following formula:

    Percent complete of parent task = sum \(planned duration of child tasks \* percent complete of child tasks\) / sum \(planned duration of child tasks\)

    For a child task, the percent complete is entered manually.


Date Calculation: All planned dates and actual dates of the child tasks are rolled up to the parent task automatically. Planned end date for a child task is calculated based on the planned start date and planned duration. If actual start is present, then planned end date is calculated from actual start date and planned duration.

Dependencies: All type of task dependencies, excluding external dependencies, are supported by the planned tasks. For more information about various dependency types, see [Project task relationships and dependencies](https://www.servicenow.com/docs/access?context=c_ProjectTaskRelationDepend&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

**Parent Topic:**[Extending the Task table with Planned tasks](c_PlannedTask.md)

