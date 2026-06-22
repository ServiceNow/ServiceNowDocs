---
title: Reassign a certification task
description: If you have the certification\_admin role, you can reassign any certification task in the Work in Progress state. Tasks in Closed Complete, Closed Incomplete, or Cancelled state cannot be reassigned. When a task is reassigned, the current task owner and the new task owner are sent a message.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/configuration-management-database-cmdb/t\_ReassignACertificationTask.html
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Certification on Core UI, Data Certification, CMDB data management, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Reassign a certification task

If you have the certification\_admin role, you can reassign any certification task in the Work in Progress state. Tasks in Closed Complete, Closed Incomplete, or Cancelled state cannot be reassigned. When a task is reassigned, the current task owner and the new task owner are sent a message.

## Before you begin

Role required: certification\_admin

## About this task

The event associated with the reassignment is named cert\_task.reassign and the email notification is named Certification Task Reassignment. To edit the text of the email message that is sent, edit the Certification Task Reassignment email notification directly.

For more information, see [Email notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/c_EmailNotifications.md).

To reassign a certification task:

## Procedure

1.  Navigate to **All** &gt; **Data Certification** &gt; **Tasks** &gt; **All Tasks**.

2.  Click a certification task Number.

3.  Enter a new name in the Assigned to field.


