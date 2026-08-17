---
title: Use the ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) skills in a Virtual Agent chat
description: ServiceNow Otto is a chat assistant that helps you complete procurement tasks through conversation. Instead of navigating forms or contacting procurement staff, you can use ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) to request products, track orders, and get help with procurement questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-va-using.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-07-30"
reading_time_minutes: 5
keywords: [generative AI, gen AI, genai, artificial intelligence]
breadcrumb: [Use ServiceNow Otto for SPO, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Use the ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) skills in a Virtual Agent chat

ServiceNow Otto is a chat assistant that helps you complete procurement tasks through conversation. Instead of navigating forms or contacting procurement staff, you can use ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) to request products, track orders, and get help with procurement questions.

**Note:** ServiceNow Otto for SPO uses generative AI to interpret your requests and generate responses. Results may not always be accurate. Review any procurement information before submitting a request.

## Start a conversation with ServiceNow Otto for SPO

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.
2.  Select the Virtual Agent chat icon \(\[Omitted image "agentic-ai-now-assist-icon.png"\] Alt text:\).
3.  In the chat, select a suggested topic or type what you need.

\[Omitted image "image.otto-spo-chat"\] Alt text: ServiceNow Otto Virtual Agent.

ServiceNow Otto for SPO interprets conversational input, so you can phrase requests different ways. For example:

-   `I need to buy office supplies`
-   `I want to order a desk lamp`
-   `Show me how to request a product`

For more information, see [Using ServiceNow® Otto for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/using-now-assist-in-va.md).

## Request and buy a product

You can make a purchase through the guided conversation in ServiceNow Otto for SPO.

1.  Select the Virtual Agent chat icon \(\[Omitted image "agentic-ai-now-assist-icon.png"\] Alt text:\).
2.  In the chat, type a message such as `I want to buy a product` or `Show me how to request something`.
3.  ServiceNow Otto for SPO displays matching options in a card carousel.
4.  Select the option that matches what you need.

If the product is in your catalog:

1.  ServiceNow Otto for SPO prompts you for purchase details, including quantity, delivery location, delivery date, and reason.
2.  Answer each question in the chat.
3.  After you answer all questions, ServiceNow Otto for SPO displays a summary of your request.
4.  Select **Submit** to complete the purchase request.

You can then track this request from Shopping Hub, Employee Center, or the Platform home page.

To learn more about quick checkout and sourcing checkout processes, see [Order a product with quick checkout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/order-a-product.md) and [Complete sourcing checkout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/complete-sourcing-checkout.md).

If the product is not in your catalog:

1.  ServiceNow Otto for SPO gathers information about what you need.
2.  ServiceNow Otto for SPO checks whether the product has a quote available.
3.  If a quote is found, ServiceNow Otto for SPO routes you to request the item.
4.  If no quote is found, ServiceNow Otto for SPO provides a form to submit an off-catalog request.

For more information on off-catalog intake forms, see [Requesting for products or services that you don't see on ShoppingHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/request-prod-serv-dont-see-sh.md).

## Ask the procurement team a question

If you need help with a product or have a question, you can submit it directly to your procurement team through the chat.

**Note:** You need the sn\_spend\_psd.requester role to submit questions to the procurement team. Check with your administrator if you are not sure whether you have this role.

To submit a question:

1.  In the chat, describe what you need or type your question.
2.  Attach documents if relevant.
3.  Select **Submit**.

ServiceNow Otto for SPO creates a procurement case with your question and attachments. Your procurement team reviews and responds.

## Track your orders and requests

Check the status of your purchases at any time through ServiceNow Otto for SPO.

1.  Select the Virtual Agent chat icon \(\[Omitted image "agentic-ai-now-assist-icon.png"\] Alt text:\).
2.  In the chat, type a message such as `Track my order` or `Show me my requests`.
3.  ServiceNow Otto for SPO prompts you to select what you want to track:
    -   Check status of procurement request
    -   Procurement request tracking AI agent
4.  ServiceNow Otto for SPO displays your recent records with status. Select any record to see more details.

## Related resources

To learn how a conversation powered by generative AI works in Virtual Agent, see [Using ServiceNow® Otto for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/using-now-assist-in-va.md).

As an administrator, you can use the ServiceNow Otto for Virtual Agent Analytics dashboard to monitor the performance of ServiceNow Otto for Virtual Agent as a self-service deflection tool. To learn more, see [Using AI Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/using-now-assist-analytics.md). The dashboard calculates the conversation deflection rate based on the resolution status associated with ServiceNow Otto query responses.

For detailed information on ServiceNow Otto for SPO, see [Explore ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-exploring.md).

For information on configuring ServiceNow Otto for SPO, see [Configure ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-now-assist-for-spo.md).

**Parent Topic:**[Use ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo-using.md)

**Related topics**  


[Summarize a procurement record in Source-to-Pay Workspace]()

[Summarize a procurement record in Shopping Hub]()

[Request the generative AI capabilites in ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) by using ServiceNow Otto panel]()

[Analyze sentiment in procurement cases]()

[Generate an email response for procurement cases]()

