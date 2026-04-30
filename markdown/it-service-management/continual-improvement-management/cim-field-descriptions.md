---
title: Improvement field descriptions
description: Improvement Initiative form and related field descriptions.
locale: en-US
release: xanadu
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Continual Improvement Management reference, Continual Improvement Management, IT Service Management]
---

# Improvement field descriptions

Improvement Initiative form and related field descriptions.

## Improvement Initiative form

<table id="table_rp2_bjj_4cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique CIM number.

</td></tr><tr><td>

Business service

</td><td>

CMDB Business service improved by the improvement initiative.

</td></tr><tr><td>

Service offering

</td><td>

Service offering associated with this improvement initiative.

</td></tr><tr><td>

Business process

</td><td>

Business process improved by the improvement initiative.

 When a business process is selected, the improvement area **Type** field on the **Details** tab is automatically set to Process.

</td></tr><tr><td>

CIM Coordinator

</td><td>

User primarily responsible for ensuring the completion of the improvement initiative.

 The CIM Coordinator must have the Improvement Coordinator role \(sn\_cim.improvement\_coordinator\).

</td></tr><tr><td>

Approver group

</td><td>

Group of users that have permission to approve the improvement initiative.

 CIM Approvers group is added with Continual Improvement Management. Default is empty.

</td></tr><tr><td>

Strategies

</td><td>

