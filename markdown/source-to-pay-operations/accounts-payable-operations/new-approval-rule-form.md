---
title: Approval Rule form
description: Use the Approval Rule form to provide details about the new approval rule.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Approval Rule form

Use the Approval Rule form to provide details about the new approval rule.

<table id="table_lsd_kd5_4wb"><thead><tr><th>

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

The name you assign to the approval rule.

</td></tr><tr><td>

Active

</td><td>

Option to decide if this rule is used to generate invoice approvals.

</td></tr><tr><td>

Approving object

</td><td>

Object you’re seeking approval for. The following options are available:-   **Invoice**
-   **Purchase Order**

To create an approval rule for an invoice, select **Invoice**.

</td></tr><tr><td>

Approving line

</td><td>

Approving object line that you're seeking approval for. For Invoice approving object, the approving line is defaulted to Invoice Line.

</td></tr><tr><td>

Approval rule type

</td><td>

The type of approval rule that determines how approval plans are generated and routed when conditions are met. The following options are available:-   Dynamic Users or Groups
-   Managerial Job Code Hierarchy
-   Managerial Hierarchy
-   Specified Users or Groups

Depending on the rule type that you select, the associated fields appear. For more information, see [Approval rule types](invoice-approval-rule-types.md).

</td></tr><tr><td>

Base approvals on

</td><td>

Invoice fields that you want to base your approvals on. Select the invoice field and move it from Available to Selected.

</td></tr><tr><td>

Allow automatic approval

</td><td>

Option to allow automatic approval of an invoice if the requester \(invoice business owner\) is the only approver.

</td></tr><tr><td>

Approval trigger conditions

</td><td>

Conditions based on the approving object that determine the conditions under which an approval plan is created.

</td></tr></tbody>
</table>**Parent Topic:**[Accounts Payable Operations reference](acc-pay-reference.md)

**Related topics**  


[Accounts Payable Operations properties](acc-pay-properties.md)

[Create New Invoice Line form](create-invoice-line-form.md)

[Create invoice cost allocation form](create-invoice-cost-allocation-form.md)

[Outbound cost allocation staging table](outbound-cost-allocation-table.md)

[Distribution set form](distribution-set-form.md)

[Create New Invoice case form](create-new-ap-case-form.md)

[Create New Invoice task form](create-apm-task-form.md)

[Invoice processing case form](invoice-processing-case-form.md)

[Tax lines](create-tax-lines-apo.md)

[Invoice exception form](exception-form-fields.md)

[Request Help form](ur-request-help-form.md)

[Master data table for Accounts Payable Operations](master-data-table-apo.md)

[Invoice exception definition form](invoice-exception-definition-form.md)

[Approval Plan form](approval-plan-form.md)

