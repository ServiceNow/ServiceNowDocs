---
title: The Communicate tab in the Major Incident workbench
description: The Communicate tab helps you understand the progress of a communication plan and its related tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/incident-management/mi-workbench-communicate-tab.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Major incident workbench UI elements, Major incident workbench, Managing major incidents, Incident Management, IT Service Management]
---

# The Communicate tab in the Major Incident workbench

The **Communicate** tab helps you understand the progress of a communication plan and its related tasks.

If there are multiple communication tasks associated with a communication plan, all the tasks appear under the respective communication plan.

\[Omitted image "communication-task-filter.png"\] Alt text: communication task filter

You can filter the communication task to view all tasks, active tasks, or completed tasks. You can also add a new communication plan by clicking **Add**. You can create a communication task for an existing plan by clicking **Add Task**. For more information, see [Add communication plan from the major incident workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/add-comm-plan-from-mim-workbench.md). If you want to add or remove recipients from a particular plan after the plan is saved, click **Manage Recipients**.

**Note:** When you create a communication task for sending an email on the Major Incident Management Workbench and select a recipient list, the recipient list is added instead of individual users. The list of users in the recipient list is calculated by the system while processing the email request, thus improving the system performance. Also, you can add users, groups, and email addresses as required in the Recipients section. Activate this feature by selecting the **Property to toggle support for Recipient List on Email Client, on Communication Tasks** \(**sn\_comm\_management.email\_client\_recipient\_items\_enabled**\) option in the Major Incident Management Properties. You can create a recipient list using a script to retrieve a custom list of users or include a pre-defined list of users.

\[Omitted image "manage-recepients.png"\] Alt text: Manage recipients

The following actions can be performed on a given communication task:

-   **Close Task**: If the task is performed at least once, closes the communication task and changes the state to Complete. Otherwise, the state changes the state to Skipped.
-   **Snooze**: Available only for recurring communication task. Enables the user to skip the communication task once and the due-in timer is refreshed.
-   **View Form**: For each task in the plan, you can navigate back to the form.
-   **View Activity**: Enables you to view activity history and post your work notes or additional comments for a communication task.

\[Omitted image "communication-task-actions.png"\] Alt text: communication task actions

You can also view the due time of upcoming tasks and the overdue time in case the task isn’t completed within the expected time.

To send a notification, click **Compose**. If the notification has to be send only once, then after sending the notification, the status of the task changes to Complete. If the task is recurring, the status of the task changes to Open. After a recurring communication task is performed, the status of the communication task changes to **Sent** followed by the number of times the recurring communication task is performed until that time. For example, Sent\(2x\) means that the communication task is performed twice.

\[Omitted image "comm-task-state.png"\] Alt text: Communication task state

Icons to the left of the Communication Task name represent the state of the communication task such as completed, skipped, or active.

Under the Work Notes &amp; Activity section, you can initiate a chat at the incident or incident communication plan level. You can also view the activity stream for that record.

## Messaging users through Slack

For Slack functionality, install [Collaboration services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/collaboration-services/collab-services-tcm.md) from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

When you add Slack as a communication channel, you can select **Compose** to convey the Slack message to the contacts that you’ve already mentioned in the communication contact while defining the communication plan. The selected contacts will receive a direct message from the Slack bot. You can perform the communication task actions such as **Closed Task**, **Snooze**, **View Form**, and **View Activity**.

**Parent Topic:**[Major incident workbench UI elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/mi-workbench-ui-elements.md)

**Related topics**  


[Major Incident workbench — Summary tab]()

[Major Incident workbench — the Post Incident Report tab]()

[Major Incident workbench — the Collaborate tab]()

