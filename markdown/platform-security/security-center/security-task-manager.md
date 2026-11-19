---
title: Security Tasks
description: Use Security Tasks to monitor, prioritize, and assign all your security-related tasks in one place.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/security-center/security-task-manager.html
release: brazil
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Security Center, Platform Security]
---

# Security Tasks

Use Security Tasks to monitor, prioritize, and assign all your security-related tasks in one place.

Track and organize all the tasks needed to improve and maintain your instance security posture using Security Tasks.

## Review and manage Security Tasks

\[Omitted image "sec-task-mgr-1.png"\] Alt text: Security Task page in Security Center

Access the Security Tasks by navigating to **All** &gt; **Security Center** &gt; **Security Tasks**. By default, all tasks are displayed in the list. You can filter upcoming, overdue, or open tasks by selecting the corresponding cards. These cards also display the current count of tasks in each of these categories. You can further refine your filter by using the normal table field filtering options and then selecting the filter button \[Omitted image "filter-panel-icon.png"\] Alt text:, then selecting the **Advanced view** button to create and save a custom filters to use later.

## User roles

The Security Tasks use the following roles.

|User|Required role|Description|
|----|-------------|-----------|
|Administrator|admin|Administrators can view, create, assign, and delete Security Tasks.|
|Security Center Viewer|sn\_vsc\_security\_center\_viewer|Viewers can view, but not create, delete or edit Security Tasks.|
|Security Task Manager|sn\_vsc\_task\_manager|Security Task Managers can work on assigned tasks, view task manager-related pages, and create and manage tasks within Security Center. They can view tasks assigned to other users but can't edit tasks assigned to other users. Task managers can't access non-task manager pages in Security Center.|
|ITIL|itil|ITIL users can interact with Security Tasks assigned to them, but can't view all tasks as the admin and Security Task manager roles can.|

## Quickly assign to yourself Security Tasks

To select multiple items, select the check box for each item in the list. When one of more tasks is selected, you can use the **Delete** button to delete the selected tasks, or the **Edit** button to assign the selected tasks to yourself.

\[Omitted image "sec-task-mgr-2.png"\] Alt text: Selected tasks on the task list

## Create Security Tasks

Create a Security Task with the **+Create Task** button, which is available various platform security pages.

For example, in Security Center, on the Best Practices tool details page, a user who has the admin role can select the **+Create Task** button to create and assign a task to complete this best practice.

<table id="table_wgc_bvj_cfc"><tbody><tr><td>

\[Omitted image "task-example-3.png"\] Alt text: Incomplete best practice record with create task button

</td><td>

\[Omitted image "sec-task-mgr-3.png"\] Alt text: Security task record

</td></tr></tbody>
</table>## Automatically generated tasks

Security Tasks can be automatically generated. Automatic Security Task generation is triggered by an associated event that occurred on the platform. Learn more about generated Security Tasks in [Automatic Security Task generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/auto-sec-task.md).

## Edit and assign Security Tasks

Edit Security Tasks to assign them to users, define due dates, and provide additional details to the users who complete these tasks. For details, see [Edit Security Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/create-edit-security-tasks.md).

## Export tasks

You can export Security Tasks into the format of your choice. For details, see [Export Security Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/export-security-tasks.md).

-   **[Automatic Security Task generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/auto-sec-task.md)**  
Your instance automatically generates Security Tasks when specific events occur, such as a breached metric threshold or a new banner announcement.
-   **[Edit Security Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/create-edit-security-tasks.md)**  
Edit or delete Security Tasks in Security Center to keep task details, assignments, and work notes current.
-   **[Export Security Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/export-security-tasks.md)**  
Export Security Tasks to Excel, CSV, JSON, or PDF files that you can download or receive by email and use in other software.

**Parent Topic:**[Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/security-center/sec-center-v2.md)

