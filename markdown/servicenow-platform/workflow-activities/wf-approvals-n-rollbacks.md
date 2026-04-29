---
title: Using workflow approval activities and rolling back workflows
description: When you work with approvals, you need to understand how approval activities interact with approval engines, how to correct a skipped approval workflow activity, and how rollbacks work.Approvals can be managed by approval activities or approval engines, but not both. Approval activities can be used if approval engines are not turned on for the table associated with the workflow.While a workflow is in an active context, an approval activity can skip to the next activity.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using workflow approval activities and rolling back workflows

When you work with approvals, you need to understand how approval activities interact with approval engines, how to correct a skipped approval workflow activity, and how rollbacks work.

**Related topics**  


[Rollback To workflow activity](https://www.servicenow.com/docs/access?context=r_RollbackTo&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

## Approval workflow activities and approval engines

Approvals can be managed by approval activities or approval engines, but not both. Approval activities can be used if approval engines are not turned on for the table associated with the workflow.

Approvals can be managed by approval activities or approval engines, but not both. Trying to use both can cause a range of issues. Approval activites are not available \(greyed out\) in the palette if approval engines are used on the specified table. If you hover over a greyed out approval activity in the palette, a comment with more information is provided. For more information about approvals and approval engines, see [Classic approvals](../../service-administration/reference/r_Approvals.md).

![Approval activities are greyed out in the palette if approval engines are used on the associated table](../../workflow-activities/image/ApprovalActivitiesEngines.png "Unavailable approval activities")

To turn approval engines off for the table, navigate to the **System Properties &gt; Approval Engines** and change the setting for the table to **Turn engines off.**

![To use approval activities, turn off approval engines for the table](../../workflow-activities/image/WFEnginesApproval.png "Turn off approval engines")

**Related topics**  


[Approval and rollback workflow activities](../../workflow-activities/concept/c_ApprovalAndRollbackActivities.md)

[Classic approvals](../../service-administration/reference/r_Approvals.md)

## Correct a skipped workflow approval activity

While a workflow is in an active context, an approval activity can skip to the next activity.

### Before you begin

Role required: admin

### About this task

An approval activity might skip for the following reasons:

-   The approval user or group is missing or invalid \(for example, sys\_id\).
-   The approval user or group became inactive after the approval record was created.
-   The activity is a [Dot-walking to data in related tables](https://www.servicenow.com/docs/access?context=c_DotWalking&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) field, such as `current.opened_by.department.manager`, and it has a missing or invalid approval user or group.
-   The business rule on the table that is associated with the workflow is invalid.

To correct a missed approval activity:

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Live Workflows** &gt; **All Contexts**.

2.  Click the date and time in the **Started** column for the workflow that is incorrectly processing approval activities.

3.  In **Related Links**, click **Show Workflow**.

4.  Review the portion of the workflow that executed, and then do one or more of the following:

    -   Verify that after approval, the workflow progressed to the next activity. If a workflow failed to progress, check the business rules. For more information, see [Debugging business rules](https://www.servicenow.com/docs/access?context=r_DebuggingBusinessRules&version=australia&pubname=australia-api-reference&ft:locale=en-US).
    -   Point to each processed approval activity to find activities where the **State** is **Finished** and **Result** is **Skipped**.
5.  Navigate to **Workflow** &gt; **Workflow Editor** and open the workflow.

6.  Double-click the skipped approval activity.

7.  Click **Users** or **Groups**.

8.  Assign an active user or group for the approval activity. For more information, see [Workflow error handling](../../workflow-administration/concept/c_WorkflowErrorHandling.md).


