---
title: Notifications for project updates in your collaboration tool
description: Receive updates related to your project on your Slack channel or Microsoft team. Analyze the delayed and overdue tasks, follow closure of milestones, and monitor changes to risk, issue, decision, action, and change request \(RIDAC\) items of your project.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [PPM Collaboration, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Notifications for project updates in your collaboration tool

Receive updates related to your project on your Slack channel or Microsoft team. Analyze the delayed and overdue tasks, follow closure of milestones, and monitor changes to risk, issue, decision, action, and change request \(RIDAC\) items of your project.

Using the automatic project status updates on the project collaboration channel or team, project managers can take informed decisions about project planning, resource management, finance allocation. The team members can understand updates made to the project and actively collaborate on any delayed or overdue tasks.

**Note:** Project managers can reach out to their system administrators to configure the application settings for these notifications according to their preferences.

## Daily notification on project status

A notification with the consolidated project status is sent to the project's channel daily at 8:00 AM which consists of the following information.

<table id="table_r3d_r3d_mmb"><thead><tr><th>

Notification

</th><th>

Information

</th></tr></thead><tbody><tr><td>

Project overview

</td><td>

-   A direct URL of the project. Clicking this URL opens the project in your ServiceNow instance.
-   Name of the project.
-   Planned start and end dates of the project.
-   State of the project, for example, Work in Progress.
-   Status of the project, for example, Green.
-   Percentage of project completion.
-   Any exceptions like estimation at completion is greater than total planned cost, planned end date is later than the approved end date, project not started on the start date, and project running late.

</td></tr><tr><td>

Project tasks due today

</td><td>

List of project tasks that have planned end date marked as today and are in the Work in Progress state. The list displays only five project tasks that are sorted alphabetically by their short description.

</td></tr><tr><td>

Overdue Tasks \(Tasks not started on planned start date\)

</td><td>

List of project tasks which have a planned start date before today but are not in either the Work in Progress or Closed states. The list displays only five project tasks that are sorted in an ascending order of the planned start dates so that you get high visibility into the tasks that are overdue for a longer period.

</td></tr><tr><td>

Delayed Tasks \(Tasks not completed on planned end date\)

</td><td>

List of project tasks which have a planned end date before today and are in the Work in Progress state. The list displays only five project tasks that are sorted in ascending order of the planned end dates so that you get high visibility into the tasks that have been delayed for a longer period.

</td></tr><tr><td>

Project tasks due within seven days

</td><td>

List of five of the following project tasks that have a planned end date within seven days from today. All these tasks are displayed in ascending order of their due dates so that you get high visibility into the tasks that are due soon.

**Note:** Tasks that in Closed state are not displayed in the list.

-   High priority risks, issues, and action items
-   Milestone or key milestone tasks

</td></tr></tbody>
</table>## Notification regarding change of project manager

When there is a change in the manager of your project, an update is made to the Project manager field of the project record.

-   A notification including the project URL is sent to your project channel on this update.
-   New project manager is added as a member of the channel.
-   If no project tasks are assigned to the old project manager, this user is removed as a member of the channel.

## Notification for other updates to the project

<table id="table_a3w_1nd_mmb"><thead><tr><th>

Notification

</th><th>

Information

</th></tr></thead><tbody><tr><td>

Project's status

</td><td>

When an update is made to the Status or State fields of the project, a notification including the project URL is sent to your project channel.

</td></tr><tr><td>

RIDAC records

</td><td>

You receive notifications in your project channel when a new RIDAC record is added to or an existing RIDAC record is updated in the project for the following scenarios. With every notification, you receive a direct URL to the corresponding record.

-   Risk
    -   New risk is created with the Probability field set to **High** or **Absolute**
    -   The Probability field for an existing risk is updated to **High** or **Absolute**
-   Issue, Decision, Action, and Change request
    -   New record is created with the priority field set to **1-Critical** or **2-High**
    -   Priority of an existing record is updated to **1-Critical** or **2-High**

</td></tr><tr><td>

Key milestone/ milestone

</td><td>

Whenever a key milestone or milestone task is Closed Complete, Closed Incomplete, and Closed Skipped, you are notified about the closure and the user who closed it, with a direct URL to the milestone task.

</td></tr></tbody>
</table>**Parent Topic:**[Using Project Management](../../project-management/concept/using-project-management.md)

