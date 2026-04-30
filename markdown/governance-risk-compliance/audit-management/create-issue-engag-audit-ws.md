---
title: Create an issue for an engagement
description: Create an issue to document policy, risk, or audit observations, or to accept any GRC problems. You can also identify the source of the issue to help analyze and classify the issues.
locale: en-US
release: xanadu
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Audit Workspace for the Audit supervisor, Audit Workspace, Audit Management, Governance, Risk, and Compliance]
---

# Create an issue for an engagement

Create an issue to document policy, risk, or audit observations, or to accept any GRC problems. You can also identify the source of the issue to help analyze and classify the issues.

## Before you begin

Role required: sn\_audit.manager, sn\_audit\_ws.supervisor

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Click the lists icon \(![List icon.](../image/ListsIcon.jpg)\).

3.  Click **All engagements** or **My engagements** in the Execution list.

4.  Click the link to the engagement record in the **Name** column.

    The engagement record details open in the **Overview** tab.

5.  Click the Other issues related list.

6.  Click **New**.

7.  On the form, fill in the fields.

<table id="table_m54_5g2_mqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identification number.

</td></tr><tr><td>

Name

</td><td>

Name of the issue.

</td></tr><tr><td>

Issue source

</td><td>

Source from where the issue was created. This field is auto-populated with one of the following options based on how the issue is created:-   Indicator Failure: Issue is created by a failure of the indicator.
-   Risk Assessment: Issue is created in a risk.
-   Risk Event: Issue is created in a risk event.
-   Control Attestation Failure: Issue is created due to a non-compliant control.
-   Control Test Failure: Issue is created when a control is ineffective and the control test is marked as closed and complete.
-   Ad-hoc: Issue is manually created.


</td></tr><tr><td>

Issue type

</td><td>

Type of issue.

</td></tr><tr><td>

Classification

</td><td>

Classification of the issue as a risk, compliance, or audit, based on the issue type.

</td></tr><tr><td>

State

</td><td>

-   New
-   Analyze
-   Respond
-   Review
-   Closed Complete
-   Closed Incomplete


</td></tr><tr><td>

Substate

</td><td>

Substate and applicable details for the substate.

</td></tr><tr><td>

Priority

</td><td>

Sequence in which an issue needs to be resolved, based on its impact and urgency:-   1 — Critical
-   2 — High
-   3 — Moderate
-   4 — Low
-   5 — Planning


</td></tr><tr><td>

Issue rating

</td><td>

Issue manager can assign a issue rating to the issue. Based on the issue rating, the **Due date** in the **Dates** tab is calculated as follows and displayed:-   Very high \(2 days\)
-   High \(4 days\)
-   Moderate \(8 days\)
-   Low \(10 days\)
-   Very Low \(15 days\)
You can manually override the **Due date**.

</td></tr><tr><td>

Description

</td><td>

Comprehensive description of the issue.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group to which the issue is assigned. Each member receives a notification when an activity occurs on this issue.

</td></tr><tr><td>

Assigned to

</td><td>

Member of the group assigned to resolve the issue.

</td></tr><tr><td>

Issue manager group

</td><td>

Group responsible for managing and reviewing the issue.

</td></tr><tr><td>

Issue manager

</td><td>

User responsible for managing and reviewing the issue.

</td></tr><tr><td>

Watch list

</td><td>

Users added to view the issue.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Due date

</td><td>

Due date is auto-populated based on a GRC property, **Auto populate due date based on issue rating**. If it is set to **Yes**, the field is auto-populated based on the predefined remediation time frame for the issue's risk rating. Otherwise, you can manually enter a due date.When an issue transitions to the **Respond** state, an entry in this field is mandatory.

</td></tr><tr><td>

Confirmed date

</td><td>

Date on which the issue is confirmed. This field is read-only, and displays the current date when the issue is moved from **New** to any of the following states:-   Analyze
-   Review
-   Respond
 **Note:** If a triage issue is converted to an actual issue, this field displays the date it was converted.

</td></tr><tr><td>

Created

</td><td>

Date and time the issue was created.

</td></tr><tr><td>

Closed

</td><td>

Date and time the issue was closed.

</td></tr><tr><td>

Planned start date

</td><td>

Date and time when the work on the issue is expected to begin.

</td></tr><tr><td>

Planned end date

</td><td>

Date and time when the work on the issue is expected to end.

</td></tr><tr><td>

Planned duration

</td><td>

Estimated duration of work time. Calculated using the **Planned start date** and **Planned end date**.

</td></tr><tr><td>

Actual start date

</td><td>

Time when work began on the issue.

</td></tr><tr><td>

Actual end date

</td><td>

Time when work on the issue was completed.

</td></tr><tr><td>

Actual duration

</td><td>

Duration of work time. Calculated using the **Actual start date** and **Actual end date**.

</td></tr><tr><td class="sub-head" colspan="2">

Details

</td></tr><tr><td>

Control/Risk

</td><td>

Control or risk associated with the issue.

</td></tr><tr><td>

Control Objective/Risk statement

</td><td>

Control objective or risk statement related to this issue.

</td></tr><tr><td>

Entity

</td><td>

Related entity.

</td></tr><tr><td>

Configuration item

</td><td>

Item associated with the issue. If all child issues have the same configuration item, it gets copied over to the parent issue.

</td></tr><tr><td>

Location

</td><td>

Location where the issue occurred.

</td></tr><tr><td>

Risk event

</td><td>

Related risk event.

</td></tr><tr><td>

Engagement

</td><td>

Related engagement.

</td></tr><tr><td>

Policy

</td><td>

Policy associated with the issue.

</td></tr><tr><td>

Authority document

</td><td>

Authority document associated with the issue.

</td></tr><tr><td class="sub-head" colspan="2">

Issue grouping

</td></tr><tr><td>

Parent issue

</td><td>

Parent issue to which the issue belongs.

</td></tr><tr><td>

Issue group rule

</td><td>

Group rule assigned to the issue.Issue group rule is used to group similar issues together into a parent issue based on conditions defined in the rule. This allows you to work on similar issues simultaneously and close out the parent issue after all issues are resolved. This closes out all the child issues.

</td></tr><tr><td class="sub-head" colspan="2">

Action plan

</td></tr><tr><td>

Recommendation

</td><td>

Resolution actions recommended by the risk, compliance, or audit teams.

</td></tr><tr><td>

Action plan

</td><td>

Plan for remediating the issue.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td>

Confidential

</td><td>

Option to enable confidentiality of the record. Only the assigned confidential users or confidential groups of users can access the record. For more information on confidential option, see [Confidentiality flag for audit and compliance records](../../grc-audit/concept/confidentiality-flag-audit-pc.md).

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Information about how to resolve the issue, or steps already taken to resolve it, if applicable. Work notes are visible to users who are assigned to the issue.

</td></tr><tr><td>

Additional comments

</td><td>

Public information about the issue.

</td></tr></tbody>
</table>8.  Click **Save**.


