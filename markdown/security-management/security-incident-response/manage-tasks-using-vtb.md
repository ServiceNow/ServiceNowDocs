---
title: Manage tasks using the Visual Task Board
description: Track and manage all the tasks associated with a major security incident using the Visual Task Board \(Kanban view\).
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Manage tasks in a Major Security Incident, Using Major Security Incident Management, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Manage tasks using the Visual Task Board

Track and manage all the tasks associated with a major security incident using the Visual Task Board \(Kanban view\).

You can use the Visual Task Board to move the cards in a step-by-step manner between lanes like Draft, Assigned or Ready, In progress, and Closed depending on the status of the tasks. An activity stream on the board displays recent activity to track task changes easily. You can add task cards from any table that extends Task to quickly track updates and edit major security incidents directly from the board.

## Create a task using the Visual Task Board

Role required: sn\_msi.workspace\_manager.

**Note:** Make sure you have installed the **MSIM VTB Task Card: 1.0.1v** app separately after installing the MSIM app.

MSI Managers can create a task in the Visual Task Board using the following steps:

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management** &gt; **Major Security Incidents**.
2.  Select the **Lists** view.
3.  Choose the required major security incident record.
4.  Select the **Tasks** tab.

    ![Create a task using the Visual Task Board](../image/msim-tasks-create-kanban-view.png "Create a task using the Visual Task Board")

5.  Select **Kanban view**, and choose **New task**.
6.  On the form, fill in the fields.

<table id="table_snp_4sn_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

A unique number that is automatically generated for the selected task. This field isn’t editable.

</td></tr><tr><td>

Incident

</td><td>

Major security incident number. This field isn’t editable.

</td></tr><tr><td>

Title

</td><td>

Provide a name for the task.

</td></tr><tr><td>

Due date

</td><td>

Select a due date and time for the task to be completed. Select a date using the **Calendar** option and specify the time on the **Select Time** section.

</td></tr><tr><td>

Description

</td><td>

Provide a unique description for the task.

</td></tr><tr><td>

Priority

</td><td>

Select the priority of the task to determine when the task is performed. The priority can be one of the following values:-   **None**
-   **1-Critical**
-   **2 - High**
-   **3 - Moderate**
-   **4 - Low**
-   **5- Planning**


</td></tr><tr><td>

State

</td><td>

Select the current state of the task. The state can be one of the following:-   **Draft**
-   **Analysis**
-   **In Progress**
-   **Closed**
The default state is **Draft**.

</td></tr><tr><td>

Assignment group

</td><td>

Select an assignment group of the user to assign the task using the search option.

</td></tr><tr><td>

Assigned to

</td><td>

Select the user to assign the task using the search option.

</td></tr><tr><td>

Affected assets

</td><td>

Select the affected assets by the task using the search option.

</td></tr><tr><td>

Affected users

</td><td>

Select the affected users by the task using the search option.

</td></tr></tbody>
</table>7.  Select **Create** to create the task.

## View and modify a task using the Visual Task Board

Role required: sn\_msi.workspace\_manager.

**Note:** Make sure you have installed the **MSIM VTB Task Card: 1.0.1v** app separately after installing the MSIM app.

MSI Managers can view the details of a task and activity information from the MSI Responders, and modify a task in the Visual Task Board using the following steps:

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management** &gt; **Major Security Incidents**.
2.  Select the **Lists** view.
3.  Choose the required major security incident record.
4.  Select the **Tasks** tab, and choose **Kanban view**.
5.  Choose the desired Task card in one of the lanes to view the details of the task.

    The Task card can be in one of the lanes: Draft, Assigned or Ready, In progress, or Closed.

6.  On the Task info section, you can modify the following details:

<table id="table_j5k_21r_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

A unique number that is automatically generated for the selected task. This field isn’t editable.

</td></tr><tr><td>

Incident

</td><td>

Major security incident number. This field isn’t editable.

</td></tr><tr><td>

Title

</td><td>

Provide a name for the task.

</td></tr><tr><td>

Due date

</td><td>

Select a due date and time for the task to be completed. Select a date using the **Calendar** option and specify the time on the **Select Time** section.

</td></tr><tr><td>

Description

</td><td>

Provide a unique description for the task.

</td></tr><tr><td>

Priority

</td><td>

Select the priority of the task to determine when the task is performed. The priority can be one of the following values:-   **None**
-   **1-Critical**
-   **2 - High**
-   **3 - Moderate**
-   **4 - Low**
-   **5- Planning**


</td></tr><tr><td>

State

</td><td>

Select the current state of the task. The state can be one of the following:-   **Draft**
-   **Analysis**
-   **In Progress**
-   **Closed**
The default state is **Draft**.

</td></tr><tr><td>

Assignment group

</td><td>

Select an assignment group of the user to assign the task using the search option.

</td></tr><tr><td>

Assigned to

</td><td>

Select the user to assign the task using the search option.

</td></tr><tr><td>

Affected assets

</td><td>

Select the affected assets by the task using the search option.

</td></tr><tr><td>

Affected users

</td><td>

Select the affected users by the task using the search option.

</td></tr></tbody>
</table>7.  Select the **Activity** section to view the activity details from the MSI Responders.

    Use the Activity section to add your work notes and comments, and post your activity privately and also add additional comments as required using the Compose section. Save the activity after you post your work notes and comments to view the added activity or worknotes in the Activity section.

    ![Activity section on the Visual Task board](../image/msim-tasks-kanban-view-update.png "Activity section on the Visual Task board") ![]( "Activity section on the Visual Task board")

    **Note:** Select the **Show more** details link to view the details of a specific security incident record, which is associated with that major security incident.

8.  Select **Save** to update the task information.

    The task information gets updated instantly.


## Delete a task using the Visual Task Board

Role required: sn\_msi.workspace\_manager.

**Note:** Make sure you have installed the **MSIM VTB Task Card: 1.0.1v** app separately after installing the MSIM app.

MSI Manager can delete a task in the Visual Task Board using following steps:

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management** &gt; **Major Security Incidents**.
2.  Select the **Lists** view.
3.  Choose the required major security incident record.
4.  Select the **Tasks** tab, and choose **Kanban view**
5.  Choose the Task card that you want to delete.
6.  In the Major security incident task pop-up, select the **Delete** option.

    The Delete task pop-up appears requesting you to confirm the deletion of the task.

7.  Select **Delete**.

**Parent Topic:**[Manage tasks in a Major Security Incident](tasks-tab.md)

**Related topics**  


[Manage tasks using the List view](manage-tasks-using-list-view.md)

