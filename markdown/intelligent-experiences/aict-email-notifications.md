---
title: AI Control Tower email notifications
description: Identify the email notifications that AI Control Tower sends automatically, the events that trigger each notification, and the recipients. These notifications keep AI Stewards, asset owners, and assignees informed so that they can take action promptly on AI asset approvals and lifecycle events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-email-notifications.html
release: zurich
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [AI Control Tower, notifications, email, approval request]
breadcrumb: [Reference, AI Control Tower, Enable AI experiences]
---

# AI Control Tower email notifications

Identify the email notifications that AI Control Tower sends automatically, the events that trigger each notification, and the recipients. These notifications keep AI Stewards, asset owners, and assignees informed so that they can take action promptly on AI asset approvals and lifecycle events.

The notifications listed in this topic are part of the base system and are sent automatically when the trigger condition is met. To customize notification content or recipients, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_CreateANotification.md).

## AI asset approval request notifications

The following notifications are sent for events related to AI asset approval requests and their associated approval tasks. AI asset approval requests are stored in the `sn_ai_governance_assessment_request` table; approval tasks are stored in the `sn_ai_governance_assessment_task` table.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Approval request — work note added|A work note is added to an AI Asset Approval Request record.|Assigned To|
|Approval request — approved or rejected|An AI Asset Approval Request is approved or rejected.|Asset Managed By|
|Approval request — comment added|A comment is posted on an AI Asset Approval Request record.|Asset Managed By|
|Approval request created — unassigned \(Stewards\)|An AI Asset Approval Request is created and remains unassigned.|AI Stewards group|
|Approval request created — unassigned \(Asset Manager\)|An AI Asset Approval Request is created and remains unassigned.|Asset Managed By|
|Approval task created|An AI Asset Approval Task record is created.|Assigned To|

## AI asset lifecycle notifications

The following notification is sent when an AI asset transitions to a terminal lifecycle state. The notification alerts downstream owners — including issue, policy exception, and case analyst owners — so that any open work tied to the asset can be resolved or reassigned.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|AI asset retirement or cancellation|An AI Asset record transitions to Retired or Cancelled state.|AI Analyst, Policy Exception Owners, Issue Owners, AI Case Analysts|

## Related information

For email notifications sent by AI Risk and Compliance workflows and inherited Risk Management processes, see [AI governance email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/airc_email_notifications.md).

