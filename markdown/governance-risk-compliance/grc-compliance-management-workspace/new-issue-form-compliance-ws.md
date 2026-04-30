---
title: Compliance Workspace issue form details
description: Field descriptions to enter on the New Issue form in the Compliance Workspace.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Manually create GRC issues using the Compliance Workspace, Manage issues using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Compliance Workspace issue form details

Field descriptions to enter on the New Issue form in the Compliance Workspace.

<table id="table_ynl_yjz_dv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identification number.

</td></tr><tr><td>

Name**Note:** Until Version 12.0.1, this label was **Short description**.

</td><td>

A name for the issue.

</td></tr><tr><td>

Issue source

</td><td>

Source from where the issue was created. This field is auto-populated with one of the following options based on how the issue is created:-   Indicator Failure: Issue is created by a failure of the indicator
-   Risk Assessment: Issue is created in a risk
-   Risk Event: Issue is created in a risk event
-   Control Attestation Failure: Issue is created due to a non-compliant control
-   Control Test Failure: Issue is created when a control is ineffective and the control test is marked as closed and complete
-   Ad-hoc: Issue is manually created

</td></tr><tr><td>

Issue type

</td><td>

Type of issue. Choices are:-   Control design effectiveness failure
-   Control operative effectiveness failure
-   Control does not meet requirement
-   Control does not exist
-   Non-compliance to a regulation
-   Non-compliance to a policy
-   Improvement or suggestion to an existing policy
-   Recommendation for a new policy
-   Process optimization or improvement
-   Observation
-   Data Breach
-   Fraud
-   Misstatement
-   Training
-   Documentation
-   Risk issue
-   Other

</td></tr><tr><td>

Classification

</td><td>

The classification of the issue as a risk, compliance, or audit, based on the issue type.

</td></tr><tr><td>

Location

</td><td>

Location where the issue occurred.

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

The substate and applicable details for the substate.

</td></tr><tr><td>

Priority

</td><td>

The sequence in which an issue needs to be resolved, based on its impact and urgency: -   **1 — Critical**
-   **2 — High**
-   **3 — Moderate**
-   **4 — Low**
-   **5 — Planning**

</td></tr><tr><td>

Issue rating

</td><td>

Starting with Version 12.0.1, the issue manager can assign the issue rating to the issue. Based on the issue rating, the **Due date** under the **Dates** tab is calculated as follows and displayed:-   Very high \(2 days\)
-   High \(4 days\)
-   Moderate \(8 days\)
-   Low \(10 days\)
-   Very Low \(15 days\)

 You can manually override the **Due date**. **Note:** Users with the sn\_grc.manager and sn\_grc\_advanced.issue\_triage\_manager role can navigate to **Policy and Compliance** &gt; **Administration** &gt; **Issue rating** and define additional issue ratings.

When the issue transitions to the **Respond** state, the Issue rating field is read only.

</td></tr><tr><td>

Description

</td><td>

Comprehensive description of the issue.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Assignment group

</td><td>

Group to which this issue has been assigned. Each member receives a notification when activity has occurred on this issue.

</td></tr><tr><td>

Assigned to

</td><td>

Member of the group assigned to resolve the issue. Starting with Version 12.0.1, the user must have at least the sn\_grc.business\_user role.

**Note:** Use the bulb icon to get suggestions on who must the issue be assigned to. The bulb icon only appears if you have the GRC: Predictive Intelligence application activated, the form is saved, the **Assigned to** field is not disabled, and the GRC Property is selected as Similarity Analysis. For more information, see [Governance, Risk, and Compliance properties](../../grc-common/reference/grc-properties.md).

Starting with Version 12.0.1, the assigned-to user receives an email notification when the issue manager [requests more information](../../grc-policy-and-compliance/task/remediate-issue.md).

Starting with Version 12.0.1, when an issue transitions to the **Respond** state, an entry in the **Assigned to** field is mandatory.

</td></tr><tr><td>

Issue manager group

</td><td>

The group responsible for managing and reviewing the issue. Starting with Version 12.0.1, the following enhancements and requirements were introduced:

-   Members of the issue manager group must have one of the following roles:
    -   sn\_audit.manager
    -   sn\_audit.user
    -   sn\_compliance.manager
    -   sn\_compliance.user
    -   sn\_grc.manager
    -   sn\_grc.user
    -   sn\_risk.manager
    -   sn\_risk.user
-   When an issue transitions to the **Analyze** state, an entry in either the **Issue manager group** or **Issue manager** field is mandatory.
-   When an issue is assigned to the group, the members receive an email notification. Additionally, the issue manager receives an email notification when the issue transitions to the **Review** state.

</td></tr><tr><td>

Issue manager

</td><td>

