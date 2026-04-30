---
title: Review CMDB Data Manager attestation tasks in CMDB Workspace or in Service Graph Workspace
description: Review attestation tasks that are assigned to you or to an assignment group that you belong to in accordance with CMDB Data Manager Attestation policies. Check the physical existence of IT infrastructure or applications associated with CIs in the attestation task and then process those CIs as appropriate.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [CIs attestation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Review CMDB Data Manager attestation tasks in CMDB Workspaceor in Service Graph Workspace

Review attestation tasks that are assigned to you or to an assignment group that you belong to in accordance with CMDB Data Manager Attestation policies. Check the physical existence of IT infrastructure or applications associated with CIs in the attestation task and then process those CIs as appropriate.

## About this task

For managers, tasks of direct reports are included, and for user group managers, tasks of members in the group are also included.

## Before you begin

Role required:

-   CMDB administrator: data\_manager\_admin or sn\_cmdb\_admin
-   CI and service owner or manager: data\_manager\_user, sn\_cmdb\_user \(already includes the data\_manager\_user role\)

Canceling an attestation task is available only for tasks that are in the 'In progress' or 'Not started' status, and the required role is data\_manager\_admin or sn\_cmdb\_admin.

## About this task

After you receive notifications about attestation tasks assigned to you, check the actual IT infrastructure or applications that you own, and then process the CIs in the task accordingly. Initially, all the CIs in the attestation task are listed in a Not Yet Reviewed list and therefore require a review. Attested CIs are then moved to an Attested CIs list, while CIs you reject are moved to a separate Rejected CIs list. After processing all the CIs in the task, you can submit and complete the task. For general information about attestation and the flow of attestation, see [CIs attestation](../concept/attesting-cis.md).

As you process the CIs in the task, only the fields **Attestation Status** \(values: **Attested**, **Rejected**, **Not Yet Reviewed**\), **Attested By**, and **Attested Date** are automatically updated. Also, details of your activities are captured in the activity stream of the task.

## Procedure

1.  Navigate to either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **My Work** in the CMDB Workspace menu bar.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, in the navigation panel select the Tasks icon, and then, in the Tasks navigation panel, select **Certification**.
    Any attestation tasks that are assigned to you or to assignment groups you belong to, appear in the **Attestation tasks** tab in the My tasks section. Attestation tasks are associated with details such as the due dates and short descriptions for those tasks. Assignment groups that you are a member of, are also listed.

2.  Select a task to review from the Attestation tasks list.

    For a bulk review, select multiple tasks or check the box next to 'Configuration Item' to review all the tasks in the list.

3.  Review details of a task:

    1.  Administrators can select **Cancel task** if attesting the CIs in the task isn't needed.

        For example, if the task was created by error. The canceled task is deleted without any further processing.

    2.  If the task isn't properly assigned, select **Reassign** and then select one of the following options.

        Depending on your selection, the task might no longer be assigned to you.

        -   **To me**: If the task isn't yet assigned to a specific user and you are the owner of the CIs who can process the task.
        -   **To other user**: If you aren't the actual owner of the CIs and there is someone else that is more appropriate as the owner for the task. In the Reassign to other user dialog box, set **Assign to** to that user and enter the reason for the reassignment. Then select **Proceed**.

            For a CI owner, only users from the assignment group that the task is currently assigned to, appear. For Admins, all users with the data\_manager\_user role appear.

        -   **Send for reassignment**: If you aren't the appropriate user for this task and the administrator needs to assign the task to someone else. In the Send for reassignment dialog box, enter the reason for the operation and then select **Submit** to send a notification to the administrator.
    3.  Select **Review CIs to attest** to continue the CI attestation process.

        If the task is not assigned to anyone, it is automatically assigned to the current user.

4.  If the Smart detection dialog box appears, select **Review** to review the CIs or **Auto-attest** to attest the detected CIs without a review.

    1.  Review the details of the CIs in the list.

    2.  Select **Auto-attest** to automatically attest all the CIs in the list and to move them to the Attested CIs list.

    3.  Select **Cancel auto-attestation** to leave all the CIs in the Not Yet Reviewed list and to later continue attesting those CIs regardless of smart detection.

    If you select **Cancel**, you can later select **Run auto-attestation** in the Smart detection widget. When reviewing the CIs to attest, the list in the Smart detection pane is filtered to CIs that are candidates for auto-attestation, letting you auto-attest all those CIs in bulk.

5.  Review the CIs in the Not Yet Reviewed list.

    You can select a CI to open a dashboard with more details such as [CI health](../concept/c_CMDBHealth.md), key properties, and [CMDB 360 data](../concept/multisource-cmdb.md). The CI health details that appear depend on settings and activation of various features.

    Use the following cards on the right hand bar to get help and status:

    -   Select Attestation actions \(![CMDB Workspace attestation actions.](../image/workspace-attestation-actions.png)\) to get help on the possible actions you can take while reviewing CIs.
    -   Select Attestation status \(![CMDB Workspace attestation status.](../image/workspace-attestation-status.png)\) to see your progress in reviewing and attesting CIs.
    -   Select Smart detection status \(![CMDB Workspace smart detection status.](../image/workspace-auto-attest-status.png)\) to see if any CIs are candidates for auto-attestation and to apply auto-attestation if applicable.
6.  In the **Details** tab of the Attestation Review CIs pane, select the CIs that you are ready to process and select an action to apply to all selected CIs.

    -   Select the CIs that you can attest their existence and select **Attest** to move them to the Attested list.

        To undo attestation, select the Attested list, select the CIs that you want to move back to the Not Yet Reviewed list and select **Unattest**. Or, select the CIs that you want to move to the Rejected list and select **Reject**.

    -   Select the CIs that you can't attest their existence and select **Reject** to move them to the Rejected list. In the Confirm rejecting CIs dialog box, enter an explanation and then select **Proceed**.

        To undo rejection, select the Rejected list, select the CIs that you want to move back to the Not Yet Reviewed list and select **Unattest**. Or, select the CIs that you want to move to the Attested list and select **Attest**.

    -   Select the CIs that shouldn't be included in this task and in future Data Manager attestation policies, and select **Exclude**. In the Confirm excluding CIs dialog box, enter an explanation and then select **Proceed**.

        Those excluded CIs are added to the exclusion list of CMDB Data Manager attestation policies. For more information, see [Manage exclusion lists for CMDB Data Manager](data-mgr-manage-ci-exclusion-wrkspc.md). Only an admin can undo this operation using the CMDB Data Manager.

    -   Select any CIs that you identify as duplicates of other CIs and select **Remove duplicates from task**. In the Confirm removing duplicate CIs dialog box, enter an explanation and then select **Proceed**.

        Those duplicate CIs are removed from the attestation task and a de-duplication task is generated for them, which is similar to the de-duplication tasks created by the Identification and Reconciliation Engine \(IRE\). For more details about how to process and remediate de-duplication tasks, see [Duplicate CIs remediation](../concept/de-duplication-tasks.md).

        **Note:** Only an admin can undo this operation.

    -   After processing all the CIs in the task, when the Not Yet Reviewed list is empty, the **Submit** button is enabled. Select **Submit**or the **Submit task** link in the 'Ready to submit' notification, and then in the Submit attestation dialog box select **Submit** to close the task.

