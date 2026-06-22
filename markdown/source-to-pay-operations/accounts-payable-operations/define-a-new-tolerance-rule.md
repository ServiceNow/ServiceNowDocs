---
title: Define an invoice tolerance rule
description: Create tolerance rules to define acceptable invoice variances based on tolerance types and invoice filters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/define-a-new-tolerance-rule.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, PO matching, invoice tolerance]
breadcrumb: [Tolerance Rules and Variances for invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Define an invoice tolerance rule

Create tolerance rules to define acceptable invoice variances based on tolerance types and invoice filters.

## Before you begin

Role required: sn\_ap\_apm.invoice\_tolerance\_admin

Enable sn\_ap\_apm.reader role to access invoice filters for tolerance rules.

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **All** &gt; **Tolerance rules**.

    \[Omitted image "apo-tolerance-rules-nav.png"\] Alt text: Navigate to Tolerance rules

2.  On the **Invoice Tolerance rule** list, select **New**.

3.  On the form, fill in the fields.

<table id="choicetable_zfx_wfs_xyb"><thead><tr><th align="left" id="d117579e122">

Field

</th><th align="left" id="d117579e125">

Description

</th></tr></thead><tbody><tr><td id="d117579e131">

**Name**

</td><td>

Name of the tolerance rule.

</td></tr><tr><td id="d117579e140">

**Active**

</td><td>

Option to make the tolerance rule available for invoice processing.

</td></tr><tr><td id="d117579e155">

**Type**

</td><td>

The tolerance type to associate with the tolerance rule.

</td></tr><tr><td id="d117579e179">

**Order**

</td><td>

Defines the priority in which you would like to process the tolerance rule. The lowest order is applied on the invoice. Example: If there are two rules applicable with the orders set as 10 and 20. Rule with order 10 is applied on the invoice.

</td></tr><tr><td id="d117579e189">

**Tolerance value**

</td><td>

Set the permissible variance limit of type numeric and positive numbers only. Example: 200

</td></tr><tr><td id="d117579e201">

**Tolerance percentage**

</td><td>

The permissible variance percentage.

</td></tr><tr><td id="d117579e214">

**Condition type**

</td><td>

Determine whether the value and percentage both need to be met or whether one of the other need to be met to skip an exception.-   **AND** - If both the **Tolerance value** and **Tolerance percentage** values should be met.
-   **OR**-Iif either the **Tolerance value** or **Tolerance percentage** values should be met.


</td></tr><tr><td id="d117579e290">

**Invoice filters**

</td><td>

Filter condition to determine the invoices for which the tolerance rule is applicable. For example: **\[Type\]\[is\]\[PO invoice\] AND \[Supplier\]\]is\]\[X\]**. You can concatenate additional filters by using **New Criteria**.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The tolerance rule is configured for the selected tolerance type.

**Parent Topic:**[Tolerance Rules and Variances for invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/tolerance-rules-and-variance.md)

