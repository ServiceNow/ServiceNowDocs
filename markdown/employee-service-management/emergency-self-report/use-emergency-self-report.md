---
title: Report and track health statuses during an emergency
description: Emergency Self Report is used by users to self-report their health status, by managers to track the health status of their users, and by response teams to view the status for all users and sort the data for analysis and action.
locale: en-US
release: yokohama
product: Emergency Self Report
classification: emergency-self-report
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Emergency Self Report, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Report and track health statuses during an emergency

Emergency Self Report is used by users to self-report their health status, by managers to track the health status of their users, and by response teams to view the status for all users and sort the data for analysis and action.

## Before you begin

Role required: sn\_imt\_quarantine.crisis\_task\_user or sn\_imt\_quarantine.humanResourceTeam

## About this task

The workflow for Emergency Self Report begins with users self-reporting their health status, managers determining the actions that must be taken related to the user's status, and a response team evaluating a unified view of the status of all reporting users.

## Procedure

-   To report your health status:

    1.  Navigate to **Emergency Self Report** &gt; **Emergency Self Report Dashboard**.

        **Note:** To report your health status in the Now Mobile app, navigate to the **Health** tab and tap the quick action icon \(![Quick action icon.](../../human-resources/reference/images/quick-action-icon.png)\) in the top-right corner.

        If you're a manager, your name is automatically selected in the **Person** field so that you can report your own health status. If you're reporting the status for a direct report, select the user's name from the **Person** field.

        If you're not a manager, you can report only your own status and the **Person** field doesn't appear.

    2.  Choose an option from the **Health status** list.

        System administrators can configure these options.

        ![Users report their own health status.](../image/employee-self-report-employee-view.png)

    3.  Click **Save**.

        The health status is updated on the left side of the screen. A message is sent to your manager, and a crisis task is generated for the response team. The crisis task can be assigned an approver, and the reporting user's assigned tasks can be reviewed.

        If Contact Tracing is installed and you selected the **In quarantine** option, a case is created automatically for the user. If an active case exists for the user at the time of reporting, a note is added to the case about the self-reporting. For more information, see ServiceNow® [Contact Tracing](../../contact-tracing/concept/exposure-case-management.md).

    4.  When you're ready to return to work, update your health status to **Return to Work**.

        A Human Resources task is created so that HR can coordinate with you. The HR task is for information, and is not updated automatically when other tasks are updated. In the manager's view, your status changes to green.

-   To evaluate the health status of your direct reports if you're a manager:

    1.  Navigate to **Emergency Self Report** &gt; **Emergency Self Report Dashboard**.

        You see a single screen view of your direct team’s status and tasks, and can select individual user records. Green tiles indicate that the user has provided no information. The tiles of affected team members are red and display an icon.

        ![Emergency Self Report manager view.](../image/employee-self-report-dashboard-manager-view-fullscreen.png)

    2.  To display a user's assigned tasks, click a tile.

    3.  To reassign tasks for the user, click the **Reassign** link in the task row, assign the task to another user, and click **Submit**.


**Parent Topic:**[Emergency Self Report](../concept/emergency-self-report.md)

**Related topics**  


[View a dashboard of all user reports if you are a response team member](view-hr-tasks-response-team.md)

