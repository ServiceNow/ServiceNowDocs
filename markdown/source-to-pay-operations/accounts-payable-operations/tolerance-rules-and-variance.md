---
title: Tolerance Rules and Variances for invoices
description: Tolerance rules define the limits set on an invoice to determine the permissible amount of variance that can be applied to an invoice before the invoice total exceeds the tolerance limit.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Tolerance Rules and Variances for invoices

Tolerance rules define the limits set on an invoice to determine the permissible amount of variance that can be applied to an invoice before the invoice total exceeds the tolerance limit.

The exception engine checks whether invoices with exceptions are configured with tolerance rules. You can customize tolerance rules of different types where the variance is compared with defined tolerance percentage and tolerance values. If the tolerance value exceeds the tolerance limit, exceptions are raised.

## Tolerance types

Accounts Payable Operations supports the following tolerance types:

-   Line amount tolerance: Avoid payment delays by defining the acceptable difference between the expected and actual total amount for specific items or services of invoice. If the actual amount exceeds the expected amount but falls within this limit, the invoice is considered valid for payment.
-   Line quantity tolerance: Ensure easy payment processing by defining the acceptable range between the expected and actual quantities of items or services listed on an invoice. If the actual quantity exceeds the purchased quantity but remains within this limit, the invoice is considered valid for payment. This is a line level tolerance.
-   Line unit price tolerance: Prevent small discrepancies from impacting payment processing and supplier relations by establishing a tolerance range for the difference between the purchase order line unit price and the actual price of an invoice. When the actual unit price falls within this specified range, the invoice is ready to be processed for payment. This is a line level tolerance.
-   Overbilling amount tolerance: Defines the maximum allowable amount of overbilling between an invoice and the corresponding purchase order. If the actual amount exceeds the expected amount but falls within this limit, the invoice is considered valid for payment. This is a header level tolerance.
-   Over tax amount and under tax amount variances: Ensure smooth payment processing by defining an acceptable range between the supplier-provided tax and system-calculated tax amounts that allows minor differences within the defined tolerance range. If the supplier-calculated tax exceeds the system-provided tax but remains within the Over tax tolerance limit or the system-calculated tax exceeds the supplier-provided tax but remains within the Under tax tolerance limit, the invoice is considered valid for payment.

    **Note:** If tax amount variance for a tax line is within the tolerance range, then supplier tax amount will be copied over to final tax amount field by default.


-   **[Define an invoice tolerance type](../task/define-a-new-tolerance-type-definition.md)**  
Define an invoice tolerance type that you can use in an exception definition.
-   **[Map invoice tolerance type with invoice exception definition](../task/map-invoice-tolerance-definition-with-tolerance-rule.md)**  
Define a new tolerance type and map them with invoice exception definition of your choice to fulfill a goal.
-   **[Define an invoice tolerance rule](../task/define-a-new-tolerance-rule.md)**  
Configure invoice tolerance rule definition for a tolerance type to be applied to invoices matching the invoice filter's conditions.
-   **[View tolerance form](../task/view-tolerance-form.md)**  
Invoice processing cases with exceptions displays the associated **Tolerance details** at header level and **Variance details** at line level.

**Parent Topic:**[Using Accounts Payable Invoice Processing](use-ap-invoice-processing.md)

**Related topics**  


[Invoice ingestion using Application programming interface \(API\)](invoice-ingestion-using-api.md)

[Rules based engine](rules-based-engine.md)

[Work with invoices](work-with-invoices.md)

[Invoice processing cases](working-with-ingestion-cases.md)

[Invoice exceptions](work-with-invoice-exceptions.md)

[Invoice approvals](invoice-approvals.md)

[View invoice documents in the Source-to-Pay Workspace](../task/view-invoice-attachment.md)

