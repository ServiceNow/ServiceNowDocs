---
title: AI worker case resolution confirmation
description: AI worker agent marks invoice cases as resolved and triggers supplier confirmation through Supplier Collaboration Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/ai-worker-case-resolution-confirmation.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-06-05"
reading_time_minutes: 3
keywords: [APO, Accounts Payable Operations, Supplier Collaboration Portals, Supplier, Case resolution, invoice inquiry case]
breadcrumb: [Use, Accounts Payable Operations, Finance and Supply Chain]
---

# AI worker case resolution confirmation

AI worker agent marks invoice cases as resolved and triggers supplier confirmation through Supplier Collaboration Portal.

When an AI worker completes the resolution of an invoice inquiry case \(and payment inquiry\) in APO, marking the case as resolved initiates an automated confirmation workflow. This workflow delivers the resolution request to the external supplier through multiple channels: the Supplier Collaboration Portal. Supplier responses are tracked and confirmation status is visible, enabling timely case closure after supplier validation is received.

## How it works

When an AI worker provides a resolution to an invoice case through the activity stream, the worker marks the case as resolved by updating the case state to **Awaiting acceptance**. This state change triggers an automated supplier confirmation workflow.

The workflow performs the following actions:

-   Captures the resolution details provided by the AI worker.
-   Identifies the supplier contact associated with the case.
-   Prepares a confirmation request message containing the resolution details.
-   Delivers the confirmation request through Supplier Collaboration Portal
-   Initiates tracking and monitoring of the supplier's response.

The supplier receives the confirmation request and uses the Supplier Collaboration Portal to validate or challenge the resolution. The supplier's response is recorded, the case status is updated accordingly, and the AI worker and relevant team members are notified of the outcome.

-   **[Invoice case resolution using AI worker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-case-resolution-using-ai-worker.md)**  
Mark an invoice inquiry case and payment inquiry as resolved to start an automated workflow that requests supplier confirmation through Supplier Collaboration Portal.
-   **[Email resolution notifications for APO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/email-resolution-notifications-for-apo.md)**  
AI worker agent resolves the case and moves it to awaiting acceptance, then sends an email with resolution details and accept/reject buttons.

**Parent Topic:**[Accounts Payable Operations overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-acc-pay-mgmt.md)

**Related topics**  


[Create a knowledge base article for invoices]()

[Invoice case categories and subcategories]()

[Using Invoice Case Management]()

[Using Accounts Payable Invoice Processing]()

[Advanced Work Assignment in Accounts Payable Operations]()

[Configure Advanced Work Assignment for Accounts Payable Operations]()

[Using Advanced Work Assignment for Accounts Payable Operations]()

[Working with Advanced Work Assignment]()

[Interaction management in Accounts Payable Operations]()

[Composing emails with predefined content]()

[Universal Request in Accounts Payable Operations]()

[Playbook for updating the invoice primary data]()

[Using Supplier Collaboration Portal in APO]()

