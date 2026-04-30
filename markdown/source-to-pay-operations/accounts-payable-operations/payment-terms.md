---
title: Payment terms
description: Specify the terms and conditions that apply to customers while paying for an invoice. These are usually imposed by suppliers during the purchase.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Master data table for Accounts Payable Operations, Accounts Payable Operations reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Payment terms

Specify the terms and conditions that apply to customers while paying for an invoice. These are usually imposed by suppliers during the purchase.

## sn\_shop\_payment\_term

You can view the payment terms referencing an invoice.

<table id="table_q5d_bk2_1yb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

String

</td><td>

The name or code of the payment term. Example: Net 060.

</td></tr><tr><td>

Type

</td><td>

Choice list

</td><td>

The values are:-   Due upon receipt
-   Fixed
-   Net

</td></tr><tr><td>

Short description

</td><td>

String

</td><td>

A short explanation of the payment term. Example: 2%14, Net 60.

</td></tr><tr><td>

Net days to pay

</td><td>

String

</td><td>

Applicable only to type “Net”.

</td></tr><tr><td>

Discount percentage

</td><td>

String

</td><td>

Applicable only to type “Net”.

</td></tr><tr><td>

Discount days

</td><td>

String

</td><td>

Applicable only to type “Net”.

</td></tr></tbody>
</table>**Parent Topic:**[Master data table for Accounts Payable Operations](master-data-table-apo.md)

