---
title: Using catalogs and autopilot in Virtual Agent
description: Use catalogs to search for and request services and products in chat widget conversations.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [virtual agent, catalogs, autopilot, requested, item, RITM, web, client, live agent]
breadcrumb: [Configure, Virtual Agent, Conversational Interfaces]
---

# Using catalogs and autopilot in Virtual Agent

Use catalogs to search for and request services and products in chat widget conversations.

The catalog feature lets you use natural language to search for and request service items in a Virtual Agent conversation. The Virtual Agent recognizes your request and presents you with the best answer. You complete the entire order in the chat, without going to a new page.

For example, if you enter `iPad`, the Virtual Agent shows you the service catalog info for an iPad. You can request the item, ask for more information on the item before deciding, or ask for something else.

If you choose to order the item, you select any available options. When you complete the order, the catalog card closes, and Virtual Agent replaces it with a Requested Item record and a link. Selecting the link takes you to the record.

![All data relevant to your order is displayed in the requested item record.](../images/va-catalogs-05.png)

If you cancel the order instead, you receive a message confirming the cancellation. For example, if you enter `iPhone` and request the item, then cancel the order, the request closes and the Virtual Agent doesn't create a record.

**Note:** Catalogs for Virtual Agent are separate from Now Assist and Multi-turn catalog ordering. For more information on how catalog search results work based on AI Search, see [Genius Results](https://www.servicenow.com/docs/access?context=genius-results-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US). For information on Multi-turn catalog ordering instead, see [Using Now Assist in Virtual Agent](../../now-assist-in-va/concept/using-now-assist-in-va.md).

## Catalog live agent autopilot experience

Autopilot is available for live agents in the CSM Workspace, and allows the live agent to assist a customer with a catalog order as well as view all information on the customer's transaction.

To use the feature, the live agent enters `/autopilot "[topic]"`, substituting `[topic]` for the catalog item topic name. The catalog item appears in the customer's chat window, and they choose any preferences for the order as usual. The live agent can see the full catalog order in the chat panel, but cannot change any details of the order themselves.

![CSM Workspace view next to customer chat window. The live agent has activated autopilot.](../images/va-catalogs-autopilot-2.png)

Once the customer completes the order, the chat panel displays the Requested Item record as usual. The live agent sees the full transcript of the customer's transaction, including the full catalog card and Requested Item record.

-   **[Set up catalog branding](../task/va-catalogs-branding.md)**  
Customize the appearance of catalogs in Virtual Agent to match your business' branding.

**Parent Topic:**[Configuring Virtual Agent](configure-virtual-agent.md)

