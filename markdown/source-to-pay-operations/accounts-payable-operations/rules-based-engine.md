---
title: Rules based engine
description: The rule based engine maps the invoice line with purchase order line using fields such as unit price, delivered unit price, exact description, exact amount and amount round off.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/rules-based-engine.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Rules based engine

The rule based engine maps the invoice line with purchase order line using fields such as unit price, delivered unit price, exact description, exact amount and amount round off.

The digitized invoice in accepted state moves to suspected duplicate state where the AP specialist verifies if the invoice is duplicate or not. When the invoice is confirmed to be not duplicate, the state of the invoice changes to received. The rules-based engine maps the fields in invoice such as unit price, derived unit price, exact description, exact amount and amount round off with the purchase order lines. If the invoice fields doesn't match with any of the fields in the purchase order lines, then the invoice state changes to matching error.

\[Omitted image "rules-based-engine.png"\] Alt text: Rules based engine

**Parent Topic:**[Using Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/use-ap-invoice-processing.md)

**Related topics**  


[Invoice ingestion using the AP Invoice API]()

[Work with invoices]()

[Invoice processing cases]()

[Invoice exceptions]()

[Tolerance Rules and Variances for invoices]()

[Invoice approvals]()

[View invoice documents in the Source-to-Pay Workspace]()

[Invoice case categories and subcategories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/working-with-cases.md)

[Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-case-mgmt-overview.md)

[Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-workspace.md)

[Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-invoice-processing.md)

[Integrate APO with other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/integrate-apo.md)

