---
title: Manage approvals from Microsoft Teams
description: Manage Concur expense approvals using Virtual Agent actionable notifications in Microsoft Teams to resolve the approval directly in the Virtual Agent conversation without involving a live agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/va-concur-ec.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Manage approvals from Microsoft Teams

Manage Concur expense approvals using Virtual Agent actionable notifications in Microsoft Teams to resolve the approval directly in the Virtual Agent conversation without involving a live agent.

## Before you begin

-   The Virtual Agent integration is supported only for users who have a user record in your ServiceNow instance. Users must link their accounts to Microsoft Teams and enable Virtual Agent notifications.
-   Install the Approvals hub integration with the SAP Concur \(sn\_ex\_cnc\) plugin.

For more information on receiving notifications, see [Conversational Integration with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/teams-conv-integration.md) and [Enable Virtual Agent notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/enable-va-notifications.md). For more information on Virtual Agent, see [Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent-landing-page.md).

Role required: approver\_user

## Procedure

1.  Launch the Microsoft Teams application.

2.  Open the **Now Virtual Agent** chat window.

3.  Enter `Show notification` in the chat window.

4.  View the report by selecting **View Report**.

    You can also view the report later by selecting **Skip** and entering `Show notification` in the chat window.

5.  View expense and receipt items by selecting **Expenses and Receipts**.

    A maximum of 12 expense items are displayed in the report. To view all items, select **View full report**.

6.  Approve or reject the report.

    **Note:** You cannot accept or reject a report if the assigned approver has been modified or the report has been updated or closed.

<table id="choicetable_wnl_kjd_4xb"><thead><tr><th align="left" id="d241693e175">

Decision

</th><th align="left" id="d241693e178">

Action

</th></tr></thead><tbody><tr><td id="d241693e184">

**Approve the report**

</td><td>

Select **Approve**.

</td></tr><tr><td id="d241693e196">

**Reject the report**

</td><td>

1.  Select **Send back**.
2.  Enter a reason for rejecting the report.


</td></tr></tbody>
</table>
**Parent Topic:**[Using Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/using-emp-center.md)

**Parent Topic:**[Employee actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/employee-sn-ms-teams.md)

**Related topics**  


[Use the Employee Center topic pages]()

[Topic managers and contributors for topic page management]()

[Use the My To-dos page]()

[Use approval experience]()

[Manage approvals from a Microsoft Outlook email]()

[Task filters on My tasks]()

[View the Recommended for you content]()

[Use Employee Center from Zoom]()

[View employee profile]()

[Use Personalized Answers]()

[Employee Profile org chart widget]()

[RTL support for Employee Center]()

[Manage favorites]()

[Access applications from App Launcher]()

[Use Guided Self-Service]()

