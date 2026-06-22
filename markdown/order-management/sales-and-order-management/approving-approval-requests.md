---
title: Working with approval requests as an approver
description: As an approver, you receive notifications informing you of approval requests for items such as customer quotes. You can approve or reject the requests in the approval workflow or from the notification reminders that you receive for approval requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/approving-approval-requests.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Working with approval requests as an approver

As an approver, you receive notifications informing you of approval requests for items such as customer quotes. You can approve or reject the requests in the approval workflow or from the notification reminders that you receive for approval requests.

## What you can do as an approver

If your advanced approval admin has defined you as an approver or a member of an approval group, you can do the following:

-   Approve or reject approval requests.
-   Approve or reject escalated approval requests if your advanced approval admin has configured the escalation feature. An escalated approver handles requests that have been reassigned when the original approver hasn't acted on requests.
-   Add other approvers, called ad-hoc approvers, if they are qualified to review approval requests and be included in the approval process.
-   If your organization uses granular delegation as part of the HR Service Delivery application, delegate your approval responsibilities.

## Approval workflow

When a sales rep \(requester\) submits an approval request, the advanced approval engine creates one or more approval requests and routes them to the appropriate approvers. As an approver, you’re responsible for only the approval steps assigned to you. Approval actions taken by another approver do not give you access to approval steps assigned to other approvers. But you can track and review the approval process for the request using the [approval workflow interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/tracking-approval-status.md).

Review the requests. You evaluate requests based on business policies, financial rules, legal rules, or other internal guidelines that your company follows:

-   Details of the approval entity, such as quotes and their related pricing
-   The approval reason or condition that triggered the request
-   Any comments provided by the requester

You can approve or reject requests from different channels, depending on how the approval process is configured and your notification preferences for various channels.

-   From the approval workflow interface in the CSM Configurable Workspace
-   From system email notifications reminding you of your approval request tasks

    For example, you may receive a simple notification for a single approval request or a consolidated email notification that has multiple approval requests. You can approve or reject requests directly from the email. For consolidated email approvals, you can:

    -   Selectively approve or reject individual requests, or approve or reject all the requests from the notification.
    -   Reply to email notifications using text commands to approve or reject specific requests, approve all requests, or reject all requests.
-   In push notifications from the ServiceNow Now® Mobile application
-   From My Approvals in the ServiceNow AI Platform

You may also receive email reminders if your approval rule admin has set up email reminders for your approval configuration.

**Note:** For more information on setting up your preferred notification channels, see [Notification Preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/preferences-landing.md).

## Rejection workflow

When you reject an approval request, the advanced approval engine updates the approval step record. Rejection helps prevent the request from progressing to the remaining approval steps and indicates that changes are required.

When you reject an approval request, you specify the reason for the rejection. If you reject the request from an email notification, an Approval Request Rejected notification is generated and sent to the requester. The notification indicates the request was rejected and the reason for rejection. The requester can modify the business item, such as a quote, and resubmit the request for approval.

## Escalation workflow

When an approver doesn't act on an approval request within a certain time period, your advanced approval admin can designate an escalation assignee to handle the request. As an escalation assignee, you receive notifications for approval requests that are reassigned to you.The original approver also receives a notification indicating the approval request has been escalated.

As an escalated assignee, you can approve or reject requests from different channels, as in the basic approval workflow.

## Adding ad-hoc approvers

You can add one or more ad-hoc approvers or approval groups when others outside the original approver list must review the request. For example, an approval request may require approval by others who are familiar with the rules or business guidelines relevant to the request. For more information on adding an ad-hoc approver, see [Add approvers to an approval request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/add-approver.md).

If you've been added as an ad hoc approver, you can accept or reject the approval request from the approval request notification. You can also approve or reject the request in the General Chain of the approval workflow interface.

## Delegating approvals

If you need to be away from work for a specific time period and can't review your approval requests, you can delegate your approval responsibilities to another coworker if the granular delegation feature in HR Service Delivery has been implemented. For more information on delegation, see [Granular Delegation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/granular-delegation/granular-delegation.md).

**Parent Topic:**[Using Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/using-advanced-approval-management.md)

