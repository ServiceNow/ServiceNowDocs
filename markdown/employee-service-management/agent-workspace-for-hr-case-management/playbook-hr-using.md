---
title: Using HR Service Delivery Playbook
description: Currently, HR Service Delivery Playbook is only available for use with lifecycle event HR cases.You can add a work note or comment to an HR lifecycle event case from Playbook.You can open a sub-case or task on an HR lifecycle event case from Playbook.You can view the activity stream in a modal from HR Playbook.Depending on the activity, you can add attachments from Playbook.You can cancel and revert work done in a lifecycle event case using the rescind process.As an HR agent, you can view emails to the opened for or subject person on a lifecycle event case.
locale: en-US
release: zurich
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Playbook, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Using HR Service Delivery Playbook

Currently, HR Service Delivery Playbook is only available for use with lifecycle event HR cases.

Playbook shows as a tab on the HR Agent Workspace form after displaying an LE case.

**Note:** The Playbook tab only appears after the HR case has moved to **Ready** or **Work in Progress**. This triggers the lifecycle event and data appears for all launched activities.

![HR Service Delivery Playbook](../image/playbook-hr-playbook-tab.png)

Selecting the Playbook tab allows you to view and work all lifecycle event activities and their child tasks in a single pane.

**Note:** Tasks that are created ad-hoc and not part of the workflow do not appear in the tab, but may be accessible in regular related lists.

-   **Lifecycle event**

    The title of the lifecycle event is at the top below the **Playbook** tab in the stage panel.

-   **Activity sets**

    The list of lanes along with their status icon appear below the lifecycle event description.![HR Agent WS - Stage panel](../image/playbook-hr-le-column.png)

    Under the New Hire Onboarding \(Demo\) lifecycle event are five \(5\) activity sets:

    -   Start onboarding
    -   Prepare for day 1
    -   Start your new job!
    -   Ramp up
    -   Initial check-in
-   **Activities**

    Click on an activity set to view the associated activities.

    ![HR Agent WS - Activity stream](../image/playbook-hr-activity-stream.png)


## HR Playbook add a note or comment

You can add a work note or comment to an HR lifecycle event case from Playbook.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select a lifecycle event case.

3.  Click an activity set.

    ![HR Agent WS - Playbook activity sets](../image/playbook-hr-activity-sets.png)

4.  Click an activity within the opened activity set.

    ![HR Agent WS - Playbook activities](../image/playbook-hr-activities.png)

5.  Click the **Add note or comment** icon ![HR Agent WS - Playbook add note or comment icon](../image/playbook-hr-comment-icon.png).

    ![HR Agent WS - Playbook click add note or comment](../image/playbook-hr-click-comment-icon.png)

6.  Select **Work notes \(Private\)** or **Comments**.

    ![HR Agent WS - Playbook compose note or comment](../image/playbook-hr-compose-comment.png)

7.  Enter text and click **Post Work notes \(Private\)** or **Post Comments**.

8.  Click the **Filter by** icon ![HR Agent WS - Playbook filter by icon](../image/playbook-hr-filter-icon.png) to filter by activities.

    ![HR Agent WS - Filter by](../image/playbook-hr-filter-by.png)

9.  Check the filters you want to show activities under.

10. Click the More Options icon ![HR Agent WS - Playbook more options icon]().

    ![HR Agent WS - Playbook more options filter](../image/playbook-hr-more-options.png)

11. Select the filters you want to use to show activities by.


## HR Playbook open a case or a task

You can open a sub-case or task on an HR lifecycle event case from Playbook.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select a lifecycle event case.

3.  Click an activity set.

    ![HR Agent WS - Playbook activity sets](../image/playbook-hr-activity-sets.png)

4.  Click an activity within the opened activity set.

    ![HR Agent WS - Playbook activities](../image/playbook-hr-activities.png)

5.  Click the **Open task** icon ![HR Agent WS - Playbook open task icon](../image/playbook-hr-open-task-icon.png).

    ![HR Agent WS - Playbook open task](../image/playbook-hr-open-task.png)

6.  The details of a sub-case or task opens.

    ![HR Agent WS - Playbook opened task](../image/playbook-hr-opened-task.png)

7.  You can make edits and click **Save**.

8.  To return to Playbook, click the **Details** tab.


## HR Playbook see activity

You can view the activity stream in a modal from HR Playbook.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select a lifecycle event case.

3.  Click an activity set.

    ![HR Agent WS - Playbook activity sets](../image/playbook-hr-activity-sets.png)

4.  Click an activity within the opened activity set.

    ![HR Agent WS - Playbook activities](../image/playbook-hr-activities.png)

5.  Click the **See activity** button.

    **Note:** Only agents with access to the case card and not assigned to the case can see this button. The Assigned to agent does not see this button.

    ![HR Agent WS - Playbook See activity button](../image/playbook-hr-see-activity.png)

    Activities can have links to training, videos, or catalog items. The state of the activity also appears to the right.![HR Agent WS - Playbook activities link](../image/playbook-hr-catalog-link.png)

    **Note:** Clicking the Catalog Item link opens the general catalog page.


## HR Playbook add attachment

Depending on the activity, you can add attachments from Playbook.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select a lifecycle event case.

3.  Click an activity set.

    ![HR Agent WS - Playbook activity sets](../image/playbook-hr-activity-sets.png)

4.  Click an activity within the opened activity set.

    ![HR Agent WS - Playbook activities](../image/playbook-hr-activities.png)

5.  Click **+Add File**.

6.  Select the file you want to up load and click **Open**.


## HR Playbook rescind an activity

You can cancel and revert work done in a lifecycle event case using the rescind process.

### Before you begin

Role required: sn\_hr\_le.case\_writer

For more information, see [Configure the rescind process for a lifecycle event](../task/configure-rescind-for-a-lifecycle-event.md).

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select a lifecycle event case.

3.  Click **Rescind**.

    ![HR Agent WS - Playbook rescind](../image/playbook-hr-rescind.png)

4.  Enter a reason for rescinding the case.

    **Note:** You cannot undo a rescind, so proceed with caution.

5.  Click **OK**.

    The rescind activities appear and future activity sets are cancelled.


## View email sent to opened for or subject person

As an HR agent, you can view emails to the opened for or subject person on a lifecycle event case.

### Before you begin

Role required: sn\_hr\_le.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select a lifecycle event case.

3.  Select an activity set.

4.  From any activity, when there is a **See email body** button, click it.

    ![HR Playbook email notification](../image/playbook-hr-email-not.png)

5.  Click the **X** at the top, right corner of the email to close it.


