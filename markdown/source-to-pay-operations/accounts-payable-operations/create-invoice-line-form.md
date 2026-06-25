---
title: Create New Invoice Line form
description: Field descriptions for the Create New Invoice Line form used to add invoice line details such as pricing, tax amounts, accounting information, and shipping addresses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/create-invoice-line-form.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [APO, Accounts Payable Operations, invoice automation, invoice management, AP automation]
breadcrumb: [Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Create New Invoice Line form

Field descriptions for the Create New Invoice Line form used to add invoice line details such as pricing, tax amounts, accounting information, and shipping addresses.

|Field|Description|
|-----|-----------|
|Invoice Line|
|Number|An auto-generated number that uniquely identifies the invoice line.|
|Invoice|Invoice for which you are creating the invoice line.|
|Status|Status of the invoice line.|
|ERP line number|Unique number generated within the ERP system for the invoice line.|
|Line description|A description of the goods or services represented by the invoice line item.|
|Summary Details|
|Purchase order line|Purchase order line item in the purchase order.|
|Invoice line quantity|The number of items that have been invoiced.|
|Line unit price|Unit price of the line item in the invoice.|
|Subtotal|The total amount for the invoice line without tax and shipping charges.|
|Tax amount|Tax amount for the invoice line item.|
|Line amount invoiced|Total amount for the invoice line item.|
|Accounting Details|
|Ledger account|The account used to generate the invoice.|
|Cost center|The cost center for which the invoice is generated.|
|Tax code|The SWIFT or BIC code for international wire transfers to the supplier's bank.|
|Ship to street|The street address to which the items on the purchase order should be shipped.|
|Ship to country|The country to which the items on the purchase order should be shipped.|
|Ship to city|The city to which the items on the purchase order should be shipped.|
|Ship to zip/postal code|The zip code to which the items on the purchase order should be shipped.|
|Ship to state/province|The state to which the items on the purchase order should be shipped.|
|Tax Details|
|Supplier tax|The total tax amount charged on the invoice line item by the supplier.|
|System tax|The total tax amount for the invoice line item calculated by the third-party tax calculation engine.|
|Final tax|The total tax amount paid for this invoice line item.|
|Unit|The unit or rate in which this product is billed by the supplier.|
|Supplier part number|The part number of the supplier product.|

-   **[Create New Invoice form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-new-invoice-form.md)**  
Field descriptions for the Create New Invoice form, organized by section, for entering invoice details, supplier information, accounting data, and address fields.
-   **[Invoice Line form tabs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-line-form-related-list.md)**  
Tab descriptions for the Invoice Line form, including invoice line details, exceptions, and goods receipts.

**Parent Topic:**[Accounts Payable Operations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/acc-pay-reference.md)

**Related topics**  


[Accounts Payable Operations properties]()

[Create invoice cost allocation form]()

[Outbound cost allocation staging table]()

[Distribution set form]()

[Create New Invoice case form]()

[Create New Invoice task form]()

[Invoice processing case form]()

[Tax lines]()

[Invoice exception form]()

[Request Help form]()

[Data required for invoice processing]()

[Invoice exception definition form]()

[Approval Rule form]()

[Approval Plan form]()

[Accounts Payable Operations glossary]()

