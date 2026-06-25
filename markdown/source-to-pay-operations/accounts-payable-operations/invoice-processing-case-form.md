---
title: Invoice processing case form
description: Field descriptions for the Invoice processing case form, including supplier information, payment terms, accounting codes, and billing addresses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-processing-case-form.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [APO, Accounts Payable Operations, invoice automation, AP automation, invoice processing]
breadcrumb: [Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice processing case form

Field descriptions for the Invoice processing case form, including supplier information, payment terms, accounting codes, and billing addresses.

|Field|Description|
|-----|-----------|
|Invoice Case|
|Type|The type of invoice.|
|Channel|The channel used to send the invoice.|
|Supplier invoice number|The invoice number of the supplier invoice.|
|Supplier tax id|The tax ID of the supplier.|
|Assignment group|Group that you want to assign this case to.|
|Assigned to|Person that you want to assign this case to.|
|Business owner|An individual or group who owns the invoice.|
|Summary details|
|Supplier|Supplier who delivers the product or service.|
|Purchase order|Purchase order associated with this invoice. This field is shown only for invoices of type **PO Invoice**.|
|Payment terms|How and when to make payment for the products and services.|
|Subtotal|The total amount from all the invoice lines without tax and shipping charges.|
|Tax amount|Tax applied on the invoice amount.|
|Shipping|Shipping charges incurred for the invoice.|
|Other charges|Other charges applied on the invoice amount.|
|Discounts|The discount applied on the invoice amount.|
|Amount invoiced \(Transactional currency\)|Total amount to be paid to the supplier including tax and shipping charges. This amount is displayed in transactional currency.|
|Dates|
|Invoice date|Date on which this invoice is created.|
|Due date|Date by when you must make the payment.|
|Accounting|
|Legal entity|The internal legal entity which incurs the cost of this invoice.|
|Default tax code|The tax code levied on the total invoice amount.|
|Default tax jurisdiction code|The tax code jurisdiction to which you must pay the tax.|
|Addresses|
|Remit to street|The street address to which the payment is made.|
|Remit to country|The country to which the payment is made.|
|Remit to city|The city to which the payment is made.|
|Remit to zip/postal code|The zip code to which this payment is made.|
|Remit to state/province|The state to which the payment is made.|
|Bill to street|The street address to which the invoice is sent.|
|Bill to country|The country to which the invoice is sent.|
|Bill to city|The city to which the invoice is sent.|
|Bill to zip/postal code|The zip code to which the invoice is sent.|
|Bill to state/province|The state to which the invoice is sent.|
|Ship to street|The street address to which the items on the purchase order should be shipped.|
|Ship to country|The country to which the items on the purchase order should be shipped.|
|Ship to city|The city to which the items on the purchase order should be shipped.|
|Ship to zip/postal code|The zip code to which the items on the purchase order should be shipped.|
|Ship to state/province|The state to which the items on the purchase order should be shipped.|

-   **[Invoice processing details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-processing-form.md)**  
Field descriptions for the Invoice attributes form stored in the \[sn\_apm\_invoice\_attribute\] table, including invoice processing details such as approval status, exception handling, and matching errors.
-   **[Invoice processing case form tabs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-processing-case-tabs.md)**  
Tab descriptions for the Invoice processing case form, including invoice details, exceptions, approvals, and related processing information.
-   **[ERP Posting error form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/erp-posting-erorr-form.md)**  
Field descriptions for the ERP Posting error form, organized by tab, for updating integration error tasks and resolving ERP posting failures.

**Parent Topic:**[Accounts Payable Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/acc-pay-reference.md)

**Related topics**  


[Accounts Payable Operations properties]()

[Create New Invoice Line form]()

[Create invoice cost allocation form]()

[Outbound cost allocation staging table]()

[Distribution set form]()

[Create New Invoice case form]()

[Create New Invoice task form]()

[Tax lines]()

[Invoice exception form]()

[Request Help form]()

[Data required for invoice processing]()

[Invoice exception definition form]()

[Approval Rule form]()

[Approval Plan form]()

[Accounts Payable Operations glossary]()

