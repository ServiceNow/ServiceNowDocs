---
title: Pre-date a project task
description: Move the planned start date of a task prior to the planned start date of a project. Adding a pre-dated task allows you to accommodate tasks which need to start before the planned start date of a project.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Change the planned start date of a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Pre-date a project task

Move the planned start date of a task prior to the planned start date of a project. Adding a pre-dated task allows you to accommodate tasks which need to start before the planned start date of a project.

## Before you begin

You should have created or added project tasks to your project.

Role required: it\_project\_manager

## About this task

Before pre-dating a project task, note the following conditions:

-   The property project.rollup\_project\_start\_date should be set to true.
-   Pre-dating a task's planned start date also moves the project's planned start date.
-   The start date of a child task cannot be moved prior to the parent task's start date. For example, if a parent task with Start no earlier than constraint starts on 20th and the child task starts on 30th, the start date of the child task can only be moved up to 20th.

## Procedure

1.  Navigate to **Project** &gt; **Projects** &gt; **All**.

2.  Select the project from the list.

3.  On the Project form, update the planned start date for a project task using either of the following options.

<table id="choicetable_h1v_kq4_nlb"><thead><tr><th align="left" id="d116324e93">

Option

</th><th align="left" id="d116324e96">

Steps

</th></tr></thead><tbody><tr><td id="d116324e102">

**From the Project Task form**

</td><td>

1.  In the Project Tasks related list, select the project task which you want to pre-date.
2.  On the Project Task form, click the **Dates** tab and update the **Planned start date** for the task.


</td></tr><tr><td id="d116324e126">

**From the Planning Console**

</td><td>

1.  On the Project form, click the **Planning Console** related link.
2.  In the Planning Console, update the start date of the project task under the **Planned start date** column.


</td></tr></tbody>
</table>4.  In the Move date dialog box, click **OK**.


