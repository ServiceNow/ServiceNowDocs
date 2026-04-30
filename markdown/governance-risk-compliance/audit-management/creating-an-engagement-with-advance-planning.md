---
title: Create an engagement with advanced planning
description: Use the advanced planning capabilities to create an engagement that automatically creates an engagement project. After an engagement project is created, you can add resource plans and cost plans to the engagement. The values of these plans roll up to the engagement and to the audit plan.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Audit Plan Overview, Use, Audit Management, Governance, Risk, and Compliance]
---

# Create an engagement with advanced planning

Use the advanced planning capabilities to create an engagement that automatically creates an engagement project. After an engagement project is created, you can add resource plans and cost plans to the engagement. The values of these plans roll up to the engagement and to the audit plan.

## Before you begin

To use the advanced planning feature, you must activate the following store applications and plugins:

-   GRC Advanced Audit plugin \(com.sn\_audit\_advanced\)
-   GRC Profiles
-   GRC Policy and Compliance Management
-   GRC Risk Management
-   GRC Advanced Core
-   GRC Advanced Risk
-   GRC Audit Management
-   Project Portfolio Management Standard

You can choose to create audit plans for the engagement.

**Note:** To know more about the applications in GRC module, see [Governance, Risk, and Compliance](../../grc-common/reference/r_WhatIsGRC.md).

Role required: sn\_audit.manager

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Engagements** &gt; **Create New**.

2.  On the form, fill in the fields.

<table id="table_nht_mjj_mv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identification number of the engagement.

</td></tr><tr><td>

Name

</td><td>

Name of the engagement.

</td></tr><tr><td>

Type

</td><td>

Type of engagement. The choices are as follows:-   None
-   Internal Audit
-   External Audit
-   SOX Audit
-   IT Audit
-   Financial Audit
-   Compliance Audit
-   Certification Audit
-   Regulatory Audit
-   Operational Audit
-   Continuous Audit
-   Vendor Audit
-   Customer Audit
-   Store Audit
-   Quality Audit
-   Project Audit
 **Note:** For more information on the types of audits, see [Audit types](../reference/types-of-audit.md).

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to the engagement.

</td></tr><tr><td>

State

</td><td>

State of the engagement. The choices are as follows:-   Scope
-   Validate
-   Fieldwork
-   Awaiting Approval
-   Follow Up
-   Closed Complete
-   Closed Incomplete
 **Note:** For more information on each of these states, see [Manage engagements](../concept/c_Engagements.md).

</td></tr><tr><td>

Percent complete

</td><td>

Percentage of the engagement that is complete.

</td></tr><tr><td>

Auditors

</td><td>

Auditors assigned to the engagement.

</td></tr><tr><td>

Approvers

</td><td>

Approvers assigned to the engagement.

</td></tr><tr><td>

Description

</td><td>

General description of the engagement.

</td></tr><tr><td>

Objectives

</td><td>

Stated objectives of the engagement.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Engagement planned start

</td><td>

Estimated start date of the engagement.

</td></tr><tr><td>

Engagement starts

</td><td>

Choice to automatically determine the start date of the engagement. The choices are as follows:-   Scope
-   Validate
-   Fieldwork


</td></tr><tr><td>

Engagement actual start

</td><td>

Actual date when the engagement begins.

</td></tr><tr><td>

Engagement planned end

</td><td>

Estimated end date of the engagement.

</td></tr><tr><td>

Engagement ends

</td><td>

Choice to automatically determine the end date of the engagement. The choices are as follows:-   Follow Up
-   Closed
 **Note:** For more information on the Follow Up and Closed states, see [Manage engagements](../concept/c_Engagements.md).

</td></tr><tr><td>

Engagement actual end

</td><td>

Actual date the engagement ends.

</td></tr><tr><td>

Fieldwork planned start

</td><td>

Estimated start date of the fieldwork.

</td></tr><tr><td>

Fieldwork planned end

</td><td>

Planned end date that was originally set in the engagement. **Note:** This field is automatically set to one day after the planned start date for fieldwork.

</td></tr><tr><td>

Fieldwork planned duration

</td><td>

