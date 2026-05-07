---
title: Time Sheet Portal
description: Time Sheet Portal categorizes and displays all your assigned tasks in a single view for a given week. The portal enables you to record time spent on tasks on a day-to-day basis and submit the time sheet in a single action.
locale: en-US
release: australia
product: Time Card Management
classification: time-card-management
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 8
breadcrumb: [Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Time Sheet Portal

Time Sheet Portal categorizes and displays all your assigned tasks in a single view for a given week. The portal enables you to record time spent on tasks on a day-to-day basis and submit the time sheet in a single action.

Time Sheet Portal works with the Task table to record the time that you spend on various task types, such as projects, incidents, problems, and change requests. It provides a complete breakdown of the time you enter for the task, task categories, and days in a week. It enables you to:

-   Generate time cards for assigned projects or project tasks.
-   Copy time cards from a previous time sheet.
-   Search and create a time card for a task that is not displayed in the assigned tasks list.
-   Edit, delete, or add notes to a time card.
-   Submit, approve, reject, and recall a time sheet.
-   View notifications for the submitted, rejected, and recalled time sheets or time cards.

Time Sheet Portal comprises of the following sections:

## Header

![Header section of Time Sheet Portal](../image/workerportalheader.png)

The Time Sheet Portal header:

-   Displays a date range of the time sheet for the selected week and provides options to navigate to the time sheet of previous or next week.
-   Provides a calendar along with the date range. Clicking a date in the calendar displays the time sheet for the week of the selected date.
-   Provides a link to navigate to the time sheet for the current week when a different time sheet is being viewed.
-   Provides an option under **My Time Sheet** that enables you to open and [edit the time sheets of your resources](../task/submit-time-sheet-other-users.md). The option is available only for a user manager.
-   Provides an option to view the time sheet in the Form view using time sheet form view icon \(![Time sheet form view icon](../image/time-sheet-form-view-icon.png)\).
-   Displays the notifications for the submitted, rejected, and recalled time sheets under the show notifications icon \(![Show notifications icon](../../../product/project-management/image/NotificationIcon.png)\). Each entry displays the number of time cards and their state. Click on a notification item to open the time sheet.

    ![Show notifications displays the list of submitted, rejected, and recalled time sheets on the Time Sheet Portal.](../image/NotificationsTimeSheetPortal.png)


## Tasks

![Tasks tab on Time Sheet Portal contains the project tasks assigned to you.](../image/workerportaltasks.png)

The **Tasks** tab displays your assigned tasks as cards. Each card provides information about a task, such as short description, state, last updated date and time, and priority. Tasks are derived from the following filter conditions:

-   All your assigned incidents, problems, or change requests that are active.
-   All your assigned incidents, problems, or change requests that are closed in the selected week.
-   All tasks for which you are hard-allocated during the selected week.
-   All your assigned projects or project tasks that are active during the selected week. Project or project tasks are derived from the following conditions:
    -   A project or project task that has started and its actual start date is before the end of the selected week.
    -   A project or project task has closed and its actual end date is after the week has begun.
    -   When there are no actual dates for a project, planned dates of the project must occur within the selected week.
-   All active stories assigned to you.
-   All active scrum tasks assigned to you or closed in the selected week.
-   All active test plans assigned to you.
-   All active defect and enhancements assigned to you or closed in the selected week.

**Note:** If the Customer Service Management plugin \(com.sn\_customerservice\) is activated, your assigned tasks that are active and closed in the selected week are also derived from the following tables:

-   Case \[sn\_customerservice\_case\]
-   Work Order \[wm\_order\]
-   Work Order Task \[wm\_task\]

On the **Tasks** tab, you can perform the following operations:

-   Type a keyword in the search field to view only cards with details that match the keyword.
-   Sort cards in ascending or descending order based on priority, irrespective of the task type.
-   View cards based on a category, such as projects, project tasks, incident, problem, change, defect, enhancement, test plans, and scrum tasks.
-   Create time cards for assigned tasks. See [Create time cards and log time through Time Sheet Portal](../task/create-timecards-through-worker-portal.md).

    **Note:** [Time sheet policies](time-sheet-policies.md) apply when you create or edit a time card.


## Group Tasks

![Group Tasks tab on Time Sheet Portal contains the tasks assigned to your assignment group.](../image/TimeSheetPortalGroupTasks.png)

The **Group Tasks** tab displays the tasks assigned to your **Assignment group**. The group tasks are displayed as cards in the tab. A card provides information about the task, such as short description, state, last updated date and time, and priority.

## Other

![Other tab on Time Sheet Portal contains operational tasks like administration, meeting, and KTLO.](../image/workerportalothertasks.png)

The **Other** tab displays cards used to log time for operational work, such as administration, meeting, and KTLO.

**Note:** The list of categories in the time card controls the list of cards displayed on the **Other** tab. If an administrator marks any of the categories as inactive in the time cards, those categories are not displayed on the **Other** tab.

## Time Sheet

![Time sheet section on Time Sheet Portal displays number of tasks and hours logged for each day and their breakdown.](../image/workerportaltimesheet.png)

Starting Australia release, time cards and time sheet portal supports resource assignments. Users can select a specific resource assignment while creating time cards and submitting a time card via time sheet portal. Your system administrator can enable the resource assignment column in time sheet portal. For more information on how to add resource assignment column to time sheet, see the Knowledge Base for [KB1649389](https://support.servicenow.com/now/nav/ui/classic/params/target/kb%3Fid%3Dkb_article_view%26sys_kb_id%3D991b2135471f4210f64de825126d4309).

The Time Sheet section:

-   Displays the date range of the time sheet for the selected week.
-   Indicates the state of the time sheet being viewed.
-   Displays the total number of tasks and hours that you have entered for each day in a week. When you click a day in the time sheet, the column for that day is highlighted in both the **Time Sheet** and **Logged Time Cards** sections. The first day displayed in the Time Sheet section is based on the value specified in the **Week starts on** field in the users [Time Sheet Policy](time-sheet-policies.md). For example, if the **Week starts on** field is set to Friday, the Time Sheet section starts with Friday.
-   Indicates the total number of hours that you entered in the time sheet. Time Sheet breakdown also displays a breakdown of user-entered hours in different work categories, such as project tasks, admin, meeting, follow on tasks, or change requests.
-   Provides options that enable you to [submit a time sheet](../task/submit-timesheet-workerportal.md) and copy time cards from a previous time sheet. For an approver, options to approve or reject a submitted time sheet and recall a processed time sheet are available.

## Logged Time Cards

![Logged Time Cards section on Time Sheet Portal contains all the tasks added to the time sheet for logging hours.](../image/workerportalloggedtimecards.png)

Each row in the Logged Time Cards section represents a time card entry for a given week. It has details such as icon for state of the time card, short description of the task, project time category, rate type, resource plan, and logged time. Each row of the time card contains options that enable you to edit, delete, or add notes to a time card. For more information, see [Create time cards and log time through Time Sheet Portal](../task/create-timecards-through-worker-portal.md).

**Note:**

-   The **Rate type** column is visible only when the **Allow multiple rate types** option in the time sheet policy of the user is selected.
-   The **Resource plan** column is visible only when the **Update actual hours and cost in resource plan/reports** option in the time sheet policy of the user is selected.

The icon beside the short description of a row indicates a time card state. The merge icon \(![Merge duplicate time cards icon](../image/MergeIcon.png)\) in a time card row indicates that a duplicate time card for the same task exists in the time sheet and provides option to merge them into a single time card.

When there are no time cards, the Logged Time Cards section displays the **Generate Time Cards** and **Copy from previous time sheet** buttons to create time cards.

**Note:** Time Sheet Portal is not designed for use on mobile devices, and may not appear as shown in this document.

-   **[Add columns to the logged time card list](../task/add-columns-to-time-card-list.md)**  
Add columns in the logged time card list on the Time Sheet Portal to show additional information that you might require to log your time cards.
-   **[Create time cards and log time through Time Sheet Portal](../task/create-timecards-through-worker-portal.md)**  
After you create time cards in Time Sheet Portal, log time in the time cards.
-   **[Submit time sheet through Time Sheet Portal](../task/submit-timesheet-workerportal.md)**  
Once you update the time sheet with time worked for a given week, submit it for approval.
-   **[Approve or reject a time sheet through Time Sheet Portal](../task/approve-reject-time-sheet-from-portal.md)**  
Review, approve, or reject a time sheet submitted by a time card user that you manage.
-   **[Log time and submit time sheets of your resources](../task/submit-time-sheet-other-users.md)**  
As a user manager, you can log time and submit the time sheet of your resources.

**Parent Topic:**[Time Card Management](time-card-management.md)

