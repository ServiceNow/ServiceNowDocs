---
title: Virtual Agent chat widget interface for NLU
description: The Natural Language Understanding \(NLU\) Virtual Agent chat widget interface captures an automated messaging session between Virtual Agent and the user. Users can see a list of all the topics that the bot can help with, enter a request, request a transfer to a live agent, send and receive attachments, and receive visual and/or audio notifications.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Virtual Agent, chat widget, interface, Service Portal, Live Agent]
breadcrumb: [Explore, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent chat widget interface for NLU

The Natural Language Understanding \(NLU\) Virtual Agent chat widget interface captures an automated messaging session between Virtual Agent and the user. Users can see a list of all the topics that the bot can help with, enter a request, request a transfer to a live agent, send and receive attachments, and receive visual and/or audio notifications.

The chat widget interface uses the Service Portal web widget, which you can configure for custom service portals. This widget is available in the CSM, HR Service Delivery, and ITSM Service Portals.

**Note:** The information in this content is applicable to only Natural Language Understanding \(NLU\) Virtual Agent. For more information about the LLM Virtual Agent end-user experience, see [Using Now Assist in Virtual Agent](../../now-assist-in-va/concept/using-now-assist-in-va.md).

A simple conversation typically includes the following elements:

-   Default welcome message from the virtual agent, followed by the first prompt for the conversation. The initial prompt asks the user to type a question or to choose from a list of available topics.
-   User response to the first prompt. In this example, the user chooses the topic for checking an IT ticket.
-   Series of prompts, acknowledgments, and responses exchanged between the virtual agent and the user until the users reach their goals or complete their tasks. You can use different rich controls in bot prompts, for example, choice lists with buttons or a carousel of images to select an item.
-   Closing message to end the conversation.

**Note:** In the Enhanced Chat experience, feedback surveys are only triggered when a live agent is involved in the conversation. For Virtual Agent only chats, the feedback topic is not triggered by design.

When your users start a conversation with the bot, they can enter a request or see a list of everything that the bot can help with. If they choose to see everything, the chat window displays all topics available to the user. Your users can use the search box to filter the list of topics.

The conversational interface offers your users several options to manage the conversation. Users can stop the current conversation and start a new one, contact support to access a live agent for immediate assistance, and control audible alerts for chats.

![The Support options menu lets users talk to a live agent if available, call or email support, and change notification settings.](../images/ConversationOptions.png "Support options menu")

When users transfer to a live agent, the chat window header changes to indicate that they are now interacting with a live agent. The attachment and send icons are available in the chat window for uploading an image, text, or PDF file and sending it to the agent.

During live chat, users can attach a file of any type \(for example an image, text, or PDF file\) and send it to the agent. The system automatically performs a virus scan on the file attachment. If the scan is successful, the file is sent to the agent.

-   If the scan fails, a message informs the user that the scan did not pass so that the user can correct the file and then upload the file again.
-   If the upload and virus scan process times out \(the upload takes too long\), a message tells the user that the file couldn't be processed and to try the file upload again.

**Note:** Most chat clients support file attachment uploads. However, the mobile chat client only supports file attachment uploads in bot conversations. Users cannot upload files in mobile chat with a live agent.

Your users automatically receive audio and visual alerts when they receive a message from a live agent or virtual agent.

-   The visual indicator displays the number of messages received, next to the chat icon in the Service Portal window. When the user opens the chat, the indicator number closes.
-   Your authenticated end users can enable or disable audible alerts of chats through the toggle switch on the chat menu \(Contact Support\).
-   Authenticated end users can also enable or disable the delivery of notifications through the toggle switch on the chat menu \(Contact Support\).
-   The default sound notification uses the sn\_va\_web\_client\_alert.mp3 audio file.
    -   You can change the sound that requesters hear by uploading your own audio file. For details, see [Manage audio files](https://www.servicenow.com/docs/access?context=t_UploadAnAudioFile&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).
    -   To turn off the audio notification for your instance, use the system parameter `sysparm_disable_audio_notifications=true`. For example: `https://<*your-instance name*>.service-now.com/nav_to.do?sysparm_disable_audio_notifications=true`

