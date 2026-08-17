---
title: Tolerance rules and variances for invoices
description: Tolerance rules define the permissible variance amount on an invoice to determine if the total exceeds tolerance limits and requires exception handling.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/tolerance-rules-and-variance.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [APO, Accounts Payable Operations, invoice management, invoice tolerance, variance threshold]
breadcrumb: [Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Tolerance rules and variances for invoices

Tolerance rules define the permissible variance amount on an invoice to determine if the total exceeds tolerance limits and requires exception handling.

The exception engine checks whether invoices with exceptions are configured with tolerance rules. You can customize tolerance rules of different types where the variance is compared with defined tolerance percentage and tolerance values. If the tolerance value exceeds the tolerance limit, exceptions are raised.

## Tolerance types

Accounts Payable Operations supports the following tolerance types:

-   Line amount tolerance: Avoid payment delays by defining the acceptable difference between the expected and actual total amount for specific items or services of invoice. If the actual amount exceeds the expected amount but falls within this limit, the invoice is considered valid for payment.
-   Line quantity tolerance: Ensure easy payment processing by defining the acceptable range between the expected and actual quantities of items or services listed on an invoice. If the actual quantity exceeds the purchased quantity but remains within this limit, the invoice is considered valid for payment. This is a line level tolerance.
-   Line unit price tolerance: Define an acceptable range between the purchase order line unit price and the actual invoice price. Small discrepancies within this range don't affect payment processing or supplier relations. If the actual unit price falls within this range, the invoice is valid for payment. This is a line level tolerance.
-   Overbilling amount tolerance: Defines the maximum allowable amount of overbilling between an invoice and the corresponding purchase order. If the actual amount exceeds the expected amount but falls within this limit, the invoice is considered valid for payment. This is a header level tolerance.
-   Over tax amount and under tax amount variances: Ensure smooth payment processing by defining an acceptable range between the supplier-provided tax and system-calculated tax amounts that allows minor differences within the defined tolerance range. If the supplier-calculated tax exceeds the system-provided tax but remains within the Over tax tolerance limit or the system-calculated tax exceeds the supplier-provided tax but remains within the Under tax tolerance limit, the invoice is considered valid for payment.

    **Note:** If tax amount variance for a tax line is within the tolerance range, then supplier tax amount will be copied over to final tax amount field by default.


-   **[Define an invoice tolerance type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/define-a-new-tolerance-type-definition.md)**  
Create tolerance types to define variance thresholds for use in exception definitions.
-   **[Map invoice tolerance type with invoice exception definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/map-invoice-tolerance-definition-with-tolerance-rule.md)**  
Map invoice tolerance type definitions with invoice exception definitions to apply custom tolerance thresholds to specific exception scenarios.
-   **[Define an invoice tolerance rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/define-a-new-tolerance-rule.md)**  
Create tolerance rules to define acceptable invoice variances based on tolerance types and invoice filters.
-   **[View tolerance form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/view-tolerance-form.md)**  
View tolerance details at the header level and variance details at the line level for invoice processing cases with exceptions.

**Parent Topic:**[Using Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-ap-invoice-processing.md)

**Related topics**  


[Invoice ingestion using the AP Invoice API]()

[Rules based engine]()

[Invoice processing]()

[Invoice processing cases]()

[Invoice exceptions]()

[Invoice approvals]()

[View invoice documents in the Source-to-Pay Workspace]()

