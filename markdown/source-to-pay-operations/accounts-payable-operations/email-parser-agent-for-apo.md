---
title: Email parser agent for APO
description: The Email parser is an intelligent AI agent that automatically processes incoming emails \(Level 1 support cases and tasks\) from suppliers and invoice owners, identifies actionable requests, classifies them, and routes them to the appropriate workflows to create invoice cases.s
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/email-parser-agent-for-apo.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-06-19"
reading_time_minutes: 1
breadcrumb: [Using AI agents in Now Assist for Accounts Payable Operations, Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Email parser agent for APO

The Email parser is an intelligent AI agent that automatically processes incoming emails \(Level 1 support cases and tasks\) from suppliers and invoice owners, identifies actionable requests, classifies them, and routes them to the appropriate workflows to create invoice cases.s

The agent intelligently distinguishes between request types such as invoice inquiries, payment inquiries, payment acceleration requests, and payment term updates. This verifies that each query is categorized correctly and routed to the appropriate business process.

## Key benefits

-   Reduced manual triage: Automated classification eliminates the need for manual email review and routing.
-   Faster query resolution: Structured data extraction enables quicker case creation and response.
-   Consistent categorization: All queries are classified using the same criteria, ensuring uniform handling across your organization.
-   Improved supplier experience: Suppliers receive faster acknowledgment and status updates on their requests.

## How it works

As a prerequisite, you must set:

-   Inbound email action- Trigger Intent to Action to true
-   Email properties-Inbound email configuration to true

When a supplier or invoice owner sends an email, the agent receives and processes the message. The agent identifies the sender's email address and validates that the sender is a registered, active supplier contact. It then analyzes the email content to determine whether it contains one or more of the following Accounts Payable Operations request types: invoice inquiry, payment inquiry.

If the email matches one of the recognized request types, the agent extracts the relevant details, maps the request type to the appropriate case category and subcategory, and initiates a case creation workflow. Informational emails that don't contain actionable requests aren't processed.

## Case creation behavior

The email parser agent follows these case creation rules:

-   For emails with one or more recognized request types, a case is created with the appropriate category and subcategory.
-   For emails with no recognized request types \(non-actionable or informational emails\), no case is created. The email is archived.

