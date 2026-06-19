---
title: Request order changes via calls
description: Use the AI voice agents to expedite delivery, change quantity, or change the shipping location for an order by using voice calls. The voice agent captures your request and creates an order case for an order case agent to resolve.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/now-assist-order-mgmt-voice-aiagent.html
release: zurich
topic_type: task
last_updated: "2026-05-21"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Now Assist for Order Management]
---

# Request order changes via calls

Use the AI voice agents to expedite delivery, change quantity, or change the shipping location for an order by using voice calls. The voice agent captures your request and creates an order case for an order case agent to resolve.

## Before you begin

Role required: sn\_customerservice.customer

## About this task

Using the order exception AI voice agent, you can do the following:

-   Submit order exception requests for orders that are not in the Draft state, including expedited delivery, a quantity change, or a shipping location change
-   Use generic keywords such as Expedite delivery, Faster delivery, Change quantity, or Ship to a different location and get responses from an agent in the context of your questions

## Procedure

1.  Call the customer support number of the Business-to-business \(B2B\) seller.

2.  When connected to the AI voice agent, state your intent for the order change, which can be to expedite delivery, change the quantity, or change the shipping location.

    For example, say "I need to request expedited shipping for my order", "I need to change the quantity on my order", or "I need to ship my order to a different address".

3.  Verify your identity when prompted by entering your phone number on the phone keypad, followed by the pound key.

4.  Enter your soft PIN on the phone keypad, followed by the pound key.

5.  Provide the order number that you want to change when prompted.

    For example, say "I need to expedite order ORD0000523", "I need to change the quantity on order ORD0000523", or "I need to change the shipping location for order ORD0000523".

6.  Specify the details of your change when prompted, which could include the revised delivery date for expedited delivery, the new quantity for a quantity change, or the new shipping address for a shipping location change.

    For example, say "I need it delivered by the end of this week", "I need to increase the quantity to 50 units", or "Ship it to my Boston warehouse instead".

    The AI voice agent captures your request without performing inventory, quantity, or quote validation, and then offers to create an order case for an order case agent to resolve in the CSM Configurable Workspace.

7.  Confirm when the agent asks whether you want to create a case for your order change request.

    For example, say "Yes, please go ahead and create the case".


## Result

The AI voice agent creates an order case for your request, with a system-generated number starting with the prefix ORDCS, and provides you with the case number over the call. Make a note of the case number, because no email confirmation is sent for order cases that are created through the voice channel.

**Parent Topic:**[Using Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/now-assist-order-management-using.md)

