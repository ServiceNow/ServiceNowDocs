---
title: Escalate a certification task
description: Users with the certification\_admin role can escalate a task in the Work in Progress state. To escalate a task, the task owner identified in the Assigned to field on the task record must have an associated manager.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data certification performance, Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Escalate a certification task

Users with the certification\_admin role can escalate a task in the Work in Progress state. To escalate a task, the task owner identified in the Assigned to field on the task record must have an associated manager.

## Before you begin

Role required: admin

## About this task

Personalize the User form to see the Manager field.

Escalating a task:

-   Sends an email message to the task owner and the manager of the task owner stating that the task has been escalated.
-   Sets the manager as the new task owner.

The event that triggers the escalation is named cert\_task.escalate and the email notification is named Escalation Notification. To edit the text of the email message that is sent, edit the Escalation Notification email notification directly.

For more information, see [Email notifications](https://www.servicenow.com/docs/access?context=c_EmailNotifications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

To escalate a certification task from the Certification Task form:

## Procedure

1.  Navigate to **All** &gt; **Data Certification** &gt; **Tasks** &gt; **All Tasks**.

2.  Select a certification task Number.

3.  Select **Escalate**.

    If the Escalate button is not available, the user in the Assigned to field does not have an associated Manager.


