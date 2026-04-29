---
title: Define policy exception approval rules
description: Approval rules define the criteria \(risk rating, policy or control objective\) that is used for sending approval requests for an exception. Rules can be configured for an application and you can identify multiple levels of approvers, as needed.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Allow policy exception requests, Enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Define policy exception approval rules

Approval rules define the criteria \(risk rating, policy or control objective\) that is used for sending approval requests for an exception. Rules can be configured for an application and you can identify multiple levels of approvers, as needed.

## Before you begin

Role required: sn\_compliance.manager

## About this task

You can configure approvals to be sent out automatically or manually after review.

**Note:** When policy exceptions are created from upstream applications \(from Vulnerability Response for example\), the policy exception must have impacted controls present before you can request approval.

For policy exceptions created using Policy and Compliance Management, exceptions can be requested for a policy without impacted controls being present, even if both policies and control objectives are added to the exception form. However, for policy exceptions created for control objectives alone, impacted controls must be present before you can request approval.

You can also use the GRC Approval Configurator to configure policy exception rules. For more information, see [Define policy exception and extension rules](define-policy-exception-verification-rules.md).

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policy Exceptions** &gt; **Approval Rule**.

2.  Click **New**.

    ![Approval rules](../image/approval-rules.png)

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Type|Defaults to Approval Rule.|
    |Name|Enter a name for this approval configuration.|
    |Short description|Provide a brief description of the purpose of the configuration.|
    |Source application|Select the application for that applies to this approval rule. Only applications that have been previously added to the Integration Registry are listed.|
    |Active|If this is selected, this approval rule is active.|
    |Risk rating|The risk rating is determined by running a risk assessment on the policy exception.|
    |Policy|Select the policy against which this policy exception is being applied.|
    |Control objective|Select the control objective that references the selected policy.|
    |Auto-trigger approvals|Select this check box to automatically trigger all approvals after the review is completed. If you do not select it, the compliance manager can manually trigger the approvals defined by this rule.|
    |Order|Order defines the precedence of triggering this rule as compared to another rule that is applicable to the exception and defined with similar criteria.|

4.  Click **Update**.

    The Approver Levels related list appears. This related list allows you to define multiple approver levels for a rule. One or more users, or a group of users can be selected as approvers for each level. Approvers must be assigned the survey\_reader role. You can make it mandatory for all selected users to approve the exception or optionally allow a single user to approve on behalf of all approvers.

    ![Approver levels](../image/approval-levels.png)

5.  Click **New**.

    ![New approval level](../image/approver-level-new.png)

6.  On the form, fill in the fields.

<table id="table_xlt_4sg_rlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for this approval level.

</td></tr><tr><td>

Description

</td><td>

Provide a brief description of the approval level.

</td></tr><tr><td>

Required approval

</td><td>

Select **One approval required** to allow a single user to approve on behalf of all approvers.Select **All users must approve** to make it mandatory that all designated users approve the selection.

</td></tr><tr><td>

Users

</td><td>

Select one or more users to act as policy exception approvers.

</td></tr><tr><td>

Groups

</td><td>

Select one or more groups to act as policy exception approvers.**Note:** Users who belong to the group must have GRC business user \(sn\_grc.business\_user\) role.

</td></tr><tr><td>

Order

</td><td>

Select the order to determine the sequence of levels used with respect to other levels \(that is, order 1 is displayed first\).

</td></tr></tbody>
</table>7.  Click **Submit**.

    If you selected the **Auto-trigger approvals** check box, the designated approvers are notified that their approvals are required. Alternatively, the approvers are notified when the compliance manager clicks the **Send for Approval** button.


**Parent Topic:**[Allow policy exception requests from other applications](../concept/allow-other-app-policy-except.md)

