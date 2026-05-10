---
title: Virtual agent flows
description: Suppliers can check the invoice and inquiry statuses, create inquiry cases in the supplier portal using the chat channel. Suppliers can also use the virtual agent to view predefined chatbot topics.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Supplier Collaboration Portal in APO, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Virtual agent flows

Suppliers can check the invoice and inquiry statuses, create inquiry cases in the supplier portal using the chat channel. Suppliers can also use the virtual agent to view predefined chatbot topics.

Suppliers can switch between a virtual agent and a live agent to address their issues. The customer service virtual agent topics \(chatbot conversations\) help suppliers complete common self-service tasks. The supplier initiates a conversation topic that consists of dialogs with the virtual agent chatbot to accomplish a goal.

Natural Language understanding \(NLU\) is integrated with the virtual agent chatbot to help suppliers with invoice and inquiry-related queries. NLU also helps suppliers to analyze, understand, and navigate to the right topic.

For more information, see [Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/connect/c_Connect.md) and [Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/virtual-agent-landing-page.md).

## Accounts Payable Operations Virtual agent flows

Supplier can choose to view the following Virtual agent flows.

## Check invoice status

The supplier provides an invoice number and the virtual agent displays the status of the invoice. The invoice status is a clickable link, which navigates suppliers to view invoice case details. For more details about the invoice, see [Work with invoices](work-with-invoices.md).

The chatbot prompts the supplier to perform the following.

1.  Add new comment-comment on the inquiry or invoice case that the supplier requested for
2.  Talk to a live agent- Accounts Payable Operations agent interacts with a supplier for an invoice or inquiry-related query
3.  Search for something else- Redirects suppliers to point 1
4.  All good thanks- Ends the chat

## Live Agent support

Suppliers are routed directly to a live Accounts Payable Operations to initiate conversations and skip the virtual agent conversation greeting. Live agents can also create Interaction records and associate with an existing invoice case. For more information on interaction records, see [Interaction management in Accounts Payable Operations](interaction-record.md). If an agent isn't available, the message **No agent available** is displayed to the user.

## Check inquiry status

The supplier provides an invoice number and the virtual agent displays the status of the inquiry. The Accounts Payable Operations agent can create a new inquiry on the invoice.

## Create new inquiry

The supplier can choose to create an inquiry case related to the invoice using the **Create inquiry** link. The **Create inquiry** link enables suppliers to choose the type of inquiry case. Suppliers use **Add new comment** to add comments related to the inquiry.

For more information on creating inquiry case, see [Submit Invoice Inquiry](../task/submit-invoice-inquiry-case.md).

## Prechat Survey

Pre-chat survey is available to supplier if the Accounts Payable admin installs the `app-supplier-awa`plugin into the system. Depending on the response received from the supplier, the chatbot directs the supplier to choose between **Talk to Live Agent** and **Accounts Payable** options. For more information on the options, see [Configure the chat channel](../task/configure-the-chat-channel.md) and [Advanced Work Assignment in Accounts Payable Operations](advanced-work-assignment.md).

.

-   **[Configure the chat channel](../task/configure-the-chat-channel.md)**  
Activate the virtual agent chatbot \(chat channel\) in the supplier portal for suppliers to complete Accounts Payable Operations related self-service tasks.

**Parent Topic:**[Using Supplier Collaboration Portal in APO](using-supplier-collaboration-portal.md)

