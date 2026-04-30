---
title: Create a task for a legal matter
description: Create a task in a legal matter or a phase of the matter that you or another user should perform to resolve the matter.
locale: en-US
release: yokohama
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Work on a legal matter, Legal Matter Management, Legal Service Delivery, Employee Service Management]
---

# Create a task for a legal matter

Create a task in a legal matter or a phase of the matter that you or another user should perform to resolve the matter.

## Before you begin

Role required: sn\_lg\_matter.matter\_fulfiller

## About this task

As a collaborator added to a legal matter, you can access and work on the legal matter just as matter owners can. However, you can't modify the **Matter owner**, **Assignment group**, and **Assignment group permission** fields.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  In the Legal Counsel Center tab, select the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, open a legal matter by selecting an option under **Matters**.

<table id="choicetable_qbl_2bj_gtb"><thead><tr><th align="left" id="d524503e105">

Option

</th><th align="left" id="d524503e108">

Steps

</th></tr></thead><tbody><tr><td id="d524503e114">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a legal matter to work on.
3.  If the legal matter is newly assigned to you, select **Start** to start working on it.

The state of the legal matter updates to Work in Progress.

</td></tr><tr><td id="d524503e143">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a legal matter to work on.


</td></tr></tbody>
</table>4.  Add tasks to a matter or a phase.

    -   To add a task to a matter, in the **Tasks** tab of the Legal Matter form, click **New**.
    -   To add a task to a phase, open a phase from the **Phases** tab and click **New** in the **Legal Matter Tasks** tab of the phase record.
5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the task.|
    |Type|Type of the task.|
    |Priority|Level of priority to work on and complete the task. The priority of a task determines its importance for resolving the matter.|
    |Phase|Phase to which the task belongs.|
    |Matter|Matter to which the task belongs.|
    |Event name|Name of the calendar event associated with the task. A calendar event with a due date helps you to track the progress of the task for specific milestones.|
    |State|Current state of the task to determine the progress of the task.|
    |Order|Order in which the task should be worked on when there are multiple tasks in a phase or matter.|
    |Assignment group|User group to which the task is assigned.|
    |Assigned to|User to whom the task is assigned. If an assignment group is selected, the list shows members of the selected group.|
    |Due date|Date to complete the task.|
    |Short description|Short description to specify the expected activities and output involved in completing the task.|
    |Notes section|
    |Additional comments|Comments or notes that the requester can also see.|
    |Work notes|Comments or notes that only authorized users related to the matter can see.|
    |Risk Details - This section appears only when Risk and Mitigation is selected from Type.|
    |Risk owner|Owner of the risk.|
    |Risk description|Description of the risk.|
    |Proposed mitigation plan|Plan to mitigate the risk.|
    |Action completed|Actions that have been completed.|
    |Interview Details - This section appears only when Interview is selected from Type.|
    |Start date and time|The date and start time of the interview.|
    |End date and time|The date and end time of the interview.|
    |Interviewee|Name of the person who you are interviewing.|
    |Additional interviewers|Names of the people who conducted the interview.|
    |Interview notes|Notes from the interview.|

6.  Click **Save**.

7.  In the contextual sidebar, add instructions and to-do items for the task.

    -   In the **Instructions** section, click **Add** to add instructions for the assigned user to do to complete the task.
    -   In the **Checklist** section, click **Create** to add to-do items to track the progress of activities in the matter task.
    -   If the matter type is set to Interview, then Interview Template component is visible in contextual sidebar.
    **Important:** To use interview templates, you must first install the Interview Templates plugin \(com.sn\_interview\_templates\) and enable the Requested RCA of Interview Templates for Legal Matter Management and Legal Counsel Center application scope.

8.  [Add an artifact \(folder\)](add-artifact-to-legal-matter.md) in which you or the assigned user can upload files related to the task or its investigation.


## Result

A legal matter task is created and is listed in the matter's **Tasks** tab. If the task was added in a phase record, then the task is also listed in the phase's **Legal Matter Tasks** tab.

**Tip:** If the new task doesn't appear in the list, click the refresh list button \(![Refresh list icon.](../image/refresh-list-icon.png)\).

