---
title: Initiate Microsoft Teams group chat from MIM workbench
description: You can initiate a Microsoft Teams group chat from the MIM workbench to work towards the resolution of the task.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Add collaborative communication task from MIM workbench, Agent actions, Use ITSM and HRSD integrations with Microsoft Teams, Use Microsoft Teams integration for Employee Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Initiate Microsoft Teams group chat from MIM workbench

You can initiate a Microsoft Teams group chat from the MIM workbench to work towards the resolution of the task.

## Before you begin

Role required: major\_incident\_manager

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Major Incidents** &gt; **Open**.

2.  Open the relevant major incident.

3.  Click **View Workbench**.

4.  Click **Collaborate** tab.

5.  Click **Initiate** button.

    ![Initiate Microsoft Teams group chat.](../images/initiate-ms-teams-group-chat.png)

6.  Within the dialog box that appears, select the participants for the chat.

    ![Participants for the group chat modal screen.](../images/initiate-ms-teams-group-chat-02.png)

    The dialog box displays the **Recommended** and **Selected** participants for the chat.

    All users from the assigned group for the ticket are in the recommended section by default. The user who initiates the chat is added to the selected list of participants.

7.  Click **Add Participants** list to:

    -   **Users**: Enter the name of the user to include in the chat.
    -   **Group**: Enter the group of users to be included in the chat.

        If the On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is activated, the On-Call Scheduling users will be added when you select a group. On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin isn't activated, it adds all users from the selected group.

    -   **Email**: Enter a valid email of the participant to be included in the chat.
8.  Click **Add to selected**.

    The **Chat Title** appears only if there are more than two participants in the chat.

9.  Click **Start Chat**.


## Result

The Microsoft Teams application opens the tab where the agent can chat with all the selected participants.

**Parent Topic:**[Add collaborative communication task from MIM workbench](add-collab-comm-task-mim-workbench.md)

