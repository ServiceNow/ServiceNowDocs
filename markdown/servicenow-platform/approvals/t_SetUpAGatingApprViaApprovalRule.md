---
title: Set up a gating approval via an approval rule
description: You can set up a gating approval via an approval rule.
locale: en-US
release: zurich
product: Approvals
classification: approvals
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Gating approvals, Approval rules, Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up a gating approval via an approval rule

You can set up a gating approval via an approval rule.

**Important:** Classic approval rules have been replaced by the Workflow Studio [Ask for Approval action](https://www.servicenow.com/docs/access?context=ask-approval-flow-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US). Use Workflow Studio to create workflow-driven approval logic that is easier to maintain and provides better reporting information.

## Before you begin

Role required: admin

## Procedure

1.  From the left navigation pane, select **System Policy** &gt; **Approval Rules**.

2.  Click **New**.

    ![Approval rule](../image/ApprovalRule.png)

<table id="table_n5t_lpl_sr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of this rule.

</td></tr><tr><td>

Table

</td><td>

Task table to which this rule applies. For most service catalog approvals, select **Request**.

**Note:** The list shows only tables and database views that are [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=zurich&pubname=zurich-application-development&ft:locale=en-US) as the approval rule.

</td></tr><tr><td>

Active

</td><td>

Indicator of whether the rule is active \(defaults to true\).

</td></tr><tr><td>

Run Rule Before

</td><td>

Indicator of whether the rule runs before or after the request record is saved. For most approvals, select this check box.

</td></tr><tr><td>

User

</td><td>

User who must approve this request \(can be empty\).

</td></tr><tr><td>

Group

</td><td>

Group that must approve this request \(can be empty\).

</td></tr><tr><td>

Set State

</td><td>

Value of the approval field on the task in after this rule runs. In most cases, select **Requested**.

</td></tr><tr><td>

Condition

</td><td>

Condition under which the rule applies.

</td></tr><tr><td>

Script

</td><td>

An optional server script to programmatically specify who the approver should be. For example, for the one-line script `current.requested_for.manager`, ServiceNow checks the requested\_for reference field on the current record. It then locates the manager field on the referenced record and assigns that person as the approver. For other examples, see the Script field on approval rules provided by ServiceNow.

</td></tr></tbody>
</table>    Notes and limitations:

    1.  You can have as many rules as you want on a given table. If more than one rule applies, you will get more than one approver.
    2.  You can't get duplicate approvers, for example, if two rules both want Fred Luddy to approve a particular request, the system will only create one approval entry for him.
    3.  By default all requests start out in a **Not yet requested** approval state. Approval notifications will not go out until the request's approval state is set to **Requested**. You can do that manually, or you can do it in script, but the easiest way to do it is to use the **Set State** field to automatically set the request to **Requested**.

**Parent Topic:**[Gating approvals](../concept/c_GatingApprovals.md)

