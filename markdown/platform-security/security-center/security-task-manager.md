---
title: Security Tasks
description: Use Security Tasks to monitor, prioritize, and assign all your security-related tasks in one place.
locale: en-US
release: yokohama
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2025-04-18"
reading_time_minutes: 3
breadcrumb: [Security Center, Platform Security]
---

# Security Tasks

Use Security Tasks to monitor, prioritize, and assign all your security-related tasks in one place.

Save time tracking and organizing all the tasks needed to improve and maintain your instance security posture using Security Tasks.

## Review and manage Security Tasks

![Security Task page in Security Center](../images/sec-task-mgr-1.png)

Access the Security Tasks by navigating to **All** &gt; **Security Center** &gt; **Security Tasks**. By default, all tasks are displayed in the list. You can easily filter upcoming, overdue, or open tasks by selecting the cards above the list. These cards also display the current count of tasks in each of these categories. You can further refine your filter by using the normal table field filtering options and then selecting the filter button \(![filter button](../images/filter-panel-icon.png)\), then selecting the Advanced view button to create and save a custom filters to use later.

## User roles

The Security Tasks use the following roles:

|User|Required role|Description|
|----|-------------|-----------|
|System Administrator|admin|System Administrators can view, create, assign, and delete Security Tasks.|
|Security Center Viewer|sn\_vsc\_security\_center\_viewer|Viewers can view, but not create, delete or edit Security Tasks.|
|Security Task Manager|sn\_vsc\_task\_manager|Security Task Managers can work on assigned tasks, view task manager-related pages, and create and manage tasks within Security center. They can view tasks assigned to other users but can't edit tasks assigned to other users. Task managers can't access non-task manager pages in Security Center.|
|ITIL|itil|ITIL users can interact with Security Tasks assigned to them, but can't view all tasks as the admin and Security Task manager roles can.|

## Quickly assign to yourself Security Tasks

Use the check boxes to the left of the items in the list to select multiple items. When one of more tasks is selected, you can use the **Delete** button to delete the selected tasks, or the **Edit** button to assign the selected tasks to yourself.

![Selected tasks on the task list](../images/sec-task-mgr-2.png)

## Create Security Tasks

Create a Security Task with the **+Create Task** button, which is available various platform security pages.

For example, in Security Center, on the Best Practices tool details page, the admin can select the **+Create Task** button to create and assign a task to complete this best practice.

![Incomplete best practices in Security Center](../images/task-example-1.png)![Best practices list](../images/task-example-2.png)

<table id="table_wgc_bvj_cfc"><tbody><tr><td>

![Incomplete best practice record with create task button](../images/task-example-3.png)

</td><td>

![Security task record](../images/sec-task-mgr-3.png)

</td></tr></tbody>
</table>## Automatically generated tasks

Security Tasks can be automatically generated. Automatic Security Task generation is triggered by an associated event that occurred on the platform. Learn more about generated Security Tasks in [Automatic Security Task generation](auto-sec-task.md).

## Edit and assign Security Tasks

Edit Security Tasks to assign them to users, define due dates, and provide additional details to the users who will complete these tasks. For details, see [Edit Security Tasks](../task/create-edit-security-tasks.md).

## Export tasks

You can export Security Tasks into the format of your choice to view on other platforms. For details, see [Export Security Tasks](../task/export-security-tasks.md).

-   **[Automatic Security Task generation](auto-sec-task.md)**  
Learn about how and when your instance generates Security Tasks.
-   **[Edit Security Tasks](../task/create-edit-security-tasks.md)**  
Learn how to create, edit, delete, or export Security Tasks in Security Center
-   **[Export Security Tasks](../task/export-security-tasks.md)**  
Learn how to export Security Tasks into files you can download and use in other software.

**Parent Topic:**[Security Center](sec-center-v2.md)

