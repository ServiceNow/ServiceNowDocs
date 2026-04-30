---
title: Request order changes using Now Assist for Order Management
description: Request expedited delivery for your order in natural language using the Now Assist Virtual Assistant on Business Portal.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-04"
reading_time_minutes: 2
keywords: [AI features, Now Assist on Business Portal]
breadcrumb: [AI agents in Order Management, Use, Now Assist for Order Management]
---

# Request order changes using Now Assist for Order Management

Request expedited delivery for your order in natural language using the Now Assist Virtual Assistant on Business Portal.

## Before you begin

The following applications must be installed and configured on your ServiceNow instance:

-   Now Assist for Platform \(sn\_genai\_platform\)
-   Now Assist for Order Management \(sn\_now\_assist\_om\)
-   Order Case Self Service \(sn\_ord\_case\_ss\)

A working Available-to-Promise \(ATP\) API call must be configured to query your external inventory systems. For more information, see [Configure ATP API for the manage order operations agent](create-atp-api-call.md).

Role required: sn\_customerservice.customer

## About this task

When you submit a request through the Virtual Assistant, the AI agent performs the following actions behind the scenes to help you quickly and efficiently:

-   Checks account information and order history.
-   Validates the intent of the request. For example, if you enter “expedite” in the Virtual Assistant, the AI agent confirms that you’re requesting expedited order delivery for your open orders.
-   Confirms the order number and your change request.
-   Calls external ATP API to validate inventory availability and feasibility of the request. For example, the AI agent makes an ATP API call to an external ERP system to check if the ordered item is in stock for early delivery.
-   Creates an order case in the ServiceNow system with requested details. If ATP call fails and the customer request is not feasible to fulfill, the AI agent still creates an order case so that the order case agent can review the request in the CSM Configurable Workspace and provide resolution.
-   Posts the summary of the conversation as a work note in the order case which can only be viewed by the agents from the CSM Configurable Workspace.

## Procedure

1.  Log in to the Business Portal.

2.  Select the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) to launch the Now Assist chat panel.

3.  In natural language, submit a request you would like for your order.

    For example, enter "Please expedite my order".

4.  If your request is interpreted correctly by the AI agent, provide your confirmation.

    You can enter "That's correct" in the response.

5.  Verify the order details displayed to you and specify an order for which you’re requesting changes.

6.  Specify a date by which you want your order to be delivered or provisioned.

    The manage order operations agent validates whether your order can be expedited and fetches the earliest possible delivery date by triggering an ATP API call.

7.  When asked about the feasible options, accept or reject the proposal in natural language.

    The AI agent creates an order case with a system-generated number starting with the prefix ORDCS. It also provides the order case link that you can select to view the order case details on the Business Portal.


**Parent Topic:**[Standalone agents in Order Management](../concept/now-assist-om-ai-agents.md)

**Related topics**  


[Configuring Now Assist for Order Management](../concept/now-assist-for-order-management-configuring.md)

