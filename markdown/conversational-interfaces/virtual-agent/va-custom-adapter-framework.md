---
title: Creating conversational custom chat integrations in Virtual Agent
description: Conversational custom chat integration framework is a powerful framework consisting of scriptable APIs and configurations to bring the ServiceNow Virtual Agent to any conversational interface.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
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

The transformation is carried out through a set of Workflow Studio scripts. If you want more information on how to use Workflow Studio, see [Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/workflow-studio.md).

## Basic integration using conversational custom chat integration framework

You can use the following links to configure a basic custom chat integration.

To see an example of a custom chat integration using Telegram Messenger, see the [Telegram demo and integration](https://developer.servicenow.com/connect.do#!/share/contents/9074784_telegram_messenger3) on the ServiceNow Developer Site. \(You may need to log in to access the demo.\)

-   **[Create a Virtual Agent conversational custom chat integration](../task/create-adapter-for-virtual-agent.md)**  
Use the Custom Chat Configuration Integration Framework \(CCCIF\) to create a conversational custom chat integration to support third-party chat clients so they can connect to the Virtual Agent Chat Server \(VACS\).
-   **[Default input and output rich controls for a custom chat integration](../reference/default-rich-controls-va-cccif.md)**  
Input and output rich controls must be mapped to your custom chat integration in the Custom Adapter Configurations \[sys\_cs\_custom\_adapter\_config\] table. If a rich control is missing an outbound transformer implementation, a response is not served to the end user and that user may get an unsatisfactory chat experience.
-   **[Modify adapter card styles for Virtual Agent](../task/modify-adapter-card-styles.md)**  
Adapter cards are defined in the Adapter Cards \[sys\_cs\_adapter\_card\] table. Each card has a template for each supported channel to ensure it displays correctly. You can modify the channel templates to accommodate your organization's style requirements.
-   **[Supported Virtual Agent and Agent Chat features for custom chat integrations](va-features-custom-chat-integrations.md)**  
The chat integrations framework supports a multitude of Virtual Agent and Agent Chat features to provide a robust conversational experience.

**Parent Topic:**[Integrating Virtual Agent with other channels](integrate-virtual-agent.md)

