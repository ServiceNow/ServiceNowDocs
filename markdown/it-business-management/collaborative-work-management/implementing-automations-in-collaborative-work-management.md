---
title: Work item automations in CWM
description: Boost team efficiency by automating monotonous actions such as sending notifications and emails, monitoring key dates, or reassigning tasks based on the conditions that suit the team's workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/implementing-automations-in-collaborative-work-management.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Collaborative Work Management, Strategic Portfolio Management]
---

# Work item automations in CWM

Boost team efficiency by automating monotonous actions such as sending notifications and emails, monitoring key dates, or reassigning tasks based on the conditions that suit the team's workflow.

When teams work together, they often spend much time and manual effort on workflow activities. To address this issue and help improve the overall team efficiency, team members can create automations for tasks in CWM Boards.

Automations in CWM are actions that are triggered when certain conditions are met. Once created, these automations are applicable to all work items in the Board that they’re created in. Some examples of automated actions are:

-   Sending an email when a task assignment is changed.
-   Updating task priority when the due date is moved.
-   Reassigning tasks when the priority is changed.
-   Sending a notification when a task is complete.
-   Notifying a task assignee dynamically when the priority is changed.

Six predefined templates are provided in the application to help you build multiple simple or complex conditions and automate actions for your work items.

\[Omitted image "cwm-automations-templates.jpg"\] Alt text: Predefined automation templates in CWM.

Based on the changing conditions of your team's workflow, you can edit, disable, or delete automations anytime later. For a Board, a maximum of 10 automations can be created, which includes all the active and inactive ones.

In this example automation, when the **Priority** of a task on this Board changes to **High**, the people in the **Assigned to** column of the task and the owners of this Space are notified of it.

Going forward, when the priority of any item of this Board changes to High, a notification is sent to the user assigned to that task and the Space owners. Thus this automation saves the time that it takes to perform this action manually instead.

**Note:** You can also send notifications to any user if you've added a custom people column in addition to the default Assigned to or Additional Assignee.

\[Omitted image "cwm-add-automation.jpg"\] Alt text: New automation in CWM Board.

Get started with automations in CWM. See [Create automations in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/create-and-manage-automations-in-cwm.md).

-   **[Create automations in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/create-and-manage-automations-in-cwm.md)**  
Add conditions to build task automations for CWM Boards and help your team save time from manual task updates.
-   **[Manage or delete automations in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/manage-or-delete-automations-in-cwm.md)**  
Edit, disable, or delete automations for your Boards in Collaborative Work Management based on the changing conditions of your team's workflow.

**Parent Topic:**[Using Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/using-collaborative-work-management.md)

