---
title: Review the policy exception and extension request
description: After reviewing a policy exception request, a compliance manager can accept or reject the request. However, if the compliance manager doesn't have enough information decide, they can request a risk assessment by the risk manager.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage policy exceptions and extensions, Classic UI, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Review the policy exception and extension request

After reviewing a policy exception request, a compliance manager can accept or reject the request. However, if the compliance manager doesn't have enough information decide, they can request a risk assessment by the risk manager.

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

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **My Policy Exceptions**.

2.  Select the policy exception.

3.  Perform one of the following actions.

<table id="choicetable_qjq_2vw_x1b"><thead><tr><th align="left" id="d227473e110">

Option

</th><th align="left" id="d227473e113">

Action

</th></tr></thead><tbody><tr><td id="d227473e119">

**To view or add impacted controls to the policy exception**

</td><td>

1.  Select the **Impacted Controls** tab.

**Note:** You can add a single control objective if your **Source type** is **Control objective**. However, if your **Source type** is **Controls**, then you can select multiple controls from different control objectives. For more information, see [Request a policy exception](request-policy-exception.md#source-type-policy-excep).

2.  Select the **Add** or **Add All** buttonto add the manually created controls.
3.  Choose the controls to associate to the policy exception.


</td></tr><tr><td id="d227473e170">

**To view mitigating controls on the policy exception**

</td><td>

Select the Mitigating Controls tab.

</td></tr><tr><td id="d227473e182">

**To view or add risks to the policy exception**

</td><td>

Select the Risks tab.

 **Note:** This option is available when Risk Management plugin is also activated.

</td></tr><tr><td id="d227473e197">

**To view or add approvers to the policy exception**

</td><td>

Select the Details tab.

 **Note:** For approvals, Approver and Risk rating fields are mandatory. Select an approver from the approval group. For example, if the approver group is Compliance Managers, then select one of the managers belonging to the Compliance Managers group.

</td></tr><tr><td id="d227473e216">

**To request extension**

</td><td>

1.  Select the **Request extension** button in the **Details** tab.
2.  Select a valid date that is later to the **Valid to** date in the **Extension date** field.
3.  Select a reason from the list in the **Extension reason** field.
4.  Select the extension reason.
5.  Enter relevant information, in the mandatory **Additional comments** field.
6.  Click the **Request** button.


</td></tr></tbody>
</table>4.  Perform one of the following actions.

<table><thead><tr><th align="left" id="d227473e277">

Option

</th><th align="left" id="d227473e280">

Action

</th></tr></thead><tbody><tr><td id="d227473e286">

**To request additional information before approval**

</td><td>

Select More \(...\) icon and select **Request more information**.

 An email notification is sent to the requester that the policy exception request was approved and goes into effect.

</td></tr><tr><td id="d227473e304">

**To provide additional information requested by approver**

</td><td>

Select **Send Information** To provide additional information requested by approver.**Note:** When an approver requests for additional information, the state changes to Analyze and substate to Awaiting requester information.

</td></tr><tr><td id="d227473e318">

**To approve the policy exception**

</td><td>

Select **Approve**.

 An email notification is sent to the requester that the policy exception request was approved and goes into effect.

</td></tr><tr><td id="d227473e336">

**To reject the policy exception**

</td><td>

Click **Reject**.

 An email notification is sent to the requester that the policy exception was rejected and the request is closed.

</td></tr><tr><td id="d227473e355">

**To approve the policy exception extension**

</td><td>

Select **Approve Extension**.

 An email notification is sent to the requester that the policy exception extension request was approved and goes into effect.

</td></tr><tr><td id="d227473e373">

**To reject the policy extension**

</td><td>

Select **Reject Extension**.

 An email notification is sent to the requester that the extension request was rejected and the request is closed.

</td></tr><tr><td id="d227473e391">

**To request a risk assessment on the policy exception**

</td><td>

Select **Request Risk Assessment**.

 An email notification is sent to the risk managers group.

 **Note:** This option is available when Risk Management is also activated.

</td></tr><tr><td id="d227473e415">

**To request business owner approval**

</td><td>

Select **Request Business Owner Approval** .

 An email notification is sent to the business owner.

</td></tr></tbody>
</table>5.  Click **Update**.


**Parent Topic:**[Manage policy exceptions and extensions](../concept/manage-policy-exceptions.md)

