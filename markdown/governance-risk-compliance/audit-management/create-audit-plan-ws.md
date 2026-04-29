---
title: Create a plan in the Audit Workspace
description: Create a plan to manage different types of audits in a periodic manner and group engagements in a logical manner.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Audit Supervisor Workspace, Audit Workspace Overview, Audit Management, Governance, Risk, and Compliance]
---

# Create a plan in the Audit Workspace

Create a plan to manage different types of audits in a periodic manner and group engagements in a logical manner.

## Before you begin

Activate the Advanced Audit plugin \(com.sn\_audit\_advanced\).

Role required: sn\_audit\_ws.supervisor or sn\_audit.manager

## About this task

When an audit plan is created and engagements are added to the plan, the plan is sent to the approver for approval.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit workspace** &gt; **Planning** &gt; **All Plans**.

2.  Alternatively, navigate to **Audit** &gt; **Audit workspace** &gt; **Planning** &gt; **My Plans**.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_r2w_hbm_5mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number of the plan.

</td></tr><tr><td>

Name

</td><td>

Name of the plan. For example, Annual Audit Plan for Payroll.

</td></tr><tr><td>

Type

</td><td>

Type of the plan. The choices are:-   None
-   Internal Audit Plan
-   External Audit Plan
-   SOX Audit
-   Compliance Audit Plan
-   Vendor Audit Plan
-   Customer Audit Plan


</td></tr><tr><td>

State

</td><td>

State of the plan. The default state is **Draft**.

</td></tr><tr><td>

Substate

</td><td>

Substate of the plan. The value in this field changes based on the workflow.

</td></tr><tr><td>

Description

</td><td>

Brief description of the plan.

</td></tr><tr><td>

Objectives

</td><td>

Objectives of the plan.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Timeframe

</td><td>

Duration of the plan. The choices are as follows:-   Annual
-   Semi-annual
-   Quarter
-   Other


</td></tr><tr><td>

Start date

</td><td>

Date the plan begins.

</td></tr><tr><td>

End date

</td><td>

Date the plan ends. This field is automatically set based on the choice made in the **Timeframe** field. If the **Timeframe** field has **Other**, then enter an end date manually.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Owning group

</td><td>

Group responsible for owning the plan.

</td></tr><tr><td>

Owner

</td><td>

Plan owner.

</td></tr><tr><td>

Approvers

</td><td>

People who must approve the plan.

</td></tr><tr><td class="sub-head" colspan="2">

Expenses

</td></tr><tr><td>

Budgeted expenses

</td><td>

Budget allocated for the engagements under the plan.

</td></tr><tr><td>

Planned expenses

</td><td>

Rolled up planned expenses from the engagements.

</td></tr><tr><td>

Actual expenses

</td><td>

Rolled up actual expenses from the engagements.

</td></tr><tr><td>

Expense notes

</td><td>

Notes about the expense details.

</td></tr><tr><td class="sub-head" colspan="2">

Resources

</td></tr><tr><td>

Budgeted resources

</td><td>

Number of hours allocated for the engagements under the plan.

</td></tr><tr><td>

Planned resources

</td><td>

Rolled up planned resources from the engagements.

</td></tr><tr><td>

Actual resources

</td><td>

Rolled up actual resources from the engagements.

</td></tr><tr><td>

Resource notes

</td><td>

Notes about the resource details.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes

</td><td>

Notes for this plan. These notes are for internal use and aren’t visible to the customers.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Additional comments about the plan that are visible to the customer.

</td></tr></tbody>
</table>5.  Save the form.

    You can monitor the state of the plan in the stepper of the Overview page as it progresses through the plan process flow.

6.  In the Engagements related list, do one of the following.

    -   To add engagements, select **New**.
    -   To add existing engagements, select **Add**.
7.  Select **Request approval**.

    The state changes from **Draft** to **Awaiting approval**.


## Result

The plan is sent for approval to the approver. After the plan is approved, the form displays the **Approved by** and **Approved on** fields with the values automatically set.

