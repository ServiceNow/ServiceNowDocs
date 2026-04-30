---
title: Request a policy exception using the Compliance Workspace
description: Use the Compliance Workspace to request exceptions for policies, control objectives, or issues by specifying the reason of exception on a particular list of the systems, applications, networks, or entities for which the exception applies. You must also specify the duration for which the exception is required.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Manage policy exceptions and extensions using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Request a policy exception using the Compliance Workspace

Use the Compliance Workspace to request exceptions for policies, control objectives, or issues by specifying the reason of exception on a particular list of the systems, applications, networks, or entities for which the exception applies. You must also specify the duration for which the exception is required.

## Before you begin

Role required: sn\_grc.business\_user, sn\_grc.business\_user\_lite

## About this task

Exceptions provide temporary relief when you are unable to meet compliance requirements due to extraordinary situations. For example, you are unable to meet a control that stipulates all critical OS servers must be patched within 48 hours after the OS vendor releases patches.

**Note:** For more information on policy exceptions, see [Manage policy exceptions and extensions](../../grc-policy-and-compliance/concept/manage-policy-exceptions.md).

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  Click **Policy exception** in the **Create** list.

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

Name

</td><td>

Name of the policy exception.

</td></tr><tr><td>

Requester

</td><td>

Person requesting the policy exception, usually the control owner.

</td></tr><tr><td>

Reason

</td><td>

Reason for requesting the policy exception. The requester can change the reason until the policy exception is approved.

</td></tr><tr><td>

Short description

</td><td>

Description for the policy exception request.

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

Justification

</td><td>

Evidence or rationale for the policy exception.

</td></tr><tr><td class="sub-head" colspan="2">

Source

</td></tr><tr id="source-type-policy-excep"><td>

Source type

</td><td>

Type of policy exception that you want to create. The options are:-   Policy: Create a policy exception based on a policy.
-   Control objective: Default is a single control objective on which the policy exception is created.

When you select a control objective, the **Impacted controls** tab appears, where you can select controls associated to the control objective.

-   Controls: Option to create a policy exception on multiple controls.

Select **Control** to associate multiple controls from different control objectives. This option supports multiple controls objectives for your policy exception, instead of creating multiple policy exceptions that could be applied on multiple controls.

-   Issue: Issue associated with this policy exception.


</td></tr><tr><td>

Policy

</td><td>

Policy for which the exception is created.

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

</td></tr><tr id="pol-ext-det-ws"><td class="sub-head" id="policy-ext-det-ws" colspan="2">

Schedule

</td></tr><tr><td>

Valid from

</td><td>

Day on which the policy exception begins.

</td></tr><tr><td>

Valid to

</td><td>

Day on which the policy exception ends. Valid to date must be after Valid from date and cannot be a past date.

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

Number of times extensions can be requested in future. `Remaining extensions = Value in the **Number of extensions allowed for a policy exception** property – Number of Approved extensions`.

</td></tr><tr><td>

Created

</td><td>

Date on which the policy exception was requested.

</td></tr><tr><td>

Date approved

</td><td>

Date on which the exception was approved.

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

Date until which the policy exception was originally requested and approved. The original**Valid to** date is populated only when the extension is approved.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Watch list

</td><td>

Users that are notified when the request is updated.

</td></tr><tr><td>

Approval group

</td><td>

Group that has the compliance manager role. If the policy exception reaches Review state you cannot edit the approval group.If you don’t provide an approval group, then the field defaults to compliance manager. Compliance manager is the default role if the policy exception is raised from any upstream application that is integrated with GRC. For example, if you raise a policy exception for a problem that is related to an incident and that problem is related to GRC.

</td></tr><tr><td>

Approver

</td><td>

User from the approval group. If the exception policy moves to the **Analyze** state, then you must select an approver.

</td></tr><tr id="take-risk-assess"><td class="sub-head" colspan="2">

Risk assessment

</td></tr><tr><td>

Method

</td><td>

Method to assess risk:-   Select risk rating: Select the risk rating associated to this policy exception.
-   Take risk assessment: Take a risk assessment to calculate the risk rating.

