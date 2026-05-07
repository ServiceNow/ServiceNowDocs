---
title: Integrate Customer Service Management Virtual Agent with Facebook Messenger \(Legacy\)
description: Integrate the Customer Service Virtual Agent with Facebook Messenger to enable bot conversations in the messenger.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chat channel, Enable communication channels, Configure, Customer Service Management]
---

# Integrate Customer Service Management Virtual Agent with Facebook Messenger \(Legacy\)

Integrate the Customer Service Virtual Agent with Facebook Messenger to enable bot conversations in the messenger.

## Before you begin

Role required: virtual\_agent\_admin or admin

-   Install the Customer Service \(com.sn\_customerservice\) plugin.
-   Install the Customer Service Virtual Agent Conversations plugin \(com.sn\_csm.virtualagent\).
-   Make sure Virtual Agent is integrated with Facebook Messenger.
-   Make sure you have the token and secret for the messenger.

For information on integrating the Virtual Agent with Facebook Messenger and for retrieving the messenger token and secret, see [Set up Virtual Agent integration for consumer messaging apps](https://www.servicenow.com/docs/access?context=va-integration-messaging-apps&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## About this task

With this integration, you can get help using Virtual Agent chatbot conversations. For more information on getting help, see [Customer Service Virtual Agent conversations](../concept/csm-virtual-agent-chatbot.md) .

## Procedure

1.  In the application navigator, enter `sys_cs_adapter_configuration_page_messenger_list.do`

2.  Select **sample-fb-messenger-app**.

    You have to be in the **Customer Service Virtual Agent Conversations** application to edit the record.

3.  In the **Messenger Page ID** field, enter your company's Facebook page ID.

4.  Right-click and select **Save**.

5.  In the **Provider Auth** field, click the information icon and open the **Message Auth** record:

    -   Go to the **Outbound message creation** field, click the information icon and open the **Token Verification** record.
    -   In the **Token** field, enter the token for the messenger application.
    -   Click **Update**.
6.  In the **Message Auth** record:

    -   Go to the **Inbound message verification** field, click the information icon, and open the **Hash Message Verification** record.
    -   In the **Secret** field, enter the app secret for the messenger application.
    -   Click **Update**.