The user responsible for managing and reviewing the issue. Starting with Version 12.0.1, the following enhancements and requirements were introduced:

-   The issue manager must have at least the sn\_grc.user role.
-   The issue manager receives an email notification when the assigned-to user [requests more information](../../grc-policy-and-compliance/task/remediate-issue.md).
-   When an issue transitions to the **Analyze** state, an entry in either this field or **Issue manager** is mandatory.
-   When an issue transitions to the **Respond** state, an entry in this field is mandatory.

</td></tr><tr><td>

Watch list

</td><td>

Users who are on the watch list for the issue.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Due date

</td><td>

\(Starting with Version 12.0.1\) This date is auto-populated based on a GRC property. Navigate to **Policy and Compliance** &gt; **Administration** &gt; **GRC Properties**. If the **Auto populate due date based on issue rating** property is set to **Yes**, this field is auto-populated based on the predefined remediation time frame for the issue's risk rating. Otherwise, you can manually enter a due date.When an issue transitions to the **Respond** state, an entry in this field is mandatory.

</td></tr><tr><td>

Confirmed date

</td><td>

\(Starting with Version 12.0.1\) The date when the issue is confirmed. This field is read-only, and displays today's date when the issue is moved from **New** to any of the following states:-   **Analyze**
-   **Review**
-   **Respond**

**Note:** If a triage issue is converted to an actual issue, this field displays the date it was converted.

</td></tr><tr><td>

Planned start date

</td><td>

Date and time that work on the issue is expected to begin.

</td></tr><tr><td>

Planned end date

</td><td>

Date and time that work on the issue is expected to end.

</td></tr><tr><td>

Duration

</td><td>

Estimated amount of work time. Calculated using the **Planned state date** and **Planned end date**.

</td></tr><tr><td>

Created

</td><td>

The date and time the issue was created.

</td></tr><tr><td>

Closed

</td><td>

The date and time the issue was closed.

</td></tr><tr><td>

Actual start date

</td><td>

Time when work began on this issue.

</td></tr><tr><td>

Actual end date

</td><td>

Time when work on this issue was completed.

</td></tr><tr><td>

Actual duration

</td><td>

Amount of work time. Calculated using the **Actual state date** and **Actual end date**.

</td></tr><tr><td class="sub-head" colspan="2">

Issue grouping

</td></tr><tr><td>

Parent issue

</td><td>

Parent issue this issue belongs to.

</td></tr><tr><td>

Issue group rule

</td><td>

Group rule assigned to this issue. The Issue group rule is used to group similar issues together into a parent issue based on conditions defined in the rule. This allows you to work on similar issues simultaneously and close out the parent issue after all issues are resolved. This closes out all the child issues.

</td></tr><tr><td class="sub-head" colspan="2">

Action plan

</td></tr><tr><td>

Recommendation

</td><td>

Resolution actions recommended by the risk, compliance, or audit teams.

</td></tr><tr><td>

Action Plan

</td><td>

The plan for remediating the issue.

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

Click the **Work notes** check box to display the **Work notes** field. Information about how to resolve the issue, or steps already taken to resolve it, if applicable. Work notes are visible to users who are assigned to the issue. Click **Post** to add your work notes to the issue.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

Public information about the issue. Click **Post** to add your comments to the issue.

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Functional domain

</td><td>

Functional domain for the issue.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Details

</td></tr><tr><td>

Control/Risk

</td><td>

The control or risk associated with the issue.When the control is associated, the corresponding entity of the control is added to the **Entity** field, and the corresponding control objective is added to the **Control Objective/Risk Statement** field. The control objective and entity are the ones that are linked to this control.

When the control is associated to the issue form, an m2m record is created in the source \[sn\_grc\_m2m\_issue\_item\] table. Whenever a record is added in the source table, a corresponding record, Issue to Entity is added in the destination \[sn\_grc\_m2m\_issue\_to\_entity\] table, and another record Issue to Content is added in the destination \[sn\_grc\_m2m\_issue\_content\] table for the associated entity and control objective of the control.

</td></tr><tr><td>

Entity

</td><td>

Related entity.

</td></tr><tr><td>

Policy

</td><td>

The policy associated with the issue.

</td></tr><tr><td>

Authority document

</td><td>

The authority document associated with the issue.

</td></tr><tr><td>

Control Objective/Risk Statement

</td><td>

The control objective or risk statement related to this issue.

</td></tr><tr><td>

Processing activity

</td><td>

 

</td></tr><tr><td class="sub-head" colspan="2">

Engagement

</td></tr><tr><td>

Engagement

</td><td>

The related engagement.

</td></tr><tr><td class="sub-head" colspan="2">

Risk Event

</td></tr><tr><td>

Risk event

</td><td>

The related risk event.

</td></tr></tbody>
</table>