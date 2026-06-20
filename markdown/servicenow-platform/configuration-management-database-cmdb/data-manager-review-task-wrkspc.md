---
title: Review CMDB Data Manager tasks in CMDB Workspace
description: Review Data Manager tasks \(mostly life-cycle tasks\) that are assigned to you or to an assignment group that you belong to in accordance with CMDB Data Manager policies.Review Data Manager tasks \(such as life-cycle tasks\) that are assigned to you, to an assignment group that you belong to, to people you manage, or to members of a group that you are the manager of. All in accordance with CMDB Data Manager policies. During the review, you can approve, cancel, reject, or reassign a task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/configuration-management-database-cmdb/data-manager-review-task-wrkspc.html
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [CMDB Data Manager experience in CMDB Workspace, CMDB data management, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Review CMDB Data Manager tasks in CMDB Workspace

Review Data Manager tasks \(mostly life-cycle tasks\) that are assigned to you or to an assignment group that you belong to in accordance with CMDB Data Manager policies.Review Data Manager tasks \(such as life-cycle tasks\) that are assigned to you, to an assignment group that you belong to, to people you manage, or to members of a group that you are the manager of. All in accordance with CMDB Data Manager policies. During the review, you can approve, cancel,reject, or reassign a task.

## Before you begin

Role required: sn\_cmdb\_user, sn\_cmdb\_editor, or sn\_cmdb\_admin

Canceling a life-cycle task is available only for tasks that are in the 'Not started' status, and the required role is data\_manager\_admin or sn\_cmdb\_admin.

## About this task

-   To review attestation tasks, see [Review attestation tasks in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/review-data-manager-attes-task.md).
-   To review certification tasks, see [Review certification tasks in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/data-certific-review-tasks.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **My Work** in the CMDB Workspace menu bar.

2.  In the My tasks section, select the **All other tasks** tab.

3.  Review the Approval tasks list view and then select the task that you want to process.

4.  Review the task details on the task form.

5.  CMDB administrators can select **Cancel task** if the task isn't needed.

    The canceled task is deleted without any further processing.

6.  Select **Reassign** if the task isn't appropriately assigned, and then select **Assign to me** or **Request reassignment** as appropriate.

7.  Select **Review records** to review the target CIs and records for the task.

    1.  Select any records that you want to exclude for the task and then select **Exclude**.

        The records being excluded for the task are also being added to the exclusion list of the associated policy type. Therefore, these records will be excluded from any future tasks of the associated policy type.

    2.  Select **Reassign** if the task isn't appropriately assigned.

    3.  Select **Reject task** to reject a task, fill in a **Reason for rejection** and then select **Save**.

        You can only reject a task that is assigned to you.

        After you reject a task, the **State** of the task is set to **Closed Canceled** and **Approval** is set to **Rejected**. Also, appropriate notifications are sent to members of the group specified in the **glide.cmdb.data\_manager.rejected.task.notification\_group** system property. For more information about how this property is used for notifications, see [Components related to CMDB Data Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/components-cmdb-data-manager.md).

    4.  Select **Assign to me** or **Request reassignment** as appropriate.

    5.  Select **Approve task** to trigger the subflow associated with the policy.


