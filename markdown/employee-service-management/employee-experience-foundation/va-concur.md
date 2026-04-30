---
title: Manage approvals from Microsoft Teams
description: Manage Concur expense approvals using Virtual Agent actionable notifications in Microsoft Teams to resolve the approval directly in the Virtual Agent conversation without involving a live agent.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Employee actions, Use ITSM and HRSD integrations with Microsoft Teams, Use Microsoft Teams integration for Employee Experience, Use, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Manage approvals from Microsoft Teams

Manage Concur expense approvals using Virtual Agent actionable notifications in Microsoft Teams to resolve the approval directly in the Virtual Agent conversation without involving a live agent.

## Before you begin

-   The Virtual Agent integration is supported only for users who have a user record in your ServiceNow instance. Users must link their accounts to Microsoft Teams and enable Virtual Agent notifications.
-   Install the Approvals hub integration with the SAP Concur \(sn\_ex\_cnc\) plugin.

For more information on receiving notifications, see [Integrating Virtual Agent with Microsoft Teams](https://www.servicenow.com/docs/access?context=teams-conv-integration&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) and [Enable Virtual Agent notifications](https://www.servicenow.com/docs/access?context=enable-va-notifications&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US). For more information on Virtual Agent, see [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

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

<table id="choicetable_wnl_kjd_4xb"><thead><tr><th align="left" id="d218971e175">

Decision

</th><th align="left" id="d218971e178">

Action

</th></tr></thead><tbody><tr><td id="d218971e184">

**Approve the report**

</td><td>

Select **Approve**.

</td></tr><tr><td id="d218971e196">

**Reject the report**

</td><td>

1.  Select **Send back**.
2.  Enter a reason for rejecting the report.


</td></tr></tbody>
</table>
**Parent Topic:**[Employee actions](../concept/employee-sn-ms-teams.md)

