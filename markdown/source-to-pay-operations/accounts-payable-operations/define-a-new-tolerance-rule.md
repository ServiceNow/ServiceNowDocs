---
title: Define an invoice tolerance rule
description: Configure an invoice tolerance rule definition for a tolerance type to be applied to invoices matching the invoice filter's conditions.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Tolerance Rules and Variances for invoices, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Define an invoice tolerance rule

Configure an invoice tolerance rule definition for a tolerance type to be applied to invoices matching the invoice filter's conditions.

## Before you begin

Role required: sn\_ap\_apm.invoice\_tolerance\_admin

Enable sn\_ap\_apm.reader role to access invoice filters for tolerance rules.

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Tolerance rules**.

2.  On the **Invoice Tolerance rule** list, select **New**.

3.  On the form, fill in the fields.

<table id="choicetable_zfx_wfs_xyb"><thead><tr><th align="left" id="d145295e95">

Field

</th><th align="left" id="d145295e98">

Description

</th></tr></thead><tbody><tr><td id="d145295e104">

**Name**

</td><td>

Name of the tolerance rule.

</td></tr><tr><td id="d145295e113">

**Active**

</td><td>

Option to make the tolerance rule to be available for invoice processing.

</td></tr><tr><td id="d145295e122">

**Type**

</td><td>

The tolerance type is associated with the tolerance rule.

</td></tr><tr><td id="d145295e138">

**Order**

</td><td>

Defines the priority in which you would like to process the tolerance rule. The lowest order is applied on the invoice. Example: If there are two rules applicable with the orders set as 10 and 20. Rule with order 10 is applied on the invoice.

</td></tr><tr><td id="d145295e147">

**Tolerance value**

</td><td>

Set the permissible variance limit of type numeric and positive numbers only. Example: 200

</td></tr><tr><td id="d145295e162">

**Tolerance percentage**

</td><td>

The permissible variance percentage.

</td></tr><tr><td id="d145295e171">

**Condition type**

</td><td>

Determine whether the value and percentage both need to be met or whether one of the other needs to be met to skip an exception.-   **AND**- If both the **Tolerance value** and **Tolerance percentage** values should be met.
-   **OR**-If either the **Tolerance value** or Tolerance percentage values should be met.


</td></tr><tr><td id="d145295e202">

**Invoice filters**

</td><td>

Filter condition to determine the invoices for which the tolerance rule is applicable. For example: **\[Type\]\[is\]\[PO invoice\] AND \[Supplier\]\]is\]\[X\]**. You can concatenate additional filters by using **New Criteria**.

</td></tr></tbody>
</table>4.  Select **Submit**.

    The tolerance rule is created and added to the Invoice tolerance rules list. You can apply the tolerance rule to an invoice.


**Parent Topic:**[Tolerance Rules and Variances for invoices](../concept/tolerance-rules-and-variance.md)

