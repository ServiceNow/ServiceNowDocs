---
title: Inbound invoice line fields
description: The Inbound invoice line table is the source table from where you import the invoice line required fields to successfully create an invoice through the integration framework.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Inbound Invoice Fields, Create New Invoice form, Create New Invoice Line form, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Inbound invoice line fields

The Inbound invoice line table is the source table from where you import the invoice line required fields to successfully create an invoice through the integration framework.

<table id="table_c3s_fj1_dwb"><thead><tr><th>

Column

</th><th>

Description

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

External invoice source \(required\)

</td><td>

Name of the third party application associated with the invoice. Derive logic from external invoice number.

</td><td>

String

</td></tr><tr><td>

Line description \(required\)

</td><td>

Description of the invoice line.

</td><td>

String

</td></tr><tr><td>

Purchase order line

</td><td>

Information of the individual lines under a purchase order and ERP PO line number.

</td><td>

String

</td></tr><tr><td>

Line quantity \(required\)

</td><td>

The number of items that have been invoiced

</td><td>

Decimal number

</td></tr><tr><td>

Line unit price \(required\)

</td><td>

Unit price of the line item in the invoice.

</td><td>

Decimal number

</td></tr><tr><td>

Payment terms

</td><td>

Conditions applied on the payment term.

</td><td>

String Example \(Net 30\)

</td></tr><tr><td>

Legal entity

</td><td>

Stores legal entity's ERP company code.

</td><td>

String

</td></tr><tr><td>

Tax amount

</td><td>

Tax rate applied on the invoice amount.

</td><td>

Decimal number

</td></tr><tr><td>

Subtotal \(required\)

</td><td>

Total amount of money to be paid to the supplier excluding tax and shipping charges.

</td><td>

Decimal number Example \(12345.65\)

</td></tr><tr><td>

Cost center

</td><td>

Combination of cost center's account number and ERP source.

</td><td>

String

</td></tr><tr><td>

GL accounts

</td><td>

Records the total number of transactions derived from GL account and ERP source.

</td><td>

String

</td></tr><tr><td>

Tax code

</td><td>

Sales tax related to locations where business transactions occur.

</td><td>

String

</td></tr><tr><td>

Currency

</td><td>

Standard Currency Code ISO 4217 \(USD, GBP, INR, etc\)

</td><td>

String

</td></tr><tr><td>

External invoice source

</td><td>

Invoice source number originated from a third party application.

</td><td>

String

</td></tr><tr><td>

ERP source \(required\)

</td><td>

The available ERP source.

</td><td>

String

</td></tr><tr><td>

Status

</td><td>

The current state of the invoice is draft.

</td><td>

String

</td></tr><tr><td>

External invoice source \(required\)

</td><td>

Name of the third party application associated with the invoice.

</td><td>

String

</td></tr></tbody>
</table>**Parent Topic:**[Inbound Invoice Fields](inbound-invoice-fields.md)

