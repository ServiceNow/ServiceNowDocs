---
title: Create a control test from an engagement
description: After defining a control, audit managers create control tests that run periodically and provide documented evidence of whether the associated control is operating correctly.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage engagements, Audit Management Overview, Audit Management, Governance, Risk, and Compliance]
---

# Create a control test from an engagement

After defining a control, audit managers create control tests that run periodically and provide documented evidence of whether the associated control is operating correctly.

## Before you begin

Role required: sn\_audit.admin and sn\_audit.manager

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Engagements** &gt; **All Engagements**.

2.  Open the engagement for the audit task you want to create.

    Assign audit tasks to engagement in one of the following states:

    -   Validate
    -   Fieldwork
    -   Awaiting approval
3.  In the **Audit Tasks** Related List, click **New**.

4.  In the Audit Tasks Interceptor, click **Control Test**.

5.  On the form, fill in the fields.

<table id="table_nht_mjj_mv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identification number.

</td></tr><tr><td>

State

</td><td>

-   Open
-   Work in Progress
-   Review
-   Closed Complete
-   Closed Incomplete
-   Closed Skipped


</td></tr><tr><td>

Parent

</td><td>

Parent audit task.

</td></tr><tr><td>

Control effectiveness

</td><td>

Control effectiveness.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to this control test.

</td></tr><tr><td>

Issue

</td><td>

Issue related to this control test.

</td></tr><tr><td>

Test plan

</td><td>

Test plan associated with this control test.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the control test.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Planned start date

</td><td>

Intended date the control test should begin.

</td></tr><tr><td>

Planned end date

</td><td>

Intended date the control test should end.

</td></tr><tr><td>

Planned duration

</td><td>

Expected duration of this control test. As with actual duration, the planned duration shows total activity time and takes the control test schedule into consideration.

</td></tr><tr><td>

Actual start date

</td><td>

Date that this control test began.

</td></tr><tr><td>

Actual end date

</td><td>

Date that this control test ended.

</td></tr><tr><td>

Actual duration

</td><td>

Duration of the control test from control test start to control test closure.

</td></tr><tr><td class="sub-head" colspan="2">

Design test

</td></tr><tr><td>

Design effectiveness

</td><td>

-   Effective
-   Ineffective


</td></tr><tr><td>

Design expectations

</td><td>

Basic requirement that should be met by a control so that it is effective. This checks if the control was designed properly to achieve the control objective.

</td></tr><tr><td>

Design assessment procedures

</td><td>

Procedure or steps to be followed to conclude whether the design of the control is effective to achieve the control objective or not. This is based on the design expectation.

</td></tr><tr><td>

Design results

</td><td>

Results of testing the design of the control based on the design assessment procedure.

</td></tr><tr><td class="sub-head" colspan="2">

Operation test

</td></tr><tr><td>

Operation effectiveness

</td><td>

-   Effective
-   Ineffective


</td></tr><tr><td>

Operation expectations

</td><td>

Expectations that should be met to ensure that the control is operating effectively to achieve the control objective.

</td></tr><tr><td>

Operation assessment procedures

</td><td>

Detailed steps, to carry out the operation expectations, which need to be performed to conclude that the control is operating successfully.

</td></tr><tr><td>

Operation results

</td><td>

Results of testing the operation of the control based on the operation assessment procedure.

</td></tr><tr><td class="sub-head" colspan="2">

Activity journal

</td></tr><tr><td>

Work notes

</td><td>

Comments that are viewable by the audit manager.

</td></tr><tr><td>

Additional comments

</td><td>

Customer-viewable comments.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td>

Confidential

</td><td>

Option to enable confidentiality of the record. Only the assigned confidential users or confidential groups of users can access the record.For more information on confidential option, see [Confidentiality flag for audit and compliance records](../concept/confidentiality-flag-audit-pc.md).

</td></tr></tbody>
</table>6.  Click **Submit**.


-   **[Automatically generate control tests from an engagement](automatically-generate-control-test.md)**  
After adding an entity to an engagement, you can automatically generate control tests.

**Parent Topic:**[Manage engagements](../concept/c_Engagements.md)

