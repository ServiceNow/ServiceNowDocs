---
title: Create New Invoice Line form
description: Use the Create New Invoice Line form to provide details about an invoice line.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Accounts Payable Operations reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Create New Invoice Line form

Use the Create New Invoice Line form to provide details about an invoice line.

|Field|Description|
|-----|-----------|
|Invoice Line|
|Number|An auto-generated number that uniquely identifies the invoice line.|
|Invoice|Invoice for which you are creating the invoice line.|
|Status|Status of the invoice line.|
|ERP line number|Unique number generated within the ERP system for the invoice line.|
|Line description|Description for the invoice line.|
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
|Tax code|Tax code of the invoice.|
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

-   **[Create New Invoice form](create-new-invoice-form.md)**  
Use the Create New Invoice form to enter the details of the new invoice.
-   **[Invoice Line form tabs](invoice-line-form-related-list.md)**  
The Invoice line form includes tabs that store invoice line information that an Accounts Payable Specialist can use to perform related tasks.
-   **[Create invoice cost allocation form](create-invoice-cost-allocation-form.md)**  
Allocate invoice line cost across multiple cost centers.
-   **[Outbound cost allocation staging table](outbound-cost-allocation-table.md)**  
The outbound cost allocation \[sn\_spend\_intg\_outbound\_invoice\_cost\_allocation\] staging table stores important data about cost allocation information so that an ERP integrator can export this data to a third-party ERP system.

**Parent Topic:**[Accounts Payable Operations reference](acc-pay-reference.md)

**Related topics**  


[Create New Invoice case form](create-new-ap-case-form.md)

[Create New Invoice task form](create-apm-task-form.md)

[Invoice processing case form](invoice-processing-case-form.md)

[Tax lines](create-tax-lines-apo.md)

[Invoice exception form](exception-form-fields.md)

[Master data table for Accounts Payable Operations](master-data-table-apo.md)

[Invoice exception definition form](invoice-exception-definition-form.md)

[Approval Rule form](new-approval-rule-form.md)

[Approval Plan form](approval-plan-form.md)

[Accounts Payable Operations glossary](../concept/apo-glossary.md#)

