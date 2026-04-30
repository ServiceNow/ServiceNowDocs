---
title: Remediate an issue in AI Risk and Compliance
description: After an issue has been created, reported, identified, triaged, and investigated, you can remediate it.
locale: en-US
release: zurich
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Remediate an issue in AI Risk and Compliance

After an issue has been created, reported, identified, triaged, and investigated, you can remediate it.

## Before you begin

Role required: sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin, sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager, sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user, sn\_ai\_case\_mgmt.ai\_case\_analyst

## About this task

Remediating an issue marks an intention to fix the underlying issue causing the control failure or risk exposure. Accepting an issue marks an intention to create an exception for a known control failure or risk. Controls that are **Accepted** remain in a non-compliant state until the control is reassessed. In this way, the issue can be used to document observations during audits.

## Procedure

1.  Open the issue you want to remediate.

2.  Click the **Remediation Tasks** tab.

    **Note:** You have two options for creating a remediation task:

    -   Click **Suggested Remediation Tasks** and click **Copy** to use an existing task as a basis for creating this task. A copy of the selected remediation task is created with certain information from that task copied to the new task. You can manually complete the other fields.
    -   Clicking **New** and manually creating the task.
3.  On the form, fill in the fields.

<table id="table_ynl_yjz_dv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identification number.

</td></tr><tr><td>

Assigned to

</td><td>

Select the user responsible for working this task.You can configure a hierarchy of users to access the remediation task. For more information, see [User hierarchy access control for issue and remediation task records](../../grc-policy-and-compliance/concept/user-hierarchy-risk-remed-task.md).

</td></tr><tr><td>

Issue

</td><td>

The issue for which this task was created.

</td></tr><tr><td>

State

</td><td>

The current state of the task.

</td></tr><tr><td>

Priority

</td><td>

Select the priority or sequence this task needs to be resolved, based on its impact and urgency.

</td></tr><tr><td>

Watch list

</td><td>

Select users who want to be notified when changes occur.

</td></tr><tr><td>

Created/Updated

</td><td>

Displays the date/time when the task was created and updated.

</td></tr><tr><td>

Name

</td><td>

Brief description of the task. This will appear in lists of tasks.

</td></tr><tr><td>

Description

</td><td>

Enter a complete description of the task.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Notes and Comments

</td></tr><tr><td>

Additional comments

</td><td>

As needed, enter any customer-facing comments related to this task.

</td></tr><tr><td>

Work notes

</td><td>

Enter any non-customer-facing notes related to the remediation of the issue.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Task Schedule

</td></tr><tr><td>

Planned duration

</td><td>

Estimated amount of work time. Calculated using the **Planned start date** and **Planned end date**.

</td></tr><tr><td>

Planned start date

</td><td>

Date and time that work on the task is expected to begin.

</td></tr><tr><td>

Planned end date

</td><td>

Date and time that work on the task is expected to end.

</td></tr><tr><td>

Actual duration

</td><td>

Amount of actual work time. Calculated using the **Actual start date** and **Actual end date**.

</td></tr><tr><td>

Actual start date

</td><td>

Time when work began on this task.

</td></tr><tr><td>

Actual end date

</td><td>

Time when work on this task was completed.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td>

Confidential

</td><td>

Option to enable confidentiality of the record. Only the assigned confidential users or confidential groups of users can access the record.For more information on confidential option, see [Confidentiality flag for audit and compliance records](../../grc-audit/concept/confidentiality-flag-audit-pc.md).

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Using AI Risk and Compliance](../concept/using-ai-risk-and-compliance.md)

