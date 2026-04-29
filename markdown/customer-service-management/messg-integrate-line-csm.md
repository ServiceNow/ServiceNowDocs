---
title: Integrating LINE with Customer Service Management
description: Deliver a pre-integrated chat conversation experience with the LINE messaging app for consumers and customer contacts. Integrate LINE with the ServiceNow Conversational Integration with LINE application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Integrating LINE with Customer Service Management

Deliver a pre-integrated chat conversation experience with the LINE messaging app for consumers and customer contacts. Integrate LINE with the ServiceNow® Conversational Integration with LINE application.

As an administrator, if you have configured the Conversational Integration with LINE application, your customer contacts and consumers can initiate a LINE chat conversation with a virtual agent or live agent. An agent can initiate a conversation or accept a conversation initiated from a LINE chat conversation. You can configure system-initiated messages to be sent to the customer. For more information, see [Configure Conversational Integration with LINE](https://www.servicenow.com/docs/access?context=messg-line-configure&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

**Note:** As an administrator, you can also use any predefined Customer Service Virtual Agent conversations to capture information from customer contacts or consumers. For more information, see [Customer Service Virtual Agent conversations](csm-virtual-agent-chatbot.md).

Key features of the integration include the following:

-   Initiate LINE chat conversations with a virtual agent, live agent, or customer.
-   Use the chat to search for articles in community posts and knowledge articles, access service catalogs, or create a customer service case.
-   View the LINE chat conversation details from which a work item was initiated in Agent Workspace.
-   Indicate your presence in the Agent Workspace Inbox with the Line service channel.
-   Make outbound chat conversations to connect with a LINE chat conversation from a customer contact or consumer, and automatically capture interaction details to simplify data entry.

## Example workflows

The following example workflow shows the use of the Conversational Integration with LINE application in helping a customer to resolve an issue with the recently purchased router:

1.  The customer initiates a LINE chat conversation using the Virtual Agent bot.
2.  The Customer Service Management application identifies the customer and starts an interaction of type **Messaging**.
3.  The customer selects the router as a product and finds knowledge articles associated with it.
4.  The customer ends the conversation because the issue was resolved with the help of a knowledge article.

The following example workflow shows the use of the Conversational Integration with LINE application in addressing customer feedback:

1.  A customer purchases a new product and opts in to receive notifications from your business on the LINE app.
2.  The customer receives a welcome message from customer support.
3.  After two months, the customer receives another message asking for feedback on the product.
4.  The customer shares negative feedback.
5.  An agent reviews the feedback and starts a conversation with the customer to offer help and find out more about the customer’s experience with the product.

## End users and roles

Users with the roles listed in the following table can use the Conversational Integration with LINE application.

|Roles|Tasks|
|-----|-----|
|agent\_workspace\_user|Accept an ongoing LINE chat conversation with a customer through the LINE service channel in Advanced Work Assignment.|
|sn\_customerservice\_manager|View details of a LINE chat conversation by using interaction records of type **Messaging** and subtype **Line**.|
|sn\_customerservice.consumer, sn\_customerservice.customer|Initiate LINE chat conversations with a virtual agent or live agent so that you can search for articles in Communities and Knowledge Management, access service catalogs, and create a customer service case.|

