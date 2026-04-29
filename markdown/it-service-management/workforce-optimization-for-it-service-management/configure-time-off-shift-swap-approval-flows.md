---
title: Configure the due date logic for shift approval flows
description: As an administrator, you can configure the due date logic for the time-off request and shift-swap request approval flows.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up, Scheduling, Workforce Optimization for ITSM, IT Service Management]
---

# Configure the due date logic for shift approval flows

As an administrator, you can configure the due date logic for the time-off request and shift-swap request approval flows.

## Before you begin

Make sure that your application is in the Shift Planning scope.

Role required: admin

## About this task

You can configure the flows to restrict who can approve the requests. For example, you can set it to only the manager of the agent's primary assignment group who can approve them. If the agent submits the request for approval within two days before the agent time-off start date, then the request for approval is auto-rejected.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    Each flow has a requester and an approver workflow.

2.  Configure the due date logic for the Time-off request flow.

<table id="table_phs_ffg_4tb"><thead><tr><th>

If

</th><th>

Then

</th><th>

Reference image

</th></tr></thead><tbody><tr><td>

**The requester is one of the managers**

</td><td>

The request is auto-approved.

</td><td>

![Time-off request auto-approval](../image/timeoff-request-autoapprove.png)

</td></tr><tr><td>

**The requester is the agent**

</td><td>

Enter the due date to approve the request.1.  Open **Else** &gt; **Ask For Approval** flow.
2.  In the **Due Date** field, select the down arrow icon \(![Down arrow icon](../image/down-arrow-icon.png)\).
3.  In the **Due Date** script window, update the value in the **dueDate.addDaysUTC\(-2\);** parameter to the number of days you want to set the due date for approval.
4.  Select **Done**.


</td><td>

![Time-off ask for approval flow](../image/time-off-ask-approval.png)

</td></tr></tbody>
</table>3.  Configure the due date for the Swap request approval flow.

<table id="table_ek2_lfg_4tb"><thead><tr><th>

If

</th><th>

Then

</th><th>

Reference image

</th></tr></thead><tbody><tr><td>

**The shift-swap requester is one of the managers**

</td><td>

The request is auto-approved.

</td><td>

![Shift-swap auto approval](../image/shift-swap-auto-approval.png)

</td></tr><tr><td>

**The shift-swap requester is an agent \(Requestee\)** and the **The shift-swap approver is the manager**

</td><td>

Enter the due date for the requestee agent to approve.

1.  Open **Else** &gt; **Ask For Approval**- Ask for Approval from Requestee Agent flow.
2.  In the **Due Date** field, select the down arrow icon \(![Down arrow icon](../image/down-arrow-icon.png)\).
3.  In the **Due Date** script window, updated the value in the **dueDate.addDaysUTC\(-2\);** parameter to the number of days you want to set the due date for approval.
4.  Select **Done**.
 Enter the due date to approve the request.

1.  Open **Ask For Approval** - Ask for an approval from Managers and additional managers of both the agents flow.
2.  In the **Due Date** field, select the down arrow icon \(![Down arrow icon](../image/down-arrow-icon.png)\).
3.  In the **Due Date** script window, updated the value in the **dueDate.addDaysUTC\(-2\);** parameter to the number of days you want to set the due date for approval.
4.  Select **Done**.


</td><td>

Enter the due date for the requestee agent to approve.![Shift swap request approval](../image/shift-swap-request-approval.png)

 Enter the due date to approve the request.![Swap request manager approval](../image/swap-request-manager-approval.png)

</td></tr></tbody>
</table>
**Parent Topic:**[Setting up Scheduling in Workforce Optimization for ITSM](../concept/setup-scheduling-configurable-workforce-optimization-itsm.md)

**Related topics**  


[Build your first flow in Flow Designer](https://www.servicenow.com/docs/access?context=build-your-first-flow&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