**Note:** This option is available only when GRC: Advanced Risk plugin is installed.

 Risk assessment can be triggered by clicking the **Assess risk** button on the form. This button is available only when **Take risk assessment** is selected.

</td></tr><tr><td>

Risk rating

</td><td>

Risk rating as determined by the risk assessment performed on the policy exception.If you had selected **Select risk rating** option in the **Method** field, then you can select a value from the list. If you select **Take risk assessment** option in the **Method** field, then this field is auto-populated with the response provided in risk assessment.

</td></tr><tr><td>

Override

</td><td>

Option to override **Risk rating** that was auto-populated based on the responses provided for the risk assessment. This field appears if the **Method** is **Take risk assessment** option.

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

Risk mitigation plan for this policy exception.

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
</table>    **Note:** In versions prior to Version 10.1, the **Risk assessment** related list was called **Business Impact Analysis** and required that the GRC: Risk Management application be activated. Starting in Version 10.1, the dependency on Risk Management has been removed and the associated field names have changed.

    **Approved extensions**, **Remaining extensions**, **Date approved**, **Extension date**, **Extension reason**, **Original valid to** fields appear only when you’ve requested an extension on the policy exception and has been approved by the approver.

    With regard to the m2m association of an issue with policy exceptions, there are certain considerations you must know about the values populating in the **Issue** field, **Control objective** field, and in the Impacted control tab:

    1.  If you select an issue in the **Source type** field, then the **Issue** reference field lists issues that have one or more active controls associated with them. Active controls are the ones in Attest, Review, or Monitor states and not in Draft or Retired states. You can navigate to the Impacted controls tab to view the controls associated to the issue.
    2.  If the issue is linked to only one control objective, then that linked control objective is populated in the **Control objective** reference field. If the issue is linked to more than one control objective, then no value is populated in the **Control objective** field. Click the **Control objective** reference field to select a control objective.
    3.  If you didn’t select an issue in the **Issue** field, but a control objective is populated in the **Control objective** reference field, then the Issue reference field will list only those issues that are linked to this control objective.
    4.  As soon as you add an issue in the **Issue** field, then all the controls linked to the issue are added in the Impacted controls tab. However, when you select a control objective in the **Control objective** reference field, then all the controls listed in the Impacted controls tab are replaced with only those controls that are linked to the selected control objective and the issue. Controls can be in any state but not in Draft or Retired state.
    5.  An impacted control linked to one issue of a policy exception will not be listed for you to add in another policy exception because that control is already listed in the Impacted control tab of the first policy exception. If you add more controls to the issue later, and when you link the issue to the second policy exception, then all the newly added controls will be added as impacted controls but not the one that was already added as an impacted control of the first policy exception.
    6.  Previously, an issue-based exception required a linked policy or control objective for additional approvals. Now, it requires any one of the following: a linked policy, control objective, or control. If a control is used, it must be linked to the policy exception itself, not just to the issue.
4.  Save the policy exception.

    The Policy exception is in **New** state.

5.  Click the **Request approval** button.

    If verification rules are configured, then verification approvals are triggered. After the verification approvals are approved, the policy exception moves to Analyse state.

    After the policy exception is approved and if the **Valid to** date is reached, then the state moves to **Closed** and the substate moves to **Expired**.

    You can also withdraw the policy exception anytime before the policy exception is approved, if it's no longer required, right from the **New** state.

6.  To withdraw the policy exception, click the **Cancel Request** button.

    The state moves to **Closed** and the substate to **Canceled**.


## What to do next

As a requester you can request extensions to a policy exception that is in the Approved state more than once. Configure the **Number of extensions allowed for a policy exception** property to request policy extension multiple times.

To set up the property, see [Configure the number of extensions allowed for a policy exception](../../grc-policy-and-compliance/task/request-policy-extension-platform.md#substeps_pol-ext-multi).

To request extension, click the **Request extension** button and [enter the details in the Request extension pop-up](../../grc-policy-and-compliance/task/request-policy-extension-platform.md#request-exten-pol-excep).

Click **Request**. You can see the policy extension details in the [Schedule tab of the Policy exception form](request-policy-exception-ws.md#pol-ext-det-ws) after the requester has requested for an extension and the policy extension has been approved by the approver.

