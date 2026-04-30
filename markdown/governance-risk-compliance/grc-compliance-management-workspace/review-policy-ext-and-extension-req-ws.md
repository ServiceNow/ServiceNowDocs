---
title: Review the policy exception and extension request using the Compliance Workspace
description: After reviewing a policy exception request using the Compliance Workspace, a compliance manager can accept or reject the request. However, if the compliance manager doesn't have enough information to decide, they can request a risk assessment by the risk manager.
locale: en-US
release: zurich
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage policy exceptions and extensions, Use, GRC Compliance Workspace, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Review the policy exception and extension request using the Compliance Workspace

After reviewing a policy exception request using the Compliance Workspace, a compliance manager can accept or reject the request. However, if the compliance manager doesn't have enough information to decide, they can request a risk assessment by the risk manager.

## Before you begin

Role required:

1.  For Requester:
    1.  sn\_grc.business\_user
    2.  sn\_grc.business\_user\_lite
    3.  sn\_compliance.policy\_exception\_employee\_user
2.  For Approver:
    1.  sn\_compliance.manager \(sn\_compliance\_ws.corporate\_compliance\_manager\)
    2.  sn\_compliance.policy\_manager

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, click the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Select **All policy exceptions** in the Policy exceptions list.

4.  Select the link to the policy exception record in the **Name** column.

5.  Perform one of the following actions.

<table id="choicetable_qjq_2vw_x1b"><thead><tr><th align="left" id="d292557e142">

Option

</th><th align="left" id="d292557e145">

Action

</th></tr></thead><tbody><tr><td id="d292557e151">

**To view or add impacted controls to the policy exception**

</td><td>

1.  Click the Impacted Controls tab.
2.  Click **Add** or **Add All**.
3.  Choose the controls to associate to the policy exception.


</td></tr><tr><td id="d292557e178">

**To view mitigating controls on the policy exception**

</td><td>

Click the Mitigating Controls tab.

</td></tr><tr><td id="d292557e187">

**To view or add risks to the policy exception**

</td><td>

Click the Risks tab.**Note:** This option is available when Risk Management plugin is also activated.

</td></tr><tr><td id="d292557e199">

**To view or add approvers to the policy exception**

</td><td>

Click the Approvers tab.

</td></tr><tr><td id="d292557e212">

**To request extension**

</td><td>

1.  Select the **Request extension** button in the **Details** tab.
2.  Select a valid date that is later to the **Valid to** date in the **Extension date** field.
3.  Select a reason from the list in the **Extension reason** field.
4.  Select the extension reason.
5.  Enter relevant information, in the mandatory **Additional comments** field.
6.  Click the **Request** button.


</td></tr></tbody>
</table>6.  Perform one of the following actions.

<table id="choicetable_rg1_mrb_gqb"><thead><tr><th align="left" id="d292557e274">

Option

</th><th align="left" id="d292557e277">

Action

</th></tr></thead><tbody><tr><td id="d292557e283">

**To request additional information before approval\(This is an approver's task.\)

**

</td><td>

Select More \(...\) icon and select **Request more information**.

 An email notification is sent to the requester that the policy exception request was approved and goes into effect.

</td></tr><tr><td id="d292557e303">

**To provide additional information requested by approver\(This is a requester's task.\)

**

</td><td>

After making changes to the policy request, select **Send Information** to provide additional information requested by approver.**Note:** When an approver requests for additional information, the state changes to Analyze and substate to Awaiting requester information.

</td></tr><tr><td id="d292557e319">

**To approve the policy exception**

</td><td>

1.  Select **Approve**.

The Approve exception request dialog appears.

2.  Review the summary, optionally add additional comments, and select **Confirm**.

To proceed with approval, both the Approver and Risk Rating fields must not be empty.

 An email notification is sent to the requester that the PER was approved and goes into effect.

</td></tr><tr><td id="d292557e350">

**To reject the policy exception**

</td><td>

1.  Select **Reject**.

The Reject exception request dialog appears.

2.  Review the summary, add the mandatory additional comments, and select **Confirm**.

If the Additional comments field is empty, you cannot reject the exception request.

 An email notification is sent to the requester that the PER was rejected and the request is closed.

</td></tr><tr><td id="d292557e382">

**To approve the policy extension**

</td><td>

1.  Select **Approve extension**.

The Approve extension request dialog appears.

2.  Review the summary, optionally add additional comments, and select **Confirm**.
 An email notification is sent to the requester that the extension request was approved and goes into effect.

</td></tr><tr><td id="d292557e411">

**To reject the policy extension**

</td><td>

1.  Select **Reject extension**.

The Reject extension request dialog appears.

2.  Review the summary, add the mandatory additional comments, and select **Confirm**.

If the Additional comments field is empty, you cannot reject the extension request.

 An email notification is sent to the requester that the extension request was rejected and the request is closed.

</td></tr><tr><td id="d292557e442">

**To request a risk assessment on the policy exception**

</td><td>

Select **Request Risk Assessment**.

 An email notification is sent to the risk managers group.

 **Note:** This option is available when Risk Management is also activated.

</td></tr><tr><td id="d292557e466">

**To request business owner approval**

</td><td>

Select **Request Business Owner Approval**.

 An email notification is sent to the business owner.

</td></tr></tbody>
</table>7.  Click **Update**.


