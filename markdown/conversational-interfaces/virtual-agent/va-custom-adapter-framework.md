---
title: Creating conversational custom chat integrations in Virtual Agent
description: Conversational custom chat integration framework is a powerful framework consisting of scriptable APIs and configurations to bring the ServiceNow Virtual Agent to any conversational interface.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-03-19"
reading_time_minutes: 1
breadcrumb: [Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Creating conversational custom chat integrations in Virtual Agent

Conversational custom chat integration framework is a powerful framework consisting of scriptable APIs and configurations to bring the ServiceNow® Virtual Agent to any conversational interface.

## How custom chat integrations work

Virtual Agent Chat Server \(VACS\) supports the following chat client integration without enhancements or plugins:

-   Microsoft Teams
-   Slack
-   Workplace
-   WhatsApp
-   LINE
-   Facebook Messenger
-   Twilio
-   Alexa
-   Amazon Connect
-   Google Assistant
-   ServiceNow® Service Portal
-   ServiceNow® Now Mobile
-   Apple Messages for Business

If you're using a chat client that is not in the list, you can create a custom integration using conversational custom chat integration framework.

You can use any channels that support conversational interfaces, such as Web Portals, Mobile Apps, Slack, Microsoft Teams, SMS, and any other channel and add ServiceNow® Virtual Agent to them.

With a conversational custom chat integration, you can manage and control how your end users' chat experience. The framework helps transform messages from a chat client to VACS, and VACS back to the chat client in a format that renders well on your chat interface.

![Custom adapter framework.](../images/custom-adapter-framework.png)

The transformation is carried out through a set of Workflow Studio scripts. If you want more information on how to use Workflow Studio, see [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## Basic integration using conversational custom chat integration framework

You can use the following links to configure a basic custom chat integration.

To see an example of a custom chat integration using Telegram Messenger, see the [Telegram demo and integration](https://developer.servicenow.com/connect.do#!/share/contents/9074784_telegram_messenger3) on the ServiceNow Developer Site. \(You may need to log in to access the demo.\)

