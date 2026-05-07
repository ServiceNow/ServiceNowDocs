---
title: Working with approval requests as an approver
description: As an approver, you receive notifications informing you of approval requests for items such as customer quotes. Review the requests, evaluating them based on business policies, financial rules, legal rules, or other internal guidelines that your company follows. You can approve or reject the requests in the approval workflow or from the notification reminders that you receive for approval requests.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Working with approval requests as an approver

As an approver, you receive notifications informing you of approval requests for items such as customer quotes. Review the requests, evaluating them based on business policies, financial rules, legal rules, or other internal guidelines that your company follows. You can approve or reject the requests in the approval workflow or from the notification reminders that you receive for approval requests.

## Approval workflow

When a sales rep \(requester\) submits an approval request, the advanced approval engine creates one or more approval requests and routes them to the appropriate approvers. As an approver, you’re responsible for only the approval steps assigned to you. Approval actions taken by another approver do not give you access to approval steps assigned to other approvers. But you can track and review the approval process for the request using the [approval workflow interface](tracking-approval-status.md)approval workflow interface.

Review the following when you receive an approval request:

-   Details of the approval entity, such as quotes and their related pricing
-   The approval reason or condition that triggered the request
-   Any comments provided by the requester

You can approve or reject requests from different channels, depending on how the approval process is configured by your approval rules admin and how you've set your notification preferences to receive notifications on various channels:

-   From the approval workflow interface in the CSM Configurable Workspace
-   From system email notifications reminding you of your approval request tasks
-   In push notifications from the ServiceNow Now® Mobile application
-   From My Approvals in the ServiceNow AI Platform

You may also receive email reminders if your approval rule admin has set up email reminders for your approval configurtion.

**Note:** For more information on setting up your preferred notification channels, see [Notification Preferences](https://www.servicenow.com/docs/access?context=preferences-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Rejection workflow

When you reject an approval request, the advanced approval engine updates the approval step record. Rejection helps prevent the request from progressing to the remaining approval steps and indicates that changes are required.

When rejecting an approval request, you provide a comment explaining the reason for rejection. Rejected requests are returned to the requester for further review or updates, depending on the approval configuration. The requester can modify the business item, such as a quote, and resubmit the request for approval.

## Escalation workflow

If the escalation feature for your configuration is enabled, and your advanced approval admin has designated you as an escalation assignee for an approval rule, you will receive notification reminders for approval requests that have been escalated and routed to you since the original approver hasn't acted on the request within a certain time period. The original approver also receives a notification indicating the approval request has been escalated.

As an escalated assignee, you can approve or reject requests from different channels, as in the basic approval workflow.

## Adding ad-hoc approvers

You can add one or more approvers or approval groups to a workflow, when an approval request requires approval by others who are familiar with the rules or business guidelines relevant to the request, but outside of the original approvers. For more information on adding an ad-hoc approver, see [Add approvers to an approval request](../task/add-approver.md).

## Delegating approvals

If you need to be away from work for a specific time period and can't review your approval requests, you can delegate your approval responsibilities to another coworker if the delegation feature in Employee Workflows has been implemented by your admin. For more information on delegation, see [Granular Delegation](https://www.servicenow.com/docs/access?context=granular-delegation&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

**Parent Topic:**[Using Advanced Approval Management](using-advanced-approval-management.md)

