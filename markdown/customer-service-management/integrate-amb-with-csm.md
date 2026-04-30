---
title: Integrating Apple Messages for Business with Customer Service Management
description: Deliver a pre-integrated chat conversation experience with the Conversational Integration with Apple Messages for Business app for consumers and customer contacts. Integrate Apple Messages for Business by using the ServiceNow Conversational Integration with Apple Messages for Business application.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating with consumer messaging apps, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Integrating Apple Messages for Business with Customer Service Management

Deliver a pre-integrated chat conversation experience with the Conversational Integration with Apple Messages for Business app for consumers and customer contacts. Integrate Apple Messages for Business by using the ServiceNow® Conversational Integration with Apple Messages for Business application.

As an administrator, if you have configured the Conversational Integration with Apple Messages for Business application, then your customer contacts and consumers can initiate a Apple Messages for Business chat conversation with a virtual agent or live agent. An agent can accept a conversation initiated from a Apple Messages for Business chat conversation. For more information, see [Conversational Integration with Apple Messages for Business](https://www.servicenow.com/docs/access?context=integration-apple-mssg&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US). Refer to the Apple [documentation](https://register.apple.com/resources/messages/messaging-documentation/) for more details about Apple Messages for Business.

**Note:** As an administrator, you can also use any predefined Customer Service Virtual Agent conversations to capture information from customer contacts or consumers. For more information, see [Customer Service Virtual Agent conversations](csm-virtual-agent-chatbot.md).

Key features of the integration include the following:

-   Customers can initiate Apple Messages for Business chat conversations with a virtual agent or live agent.
-   Use the chat to search for articles in community posts and knowledge articles, access service catalogs, or create a customer service case.
-   View the Apple Messages for Business chat conversation details from which a work item was initiated in Agent Workspace.
-   Indicate your presence in the Agent Workspace Inbox with the Apple Messages for Business service channel.

## Example workflow

In this example workflow, the Conversational Integration with Apple Messages for Business application is used to resolve a consumer issue:

1.  A customer wants to get a replacement credit card, and initiates a Apple Messages for Business chat conversation on iMessage using the Virtual Agent bot.
2.  The Customer Service Management application identifies the customer and starts an interaction of type **Messaging**.
3.  The customer is presented with a list of credit card options that they own and picks that card that they want to replace.
4.  A form opens and asks about the reason for replacement, date lost, address, and phone number. The customer submits the form.
5.  The customer selects the iMessage app to schedule the delivery.
6.  The replacement card is scheduled to arrive in 3-5 business days.
7.  The customer additionally wants to know about home refinance options, and is shown links on refinancing.
8.  The customer then selects to chat with a live agent.
9.  A live agent schedules a call back with a mortgage specialist. The Customer Service Management application starts another interaction of type **Messaging**.
10. The customer sends feedback on the interaction using the quick reply action.

## End users and roles

Users with the roles listed in the following table can use the Conversational Integration with Apple Messages for Business application.

|Roles|Tasks|
|-----|-----|
|agent\_workspace\_user|Accept an ongoing Apple Messages for Business chat conversation with a customer through the Apple Messages for Business service channel in Advanced Work Assignment.|
|sn\_customerservice\_manager|View details of a Apple Messages for Business chat conversation by using interaction records of type **Messaging** and subtype Apple.|
|sn\_customerservice.consumer, sn\_customerservice.customer|Initiate Apple Messages for Business chat conversations with a virtual agent or live agent so that you can search for articles in Communities and Knowledge Management, access service catalogs, and create a customer service case.|

