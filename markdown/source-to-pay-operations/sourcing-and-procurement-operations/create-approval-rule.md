---
title: Create an approval rule
description: Approve a purchase requisition, purchase order, sourcing request, or invoice, by defining an approval strategy and creating approval rules. This is a one-place configuration that can drive any kind of approval process that your organization may need.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [create approval rule, approval rule, procurement approval process]
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create an approval rule

Approve a purchase requisition, purchase order, sourcing request, or invoice, by defining an approval strategy and creating approval rules. This is a one-place configuration that can drive any kind of approval process that your organization may need.

## Before you begin

To create an approval rule, you must have set up your product catalog \(with the necessary product categories, product models, and supplier products\) and should be able to raise a purchase requisition or sourcing request. For more information on how to set up your product catalog, see [Create a product category](create-product-model-categories.md), [Create a product model](create-product-models.md), and [Add a supplier product](add-supplier-product.md). You should have also set up the sys\_user record appropriately to include relevant details such as job codes, managers.

Role required: sn\_shop.procurement\_administrator

## About this task

You can create an approval rule to determine how approval plans are generated and routed when conditions are met, from the Sourcing and Purchasing Automation module.

![Approval rule.](../image/create_approval_rule.png)

## Procedure

1.  Navigate to **All** &gt; **Sourcing and Purchasing Automation** &gt; **Administration ** &gt; **Approval Rule **.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ptd_d5y_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier for the approval rule.

</td></tr><tr><td>

Name

</td><td>

Name you assign to the approval rule.

</td></tr><tr><td>

Active

</td><td>

Option to decide if this rule is used to generate approvals during the purchase requisition process.

</td></tr><tr><td>

Approving object

</td><td>

Object you’re seeking approval for. The following options are available:-   Invoice
-   Purchase Order
-   Purchase Requisition
-   Sourcing Request
It's defaulted based on the approving object selected. For sourcing request and purchase requisition it’s purchase requisition line, for purchase order it’s purchase order line, and for invoice it’s invoice line.

**Note:** While full approval workflows, including approval engine, state flows, and email notifications, are provided for purchase requisitions and sourcing requests, additional implementation is required in defining state flows and email notifications for purchase order and invoice approval rules.

</td></tr><tr><td>

Approving line

</td><td>

Approving object line you're seeking approval for.

</td></tr><tr><td>

Approval rule type

</td><td>

Type of approval rule that determines how approval plans are generated and routed when conditions are met. The following options are available:

 -   Dynamic Users or Groups
-   Managerial Job Code Hierarchy
-   Managerial Hierarchy
-   Specified Users or Groups
-   Cost Center Managers

**Note:** This option is available only when the approving object is a purchase requisition.

 Depending on the rule type you select, the associated fields appear. For more information on these rules, see [Approval rule types](../reference/approval-rule-types.md).

</td></tr><tr><td>

Base approvals on

</td><td>

Business owner who the approval rule is based on.

</td></tr><tr><td>

Users

</td><td>

Specified users who should receive the approval based on the approval trigger.

</td></tr><tr><td>

Groups

</td><td>

Users in the specified groups who should receive the approval based on the approval trigger.

</td></tr><tr><td>

Approval sequence

</td><td>

Sequence in which the approval rules should be triggered. For more information on this, see [Approval rule grouping and sequencing](../reference/approval-rule-sequencing.md).

</td></tr><tr><td>

Approval required from

</td><td>

Determines the managers who should receive the approval request during the purchase requisition process.

</td></tr><tr><td>

Allow automatic approval

</td><td>

Determines if self-approval is to be enabled. By default, this flag is checked or set to true, enabling the self-approval functionality, where the requester has the approving authority. However, if the flag is cleared or set to false, the requester is included to be an active approver in the approval engine’s generated approval list, thus overriding the default self-approval functionality. The requester now needs to provide an explicit approval decision by completing an approval task.

</td></tr><tr><td>

Purchasing user

</td><td>

User for whom approvals are triggered.

</td></tr><tr><td>

Send approval to purchasing users

</td><td>

Options to send an approval dynamically to a user or group related to the purchasing user.

</td></tr><tr><td>

Authorized job codes

</td><td>

One or more job codes that can automatically approve purchases up to the specified limit.

</td></tr><tr><td>

Approved purchasing limit

</td><td>

Reference currency threshold within which users with the specified job codes can approve purchase requisitions.

</td></tr><tr><td>

Approval routing method

</td><td>

Method of routing the approvals. The options are sequentially and in parallel.

</td></tr><tr><td>

Approval decision method

</td><td>

Method of approving the rule. You can select if all approvers must approve the rule or any approver can approve it.

</td></tr><tr><td>

Approval trigger conditions

</td><td>

Conditions based on the approving object that determine the conditions under which an approval plan is created.The trigger conditions are based on the Approving Object table and enable the user to dot-walk. For example, if the user wants to create trigger conditions from the maximum budget of a sourcing request, they should walk from maximum budget to amount, and then create the conditions.

**Note:** Approvals are individually evaluated for each approving object. For example, creating the same approval for a sourcing request and a purchase requisition results in approvals getting triggered twice. To prevent this, the admin can configure approvals from not getting created in a purchase requisition if it's backed by a sourcing request that isn't empty. This is done from the approval trigger conditions.

</td></tr></tbody>
</table>4.  Select **Submit**.


-   **[Approval rule types](../reference/approval-rule-types.md)**  
Approval rule types determine the methods by which approvals are created during the purchase requisition process.
-   **[Approval rule considerations](../reference/approval-rule-considerations.md)**  
Factors like currency, which includes foreign exchange, reference, and transactional, decide the approval rules to be triggered. Some of the other factors are purchasing limit, line amount, and received lines, among others.
-   **[Approval rule grouping and sequencing](../reference/approval-rule-sequencing.md)**  
As a Procurement Administrator, you can associate approval rules with approval groups and define the sequence to determine when these rules should be triggered. With this association, a set of approval rules within a rule group is triggered in sequence, instead of all of them being evaluated simultaneously.

**Parent Topic:**[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)

