---
title: AI Control Tower email notifications
description: Email notifications are sent automatically when specific events occur across AI Control Tower workflows.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 1
breadcrumb: [Reference, AI Control Tower, Enable AI experiences]
---

# AI Control Tower email notifications

Email notifications are sent automatically when specific events occur across AI Control Tower workflows.

Email notifications are sent automatically when specific events occur across AI Control Tower workflows. These notifications help ensure timely awareness, review, and action activities in AI Control Tower.

These notifications are part of the base system. To customize notification content or recipients, see Create an email notification

## AI Asset Approval Request

The following notifications are sent for events related to AI asset approval requests and associated approval tasks.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|Approval request – work note added|A work note is added to an AI Asset Approval Request record.|Assigned To|
|Approval request – approved / rejected|An AI Asset Approval Request is approved or rejected.|Asset Managed By|
|Approval request – comment added|A comment is posted on an AI Asset Approval Request record.|Asset Managed By|
|Approval request created – unassigned \(Stewards\)|An AI Asset Approval Request is created and remains unassigned.|AI Stewards Group|
|Approval request created – unassigned \(Asset Manager\)|An AI Asset Approval Request is created and remains unassigned.|Asset Managed By|
|Approval task created|An AI Asset Approval Task record is created.|Assigned To|

## AI Asset

The following notification is sent when an AI asset is retired or cancelled.

|Notification|Trigger condition|Recipients|
|------------|-----------------|----------|
|AI asset retirement / cancellation|An AI Asset record transitions to Retired or Cancelled state.|AI Analyst, Policy Exception Owners, Issue Owners, AI Case Analysts|

## Related information

See AI governance email notifications for email notifications for AI governance workflows, including AI Risk and Compliance, and inherited Risk Management processes.

