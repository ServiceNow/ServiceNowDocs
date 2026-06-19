---
title: Inbound Invoice Fields
description: Field descriptions, data types, and mandatory fields for the Inbound Invoice table used to import invoice data through the integration framework to create invoices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/inbound-invoice-fields.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, inbound integration]
breadcrumb: [Create New Invoice form, Create New Invoice Line form, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Inbound Invoice Fields

Field descriptions, data types, and mandatory fields for the Inbound Invoice table used to import invoice data through the integration framework to create invoices.

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
</table>-   **[Inbound invoice line fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/inbound-invoice-line-fields.md)**  
Field definitions and data types for the Inbound Invoice Line \[u\_inbound\_invoice\_line\] table used to map invoice line data for import through the integration framework.
-   **[Inbound invoice payment fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/inbound-invoice-payment-fields.md)**  
Field descriptions and data types for inbound invoice payment records used to import supplier invoice payment data into Accounts Payable Operations.

**Parent Topic:**[Create New Invoice form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-new-invoice-form.md)

