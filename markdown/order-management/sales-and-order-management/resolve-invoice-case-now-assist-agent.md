---
title: Resolve invoice disputes using agentic workflow
description: Resolve invoice dispute cases using Now Assist directly from the CSM/FSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/resolve-invoice-case-now-assist-agent.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Now Assist for Order Management, Sales Customer Relationship Management]
---

# Resolve invoice disputes using agentic workflow

Resolve invoice dispute cases using Now Assist directly from the CSM/FSM Configurable Workspace.

## Before you begin

The invoice dispute assist agentic workflow must be made available on the Now Assist panel. For more information, see [Make the invoice dispute assist workflow available in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/enable-invoice-dispute-assist-agentic-workflow.md).

Now Assist for CSM must be installed to enable generative AI capabilities in the CSM/FSM Configurable Workspace. For more information, see [Install Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/activate-now-assist-for-customer-service-management-csm.md).

Chat Summarization must be configured to use the summarization and recommendation features. For more information, see [Configure chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/configure-chat-summarization-in-now-assist_0.md).

Role required: awa\_agent, sn\_csm\_invoice.agent, sn\_otc.accounts\_receivable\_agent, and now\_assist\_panel\_user

## About this task

When a customer escalates an invoice dispute to a human agent either through a Virtual Assistant handoff or by contacting support directly, you can launch the Now Assist panel from the CSM/FSM Configurable Workspace to help accelerate resolution. The invoice dispute assist agentic workflow fetches the invoice case details, finds similar resolved cases, validates the dispute using an API call, and guides you through closing the case with the appropriate resolution.

When a customer is transferred from the Virtual Assistant, the interaction record opens automatically with a conversation summary, giving you full context of the dispute discussed on the Virtual Assistant side.

You can also use the summarize and chat recommendation features in the Active Chat to improve productivity. For more information, see [Summarize a chat conversation by using Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-summarize-chat.md) and [Generate a chat reply recommendation by using Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/generate-chat-reply-recommendations.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  If you're assisting a customer via the live chat, accept the chat.

    1.  Select the Inbox icon \[Omitted image "inbox-outline-24.svg"\] Alt text:.

    2.  Change the status to **Available** to be able to accept the live chat.

    3.  Join the chat by selecting **Accept**.

        The Active Chat panel opens with an AI-generated summary of the conversation between the AI agent and the customer, including the disputed invoice number and the issue described by the customer. The associated interaction record opens alongside.

    4.  Access the invoice case details by selecting the **Related Tasks** tab.

        The case number, priority, state, and short description details are displayed for the associated invoice case.

3.  Launch the Now Assist panel by selecting the Now Assist icon \[Omitted image "icon-ai-sparkle.png"\] Alt text:.

    The Now Assist panel is context-aware. When you launch it from an open interaction record or invoice case record, it tailors its responses to that record.

4.  Launch the invoice dispute assist agentic workflow using either methods.

    -   Select the **Invoice Dispute Assist** pill in the Now Assist panel.
    -   Type your query in natural language, for example, `Help me resolve this invoice dispute`.
    The invoice dispute assist agentic workflow invokes the invoice dispute support assistant AI agent. The AI agent fetches the invoice case and prompts you to confirm if it's valid.

5.  If the invoice case fetched by the AI agent is correct, select **Yes**.

    Otherwise, enter the invoice case you need help with.

    The AI agent validates the invoice case and then provides you the options for resolving the case.

6.  Select **Find similar cases** to view previously resolved cases with a similar dispute pattern.

    The AI agent lists similar cases from the same account, matched by common dispute types and resolution patterns, such as credit note or replacement order, to help you determine the appropriate course of action.

7.  Select **Validate invoice dispute** to verify the customer's claim.

    The AI agent triggers an ATP API call to cross-check the claimed quantity against delivery records and returns a validation status. If delivery records are unavailable, the AI agent validates the dispute against the original order line quantity. If validated, the invoiced and delivered quantities are displayed for your review.

8.  Select **View invoice details** to review the invoice number, status, account, and associated invoice lines before closing the case.

9.  If everything looks good, select **Close the case** and choose a resolution option.

    -   Select **Issue a credit note for the missing quantity** to generate a credit for the disputed quantity.
    -   Select **Place an order for the remaining quantity** to fulfill the outstanding items.
    -   Select **Close the case as invalid dispute** if the validation confirms that the customer's claim is invalid or not supported.
    The invoice case State is changed to Closed and the Resolution code is auto-populated depending on the resolution. Based on the selection, credit note number or order details are posted to the Resolution notes and Work notes of the invoice case.


## Result

When the dispute is resolved, the invoice case is closed with the resolution details documented in the case notes, and an email notification is sent to the customer with a summary and a hyperlink to the case.

**Parent Topic:**[Using Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/now-assist-order-management-using.md)

**Related topics**  


[Using Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

[Summarize a chat conversation by using Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-summarize-chat.md)

