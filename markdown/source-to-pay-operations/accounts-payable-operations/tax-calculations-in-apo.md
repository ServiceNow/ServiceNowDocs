---
title: Tax calculations
description: Calculate the final tax for an invoice based on the tax type and the tax tolerance variance.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Tax calculations

Calculate the final tax for an invoice based on the tax type and the tax tolerance variance.

The Accounts Payable Operations application enables the validation of supplier-provided taxes for enhanced tax compliance and improved operational effectiveness.

Tax specialists create tax types of either indirect tax or withholding tax. One or more tax lines are added to invoice lines. Based on the tax type, the supplier tax is calculated against the invoice line amount. If the supplier tax amount is greater than the system tax amount, an overtax amount variance is calculated. If the supplier tax is less than the system tax amount, an under-tax variance is calculated. You can choose to accept the system tax or the supplier tax,which will determine the final tax that is calculated and displayed on the invoice tax line and invoice header.

For example, for an invoice line amount of $1000, add a tax line of the indirect tax type with a supplier tax of $100. The final tax amount would be calculated as the sum of $1000 and $100, for a total of $1100. If you select the withholding tax type, the final tax amount is calculated as the difference between the invoice line amount of $1000 and the supplier tax of $100, for a total of $900.

-   **[Create tax codes to be added in an invoice](../task/create-tax-code.md)**  
Create tax codes to be added in an invoice.
-   **[Create tax types to be used in an invoice](../task/create-tax-types.md)**  
Create tax types to be added in the invoice.

**Parent Topic:**[Create an invoice manually](../task/create-invoice.md)

