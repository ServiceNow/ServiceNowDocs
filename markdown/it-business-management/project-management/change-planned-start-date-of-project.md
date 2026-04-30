---
title: Change the planned start date of a project
description: Adjust the schedule of a project by changing the planned start date of a project and shifting it later or earlier than the current planned schedule.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Change the planned start date of a project

Adjust the schedule of a project by changing the planned start date of a project and shifting it later or earlier than the current planned schedule.

## Before you begin

Role required: it\_project\_manager

## About this task

Changing the planned start date of a project to a new date also moves all its tasks and subprojects relative to the updated start date of the project. You can change the planned start date of a project when the following conditions are true:

-   The **State** of the project is Pending or Open.
-   To move the start date of a project in WIP state, set the **Enable move project for WIP projects** property \(**com.snc.project.move\_project.wip**\) to true. The default value of this property is false.
-   No project\_funding records are selected for execution.
-   The project actual dates are not populated.

**Note:**

-   The **Move project** option is available for a project only when it has a task or subproject.
-   If an agile phase with sprints is associated to the project, then changing the planned start date of the project also clears the start and end dates of the sprints.

## Procedure

1.  Change the planned start date of a project using either of the following options.

<table id="choicetable_bx2_kjj_wfb"><thead><tr><th align="left" id="d284796e105">

Option

</th><th align="left" id="d284796e108">

Steps

</th></tr></thead><tbody><tr><td id="d284796e114">

**From the Planning console**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **Project Workspace**.
2.  Open the project for which you want to change the planned start date.
3.  In the Planning Console, click the more actions icon \(![More Actions icon](../../planning-and-policy/image/gannt_chart_icon.png)\) and then select the **Move project** option.


</td></tr><tr><td id="d284796e156">

**From the Project form**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **All**.
2.  Open a project for which you want to change the planned start date.
3.  On the Project form, click the **Move project** related link.


</td></tr></tbody>
</table>2.  In the dialog box, pick a date.

3.  Select or clear the **Move all tasks regardless of constraint type** check box.

    -   Clearing the check box moves the tasks with Start ASAP constraint only to the new project date.
    -   Selecting the check box moves all the project tasks irrespective of their constraints to the new project date with the same offset except the task with Start ASAP constraint.
    This check box is selected by default.

    **Note:** The tasks in WIP and Close states are not moved.

4.  Click **OK**.


## Result

-   The planned start date of the project is updated to the new date.
-   Program dates are updated relative to the project start date.
-   If the **Move all tasks regardless of constraint type** check box is selected, all project tasks with Start on specific date and Start no earlier than constraints are moved to a new start date by the same offset as from the earlier project start date. The constraint date is also moved by the same offset.

    For example, say a project is starting on November 10 with a Start On task starting on November 15, giving an offset of five days. If you move the project start date to November 20, then the task start date will be moved to November 25, maintaining the five-day offset from the project start date.

-   All project tasks with Start ASAP constraint are moved to the new start date based on the **Constraint Date** field on the project form. The tasks must be in the Open or Pending state.
-   If the **Change Resource Plan and Cost Plan Start Date with Demand or Project Start Date Change** property is selected, all related entities like cost plan, resource plan, and benefit plans are moved relative to the project start date. For more information on how to set this property, see [Properties installed with Project Management](../reference/r_InstalledWithProjectManagement.md#project_application_properties).

