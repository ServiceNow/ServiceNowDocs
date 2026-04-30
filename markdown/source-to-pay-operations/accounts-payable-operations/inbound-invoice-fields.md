---
title: Inbound Invoice Fields
description: The Inbound invoice table is the source table from where you import the invoice required fields to successfully create an invoice through the integration framework.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create New Invoice form, Create New Invoice Line form, Accounts Payable Operations reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Inbound Invoice Fields

The Inbound invoice table is the source table from where you import the invoice required fields to successfully create an invoice through the integration framework.

<table id="table_c3s_fj1_dwb"><thead><tr><th>

Column

</th><th>

Description

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

Invoice Type \(Mandatory\)

</td><td>

Details about the invoice.

</td><td>

Choice Examples: invoice/non\_ po\_invoice, debit \_memo, credit\_memo

</td></tr><tr><td>

Supplier invoice number

</td><td>

The invoice number of the supplier and ERP source and ERP invoice number

</td><td>

String

</td></tr><tr><td>

Business owner

</td><td>

email of business the owner who owns the application from the business side

</td><td>

String

</td></tr><tr><td>

Supplier \(Mandatory\)

</td><td>

Name of the ERP supplier code

</td><td>

String

</td></tr><tr><td>

Purchase order

</td><td>

Binding contract between a buyer and a supplier that authorizes a purchasing transaction. Derived from ERP source and supplier

</td><td>

String

</td></tr><tr><td>

Invoice date \(Mandatory\)

</td><td>

The date on which the invoice is created.

</td><td>

String \(yyyy-mm-dd\)

</td></tr><tr><td>

Payment terms

</td><td>

Conditions applied on the payment term.

</td><td>

String

</td></tr><tr><td>

Legal entity

</td><td>

Stores Legal entity's ERP company code

</td><td>

String

</td></tr><tr><td>

Tax amount

</td><td>

Tax rate applied on the invoice amount

</td><td>

Decimal number

</td></tr><tr><td>

Shipping amount

</td><td>

Shipping charges incurred for the invoice

</td><td>

Decimal number

</td></tr><tr><td>

Subtotal \(Mandatory\)

</td><td>

Total amount of money to be paid to the supplier excluding tax and shipping charges.

</td><td>

Decimal number. Example 12345.65

</td></tr><tr><td>

Other charges

</td><td>

Additional charges incurred on the invoice

</td><td>

Decimal number

</td></tr><tr><td>

Discounts

</td><td>

Reduction on the total amount incurred on the invoice

</td><td>

Decimal number

</td></tr><tr><td>

Currency

</td><td>

Currency code standard of amount exchanged. ISO 4217 currency code \(USD, GBP, INR, etc\)

</td><td>

String

</td></tr><tr><td>

External invoice number \(Mandatory\)

</td><td>

Invoice number originated from a third party application.

</td><td>

String

</td></tr><tr><td>

ERP source \(Mandatory\)

</td><td>

The available ERP

</td><td>

String

</td></tr><tr><td>

Status

</td><td>

Current state of the invoice is Draft

</td><td>

String

</td></tr><tr><td>

External invoice source \(Mandatory\)

</td><td>

Name of the third party application associated with the invoice.

</td><td>

String

</td></tr></tbody>
</table>-   **[Inbound invoice line fields](inbound-invoice-line-fields.md)**  
The Inbound invoice line table is the source table from where you import the invoice line required fields to successfully create an invoice through the integration framework.
-   **[Inbound invoice payment fields](inbound-invoice-payment-fields.md)**  
The Inbound invoice payment details needed for a supplier to complete the transaction.

**Parent Topic:**[Create New Invoice form](create-new-invoice-form.md)

