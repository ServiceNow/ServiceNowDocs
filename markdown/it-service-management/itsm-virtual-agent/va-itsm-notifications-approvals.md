---
title: Actionable notifications for approvals in ITSM Virtual Agent
description: Notify employees of approvals for requests with notifications from ITSM Virtual Agent.
locale: en-US
release: zurich
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Pre-built actionable notifications, ITSM Virtual Agent, IT Service Management]
---

# Actionable notifications for approvals in ITSM Virtual Agent

Notify employees of approvals for requests with notifications from ITSM Virtual Agent.

You must activate notifications in Workflow Studio in order to use them. For details, see [Set up actionable notifications for ITSM Virtual Agent](../task/setup-actionable-notifications.md).

Some of the default actionable notifications in ITSM Virtual Agent that need approvals are as follows:

## Approval request for requested items

Virtual Agent sends a notification to the approver of a Service Catalog item request. The approver can choose to view the request details or skip the notification.

Approvers can approve or reject the request directly in the chat. Approvers can also add comments to rejected requests directly in the chat.

## Approval request for requests

When an approval for a change is requested, Virtual Agent sends a notification to the end user who made the change request. The end user can be either the requester or the approver. Virtual Agent sends the notification to the end user, as applicable, who can then approve or reject the request, see details, or skip the notification.

![Notification for approval details not configured task table.](../image/ApprovalsTask1.png)

The fields shown below are the default fields for any task table \(the **Show Details** field is not configured for the Task extended table\).

![Actionable notification for approval details not configured on the task table.](../image/ApprovalsTask2.png)

The fields below are the fields configured in the \_show\_approval\_details\_ topic \(the **Show Details** field is configured for the Task extended table\). Admin users can configure these fields by duplicating the topic and editing the approval\_default\_task\_fields script variable within the topic.

![Actionable notification for approval details configured on the task table.](../image/ApprovalsTask4.png)

## KB request approved or rejected

Virtual Agent sends a notification when an approval for a knowledge article is requested. End users approve or reject the request, see details, or skip the notification.

![Approval for knowledge article fields configured.](../image/ApprovalKnowledge3.png)

The fields shown here are the fields configured in the \_show\_approval\_details\_ topic.​ Admin users can configure these fields by duplicating the topic and editing the approval\_default\_task\_fields script variable within the topic.

![Approval for knowledge article fields configured.](../image/ApprovalKnowledge4.png)

For non-task tables, when no fields are configured in the \_show\_approval\_details\_ topic, a message displays with a link to the record being reviewed.

![Notification for knowledge article approval.](../image/ApprovalKnowledge2.png)

## Other approval

Virtual Agent sends a notification to the approver when a non-task record \(such as a Knowledge Base article\) needs approval. The approver can choose to view the request details or skip the notification.

## Request approval reminder

Virtual Agent sends a notification to remind the approver of a pending Service Catalog request. The approver can choose to view the request details or skip the notification.

## Request approved or rejected

Virtual Agent sends a notification to the requester of a Service Catalog item when their request has been approved or rejected. The requester can choose to view the request details or skip the notification.

## Task approval

Virtual Agent notifies the approver about a newly created task that needs review and approval.

This notification is not applicable for tasks such as Change or Standard Change. It is also not applicable to Requests \(sc\_requests\) and Requested Items \(sc\_req\_item\).

**Parent Topic:**[ITSM Virtual Agent pre-built actionable notifications](../concept/itsm-actionable-notifications.md)

