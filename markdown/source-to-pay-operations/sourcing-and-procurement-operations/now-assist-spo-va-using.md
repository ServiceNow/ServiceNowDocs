---
title: Request the generative AI capabilities by using the Now Assist for SPO Virtual Agent
description: Request the contextual generative AI capabilities by using the conversational interface in Now Assist for SPO Virtual Agent.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
keywords: [generative AI, gen AI, genai, artificial intelligence]
breadcrumb: [Using Now Assist for Sourcing and Procurement Operations \(SPO\), Now Assist for Sourcing and Procurement Operations \(SPO\), Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Request the generative AI capabilities by using the Now Assist for SPO Virtual Agent

Request the contextual generative AI capabilities by using the conversational interface in Now Assist for SPO Virtual Agent.

As a requester, you can use the predefined topics \(chatbot conversations\) designed to help you complete common self-service tasks, such as buying a product or knowing the current status of a purchase requisition, sourcing request, or procurement case.

As a requester, you can use the Now Assist for SPO Virtual Agent to search against the existing products in the product catalog and displays the available products. You can also use it to inquire about the status of the procurement records, such as sourcing requests, purchase requisitions, procurement cases, and purchase orders.

Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** and select the Virtual Agent chat icon \(![Chat icon.](../../supplier-lifecycle-operations/image/open-chat-window-icon.png)\) to start a conversation.

## Using predefined topic to buy a product

As a requester, you can start by selecting **View all topics**.

![View all topics](../image/na-va-start.png "Now Assist for SPO Virtual Agent starting screen")

Then, select the **Buy a product** topic.

![All topics in NA for SPO virtual agent.](../image/na-va-all-topics.png "Available Topics in Now Assist for SPO Virtual Agent")

You could also directly start typing what you need, in which case the utterance detection mechanism uses Genius Results to retrieve Virtual Agent topics, catalog items, and Q&amp;A results, and displays them to the requester within a card carousel. For details, see [Using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

The Virtual Agent engages you in a guided conversation, asking you relevant questions along the way to help you submit your purchase, sourcing, and off-catalog requests, as well as procurement cases, independently, without the need to reach out to fulfillers. You can then review and track these request records from Shopping Hub, Employee Center, or Platform.

If a product is found with or without a price in the catalog, the requester can then fill out the intake questions through a simple conversation, and then submit the purchase request after reviewing the summary of responses. They can also edit a response before submitting.

![Catalog conversation](../image/conv-catalog.png "Catalog conversation")

If a product or service isn’t found in the catalog, the chatbot gathers more information, such as checking for availability of quotes, and routes the requester to the corresponding off-catalog intake form.

![Off-catalog conversation](../image/conv-off-catalog.png "Off-catalog conversation")

It also provides the requester with the option to submit a question to the procurement team about the required product or service, with relevant attachments, if any, all through a conversation.

**Note:** You can ask a question to the procurement team, and create a corresponding procurement case, only if you have the sn\_spend\_psd.requestor role. Ensure that you admin has assigned that role to you.

To learn more about quick checkout and sourcing checkout processes, see [Order a product with quick checkout](../task/order-a-product.md) and [Complete sourcing checkout](../task/complete-sourcing-checkout.md) respectively. For more information on off-catalog intake forms, see [Requesting for products or services that you don't see on ShoppingHub](request-prod-serv-dont-see-sh.md).

## Using predefined topic to track requests

As a requester, you can engage with the Now Assist for SPO Virtual Agent and inquire about the status of your recent purchase or request by selecting the **Track my procurement purchases/requests** topic.

![Track requests topic.](../image/na-va-all-topics-track.png)

You can inquire about the following records to the virtual agents:

-   Purchase requisition \(PR\)
-   Sourcing request \(SR\)
-   Purchase order \(PO\)
-   Procurement Case \(PC\)

For example, You can ask whether the purchase requisition PR0001002 has already been approved.

![Purchase requisition inquiry](../image/conv-pr-inquiry.png "Purchase requisition status inquiry")

The chatbot provides you the current status of the PR that you inquired about.

![Purchase requisition inquiry response](../image/conv-pr-response.png "Purchase requisition inquiry response")

You can choose either to close the conversation or check the status of another record.

## Searching for requests by specifying a time period

The Now Assist for SPO Virtual Agent also enables you to search for requests by specifying the time period when the request was opened. Here are a few examples:

-   What's the status of the purchase I made last month
-   Just send me the status of my purchases made 3 weeks ago
-   Can I get an update on the purchase I requested in August 2024

## NOW Assist for SPO can't find any result

If the Now Assist for SPO Virtual Agent is unable to search for your specific request, the following occurs:

-   The Now Assist for SPO Virtual Agent prompts you, as follows, to provide more context if the results don't meet your needs.

    `I'm sorry, I couldn't find what you needed. Could you rephrase your request or provide more context?`

-   The Now Assist for SPO Virtual Agent prompt users up to two times to rephrase their request before displaying the following message:

    ![VA for SPO prompts user twice before displaying this message.](../image/na-va-unable-find.png)

-   If there’s no chat activity for 900 seconds, the Now Assist for SPO Virtual Agent ends the chat.

    ![Message shown after prolonged inactivity.](../image/conv-inactivity.png)


## Additional Information

Now Assist in Virtual Agent provides your users with an interactive generative Artificial Intelligence \(AI\) experience. A friendly, natural language conversation is easier to understand and makes requesters more comfortable with talking to a bot. To learn how a conversation powered by generative AI might look in Virtual Agent, see [Using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

As an administrator, you can use the Now Assist in Virtual Agent Analytics dashboard to monitor the performance of Now Assist in Virtual Agent as a self-service deflection tool. To learn more, see [Analyzing Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now_assist_in_virtual_agent_analytics_dashboard&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US). Now Assist in Virtual Agent Analytics calculates the conversation deflection rate based on the resolution status associated with Now Assist query responses. For more information, see [Understanding conversation deflection rate](https://www.servicenow.com/docs/access?context=understanding-deflection-rate&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

For detailed information on Now Assist in Virtual Agent in general, and Now Assist for SPO in particular, see [Exploring Now Assist for Sourcing and Procurement Operations \(SPO\)](now-assist-spo-exploring.md).

For information on configuring Now Assist for SPO, see [Configuring Now Assist for Sourcing and Procurement Operations \(SPO\)](../task/configure-now-assist-for-spo.md)

**Parent Topic:**[Using Now Assist for Sourcing and Procurement Operations \(SPO\)](now-assist-spo-using.md)

**Related topics**  


[Summarize a record by using Now Assist for Sourcing and Procurement Operations \(SPO\) in Source-to-Pay Workspace](../task/now-assist-spo-summarize-record.md)

