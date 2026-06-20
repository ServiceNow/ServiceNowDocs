---
title: Approve or reject a CMDB Data Manager task \(in Core UI\)
description: If you are an authorized approver, you might receive an email notification directing you to review a CMDB Data Manager policy task. Approve the task in the CMDB Data Manager legacy build on Core UI, to continue its processing, or reject the task to send it to the CMDB Data Manager administrator for a more detailed review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/configuration-management-database-cmdb/review-data-manager-task.html
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CMDB Data Manager \(Core UI\), CMDB data management, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Approve or reject a CMDB Data Manager task \(in Core UI\)

If you are an authorized approver, you might receive an email notification directing you to review a CMDB Data Manager policy task. Approve the task in the CMDB Data Manager legacy build on Core UI,to continue its processing, or reject the task to send it to the CMDB Data Manager administrator for a more detailed review.

## Before you begin

Role required:

-   data\_manager\_admin: Full access to policy tasks and can set state to 'Work in progress' of an unassigned task.
-   data\_manager\_user: Read access to policy tasks and can approve or reject an assigned policy task.

## About this task

Authorized approvers for a task are all users in the assignment group of the task, with the data\_manager\_user or data\_manager\_admin roles.

For information about using the more advanced CMDB Data Manager in CMDB Workspace, see [CMDB Data Manager experience in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/data-mgr-exp-cmdb-workspace.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Data Manager**.

2.  On the CMDB Data Manager landing page, in the Open Policy Tasks tile, select **View Open Tasks**.

3.  On the CMDB Data Management Task Control list view, select a task to review.

4.  Select the **Approvers** tab in the related lists section.

5.  In a record where you are the **Approver**, select the **Requested** value in the **State** column.

6.  On the Approval form, set **State** to your approval choice such as **Approved** or **Rejected**.

7.  Select **Update**.


## Result

1.  The **Approval** field of the task is set to **Approved** or **Rejected**.
2.  If the task is approved, then the policy subflow is triggered to continue processing the policy tasks for the target CIs.

