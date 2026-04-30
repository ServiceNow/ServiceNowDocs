---
title: Certification follow-on tasks
description: The ServiceNow system can automatically generate and assign follow-on tasks to correct discrepancies detected during compliance audits.Users with the certification role can only access follow-on tasks assigned to them but can reassign these tasks to other users.Users with the certification\_admin or admin role can see all follow-on tasks.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Certification follow-on tasks

The ServiceNow system can automatically generate and assign follow-on tasks to correct discrepancies detected during compliance audits.

The system property **glide.allow.new.cert\_follow\_on\_task** is set to true by default, allowing for new follow on tasks to be created for the same failure, at each audit run. You can set this property to false, to configure audit to use the same follow-on task for the same audit failure across multiple runs.

The system property **glide.allow.new.cert\_follow\_on\_task** applies only to audits which aren't scripted.

The system property **glide.allow.new.cert\_follow\_on\_task** applies only to audits which aren't scripted.

You configure and assign follow-on tasks to qualified users or groups in the audit record. A user with the certification\_admin role can reassign any follow-on task. The Audit Results related list in the Follow On Task form contains links to the records that failed.

## Access follow-on tasks

Users with the certification role can only access follow-on tasks assigned to them but can reassign these tasks to other users.

### Procedure

1.  Navigate to **All** &gt; **Compliance** &gt; **My Follow On Tasks**.

    The list contains all active follow-on tasks assigned to the logged in user.

2.  Open a task.

    The record shows the specifics of the task, the task activity, and the failed audit results.

3.  Open records from the **Audit Results** related list to see each discrepancy.

4.  Go to the CI named in the record and perform the work to bring it into compliance.

5.  Update the **State** field in the follow-on task record and add work notes as you correct each discrepancy.

    When you change the state, the system updates the task activity appropriately.

    When the task is **Closed Complete** it no longer appears on the **My Work** list.


## Manage follow-on tasks

Users with the certification\_admin or admin role can see all follow-on tasks.

### Before you begin

Role required: none

### About this task

Tasks are pre-assigned to a user or group as specified in the audit record, but users with the certification\_admin role can reassign the task.

### Procedure

1.  Navigate to the appropriate application:

    -   **Compliance** &gt; **Architecture Compliance** &gt; **Follow On Tasks**
    -   **Compliance** &gt; **Desired State** &gt; **Follow On Tasks**
    -   **Compliance** &gt; **Scripted Audits** &gt; **Follow On Tasks**
    The list of follow-on tasks appears, filtered by audit type.

2.  Open a task.

    The **Audit** and **Configuration item** fields are read-only for all users.

3.  Edit the **Change group** or the **Assigned to** field if necessary.

4.  Edit the **Short description** field if necessary.

    The short description is inherited from the **Task description** field in the Audit form.

5.  Use the links in the **Audit Results** related list to open the individual records that failed the audit.

6.  If you update the follow-on task record, be sure to add work notes.


