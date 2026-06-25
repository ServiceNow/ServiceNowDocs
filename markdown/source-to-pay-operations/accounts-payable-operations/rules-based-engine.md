---
title: Rules based engine
description: The rule-based engine maps the invoice line to purchase order lines using fields such as unit price, delivered unit price, exact description, exact amount and amount round off.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/rules-based-engine.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, purchase order, PO]
breadcrumb: [Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Rules based engine

The rule-based engine maps the invoice line to purchase order lines using fields such as unit price, delivered unit price, exact description, exact amount and amount round off.

The digitized invoice in accepted state moves to suspected duplicate state where the AP specialist verifies if the invoice is duplicate or not. When the invoice is confirmed to be not duplicate, the state of the invoice changes to received. The rules-based engine maps the fields in invoice such as unit price, derived unit price, exact description, exact amount and amount round off with the purchase order lines. If the invoice fields doesn't match with any of the fields in the purchase order lines, then the invoice state changes to matching error.

\[Omitted image "rules-based-engine.png"\] Alt text: Rules based engine

**Parent Topic:**[Using Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-ap-invoice-processing.md)

**Related topics**  


[Invoice ingestion using Application programming interface \(API\)]()

[Work with invoices]()

[Invoice processing cases]()

[Invoice exceptions]()

[Tolerance Rules and Variances for invoices]()

[Invoice approvals]()

[View invoice documents in the Source-to-Pay Workspace]()

