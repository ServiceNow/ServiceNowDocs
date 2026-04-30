---
title: Tolerance Rules and Variances for invoices
description: Setting tolerance rules to determine the permissible amount of variance applied on an invoice's total value enables you to avoid payment delays and make payment processing more efficient.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Tolerance Rules and Variances for invoices

Setting tolerance rules to determine the permissible amount of variance applied on an invoice's total value enables you to avoid payment delays and make payment processing more efficient.

You can customize tolerance rules that compare invoices with defined tolerance percentages and values. If the differential is within the limit, the invoice is considered valid for payment. If it is greater than the tolerance limit, exceptions are raised.

## Tolerance types

Accounts Payable Operations supports the following tolerance types:

-   **Line amount tolerance**: Avoid payment delays by defining the acceptable difference between the expected and actual total amount for specific items or services of the invoice.
-   **Line quantity tolerance**: Ensure easy payment processing by defining the acceptable range between the expected and actual quantities of items or services listed on an invoice. This is a line level of tolerance.
-   **Line unit price tolerance**: Avoid small discrepancies from impacting payment processing and supplier relations by establishing a tolerance range for the difference between the purchase order line unit price and the actual price of an invoice. This is a line level of tolerance.
-   **Overbilling amount tolerance**: Avoid overbilling between an invoice and the corresponding purchase order by setting a tolerance range for the difference between the actual amount value and the expected amount. This is a header level tolerance.
-   **Over tax amount** and **under tax amount** variances: Confirm smooth payment processing by defining an acceptable range between the supplier-provided tax and system-calculated tax amounts that indicates acceptable minor differences within the defined tolerance range.

    **Note:** If the tax amount variance for a tax line is within the tolerance range, then supplier tax amount is copied over to the final tax amount field by default.


-   **[Define a custom invoice tolerance type](../task/define-a-new-tolerance-type-definition.md)**  
Define a custom invoice tolerance type that you can use in an exception definition to make payment processing more efficient.
-   **[Associate invoice tolerance type with invoice exception definition](../task/map-invoice-tolerance-definition-with-tolerance-rule.md)**  
Define a new tolerance type and associate it with an invoice exception definition.
-   **[Define an invoice tolerance rule](../task/define-a-new-tolerance-rule.md)**  
Configure an invoice tolerance rule definition for a tolerance type to be applied to invoices matching the invoice filter's conditions.
-   **[View tolerance form](../task/view-tolerance-form.md)**  
View the invoice processing cases with exceptions in the tolerance form with **Tolerance details** at header level and **Variance details** at line level.

**Parent Topic:**[Using Accounts Payable Invoice Processing](use-ap-invoice-processing.md)

**Related topics**  


[Work with invoices](work-with-invoices.md)

[Invoice processing cases](working-with-ingestion-cases.md)

[Invoice exceptions](work-with-invoice-exceptions.md)

[Invoice approvals](invoice-approvals.md)

[View invoice documents in the Source-to-Pay Workspace](../task/view-invoice-attachment.md)

