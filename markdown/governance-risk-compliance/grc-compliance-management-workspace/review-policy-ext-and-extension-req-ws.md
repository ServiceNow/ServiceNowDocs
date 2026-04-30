---
title: Review the policy exception and extension request using the Compliance Workspace
description: After reviewing a policy exception request using the Compliance Workspace, a compliance manager can accept or reject the request. However, if the compliance manager doesn't have enough information to decide, they can request a risk assessment by the risk manager.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage policy exceptions and extensions using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Review the policy exception and extension request using the Compliance Workspace

After reviewing a policy exception request using the Compliance Workspace, a compliance manager can accept or reject the request. However, if the compliance manager doesn't have enough information to decide, they can request a risk assessment by the risk manager.

## Before you begin

Role required: sn\_compliance.manager

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, click the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Click **All policy exceptions** in the Policy exceptions list.

4.  Click the link to the policy exception record in the **Name** column.

5.  Perform one of the following actions.

<table id="choicetable_qjq_2vw_x1b"><thead><tr><th align="left" id="d261345e109">

Option

</th><th align="left" id="d261345e112">

Action

</th></tr></thead><tbody><tr><td id="d261345e118">

**To view or add impacted controls to the policy exception**

</td><td>

1.  Click the Impacted Controls tab.
2.  Click **Add** or **Add All**.
3.  Choose the controls to associate to the policy exception.


</td></tr><tr><td id="d261345e145">

**To view mitigating controls on the policy exception**

</td><td>

Click the Mitigating Controls tab.

</td></tr><tr><td id="d261345e154">

**To view or add risks to the policy exception**

</td><td>

Click the Risks tab.**Note:** This option is available when Risk Management plugin is also activated.

</td></tr><tr><td id="d261345e166">

**To view or add approvers to the policy exception**

</td><td>

Click the Approvers tab.

</td></tr><tr><td id="d261345e179">

**To request extension**

</td><td>

1.  Click the **Request extension** button in the **Details** tab.
2.  Select a valid date that is later to the **Valid to** date in the **Extension date** field.
3.  Select a reason from the list in the **Extension reason** field.
4.  Enter relevant information, if any, in the **Additional comments** field.
5.  Click the **Request** button.


</td></tr></tbody>
</table>6.  Perform one of the following actions.

<table id="choicetable_rg1_mrb_gqb"><thead><tr><th align="left" id="d261345e237">

Option

</th><th align="left" id="d261345e240">

Action

</th></tr></thead><tbody><tr><td id="d261345e246">

**To request additional information before approvalThis is an approver's task.

**

</td><td>

Select More \(...\) icon and select **Request more information**.An email notification is sent to the requester that the policy exception request was approved and goes into effect.

</td></tr><tr><td id="d261345e262">

**To provide additional information requested by approverThis is a requester's task.

**

</td><td>

After making changes to the policy request, select **Send Information** to provide additional information requested by approver.**Note:** When an approver requests for additional information, the state changes to Analyze and substate to Awaiting requester information.

</td></tr><tr><td id="d261345e278">

**To approve the policy exception**

</td><td>

-   Click **Approve**.

The Approve exception request dialog appears.

-   Review the summary, optionally add additional comments, and select **Confirm**.
 An email notification is sent to the requester that the PER was approved and goes into effect.

</td></tr><tr><td id="d261345e311">

**To reject the policy exception**

</td><td>

-   Click **Reject**.

The Reject exception request dialog appears.

-   Review the summary, add the mandatory additional comments, and select **Confirm**.

If the Additional comments field is empty, you cannot reject the extension request.

 An email notification is sent to the requester that the PER was rejected and the request is closed.

</td></tr><tr><td id="d261345e347">

**To approve the policy extension**

</td><td>

-   Click **Approve Extension**.

The Approve extension request dialog appears.

-   Review the summary, optionally add additional comments, and select **Confirm**.
 An email notification is sent to the requester that the extension request was approved and goes into effect.

</td></tr><tr><td id="d261345e380">

**To reject the policy extension**

</td><td>

-   Click **Reject Extension**.

The Reject extension request dialog appears.

-   Review the summary, add the mandatory additional comments, and select **Confirm**.

If the Additional comments field is empty, you cannot reject the extension request.

 An email notification is sent to the requester that the extension request was rejected and the request is closed.

</td></tr><tr><td id="d261345e415">

**To request a risk assessment on the policy exception**

</td><td>

Click **Request Risk Assessment**.

 An email notification is sent to the risk managers group.

 **Note:** This option is available when Risk Management is also activated.

</td></tr><tr><td id="d261345e439">

**To request business owner approval**

</td><td>

Click **Request Business Owner Approval** .

 An email notification is sent to the business owner.

</td></tr></tbody>
</table>7.  Click **Update**.


