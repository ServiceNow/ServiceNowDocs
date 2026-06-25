---
title: Approval Rule form
description: Use the Approval Rule form when creating or configuring an approval rule to generate and route invoice or purchase order approvals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/new-approval-rule-form.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [APO, Accounts Payable Operations, invoice automation, AP automation, finance automation]
breadcrumb: [Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Approval Rule form

Use the Approval Rule form when creating or configuring an approval rule to generate and route invoice or purchase order approvals.

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

Depending on the rule type that you select, the associated fields appear. For more information, see [Approval rule types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-approval-rule-types.md).

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
</table>**Parent Topic:**[Accounts Payable Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/acc-pay-reference.md)

**Related topics**  


[Accounts Payable Operations properties]()

[Create New Invoice Line form]()

[Create invoice cost allocation form]()

[Outbound cost allocation staging table]()

[Distribution set form]()

[Create New Invoice case form]()

[Create New Invoice task form]()

[Invoice processing case form]()

[Tax lines]()

[Invoice exception form]()

[Request Help form]()

[Data required for invoice processing]()

[Invoice exception definition form]()

[Approval Plan form]()

[Accounts Payable Operations glossary]()

