---
title: Create email notifications
description: Vulnerability administrators can edit the notification or add new ones, specifying when to send the notification, who receives the notification, and what content is in the notification.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Create email notifications

Vulnerability administrators can edit the notification or add new ones, specifying when to send the notification, who receives the notification, and what content is in the notification.

## Before you begin

Role required: sn\_vulc.admin

## About this task

You can create email templates for different types of email notifications. For more on how to create email templates, see [Define Vulnerability Response email templates](../../vulnerability-response/task/t_DefiningEmailTemplates.md).

## Procedure

1.  Navigate to **All** &gt; **Vulnerability Response** &gt; **Administration** &gt; **Notifications**.

2.  Select the remediation target notification record or select **New**.

3.  Fill in the fields on the form, as appropriate.

    For more information on the form fields, see Create an email notification.

4.  Select **Preview Notification** to view the message.


## Result

Starting from v14.11 of Configuration Compliance, when a recipient clicks the links in an email notification, the records open in the Vulnerability Manager Workspace or IT Remediation Workspace based on their role.

-   Links open in the Vulnerability Manager Workspace for the users with the sn\_vulc.admin role.
-   Links open in the IT Remediation Workspace for the users with the sn\_vulc.remediation\_owner role.

If the recipient doesn’t have any of the preceding roles, the links in an email notification open in the classic UI.

