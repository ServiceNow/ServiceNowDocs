---
title: Email parser agent for Sourcing and Procurement Operations
description: The email parser agent for Sourcing and Procurement Operations processes inbound emails and creates the appropriate procurement cases without manual intervention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/email-parser-agent-spo.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 2
keywords: [Email parser for SPO, Email parser for Sourcing and Procurement Operations, Intent to action]
breadcrumb: [Use agentic workflows, Now Assist for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Email parser agent for Sourcing and Procurement Operations

The email parser agent for Sourcing and Procurement Operations processes inbound emails and creates the appropriate procurement cases without manual intervention.

## Prerequisites

To enable the email parser agent in Sourcing and Procurement Operations, complete the following prerequisites:

-   Install the Notifications Email Agents plugin \(sn\_notif\_agents\). For more information, see [Activate Notifications Email Agents plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/activate-notifications-email-agents-plugin.md).
-   Enable the **Trigger Intent to Action** property on the Inbound Email Actions page. For more information, see [Enable intent to action workflow from inbound actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/enable-intent-to-action.md).
-   Enable the **Email receiving enabled** property for Inbound Email Configuration on the Email Properties page to receive emails. For more information, see [Inbound email configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_InboundMailConfiguration.md).

## Intent to action agentic workflow

When an email arrives in the configured SPO mailbox, the email parser agent triggers immediately and performs the following actions:

1.  Receives the inbound email. The agent monitors a dedicated email address configured for the SPO instance.
2.  Processes the email content. The agent reads the subject and body, then maps the content against predefined intent categories.
3.  Determines the intent. The agent determines what kind of procurement action is being requested.
4.  Creates the appropriate case. Depending on the intent, the agent creates one or more of the following:
    -   A procurement case, for purchase order details, negotiation information, or other case-related requests.
    -   A Universal Request, for supplier case inquiries.
5.  Sends a confirmation email. The agent sends a notification to the requester for each case created, using existing SPO email templates. The notification includes a link to the relevant case in Employee Center.

A single email can contain multiple intents. For example, an email can contain a question about a negotiation and a question about a supplier case. The agent determines each intent independently, creates the corresponding cases, and sends a separate confirmation email for each.

**Parent Topic:**[Use agentic workflows in Now Assist for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/agentic-ai-now-assist-spo.md)

**Related topics**  


[Conversational intake for sourcing and procurement agentic workflow]()

[Enable AI agents for the Conversational intake for sourcing and procurement agentic workflow in the Now Assist panel]()

[Enable AI agents for the Conversational intake for sourcing and procurement agentic workflow in Virtual Agent]()

[Submit a purchase request using the Now Assist AI agent]()

[Update the product category or spend category in the Now Assist panel]()

