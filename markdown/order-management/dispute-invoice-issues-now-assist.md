---
title: Dispute invoice issues using Now Assist Virtual Assistant
description: Dispute invoice issues such as quantity discrepancies in a guided conversational flow using Now Assist Virtual Assistant from the Business Portal, without needing to contact support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/dispute-invoice-issues-now-assist.html
release: australia
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Now Assist for Order Management, Sales Customer Relationship Management]
---

# Dispute invoice issues using Now Assist Virtual Assistant

Dispute invoice issues such as quantity discrepancies in a guided conversational flow using Now Assist Virtual Assistant from the Business Portal, without needing to contact support.

## Before you begin

The following applications must be installed and configured on your ServiceNow instance:

-   Now Assist for Platform \(sn\_genai\_platform\)
-   Now Assist for Order Management \(sn\_now\_assist\_om\)
-   Invoice Case Self Service \(sn\_invoice\_case\_ss\)

Role required: sn\_customerservice.customer

## About this task

When you describe your issue on the Now Assist panel, the AI agent validates the dispute using an Available-to-Promise \(ATP\) API call and presents resolution options, such as a credit note or fulfillment of outstanding items.

If you express dissatisfaction or explicitly request human assistance at any point, the AI agent transfers the conversation to a human agent.

## Procedure

1.  Log in to the Business Portal.

2.  Launch the Now Assist chat panel by selecting the Now Assist icon \[Omitted image "icon-ai-sparkle.png"\] Alt text:.

    Now Assist uses the context of the current page to tailor its responses and offer support. For example, launching it from an invoice details page offers help in the context of that invoice.

3.  In natural language, describe the invoice issue you want to dispute.

    For example, enter `I want to dispute an invoice for incorrect quantity`.

    A list of invoices related to your account is displayed.

4.  If the invoice you want to dispute is listed, confirm by responding affirmatively.

    For example, select **Proceed with ARINV0001003**.

    Alternatively, you can provide a different invoice number or enter product name or invoice date to help identify your invoice.

    The AI agent validates and fetches the invoice details along with the invoice lines.

5.  Select the invoice line you want to dispute.

    The AI agent validates the invoice line details and displays the following information:

    -   Invoice line number
    -   Product
    -   Quantity
6.  If the invoice line you want to dispute is correct, select **Yes**.

7.  Describe the issue when prompted.

    For example, to dispute quantity mismatch, you can enter `I ordered 10 items, but received only 9`.

    The AI agent validates the dispute by triggering an ATP API call. Depending on the outcome, one of the following happens:

    -   Validated: An invoice case is created with the state set to Work in Progress and the agent presents resolution options for the quantity discrepancy. You also receive an email notification with the case details.
    -   Not validated: The agent notifies you that the dispute could not be confirmed. If you disagree with the outcome, you can request to chat with a human agent.
8.  If the dispute is not validated, select one of the following options.

    -   Upload a delivery note as additional proof of your claim.
    -   Connect with a live agent for further assistance.
9.  If you opted to upload a delivery note, upload the document when prompted.

    Supported formats include PDF, JPG, and PNG. The maximum file size is 5 MB.

    The AI agent uses extracts the following details from the uploaded document:

    -   Invoice number
    -   Order number, if available
    -   Description
    -   Product offer or sold product
    -   Quantity
    The AI agent compares the received quantity on the delivery note against the invoiced quantity.

10. If the dispute is validated, select a resolution option for the quantity discrepancy.

    |Option|Description|
    |------|-----------|
    |**Receive a credit note for the missing quantity**|Request a credit for the disputed quantity|
    |**Receive or order the remaining quantity**|Request delivery of the remaining items|

    If you're not satisfied with the resolution options, you can request to be transferred to a human agent. The AI agent uses sentiment analysis to detect dissatisfaction. You can also explicitly ask to chat with a human agent. For example, you can enter `I'd like to speak with an agent` or select **Connect with a live agent**.

    Depending on the resolution option you select, a credit note is issued or an order for the outstanding items is created. The invoice case state is updated to Closed.


## Result

When the dispute is resolved, an email notification is sent to you with a summary and a hyperlink to the case.

**Parent Topic:**[Using Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-management-using.md)

**Related topics**  


[Resolve invoice disputes using agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/resolve-invoice-case-now-assist-agent.md)

