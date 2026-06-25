---
title: Request order changes using Now Assist Virtual Assistant
description: Request an expedited delivery, a quantity change, or a shipping location change for your order in natural language using the Now Assist Virtual Assistant on the Business Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/request-order-changes-now-assist.html
release: australia
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 5
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Now Assist for Order Management, Sales Customer Relationship Management]
---

# Request order changes using Now Assist Virtual Assistant

Request an expedited delivery, a quantity change, or a shipping location change for your order in natural language using the Now Assist Virtual Assistant on the Business Portal.

## Before you begin

The following applications must be installed and configured on your ServiceNow instance:

-   Now Assist for Platform \(sn\_genai\_platform\)
-   Now Assist for Order Management \(sn\_now\_assist\_om\)
-   Order Case Self Service \(sn\_ord\_case\_ss\)

The scripted extension points that the chat assistant uses to validate order exception requests such as delivery availability, quantity, shipping location, and quote threshold must be configured. For more information, see [Configure scripted extension points for the manage order operations agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-atp-api-call.md).

Role required: sn\_customerservice.customer

## About this task

When you submit a request through the Virtual Assistant, the AI agent performs the following actions behind the scenes to help you quickly and efficiently:

-   Checks account information and order history.
-   Validates the intent of the request, which can be an expedited delivery, a quantity change, or a shipping location change. For example, if you enter `expedite`, `change quantity`, or `ship to a different location` in the Virtual Assistant, the AI agent confirms the request type for your open orders.
-   Confirms the order number and your change request.
-   After you confirm all the requested changes, creates an order case in the ServiceNow CRM and stamps the requested changes on the requested fields of the order case lines.
-   Calls the configured scripted extension points to validate inventory availability, quantity feasibility, shipping location feasibility, and quote thresholds for the request. For example, the AI agent calls orderExceptionCheckEP to check whether the ordered item is in stock for early delivery, or ThresholdCheckForQuote to determine whether a quantity change requires a quote. If you approve the validation results, the AI agent stamps the approved values on the approved fields of the order case lines.
-   Posts the summary of the conversation as a work note in the order case, which can only be viewed by the agents from the CSM Configurable Workspace.

## Procedure

1.  Log in to the Business Portal.

2.  Launch the Now Assist chat panel by selecting the Now Assist icon \[Omitted image "icon-ai-sparkle.png"\] Alt text:.

3.  In natural language, submit a request that you would like for your order.

    For example, enter `Expedite my order`, `Increase the quantity on my order`, or `Change the shipping location for my order`.

4.  If the AI agent interprets your request correctly, provide your confirmation.

    You can enter `That's correct` in the response.

5.  Verify the order details that are displayed and specify an order that you’re requesting changes for.

6.  Select the order line item that you want to change or enter the product name.

    If the selected line item is part of a bundle, the AI agent automatically includes the parent, child, and sibling lines of the bundle in your request. If the selected line item is independent, the AI agent applies the request only to that line.

    You can request multiple exception types \(an expedited delivery, a quantity change, and a shipping location change\) on the same order line.

7.  Specify the details of your change when prompted.

    -   Revised delivery date for expedited delivery
    -   New quantity for a quantity change
    -   New shipping address for a shipping location change
    The manage order operations AI agent validates feasibility for your request by calling the configured scripted extension points. For an expedited delivery, the agent fetches the earliest possible delivery date. For a quantity change, the agent validates the requested quantity and determines whether the change requires a quote. For a shipping location change, the agent validates whether the new location is serviceable.

    After you confirm the requested changes, the AI agent creates an order case with a system-generated number starting with the prefix ORDCS and stamps the requested changes on the requested fields of the order case lines. You receive an email confirming that your order case has been opened and is under review.

8.  When asked about the feasible options, accept or reject the proposal in natural language.

    If you approve the validation results, the AI agent stamps the approved values on the approved fields of the order case lines and posts a summary of the conversation as a work note on the case. The AI agent provides the order case link so that you can view the case details on the Business Portal. If you reject the validation results, the AI agent offers to connect you to a live agent and the order case remains in progress.

9.  If the AI agent prompts you for a quote, indicate whether you need a quote for your change.

    The AI agent prompts you for a quote when the requested change exceeds the configured price threshold. If you decline the quote, the AI agent offers to connect you to a live agent and the order case remains in progress.

10. If a quote is created, review the proposed quote and accept or reject it.

    If you accept the quote, the quote moves to the Accepted state, the order case is closed, and the order case lines are moved to the Resolved Accepted state. The quote details are recorded in the resolution code and resolution note. You receive a confirmation email with the order case resolution and quote details.

    If you reject the quote, the AI agent offers to connect you to a live agent and the order case remains in progress.


**Parent Topic:**[Using Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-management-using.md)

**Related topics**  


[Configure Now Assist for Sales Force Automation \(SFA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-now-assist-som.md)

