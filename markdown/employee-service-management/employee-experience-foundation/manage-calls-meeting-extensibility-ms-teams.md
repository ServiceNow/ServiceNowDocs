---
title: Manage calls using Meeting Extensions
description: Use Meeting Extensions to start conference calls to discuss the resolution for a major incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/manage-calls-meeting-extensibility-ms-teams.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use Microsoft Teams Meeting Extensions, Use Microsoft Teams integration for Agent Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Manage calls using Meeting Extensions

Use Meeting Extensions to start conference calls to discuss the resolution for a major incident record.

## Before you begin

Role required: itil, itil\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Major incidents** &gt; **Open**.

2.  Open the relevant major incident.

3.  Select **View Workbench**.

4.  Select **Collaborate** tab.

5.  Select **Add** that appears in **Communication Tasks** section.

6.  On the form, fill the fields.

    |Field|Description|
    |:----|:----------|
    |Communication Plan|List to select a new communication plan or to select an existing plan and add communication tasks to the plan.|
    |Task Short description|Brief description of what the communication task is all about.|
    |Channels|Select Microsoft Teams group chat.|
    |Frequency|Frequency at which a specific task must be executed. A task can be executed only once or on specific durations.|
    |Due in \(Minutes\)|Time span when the task must be executed after the task initiates. For recurring tasks, it also indicates the time span after which the task must repeat.|

    \[Omitted image "collab-task2.png"\] Alt text: Add collaboration communication task.

7.  Select **Next**.

8.  In the **Manage Recipients** tab, add the users required to be involved in the major incident communication plan.

9.  Select **Add**.

    The task appears in the **Collaborate** tab.

10. Select **Initiate** button.

11. Within the dialog box that appears, select the participants for the chat.

    \[Omitted image "initiate-tech-call.png"\] Alt text: Participants for the group chat modal screen.

    The dialog box displays the **Recommended** and **Selected** participants for the chat.

    All users from the assigned group for the ticket are in the recommended section by default. The user who initiates the chat is added to the selected list of participants.

12. Select **Add Participants** list to:

    -   **Users**: Enter the name of the user to include in the chat.
    -   **Group**: Enter the group of users to be included in the chat.

        If the On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is activated, the On-Call Scheduling users are added when you select a group. On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin isn't activated, it adds all users from the selected group.

    -   **Email**: Enter a valid email of the participant to be included in the chat.
13. Select **Add to selected**.

    The **Chat Title** appears only if there are more than two participants in the chat.

14. Select **Start**.

    The Microsoft Teams application opens the tab where the agent can chat with all the selected participants.

15. Select \[Omitted image "show\_hide\_conversation.png"\] Alt text: Show and Hide conversation to toggle between show and hide conversation.

16. Select **ServiceNow Meeting Extensions** tab.

    \[Omitted image "me-ms-teams01.png"\] Alt text: ServiceNow Meeting Extensibility tab.

    -   **Details** tab: Displays the details of the major incident. Select **View in workbench** to open the major incident in ServiceNow.
    -   **Communication Tasks** tab: Displays the communication tasks of this major incident.
17. Select **Communication Tasks** tab.

    \[Omitted image "communications-tasks-ms-teams-01.png"\] Alt text: Communication tasks tab in Microsoft Teams

    -   The information in the **Details** tab, and the **Communication Tasks** tab is automatically updated during the meeting whenever the major incident is updated from ServiceNow.
    -   The timer color in Microsoft Teams changes when the remaining time goes past 75% of the stipulated time.
18. To move the major incident to resolved state, open the major incident in the major incident workbench, and select **Resolve**.

    \[Omitted image "major-incident-resolved-01.png"\] Alt text: Major incident is resolved

    The state is updated in the Microsoft Teams meeting.


**Parent Topic:**[Use Microsoft Teams Meeting Extensions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/c-agent-ex-use-meet-ext.md)

