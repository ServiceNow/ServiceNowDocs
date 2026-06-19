---
title: Inbound invoice payment fields
description: Field descriptions and data types for inbound invoice payment records used to import supplier invoice payment data into Accounts Payable Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/inbound-invoice-payment-fields.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, supplier, inbound integration]
breadcrumb: [Inbound Invoice Fields, Create New Invoice form, Create New Invoice Line form, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Inbound invoice payment fields

Field descriptions and data types for inbound invoice payment records used to import supplier invoice payment data into Accounts Payable Operations.

|Column|Description|Data type|
|------|-----------|---------|
|Payment amount|Payment details about the invoice|Decimal number|
|ERP invoice number|The ERP invoice number of the supplier invoice|String|
|Payment date|The date on which the invoice payment was completed|String \(yyy-mm-dd\)|
|Payment method|Mode of payment|Choice Example: bank\_transfer/ cash\_payment/ cheque /credit\_card /debit\_card /wire\_transfer|
|Payment reference ID|A unique ID to track the payment details|Alpha numeric|
|Remit to city|The city to which the payment is made|String|
|Remit to country|The country to which the payment is made in ISO 3166 format. Example:US|String|
|Remit to state/province|The state or province to which the payment is made|String|
|Remit to street|The street address to which the payment is made|String|
|Remit to zip/postal code|The zip or postal code address to which the payment is made|String|
|Scheduled payment date|The date at which the payment will be made|String \(yyyy-mm-dd\)|
|ERP supplier code|Integer ERP code of the supplier in the ERP system|Combination of ERP supplier code and ERP source|
|ERP Source|The available ERP|String|
|Currency|Standard of amount exchangedin Currency Code ISO 4217 format \(USD, GBP, INR, etc\)|String|

**Parent Topic:**[Inbound Invoice Fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/inbound-invoice-fields.md)

