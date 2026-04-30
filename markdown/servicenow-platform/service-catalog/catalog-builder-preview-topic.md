---
title: Catalog builder preview topic conversation
description: From the catalog builder, a user can preview a catalog item in a Virtual Agent conversation.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a catalog item using a template, Creating or editing catalog item template, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog builder preview topic conversation

From the catalog builder, a user can preview a catalog item in a Virtual Agent conversation.

This conversation uses the Request Catalog Item topic block. For information on this topic block, see [Service Catalog topic blocks in Virtual Agent powered by NLU](request-topic-blocks-va.md).

The Service Management Virtual Agent Topic Blocks plugin \(com.glideapp.cs.sm\_topic\_blocks\) and one of these plugins should be installed.

-   Glide Virtual Agent \(com.glide.cs.chatbot\)
-   Glide Virtual Agent Lite \(com.glide.cs.chatbot.lite\)

In catalog builder, when the user selects the required item and navigates to preview it, the following scenarios are possible:

-   If the item is supported in the conversation mode, you can preview the item in the Virtual Agent conversation by answering the questions but cannot submit a request for the item. For information about when a catalog item is supported in the conversation mode, see [Service Catalog topic blocks in Virtual Agent powered by NLU](request-topic-blocks-va.md).
-   If the item is not supported in the conversation mode, a link is provided for the portal preview of the item.
-   When the required plugins are not installed, an illustration displaying a sample conversational experience for the catalog item submission appears.

**Parent Topic:**[Create a catalog item using a template](../task/create-item-cat-builder.md)

**Related topics**  


[Service Catalog topic blocks in Virtual Agent powered by NLU](request-topic-blocks-va.md)