Number of days and hours planned for fieldwork. The duration and planned start date of fieldwork are used to calculate the planned end date. If audit tasks are defined, this field is automatically set to the longest planned duration from the audit tasks.

</td></tr><tr><td>

Fieldwork actual start

</td><td>

Actual start date of the fieldwork. If audit tasks are defined, this field is automatically set to the earliest actual start date from the audit tasks.

</td></tr><tr><td>

Fieldwork actual end

</td><td>

Actual end date of the fieldwork. If audit tasks are defined, this field is automatically set to the latest actual end date from the audit tasks.

</td></tr><tr><td>

Fieldwork actual duration

</td><td>

Duration of fieldwork start date and end date.

</td></tr><tr><td class="sub-head" colspan="2">

Results

</td></tr><tr><td>

Result

</td><td>

Results of the engagement. The choices are as follows:-   Satisfactory
-   Adequate
-   Inadequate


</td></tr><tr><td>

Opinion

</td><td>

Justification for the selected result.

</td></tr><tr><td class="sub-head" colspan="2">

Report

</td></tr><tr><td>

Knowledge base

</td><td>

Knowledge base to use to select the report template.

</td></tr><tr><td>

Report template

</td><td>

Template that is used to generate the knowledge base article which reports the engagement results.

</td></tr><tr><td>

KB article

</td><td>

Recently generated knowledge base article which contains the engagement results.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Additional comments

</td><td>

Comments that are viewable by customers.

</td></tr><tr><td>

Work notes

</td><td>

Comments that are viewable by the administrator and by the audit manager.

</td></tr><tr><td class="sub-head" colspan="2">

Plan Details

</td></tr><tr><td>

Parent plan

</td><td>

Plan to associate the engagement with.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td>

Confidential

</td><td>

Option to enable confidentiality of the record. Only the assigned confidential users or confidential groups of users can access the record.For more information on confidential option, see [Confidentiality flag for audit and compliance records](../concept/confidentiality-flag-audit-pc.md).

</td></tr><tr><td class="sub-head" colspan="2">

Expenses and Resources

</td></tr><tr><td>

Budgeted expenses

</td><td>

Budgeted expenses for the engagement.

</td></tr><tr><td>

Planned expenses

</td><td>

Estimated expenses for the engagement. If the cost plan is defined, this field automatically displays the estimated expenses.

</td></tr><tr><td>

Remaining budgeted expenses

</td><td>

Difference between **Budgeted expenses** and **Planned expenses**. This field is automatically set.

</td></tr><tr><td>

Actual expenses

</td><td>

Actual expenses incurred. If timecards are defined, this field is automatically set.

</td></tr><tr><td>

Budgeted resources

</td><td>

Budgeted resources for the engagement, in hours.

</td></tr><tr><td>

Planned resources

</td><td>

Estimated resources for the engagement, in hours. If resource plans are defined, this field is automatically set.

</td></tr><tr><td>

Actual resources

</td><td>

Actual resources for the engagement, in hours. If timecards are defined, this field is automatically set.

</td></tr><tr><td class="sub-head" colspan="2">

Project Details

</td></tr><tr><td>

Project

</td><td>

Automatically created engagement project. This field is populated when you click **Validate and Plan**. **Note:** This field also gets populated when you click **Enable Advanced Planning** on the engagement, in the Validate or Fieldwork state. This field also gets populated if any of the following are true:

-   The field is already linked to a plan with advanced planning capabilities.
-   The user has the required roles.
-   The engagement is in the correct state.


</td></tr><tr><td>

Time card approver

</td><td>

Person assigned to the engagement. You can also change the approver in this field.**Note:** If more than one user is selected, then everyone on the list must approve the time cards.

</td></tr></tbody>
</table>3.  Click **Validate and Plan**.

    **Note:** The **Validate and Plan** button only appears if the Advanced Audit plugin is activated.

    The project details are populated.

4.  Click **Enable Advanced Planning**.


## Result

An engagement project is created in the background for the engagement. The Resource Plan and Cost Plan related lists also appear.

## What to do next

[Create a resource plan](https://www.servicenow.com/docs/access?context=t_CreateResourcePlanProjectTask&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) and [Create a cost plan](https://www.servicenow.com/docs/access?context=t_CreateAProjectCostPlan&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US).

