---
title: Create an engagement
description: Audit managers create engagements to manage audit information and collect entities, controls, and control tests that are relevant to the audit.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-11-17"
reading_time_minutes: 4
breadcrumb: [Manage engagements, Use, Audit Management, Governance, Risk, and Compliance]
---

# Create an engagement

Audit managers create engagements to manage audit information and collect entities, controls, and control tests that are relevant to the audit.

## Before you begin

Role required: sn\_audit.admin or sn\_audit.manager

**Note:** For more information on engagements, see [Manage engagements](../concept/c_Engagements.md).

## About this task

To know more about how to define a control and control objective, see:

-   [Create a control](../../grc-policy-and-compliance/task/t_CreateAControl.md)
-   [Create a control objective](../../grc-policy-and-compliance/task/t_CreateAPolicyStatement.md)

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

A unique identification number.

</td></tr><tr><td>

State

</td><td>

-   Scope
-   Validate and plan
-   Fieldwork
-   Awaiting approval
-   Follow up
-   Closed


</td></tr><tr><td>

Name

</td><td>

Name of the engagement.

</td></tr><tr><td>

Type

</td><td>

Type of engagement. The choices are:-   None
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


</td></tr><tr><td>

Percent complete

</td><td>

Number that represents the percentage of the engagement that has been completed.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to the engagement.

</td></tr><tr><td>

Auditors

</td><td>

Auditors were assigned to the engagement.

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

Audit Period Start

</td><td rowspan="2">

**Note:** The Audit period start and end is available from Yokohama patch 10 and Zurich patch 4 release. To enable this feature, see [Schedule job for audit date enhancement](schedule-job-for-audit-date.md).

To enable Audit period start and end for older version, see [Create exclusion table for audit date](create-exclusion-table-for-audit-date.md).

Enables auditing of past or future periods within an ongoing engagement. Only indicator results falling within the specified audit period will be displayed. These fields enable you to specify the time period being audited, separate from the overall Engagement time frame.

</td></tr><tr><td>

Audit Period End

</td></tr><tr><td>

Engagement planned start

</td><td>

Estimated start date of the engagement.

</td></tr><tr><td>

Engagement starts

</td><td>

Choice to automatically determine the start date of the engagement. The choices are:-   Scope
-   Validate
-   Fieldwork


</td></tr><tr><td>

Engagement actually start

</td><td>

Actual date the engagement begins.

</td></tr><tr><td>

Engagement planned end

</td><td>

Estimated end date of the engagement.

</td></tr><tr><td>

Engagement ends

</td><td>

Choice to automatically determine the start date of the engagement. The choices are:-   Follow Up
-   Closed


</td></tr><tr><td>

Engagement actual end

</td><td>

The actual date that the engagement ends.

</td></tr><tr><td>

Fieldwork planned start

</td><td>

Estimated start date of the fieldwork.

</td></tr><tr><td>

Fieldwork planned end

</td><td>

Planned end date that was originally set in the engagement. **Note:** This field sets the value as one day plus the planned start date for fieldwork by default.

</td></tr><tr><td>

Fieldwork planned duration

</td><td>

Number of days and hours planned for fieldwork. The duration and planned start date of fieldwork are used to calculate the planned end date. If audit tasks are defined, this field is populated with the longest planned duration from the audit tasks.

</td></tr><tr><td>

Fieldwork actual start

</td><td>

Actual start date of the fieldwork. If audit tasks are defined, this field is populated with the earliest actual start date from the audit tasks.

</td></tr><tr><td>

Fieldwork actual end

</td><td>

Actual end date of the fieldwork. If audit tasks are defined, this field is populated with the latest actual end date from the audit tasks.

</td></tr><tr><td>

Fieldwork actual duration

</td><td>

Duration of fieldwork start date and end date.

</td></tr><tr><td class="sub-head" colspan="2">

Results

</td></tr><tr><td>

Result

</td><td>

-   Satisfactory
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

Knowledge base to be used.

</td></tr><tr><td>

Report template

</td><td>

Template to be used to generate the knowledge base article reporting the engagement results.

</td></tr><tr><td>

KB article

</td><td>

Recently generated knowledge base article containing the engagement results

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Additional comments

</td><td>

Customer-viewable comments.

</td></tr><tr><td>

Work notes

</td><td>

Comments that are viewable by the admin audit manager.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td>

Confidential

</td><td>

Option to enable confidentiality of the record. Only the assigned users or groups of users can access the record.For more information on the confidential option, see [Confidentiality flag for audit and compliance records](../concept/confidentiality-flag-audit-pc.md).

</td></tr></tbody>
</table>3.  Select **Submit**.


-   **[Schedule job for audit date enhancement](schedule-job-for-audit-date.md)**  
Scheduled Jobs are automated pieces of work that can be performed at a specific time or on a recurring schedule. Execute this scheduled job to enable enhanced audit date behavior. The audit date enhancements provide improved handling of fieldwork dates at the engagement level, making them independent of child audit task dates.
-   **[Create exclusion table for audit date](create-exclusion-table-for-audit-date.md)**  
Create exclusion lists for the various policy types used in Audit Management.

**Parent Topic:**[Manage engagements](../concept/c_Engagements.md)

