---
title: Mark a certification task as closed incomplete
description: Mark a task as closed incomplete if, for example, only some of the elements can be certified.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Mark a certification task as closed incomplete

Mark a task as closed incomplete if, for example, only some of the elements can be certified.

## Before you begin

Role required: admin

## About this task

The following users can mark a task as closed incomplete:

-   Users with the certification\_admin role.
-   User identified in the Assigned to field on the certification task record.

To mark a task as closed incomplete:

## Procedure

1.  Navigate to **All** &gt; **Data Certification** &gt; **Tasks** and select **All Tasks**, or **My Tasks**.

2.  Click a certification task Number.

3.  In Work Notes, enter information about why the task could not be completed.

4.  Click **Close Incomplete**.

    If at least one task on a certification instance is marked Closed Incomplete, the Completed date and Percent complete fields on the certification instance record are not updated. A user with the certification\_admin role can:

    -   Complete the incomplete task or tasks.
    -   Cancel the incomplete task or tasks.
    When all tasks on the certification instance are Closed Complete or Cancelled:

    -   The system sets the Completed date field on the certification instance record to the current date and time.
    -   The Percent complete field on the certification instance record is set to 100 percent.

