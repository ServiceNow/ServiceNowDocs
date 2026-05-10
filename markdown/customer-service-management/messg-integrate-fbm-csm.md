---
title: Integrating Facebook Messenger with Customer Service Management
description: Integrate Facebook Messenger chat conversations with your ServiceNow instance so that consumers and customer contacts can communicate with your business using the Conversational Integration with Facebook Messenger application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating with consumer messaging apps, Integrate, Customer Service Management]
---

# Integrating Facebook Messenger with Customer Service Management

Integrate Facebook Messenger chat conversations with your ServiceNow® instance so that consumers and customer contacts can communicate with your business using the Conversational Integration with Facebook Messenger application.

As an administrator, if you have configured the Conversational Integration with Facebook Messenger application, your customer contacts and consumers can initiate a Facebook Messenger chat conversation with a virtual agent or live agent. An agent can accept a conversation initiated from a Facebook Messenger chat conversation. For more information, see [Configure Conversational Integration with Facebook Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/messg-fbm-configure.md).

**Note:** As an administrator, you can also use any predefined Customer Service Virtual Agent conversations to capture information from customer contacts or consumers. For more information, see [Customer Service Virtual Agent conversations](csm-virtual-agent-chatbot.md).

## Key features

-   **Customer experience**

    Initiate Facebook Messenger chat conversations with a virtual agent or live agent to search for articles in community posts and knowledge articles, access service catalogs, or create a customer service case.

-   **Agent experience**
    -   View the Facebook Messenger chat conversation details from which the work item was initiated in Agent Workspace after accepting a work item associated with the Facebook Messenger service channel.
    -   Indicate your presence in the Agent Workspace Inbox with the Facebook Messenger service channel.
    -   Make outbound chat conversations to connect with a Facebook Messenger chat conversation from a customer contact or consumer and automatically capture interaction details to simplify data entry.

## End users and roles

Users with the roles listed in the following table can use the Conversational Integration with Facebook Messenger application.

|Roles|Tasks|
|-----|-----|
|agent\_workspace\_user|Accept an ongoing Facebook Messenger chat conversation with a customer through the Facebook Messenger service channel in Advanced Work Assignment.|
|sn\_customerservice\_manager|View details of a Facebook Messenger chat conversation using the interaction record of the type as **Messaging** and subtype as **Facebook Messenger**.|
|sn\_customerservice.consumer, sn\_customerservice.customer|Initiate Facebook Messenger chat conversations with a virtual agent or live agent to search for articles in Communities and Knowledge Management, access service catalogs, and create a customer service case.|

## Example workflow

The following example workflow shows the use of the Conversational Integration with Facebook Messenger application in helping a customer to resolve an issue with the recently purchased router:

1.  The customer initiates a Facebook Messenger chat conversation using the Virtual Agent bot.
2.  The Customer Service Management application identifies the customer and starts an interaction of type **Messaging**.
3.  The customer selects the router as a product and finds knowledge articles associated with it.
4.  The customer ends the conversation because the issue was resolved with the help of a knowledge article.

