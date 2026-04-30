---
title: Review certification tasks
description: Review the values of record fields and CI attributes in certification tasks assigned to you, and then certify, edit, or fail the review according to your findings. For managers, tasks of direct reports are included, and for user group managers, tasks of members in the group are also included.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Data Certification experience in a workspace, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Review certification tasks

Review the values of record fields and CI attributes in certification tasks assigned to you, and then certify, edit, or fail the review according to your findings.For managers, tasks of direct reports are included, and for user group managers, tasks of members in the group are also included.

## Before you begin

Role required: sn\_cmdb\_user, sn\_cmdb\_editor, or sn\_cmdb\_admin

Canceling a certification task is available only for tasks that are in the 'In progress' or 'Not started' status, and the required role is data\_manager\_admin or sn\_cmdb\_admin.

## About this task

If a certification task isn't properly assigned, you can reassign it to another user if you know who the appropriate reviewer is, or request an administrator to reassign the task.

**Note:**

-   If the policy is configured to disallow empty attribute values, you will only be able to fail certification of the associated CIs, but you won't be able to certify them unless you populate the empty attributes first.
-   If the policy is configured to disallow updates to field values, you won't be able to update non-compliant CIs, resulting in failing their certification.

## Procedure

1.  Navigate to the Certification tasks list in either of the following ways.

    -   Navigate to **Workspaces** &gt; **CMDB Workspace**, then select **My Work** in the CMDB Workspace menu bar. In the My tasks section, select the Certification tasks tab.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace**. On the Home view in CMDB Workspace, select the **Data Certification Dashboard** quick link. Then, on the Data Certification Dashboard, drill down to the Certification tasks list from a certification instance card or from the Workload and Aging tasks tiles, as described in [Data Certification Dashboard](../concept/data-cert-dashboard-workspace.md).
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and in the navigation panel select the Tasks icon. In the Tasks navigation panel select **Certification** and on the Data Certification page, select the Certification tasks tab.
2.  In the Certification tasks list, select multiple tasks to reassign tasks in bulk.

    1.  Select the Certification tasks tab, then the task or tasks that you want to reassign.

        -   Select **Reassign**: Reassign a task to another group or user if you aren't the appropriate user to review the field values and you know who the appropriate reviewer is.
            -   **Assignment group**: Select the assignment group the user belongs to.
            -   **Assign to:** Search for the appropriate reviewer to reassign this task to.
            -   **Submit a reason for this action**: Enter a reason why you are reassigning the task.
        -   Select the **Reassign** drop-down menu then select **Assign to me**: Assign the task that isn't assigned, to yourself, if you are the appropriate reviewer for this task.
        -   Select the **Reassign** drop-down menu then select **Request reassignment**: Request to reassign the task, that is assigned to you incorrectly, to someone else. Enter a reason why the task needs to be reassigned, then select **Submit**.
    2.  Select **Proceed**.

3.  In the Certification tasks tab, select the certification task that you want to review.

4.  Review the details of the certification task, then select **Review records to certify**.

    **Note:** You can reassign the tasks on this page, see Step 2 to review the reassignment options.

5.  Select the records that you want to conclude the review for in the Review not completed tab, and then select **Certify** or **Fail**.

    You can select all the records showing on the page for bulk processing by selecting the check box in the first column header, and then selecting the **Select all &lt;n&gt; item/s in this list** link that appears.

    -   The review conclusion of certified or failed is applied in bulk only to those certification fields in the selected records, which are still pending a review. For example, a certification field that is already marked as certified, isn't affected by selecting **Fail**. Only the unreviewed fields are marked as failed. Records whose review is concluded are moved to the Review completed tab.
    -   If the policy is configured to disallow empty attribute values, then CIs with empty fields won't be certified when you select **Certify**. In this situation, to certify those CIs, you must first populate the empty attributes.
6.  Select the records that you want to review in details and then select **Review records**.

    A check mark next to a column header, denotes the fields whose values are included in this certification review \(certification fields\). All other columns show additional fields that are included only to help you identify records \(display fields\).

    When you select records \(or CIs\) to review, the fields \(or attributes\) for the selected records appear on the right, in a separate field review section. When you select a single record to review, the field values of the selected record appear. When you select multiple records to review, the field values don't appear. In that section, select the fields to apply your review results, or select **Select all fields** to apply the review results to all fields.

    |Option|Description|
    |------|-----------|
    |**Fail selected fields**|Select this to denote field values that are incorrect. When you're finished, the records will move to the Review completed tab.|
    |**Certify selected fields**|Select this to confirm field values that are correct. When you're finished, the records will move to the Review completed tab.|
    |**Edit fields**|Select this to update the fields whose value is incorrect. When you're finished, select **Update**. You can continue and certify the updated fields.|

7.  Select **Submit** when all the records have been reviewed.

    The **Submit** button isn't available until all the records in the task are reviewed and the task is complete.Alternatively, you can select the **Submit task** link in the 'Ready to submit' notification.


## What to do next

You can review the certification results in the Review completed tab, and change certification results or edit field values.

