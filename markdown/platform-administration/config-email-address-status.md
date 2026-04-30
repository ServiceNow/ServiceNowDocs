---
title: Configure bounce email address status
description: Configure a bounced email address status according to type, class, subject, and details.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Email bounce management, Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure bounce email address status

Configure a bounced email address status according to type, class, subject, and details.

## Before you begin

Role required: admin

## About this task

For detailed information on status codes and explanations of the components, see [RFC Status codes](https://www.rfc-editor.org/rfc/rfc3463).

## Procedure

1.  Navigate to **All** &gt; **System Mailboxes** &gt; **Administration** &gt; **Bounce Email Address Status**.

2.  Select **New**.

3.  Select the **Type** and enter the **Class**, **Subject**, and **Detail**.

    **Note:** For example: Status code patterns for 5.1.\* are blocked by default, if 5, 1, and 2 are entered as the Class, Subject, and Detail, the Type is selected as unblocked then only 5.1.2 is unblocked. All other status codes patterns for 5.1.\* are still blocked.

4.  Select **Submit**.


**Parent Topic:**[Email bounce management](../concept/email-bounce.md)

**Related topics**  


[Check the status of bounced email addresses](change-bounce-email-status.md)

