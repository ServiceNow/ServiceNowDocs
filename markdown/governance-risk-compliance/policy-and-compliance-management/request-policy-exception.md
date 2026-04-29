---
title: Request a policy exception
description: Users can request exceptions for policies, control objectives, or issues by specifying the reason of exception on a particular list of the systems, applications, networks, or entities for which the exception will apply. The user must also specify the duration for which the exception is required.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage policy exceptions and extensions, Classic UI, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Request a policy exception

Users can request exceptions for policies, control objectives, or issues by specifying the reason of exception on a particular list of the systems, applications, networks, or entities for which the exception will apply. The user must also specify the duration for which the exception is required.

## Before you begin

Role required: sn\_grc.business\_user, sn\_grc.business\_user\_lite

## About this task

Exceptions provide temporary relief for users unable to meet compliance requirements due to extraordinary situations. For example, if the user is unable to meet a control that stipulates that all critical OS servers must be patched within 48 hours after the OS vendor releases patches.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **My Policy Exceptions**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_epy_qrq_f5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identification number.

</td></tr><tr><td>

Requester

</td><td>

Person requesting the policy exception, usually the control owner.

</td></tr><tr><td>

Approval group

</td><td>

Group that has the compliance manager role. You cannot edit the approval group if the policy exception reaches Review state.If you do not provide an approval group, then the field defaults to compliance manager. Compliance manager is the default role if the policy exception is raised from any upstream application that is integrated with GRC. For example, if you raise a policy exception for a problem that is related to an incident and that problem is related to GRC.

</td></tr><tr><td>

Approver

</td><td>

User from the approval group. If the exception policy moves to the **Analyze** state, then you must select an approver.

</td></tr><tr><td>

State

</td><td>

State of the policy exception within the approval workflow.

</td></tr><tr><td>

Substate

</td><td>

Approval substate of the policy exception within the approval workflow.

</td></tr><tr><td>

Priority

</td><td>

Approval priority of this policy exception

</td></tr><tr><td>

Watch list

</td><td>

Users that are notified when the request is updated.

</td></tr><tr><td>

Name

</td><td>

Unique name of the policy exception.

</td></tr><tr><td>

Reason

</td><td>

Reason for requesting the policy exception. The requester can change the reason until the policy exception is approved.

</td></tr><tr><td>

Justification

</td><td>

Statement of explanation for the policy exception. Justification is also displayed in the **Additional comments** field of the **Comments** tab.

</td></tr><tr><td class="sub-head" colspan="2">

Source

</td></tr><tr><td id="source-type-policy-excep">

Source type

</td><td>

Type of policy exception that you want to create. The options are:-   Policy: Create a policy exception based on a policy.
-   Control objective: Default is a single control objective on which the policy exception is created.

When you select a control objective, the**Impacted controls** tab appears, where you can select controls associated to the control objective.

-   Controls: Option to create a policy exception on multiple controls.

Select **Control** to associate multiple controls from different control objectives. This option supports multiple controls objectives for your policy exception, instead of creating multiple policy exceptions that could be applied on multiple controls.

-   Issue: Issue associated with this policy exception.


</td></tr><tr><td>

Control objective

</td><td>

Control objective associated with this policy exception.

</td></tr><tr><td>

Issue

</td><td>

Issue associated with this policy exception.

</td></tr><tr><td>

Target record

</td><td>

Target record table on which the policy exception is applied. This table is also referenced in the **Policy exception target table** field of the Policy Exception Integration Registry form.

</td></tr><tr><td class="sub-head" colspan="2">

Risk assessment

</td></tr><tr><td>

Risk rating

</td><td>

Select the risk rating as determined by the risk assessment performed on the policy exception.

</td></tr><tr><td>

Risk description

</td><td>

Description of the risk as performed by the risk manager during risk assessment.

</td></tr><tr><td>

Analysis of risk and impact

</td><td>

Details on the likelihood of this risk occurring and residual impacts of this risk on the policy exception.

</td></tr><tr><td>

Risk mitigation plan

</td><td>

The risk mitigation plan for this policy exception.

</td></tr><tr><td class="sub-head" id="policy-ext-det" colspan="2">

Schedule

</td></tr><tr><td>

Valid from

</td><td>

Day on which the policy exception begins.

</td></tr><tr><td>

Valid to

</td><td>

Day on which the policy exception ends.**Valid to** date must be after **Valid from** date and cannot be a past date.

</td></tr><tr><td>

Duration

</td><td>

Number of days between the **Valid from** and **Valid to** dates.

</td></tr><tr><td>

Approved extensions

</td><td>

Number of times extensions have been requested so far and have been approved.

</td></tr><tr><td>

Remaining extensions

</td><td>

Number of times extensions can be requested in future.`Remaining extensions = Value in the **Number of extensions allowed for a policy exception** property – Number of Approved extensions`.

</td></tr><tr><td>

Created

</td><td>

Date on which the policy exception was requested.

</td></tr><tr><td>

Date approved

</td><td>

Date on which the request was approved.

</td></tr><tr><td>

Extension date

</td><td>

Requested extension date, which is after the **Valid to** date.

</td></tr><tr><td>

Extension reason

</td><td>

Reason for extension.

</td></tr><tr><td>

Original valid to

</td><td>

Date until which the policy exception was originally requested and approved. The original **Valid to** date is populated only when the extension is approved.

</td></tr><tr><td class="sub-head" colspan="2">

Comments

</td></tr><tr><td>

Work Notes

</td><td>

Work notes can be used by exception reviewers and approvers to share Information about the exception.

</td></tr><tr><td>

Additional comments

</td><td>

These comments are used by the reviewer to communicate additional information to the exception requester.

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td>

Confidential

</td><td>

Option to enable confidentiality of the record. Only the assigned confidential users or confidential groups of users can access the record.For more information on confidential option, see [Confidentiality flag for audit and compliance records](../../grc-audit/concept/confidentiality-flag-audit-pc.md).

</td></tr></tbody>
</table>    **Note:** In versions prior to Version 10.1, the **Risk assessment** tab was called **Business Impact Analysis** and required that the GRC: Risk Management application be activated. Starting in Version 10.1, the dependency on Risk Management has been removed and the associated field names have changed.

    **Approved extensions**, **Remaining extensions**, **Date approved**, **Extension date**, **Extension reason**, **Original valid to** fields appear only when you have requested an extension on the policy exception and has been approved by the approver.

4.  Save the policy exception.

5.  Click any of the tabs to view the various types of information for the policy exception

6.  Click **Update**.


**Parent Topic:**[Manage policy exceptions and extensions](../concept/manage-policy-exceptions.md)

