---
title: Define an invoice tolerance rule
description: Configure invoice tolerance rule definition for a tolerance type to be applied to invoices matching the invoice filter's conditions.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tolerance Rules and Variances for invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Define an invoice tolerance rule

Configure invoice tolerance rule definition for a tolerance type to be applied to invoices matching the invoice filter's conditions.

## Before you begin

Role required: sn\_ap\_apm.invoice\_tolerance\_admin

Enable sn\_ap\_apm.reader role to access invoice filters for tolerance rules.

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **All** &gt; **Tolerance rules**.

    ![Navigate to Tolerance rules](../image/apo-tolerance-rules-nav.png)

2.  On the **Invoice Tolerance rule** list, select **New**.

3.  On the form, fill in the fields.

<table id="choicetable_zfx_wfs_xyb"><thead><tr><th align="left" id="d200188e93">

Field

</th><th align="left" id="d200188e96">

Description

</th></tr></thead><tbody><tr><td id="d200188e102">

**Name**

</td><td>

Name of the tolerance rule.

</td></tr><tr><td id="d200188e111">

**Active**

</td><td>

Option to make the tolerance rule available for invoice processing.

</td></tr><tr><td id="d200188e120">

**Type**

</td><td>

The tolerance type to associate with the tolerance rule.

</td></tr><tr><td id="d200188e129">

**Order**

</td><td>

Defines the priority in which you would like to process the tolerance rule. The lowest order is applied on the invoice. Example: If there are two rules applicable with the orders set as 10 and 20. Rule with order 10 is applied on the invoice.

</td></tr><tr><td id="d200188e139">

**Tolerance value**

</td><td>

Set the permissible variance limit of type numeric and positive numbers only. Example: 200

</td></tr><tr><td id="d200188e148">

**Tolerance percentage**

</td><td>

The permissible variance percentage.

</td></tr><tr><td id="d200188e157">

**Condition type**

</td><td>

Determine whether the value and percentage both need to be met or whether one of the other need to be met to skip an exception.-   **AND** - If both the **Tolerance value** and **Tolerance percentage** values should be met.
-   **OR**-Iif either the **Tolerance value** or **Tolerance percentage** values should be met.


</td></tr><tr><td id="d200188e191">

**Invoice filters**

</td><td>

Filter condition to determine the invoices for which the tolerance rule is applicable. For example: **\[Type\]\[is\]\[PO invoice\] AND \[Supplier\]\]is\]\[X\]**. You can concatenate additional filters by using **New Criteria**.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Tolerance Rules and Variances for invoices](../concept/tolerance-rules-and-variance.md)

