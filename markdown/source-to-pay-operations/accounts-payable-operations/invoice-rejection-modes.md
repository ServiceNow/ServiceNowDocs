---
title: Invoice rejection modes
description: Invoice rejection modes control how Accounts Payable Operations handles exceptions that require an invoice to be rejected, either automatically by the system or through manual review by an AP specialist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-rejection-modes.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Create an invoice line manually, Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice rejection modes

Invoice rejection modes control how Accounts Payable Operations handles exceptions that require an invoice to be rejected, either automatically by the system or through manual review by an AP specialist.

When the exception engine processes an invoice, it evaluates each exception associated with that invoice. The **Rejection mode** field on each exception rule table determines whether the invoice is rejected without AP intervention or routed to an AP specialist for review.

When rejection mode is set to "None" in APO, the system disables the ability to manually reject invoices.

## Manual rejection mode

When manual rejection is triggered, the invoice is routed to an AP specialist for review. The specialist reviews the flagged exceptions and confirms the rejection. The system supports this workflow by displaying the following on the invoice case:

-   A notification that exceptions flagged for manual rejection mode require review.
-   A **Reject invoice** button that the AP specialist selects to initiate the rejection.

When the AP specialist selects **Reject invoice**, the system prompts them to enter a rejection reason. After confirmation, the system cancels the exception and invoice, populates the appropriate comments in the audit history and activity stream, and sends an email notification to the supplier with the rejection comments.

## Condition builder

The exception rule allows AP admin to add conditions to any invoice exception definition by Legal entity, Supplier type and many more as shown in the following screen shot:\[Omitted image "inv-exception-defn.png"\] Alt text: Invoice exception definition configured with rule For more information on the fields in the exception rule, see [Invoice Exception Rule Form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-exception-rule-form.md).

**Parent Topic:**[Create an invoice line manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice-line.md)

**Related topics**  


[Invoice Exception Rule Form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-exception-rule-form.md)

