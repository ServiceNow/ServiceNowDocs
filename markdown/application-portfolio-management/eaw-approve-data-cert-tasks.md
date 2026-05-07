---
title: Review and certify data certification tasks
description: You can review and complete data certification tasks to confirm that records meet the standards defined in a certification policy. Certification tasks are generated when a policy is run and are assigned based on the policy's assignment configuration.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-30"
reading_time_minutes: 2
breadcrumb: [Working with data certification, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Review and certify data certification tasks

You can review and complete data certification tasks to confirm that records meet the standards defined in a certification policy. Certification tasks are generated when a policy is run and are assigned based on the policy's assignment configuration.

## Before you begin

You must be assigned a certification task as a user or as a member of an assigned user group.

Role required: sn\_apm.apm\_analyst

## About this task

Certification tasks are generated when a data certification policy is run. The review experience in the Enterprise Architecture Workspace uses the underlying Data Certification workflow to review and complete certification tasks directly in the workspace.

If a certification task is assigned incorrectly, you can reassign the task or request reassignment. If you don't know the appropriate reviewer, request an administrator to reassign the task.

Policy configuration can affect review behavior:

-   If empty attribute values are disallowed, you can mark certification as failed for records with empty fields, but you must populate those fields before you can certify them.
-   If updates to field values are disallowed, you can't update noncompliant records and must mark their certification as failed.

## Procedure

1.  Navigate to **Workspaces &gt; Enterprise Architecture Workspace**.

2.  Select the **My Certifications** tab to view certification tasks assigned to you.

3.  Select the certification task that you want to review.

4.  Review the task details, including the policy, scope, and instructions.

5.  Select **Review records to certify**.

6.  In the **Review not completed** tab, review the records included in the task.

7.  Select the appropriate certification status:

    -   Select **Certify** to verify that the data is correct.
    -   Select **Fail** to indicate that the data doesn't meet certification requirements.
8.  Select individual records to review field-level details.

9.  In the Certification tasks list, select multiple tasks to reassign tasks in bulk.

    1.  Select the Certification tasks tab, then the task or tasks that you want to reassign.

        -   Select **Reassign**: Reassign a task to another group or user if you aren't the appropriate user to review the field values and you know who the appropriate reviewer is.
            -   **Assignment group**: Select the assignment group the user belongs to.
            -   **Assign to:** Search for the appropriate reviewer to reassign this task to.
            -   **Submit a reason for this action**: Enter a reason why you are reassigning the task.
        -   Select the **Reassign** drop-down menu then select **Assign to me**: Assign the task that isn't assigned to yourself if you are the appropriate reviewer for this task.
        -   Select the **Reassign** drop-down menu then select **Request reassignment**: Request to reassign the task, that is assigned to you incorrectly, to someone else. Enter a reason why the task needs to be reassigned, then select **Submit**.
    2.  Select **Proceed**.

10. After all records in the task are reviewed, select **Submit**.


## Result

The certification task is completed only after all records are reviewed. Records whose review is completed move to the **Review completed** tab.

## What to do next

Certification results are applied only to fields that are still pending review. Fields already marked as certified are not affected when you fail certification.

Certification fields are indicated by a check mark in the column header. Other fields are displayed only to help identify the record.

**Parent Topic:**[Working with data certification](../../concept/eaw-concept/eaw-work-with-data-cert.md)

