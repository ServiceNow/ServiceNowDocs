---
title: Request order changes via calls
description: Use the AI voice agents to create and manage cases for any order or invoice-related issues such as expediting orders, disputing order quantity with voice calls.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Now Assist for Order Management]
---

# Request order changes via calls

Use the AI voice agents to create and manage cases for any order or invoice-related issues such as expediting orders, disputing order quantity with voice calls.

## Before you begin

Role required: sn\_customerservice.customer

## About this task

Using the order exception AI voice agent, you can do the following:

-   Expedite order delivery dates for orders that are not in the Draft state
-   Use generic keywords such as Expedite delivery or Faster delivery and get responses from an agent in the context of your questions

## Procedure

1.  Call the customer support number of the Business-to-business \(B2B\) seller.

2.  When connected to the AI voice agent, state your intent to expedite your order.

    For example, say "I need to request expedited shipping for my order".

3.  Verify your identity when prompted by entering your phone number on the phone keypad, followed by the pound key.

4.  Enter your soft PIN on the phone keypad, followed by the pound key.

5.  Provide the order number that you want to expedite when prompted.

    For example, say "I need to expedite order ORD0000523".

6.  Specify the date that you need your order delivered by when prompted.

    For example, say "I need it delivered by the end of this week".

    The AI voice agent attempts to validate availability and retrieve the earliest possible delivery date using an Available-to-Promise \(ATP\) API call. If the system is unable to retrieve availability, the agent proceeds with your request and offers to create an order case to escalate the matter.

7.  Confirm when the agent asks whether you want to create a case for the expedited shipping request.

    For example, say "Yes, please go ahead and create the case".


## Result

The AI voice agent creates an order case based on an agreement of proposed delivery dates with the customer starting with the prefix ORDCS and provides you with the case number over the call.

**Parent Topic:**[Using Now Assist for Order Management](now-assist-order-management-using.md)

