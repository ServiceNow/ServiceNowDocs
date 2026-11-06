---
title: Communicate tab in the Major Incident workbench
description: The Communicate tab helps you understand the progress of a communication plan and its related tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/mi-workbench-communicate-tab.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Major incident workbench UI elements, Major incident workbench, Managing major incidents, Incident Management, IT Service Management]
---

# Communicate tab in the Major Incident workbench

The **Communicate** tab helps you understand the progress of a communication plan and its related tasks.

When a communication plan has multiple communication tasks, all the tasks appear under that plan.

\[Omitted image "communication-task-filter.png"\] Alt text: Communication task filter showing all, active, and completed task options

You can filter communication tasks to view all tasks, active tasks, or completed tasks. You can also add a communication plan by selecting **Add**. You can create a communication task for an existing plan by selecting **Add Task**. For steps to add a communication plan, see [Add a communication plan in the workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/add-comm-plan-from-mim-workbench.md). To add or remove recipients from a plan after it's saved, select **Manage Recipients**.

**Note:** When you create a communication task for sending an email in the major incident workbench and select a recipient list, the recipient list is added instead of individual users. The system calculates the users in the recipient list while processing the email request, which helps improve system performance. You can also add users, groups, and email addresses as required in the Recipients section. Activate this feature by selecting the **Property to toggle support for Recipient List on Email Client, on Communication Tasks** \(**sn\_comm\_management.email\_client\_recipient\_items\_enabled**\) option in the Major Incident Management Properties. You can create a recipient list using a script to retrieve a custom list of users or include a predefined list of users.

\[Omitted image "manage-recepients.png"\] Alt text: Manage recipients

You can perform the following actions on a communication task:

-   **Close Task**: Closes the communication task. If the task was performed at least once, the state changes to Complete. Otherwise, the state changes to Skipped.
-   **Snooze**: Skips the communication task one time and refreshes the due-in timer. Available only for recurring communication tasks.
-   **View Form**: Opens the form for the task in the plan.
-   **View Activity**: Displays the activity history, where you can post work notes or additional comments for a communication task.

\[Omitted image "communication-task-actions.png"\] Alt text: Communication task actions menu with Close Task, Snooze, View Form, and View Activity options

You can also view the due time of upcoming tasks and the overdue time if the task isn’t completed within the expected time.

To send a notification, select **Compose**. If the notification is sent only once, the status of the task changes to Complete after it's sent. If the task is recurring, the status of the task changes to Open. After each recurrence, the status changes to **Sent** followed by the recurrence count. For example, Sent\(2x\) means the task ran twice.

\[Omitted image "comm-task-state.png"\] Alt text: Communication task state

Icons next to the communication task name represent the state of the task, such as completed, skipped, or active.

Under the Work Notes &amp; Activity section, you can initiate a chat at the incident or incident communication plan level. You can also view the activity stream for that record.

## Messaging users through Slack

For Slack functionality, install [Collaboration services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/collaboration-services/collab-services-tcm.md) from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

When you add Slack as a communication channel, you can select **Compose** to send the Slack message to the contacts that you specified when defining the communication plan. The selected contacts receive a direct message from the Slack bot. You can perform the communication task actions such as **Close Task**, **Snooze**, **View Form**, and **View Activity**.

**Parent Topic:**[Major incident workbench UI elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/mi-workbench-ui-elements.md)

**Related topics**  


[Summary tab in the Major Incident workbench]()

[Post Incident Report tab in the Major Incident workbench]()

[Collaborate tab in the Major Incident workbench]()

