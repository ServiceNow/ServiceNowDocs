---
title: Invoice tolerance rule form
description: Create tolerance rules that can be applied on an invoice.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2024-09-11"
reading_time_minutes: 1
breadcrumb: [Invoice processing case form, Accounts Payable Operations reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice tolerance rule form

Create tolerance rules that can be applied on an invoice.

## Invoice tolerance rule

The following table displays the fields in the invoice tolerance rule form.

<table id="table_tkd_trp_rcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the tolerance rule.

</td></tr><tr><td>

Active

</td><td>

Option to make the tolerance rule to be available for invoice processing.

</td></tr><tr><td>

Type

</td><td>

The tolerance type is associated with the tolerance rule.

</td></tr><tr><td>

Order

</td><td>

Priority in which you would like to process the tolerance rule. The lowest order is applied on the invoice. Example: If there are 2 rules applicable with the orders set as 10 and 20. Rule with order 10 is applied on the invoice.

</td></tr><tr><td>

Tolerance value

</td><td>

The permissible variance limit of type numeric and positive numbers only. Example: 200

</td></tr><tr><td>

Tolerance percentage

</td><td>

The permissible variance percentage.

</td></tr><tr><td>

Condition type

</td><td>

Determine whether the value and percentage both need to be met or whether one of the other needs to be met to skip an exception. Determine whether the value and percentage both need to be met or whether one of the other needs to be met to skip an exception.-   **AND**- If both the **Tolerance value** and **Tolerance percentage** values should be met.
-   **OR**-If either the **Tolerance value** or Tolerance percentage values should be met.

</td></tr><tr><td>

Invoice filters

</td><td>

Filter condition to determine the invoices for which the tolerance rule is applicable. For example: **\[Type\]\[is\]\[PO invoice\] AND \[Supplier\]\]is\]\[X\]**. You can concatenate additional filters by using **New Criteria**.

</td></tr></tbody>
</table>**Parent Topic:**[Invoice processing case form](invoice-processing-case-form.md)

