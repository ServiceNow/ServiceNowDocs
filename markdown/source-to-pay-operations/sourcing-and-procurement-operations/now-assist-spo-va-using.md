---
title: Use the Now Assist for Sourcing and Procurement Operations \(SPO\) skills in a Virtual Agent chat
description: Request the contextual generative AI capabilities by using the conversational interface in the Now Assist for Sourcing and Procurement Operations \(SPO\) in a Virtual Agent chat.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [generative AI, gen AI, genai, artificial intelligence]
breadcrumb: [Use, Now Assist for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Use the Now Assist for Sourcing and Procurement Operations \(SPO\) skills in a Virtual Agent chat

Request the contextual generative AI capabilities by using the conversational interface in the Now Assist for Sourcing and Procurement Operations \(SPO\) in a Virtual Agent chat.

As a requester, you can use the predefined topics \(chatbot conversations\) that are designed to help you complete common self-service tasks, such as buying a product or knowing the status of a purchase requisition, sourcing request, or procurement case.

As a requester, you can use the Now Assist for SPO skills in a Virtual Agent chat to search against the existing products in the product catalog or to display the available products. You can also inquire about the status of the procurement records, such as sourcing requests, purchase requisitions, procurement cases, and purchase orders.

To start a conversation, navigate to **All** &gt; **Self-Service** &gt; **Employee Center** and select the Virtual Agent chat icon \(![Chat icon.](../../supplier-lifecycle-operations/image/open-chat-window-icon.png)\).

## Using a predefined topic to buy a product

As a requester, you can start by selecting **Show all my options** as shown in the following example.

![Show all my options in the starting screen.](../../source-to-pay-operations/image/na-va-start.png "Starting screen for the Now Assist for SPO in a Virtual Agent chat")

Then, select the **Request to buy something** topic as shown in the following example.

![Request to buy something was selected in All Topics.](../image/now-assist-spo-request-buy.png "All topics in the Now Assist for SPO in a Virtual Agent chat")

You could also directly start entering the instructions. The utterance detection mechanism uses Genius Results to retrieve Virtual Agent topics, catalog items, and Q&amp;A results, and displays them to the requester within a card carousel. The following example shows the available products in the search results.

![List of products that is based on a search result.](../image/now-assist-spo-products.png "Products available based on search results")

For details, see Using Now Assist in Virtual Agent.

Virtual Agent engages you in a guided conversation, asking you relevant questions to help you submit your purchase, sourcing, and off-catalog requests, as well as procurement cases, without the need to reach out to fulfillers. You can then review and track these request records from Shopping Hub, Employee Center, or Platform.

If a product is found with or without a price in the catalog, the requester can then fill out the intake questions through a simple conversation and then submit the purchase request after reviewing the summary of responses. They can also edit a response before submitting. The following example shows a catalog conversation.

![Catalog conversation.](../../source-to-pay-operations/image/conv-catalog.png "Catalog conversation")

If a product or service isn’t found in the catalog, the chatbot gathers more information, such as checking for availability of quotes, and routes the requester to the corresponding off-catalog intake form as shown in the following example.

![Off-catalog conversation.](../../source-to-pay-operations/image/conv-off-catalog.png "Off-catalog conversation")

It also provides the requester with the option to submit a question to the procurement team about the required product or service, with relevant attachments, if any, all through a conversation.

**Note:** You can ask a question to the procurement team, and create a corresponding procurement case, only if you have the sn\_spend\_psd.requestor role. Verify that your administrator has assigned that role to you.

To learn more about quick checkout and sourcing checkout processes, see [Order a product with quick checkout](../task/order-a-product.md) and [Complete sourcing checkout](../task/complete-sourcing-checkout.md). For more information on off-catalog intake forms, see [Requesting for products or services that you don't see on ShoppingHub](request-prod-serv-dont-see-sh.md).

## Using a predefined topic to track requests

As a requester, you can inquire about the status of your recent purchase or request by selecting the **Track purchases or procurement requests** topic as shown in the following example.

![Track purchases and procurement requests.](../image/now-assis-spo-track-purchase.png)

You can inquire about the following records to the virtual agents:

-   Purchase requisition \(PR\)
-   Sourcing request \(SR\)
-   Procurement Case \(PC\)

For example, let's say that you ask whether the purchase requisition PR0001002 has already been approved as shown in the following example.

![Purchase requisition inquiry.](../../source-to-pay-operations/image/conv-pr-inquiry.png "Purchase requisition status inquiry")

The following example shows that the chatbot has provided you with the current status of the purchase requisition that you inquired about.

![Purchase requisition inquiry response.](../../source-to-pay-operations/image/conv-pr-response.png "Purchase requisition inquiry response")

You can choose either to close the conversation or check the status of another record.

## Searching for requests by specifying a time period

The Now Assist for SPO in a Virtual Agent chat also enables you to search for requests by specifying the time period when the request was opened. Here are a few examples:

-   What's the status of the purchase I made last month
-   Just send me the status of my purchases made 3 weeks ago
-   Can I get an update on the purchase I requested in August 2024

## When Virtual Agent requires more information about your request

If the Virtual Agent requires more information to search for your specific request, the following event occurs:

-   The Now Assist for SPO in a Virtual Agent chat provides you options to understand your requirement.

    For example, let's say you want to buy something as shown in the following example.

    ![Now Assist for SPO in a Virtual Agent provides you options to understand your requirement.](../image/na_disambiguation_input.png)

-   The Now Assist for SPO in a Virtual Agent chat displays the results based on your request:

    ![Now Assist for SPO in a Virtual Agent displays the result based on your request.](../image/na_disambiguation_output.png)


## When Virtual Agent has no results for your request

If the Virtual Agent is unable to search for your specific request, the following event occurs:

-   The Now Assist for SPO in a Virtual Agent chat instructs you to provide more context if the results don't meet your needs.

    `I'm sorry, I couldn't find what you needed. Could you rephrase your request or provide more context?`

-   The Now Assist for SPO in a Virtual Agent chat instructs users up to two times to rephrase their request before displaying the following message:

    ![Now Assist for SPO in a Virtual Agent chat instructs a user twice before displaying this message.](../../source-to-pay-operations/image/na-va-unable-find.png)

-   If there’s no chat activity for 900 seconds, the Now Assist for SPO in a Virtual Agent chat ends as shown in the following example.

    ![Message shown after prolonged inactivity.](../../source-to-pay-operations/image/conv-inactivity.png)


## Additional Information

Now Assist in Virtual Agent provides your users with an interactive generative AI experience. A friendly, natural language conversation is easier to understand and makes requesters more comfortable with talking to a bot. To learn how a conversation that is powered by generative AI might look in Virtual Agent, see Using Now Assist in Virtual Agent.

As an administrator, you can use the Now Assist in Virtual Agent Analytics dashboard to monitor the performance of Now Assist in Virtual Agent as a self-service deflection tool. To learn more, see Using Now Assist Analytics. Now Assist in Virtual Agent Analytics calculates the conversation deflection rate that is based on the resolution status associated with Now Assist query responses.

For detailed information on Now Assist in Virtual Agent in general, and Now Assist for SPO in particular, see [Explore Now Assist for Sourcing and Procurement Operations \(SPO\)](now-assist-spo-exploring.md).

For information on configuring Now Assist for SPO, see [Configure Now Assist for Sourcing and Procurement Operations \(SPO\)](../task/configure-now-assist-for-spo.md).

**Parent Topic:**[Use Now Assist for Sourcing and Procurement Operations \(SPO\)](now-assist-spo-using.md)

**Related topics**  


[Summarize a record by using Now Assist for Sourcing and Procurement Operations \(SPO\) in Source-to-Pay Workspace](../task/now-assist-spo-summarize-record.md)

[Summarize a record by using Now Assist for Sourcing and Procurement Operations \(SPO\) in Shopping Hub](../task/now-assist-spo-summarize-shopping.md)

[Request the generative AI capabilites in Now Assist for Sourcing and Procurement Operations \(SPO\) by using Now Assist panel](../task/request-gen-ai-capabilities-spo-now-assist-panel.md)

[Generate email responses](../task/email-response-na-spo.md)

[Analyze sentiment in procurement cases](../task/analyze-sentiments-na-spo.md)

