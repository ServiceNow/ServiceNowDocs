---
title: Integrating WhatsApp with Customer Service Management through Twilio
description: Deliver a pre-integrated chat conversation experience with the WhatsApp messaging app for consumers and customer contacts. Integrate WhatsApp by using the ServiceNow Conversational Integration with WhatsApp \(powered by Twilio\) application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Integrating WhatsApp with Customer Service Management through Twilio

Deliver a pre-integrated chat conversation experience with the WhatsApp messaging app for consumers and customer contacts. Integrate WhatsApp by using the ServiceNow® Conversational Integration with WhatsApp \(powered by Twilio\) application.

As an administrator, if you have configured the Conversational Integration with WhatsApp \(powered by Twilio\) application, then your customer contacts and consumers can initiate a WhatsApp chat conversation with a virtual agent or live agent. An agent can initiate a conversation or accept a conversation initiated from a WhatsApp chat conversation. For more information, see Configure Conversational Integration with WhatsApp \(powered by Twilio\).

**Note:** As an administrator, you can also use any predefined Customer Service Virtual Agent conversations to capture information from customer contacts or consumers. For more information, see [Customer Service Virtual Agent conversations](csm-virtual-agent-chatbot.md).

Key features of the integration include the following:

-   Initiate WhatsApp chat conversations with a virtual agent, live agent, or customer.
-   Use the chat to search for articles in community posts and knowledge articles, access service catalogs, or create a customer service case.
-   View the WhatsApp chat conversation details from which a work item was initiated in Agent Workspace.
-   Indicate your presence in the Agent Workspace Inbox with the WhatsApp service channel.
-   Make outbound chat conversations to connect with a customer's WhatsApp chat conversation, and automatically capture interaction details to simplify data entry.

## Example workflows

The following example workflow shows the use of the Conversational Integration with WhatsApp \(powered by Twilio\) application in resolving a consumer issue:

1.  A customer has an issue with a product and initiates a WhatsApp chat conversation using the Virtual Agent bot.
2.  The Customer Service Management application identifies the customer and starts an interaction of type **Messaging**.
3.  The customer selects the product and views the knowledge articles associated with the product.
4.  The customer then selects to chat with a live agent.
5.  A live agent accepts the customer request. The Customer Service Management application starts another interaction of type **Messaging**.
6.  The live agent creates a case on the product, and then closes the conversation.

The following example workflow shows the use of the Conversational Integration with WhatsApp \(powered by Twilio\) application in addressing customer feedback:

1.  A customer purchases a new product and opts in to receive notifications from your business on the WhatsApp app.
2.  The customer receives a welcome message from customer support.
3.  After two months, the customer receives another message asking for feedback on the product.
4.  The customer shares negative feedback.
5.  An agent reviews the feedback and starts a conversation with the customer to offer help and find out more about the customer’s experience with the product.

## End users and roles

The users with the roles listed in the following table can use the Conversational Integration with WhatsApp \(powered by Twilio\) application.

|Roles|Tasks|
|-----|-----|
|agent\_workspace\_user|Accept an ongoing WhatsApp chat conversation with a customer through the WhatsApp service channel in Advanced Work Assignment.|
|sn\_customerservice\_manager|View details of a WhatsApp chat conversation by using interaction records of type **Messaging** and subtype **WhatsApp**.|
|sn\_customerservice.consumer, sn\_customerservice.customer|Initiate WhatsApp chat conversations with a virtual agent or live agent so that you can search for articles in Communities and Knowledge Management, access service catalogs, and create a customer service case.|