Strategic objectives impacted by the improvement initiative. Multiple strategic objectives can be selected. Strategic objectives can be added from the lookup list.

 The lookup list contains both Continual Improvement Management strategic objectives and business [enterprise strategies](https://www.servicenow.com/docs/access?context=create-a-enterprise-strategy&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US) to align with the improvement initiative.

 An enterprise strategy can be added from the navigation menu **Continual Improvement** &gt; **Enterprise Strategies**.

 Also accessible through **Business Planner** and **Organization** navigation menus.

**Note:** If the improvement initiative does not align with a company strategic objective, you can click **Reject** in the header bar to reject the improvement initiative.

</td></tr><tr><td>

State

</td><td>

[State of the improvement initiative](cim-reference.md). This field is read only.

-   New
-   Accepted
-   Assess
-   Approved
-   In Progress
-   On Hold
-   Monitor/Review
-   Closed
-   Canceled

</td></tr><tr><td>

On hold reason

</td><td>

Reason for putting the improvement initiative on hold.**Note:** This field is shown only when the state is on hold.

When an improvement initiative is placed on hold, all CIM tasks are also placed on hold, but the state can be changed manually.

When the improvement initiative is taken off hold, the CIM tasks are returned back to their previous state unless they were changed manually.

</td></tr><tr><td>

Priority

</td><td>

Sequence in which an incident or problem is to be worked on, based on impact and urgency.

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

</td></tr><tr><td>

Effort estimate

</td><td>

Estimate of effort to complete all required tasks for the improvement initiative.

-   Small
-   Medium
-   Large
-   Extra Large

</td></tr><tr><td>

Benefits

</td><td>

Expected level of benefits achieved by completing the improvement initiative.

</td></tr><tr><td>

Percent complete

</td><td>

Percentage of work completed. The percentage is based on the completed state of the CIM phases that belong to this improvement initiative. For example, if there are five CIM phases, each contributes to 20% completion.

</td></tr><tr><td>

Short description

</td><td>

Brief explanation of the improvement initiative.

</td></tr><tr><td>

Business justification

</td><td>

Description about the importance of the improvement and additional details that includes metrics or KPIs used to measure the success.

</td></tr></tbody>
</table>## Goals tab

<table id="table_qvh_gkj_4cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Success measurement method

</td><td>

-   Automated: PA Indicator: An improvement KPI.
-   Reports: Reports to track progress. Users who do not use performance analytics can add reports to track the initiatives.
-   Survey and Assessment: An Assessment metric type.
-   Manual: All other types.

</td></tr><tr><td>

Improvement KPI

</td><td>

Primary KPI used to measure the improvement of the improvement initiative.

 The Show Score Card icon launches the Performance Analytics score card for the improvement KPI.

**Note:** This field is shown only when the **Success Measurement Method** field is set to **Automated: PA Indicator**.

</td></tr><tr><td>

Breakdown

</td><td>

The breakdown of the improvement KPI, if one exists.

**Note:** This field is shown only when an improvement KPI is selected for the **Automated: PA Indicator** success measurement method.

</td></tr><tr><td>

Element

</td><td>

The element of the KPI breakdown.

**Note:** This field is shown only when a breakdown is selected.

</td></tr><tr><td>

2nd Breakdown

</td><td>

The second-level breakdown of the improvement KPI, if one exists.

**Note:** This field is shown only after the first breakdown is selected.

</td></tr><tr><td>

2nd Element

</td><td>

The element of the second-level KPI breakdown.

**Note:** This field is shown only when a second-level breakdown is selected.

</td></tr><tr><td>

Time Series

</td><td>

Time series for the improvement KPI.

**Note:** This field is shown only when an improvement KPI is selected.

</td></tr><tr><td>

Survey &amp; Assessment

</td><td>

Assessment metric type associated with the improvement initiative.**Note:** This field is shown only for the Survey &amp; Assessment success measurement method.

If the improvement initiative was created from within the Survey Management application, this field is not automatically populated.

</td></tr><tr><td>

Base value

</td><td>

Base value of the success measurement method when the target is set.

</td></tr><tr><td>

Percentage improvement

</td><td>

Percent improvement target.

**Note:** This field is shown only when an improvement KPI is selected.

If the KPI is a percent type, then this field is calculated automatically \(based on **Base value** and **Target value** fields\).

</td></tr><tr><td>

Target value

</td><td>

Absolute target value.

 **Note:** For the **Automated: PA Indicator** success measurement method, if the KPI is not a percent type, then this field is calculated automatically \(based on base value and percentage improvement\).

If the target value is already set on the indicator, breakdown, element, and aggregation, this field is automatically set. However, you can override this value by specifying a percent in the **Percent Improvement** field.

 The target value set in this field is synced with the Performance Analytics indicator target for the KPI \(**Performance Analytics** &gt; **Indicator** &gt; **Targets**\).

</td></tr><tr><td>

Target review date

</td><td>

Date the goal should be achieved.

**Note:** For the **Automated: PA Indicator** success measurement method, even if the target date is already set on the indicator, breakdown, element, and aggregation, this field is not automatically set.

</td></tr><tr><td>

Expected outcomes

</td><td>

Tangible artifacts and updates expected by the improvement initiative \(for example, updated process published in new template, work Instructions, and FAQ published in knowledge base\).

</td></tr></tbody>
</table>## Details tab

<table id="table_ux5_3w2_wcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requested for

</td><td>

User for which the improvement initiative was created.

</td></tr><tr><td>

Type

</td><td>

Area improved by the improvement initiative. One or many areas may be selected.

-   People
-   Process
-   Technology

 When a value is selected for the **Business Process** field, the **Type** field is automatically set to Process.

</td></tr><tr><td>

Watch list

</td><td>

Users notified when updates are made to the improvement initiative.

</td></tr><tr><td>

Parent initiative

</td><td>

Parent initiative associated with this child initiative.

 When a parent initiative is selected, all associated child initiatives display in the **Child Initiatives** related list.

</td></tr><tr><td>

Source/Parent

</td><td>

Source or parent application from which the improvement initiative was created.

-   Coaching Opportunity \(COP\)

Coaching opportunity record to which the improvement initiative is linked.

-   CMDB

Remediate Duplicate Tasks record to which the improvement initiative is linked.

-   Demand \(DMND\)

Demand record to which the improvement initiative is linked.

-   GRC issue

Issue record to which the improvement initiative is linked.

-   Incident \(INC\)

Incident record to which the improvement initiative is linked.

-   Problem \(PRB\)

Problem record to which the improvement initiative is linked.

-   \(Survey\) Assessment Metric Type

Assessment metric type for the survey definition record to which the improvement initiative is linked.


**Note:** This field is shown only when an improvement initiative is created from Coaching, CMDB, Demand Management, GRC, Incident Management, Problem Management, or Survey Management applications.

</td></tr></tbody>
</table>## Schedule tab

|Field|Description|
|-----|-----------|
|Planned start date|Expected start date. By default, this field displays the date and time when the CIM initiative was created.|
|Planned end date|Expected end date. By default, this field displays the date and time for the day after the planned start date.|
|Actual start date|The date and time when the progress on a new initiative starts.|
|Actual end date|The date and time when the last task associated with an initiative is completed.|

## Notes tab

<table id="table_smj_hkj_4cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional comments \(customer visible\)

</td><td>

Check box to show additional comments that are visible to the customer.

 If checked, the **Additional comments \(Customer visible\)** field content is shown.

</td></tr><tr><td>

Work notes

</td><td>

Work notes relating to the improvement initiative.

**Note:** Required when submitting the improvement initiative for reapproval.

</td></tr></tbody>
</table>## Closure Notes tab

<table id="table_d1q_hkj_4cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Closure code

</td><td>

-   Successful: Goals met.
-   Withdrawn: No longer needed/applicable.
-   Unsuccessful: Goals not met.

</td></tr><tr><td>

Achieved outcome category

</td><td>

-   Cost Reduction
-   Revenue Generation
-   Time Savings
-   Customer Satisfaction
-   Quality Improvement

</td></tr><tr><td>

Close notes

</td><td>

Notes regarding the improvement initiative closure.

</td></tr></tbody>
</table>## CIM Phases related list

<table id="table_b4w_hkj_4cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique CIMT phase number.

</td></tr><tr><td>

Parent

</td><td>

Improvement initiative to which the CIM phase belongs. There can be multiple CIM phases per improvement initiative.

 The CIM phase groups the tasks, sets a planned end date, and shows the percent complete for tracking purposes.

</td></tr><tr><td>

Percent complete

</td><td>

Percentage of work completed.

 Percentage is based on the completed state of the CIM tasks that belong to this CIM phase.

 For example, if there are five CIM tasks, each contributes to 20% completion.

</td></tr><tr><td>

Planned end date

</td><td>

Estimated phase end date.

</td></tr><tr><td>

Actual end date

</td><td>

End date of the phase.

</td></tr><tr><td>

Short Description

</td><td>

Short description of the phase.

</td></tr><tr><td>

Description

</td><td>

\(Required\) Full description of the phase.

</td></tr></tbody>
</table>## CIM Tasks related list

<table id="table_jp1_3kj_4cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique CIMT task number.

</td></tr><tr><td>

Parent

</td><td>

If the CIM task is tied to a CIM phase, the improvement phase number to which the CIM task belongs. A CIM task can only be tied to one CIM phase.

 You can also create a CIM task directly from a CIM initiative.

 CIM tasks consist of the work required to complete the improvement initiative.

</td></tr><tr><td>

Active

</td><td>

Check box that indicates whether the task is active.

</td></tr><tr><td>

Assigned to

</td><td>

User primarily responsible for completion of the task.

</td></tr><tr><td>

Improvement Initiative

</td><td>

Improvement initiative number to which the CIM task belongs.

</td></tr><tr><td>

Priority

</td><td>

Sequence in which an incident or problem is to be worked on, based on impact and urgency.

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

</td></tr><tr><td>

State

</td><td>

[State of the task](cim-reference.md).

-   Pending
-   Open
-   Work In Process
-   Closed Complete
-   Closed Incomplete
-   Closed Skipped
-   On Hold

</td></tr><tr><td>

On Hold Reason

</td><td>

Reason for putting the CIM task on hold.**Note:** This field is shown only when the state is on hold.

When an improvement initiative is placed on hold, all CIM tasks are also placed on hold, but the state can be changed manually.

When the improvement initiative is taken off hold, the CIM tasks are returned back to their previous state \(unless they were changed manually\).

</td></tr><tr><td>

Planned end date

</td><td>

Estimated end date of the task.

</td></tr><tr><td>

Short Description

</td><td>

Short description of the task.

</td></tr><tr><td>

Description

</td><td>

Full description of the task.

</td></tr><tr><td>

Work notes

</td><td>

Work notes for the task.

</td></tr></tbody>
</table>## Impacted KPIs related list

<table id="table_x5d_3kj_4cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Improvement Initiative

</td><td>

Improvement initiative number to which the impacted KPI belongs.

</td></tr><tr><td>

Impacted KPI

</td><td>

Other related KPIs \(independent of the **Improvement KPI**\) that are affected by changes made as a result of the improvement initiative.

</td></tr><tr><td>

Breakdown

</td><td>

The breakdown of the impacted KPI.

**Note:** This field is shown only when an impacted KPI is selected.

</td></tr><tr><td>

Element

</td><td>

The element of the KPI breakdown.

**Note:** This field is shown only when a breakdown is selected.

</td></tr><tr><td>

Breakdown Level 2

</td><td>

The second-level breakdown of the improvement KPI, if one exists.

**Note:** This field is shown only after the first breakdown is selected.

</td></tr><tr><td>

Element Level 2

</td><td>

The element of the second-level KPI breakdown.

**Note:** This field is shown only when a second-level breakdown is selected.

</td></tr><tr><td>

View Scorecard

</td><td>

Related link to view the scorecard for the KPI.

**Note:** The View KPI details button displays the details of the improvement KPI.

</td></tr></tbody>
</table>## Approvers related list

<table id="table_zmg_3kj_4cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

[State of the approval](cim-reference.md).

-   Not Yet Requested
-   Requested
-   Approved
-   Rejected
-   Canceled
-   No Longer Required

</td></tr><tr><td>

Approver

</td><td>

User authorized to approve the improvement initiative.

 Approvers are members of the group set in the **Approver Group** field on the Improvement Initiative form.

</td></tr><tr><td>

Comments

</td><td>

Comments for the approval improvement initiative.

</td></tr><tr><td>

Created

</td><td>

Date the improvement initiative was created.

</td></tr></tbody>
</table>**Parent Topic:**[Continual Improvement Management reference](cim-reference.md)

