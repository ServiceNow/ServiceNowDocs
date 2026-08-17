---
title: Standard chat
description: ServiceNow Otto panel standard chat brings conversational support to a dynamic window where you can manage multiple active conversations and access superior search capabilities. Leverage generative AI to boost your productivity—summarize chats, cases, or incidents, request help, and generate resolution notes all in one place.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-panel-standard.html
release: zurich
topic_type: concept
last_updated: "2025-07-16"
reading_time_minutes: 5
breadcrumb: [ServiceNow Otto panel, AI Experiences, Exploring AI Admin Hub, AI Admin Hub, Enable AI experiences]
---

# Standard chat

ServiceNow Otto panel standard chat brings conversational support to a dynamic window where you can manage multiple active conversations and access superior search capabilities. Leverage generative AI to boost your productivity—summarize chats, cases, or incidents, request help, and generate resolution notes all in one place.

**Note:** Next Experience must be enabled to use the ServiceNow Otto panel standard chat. For more information, see [Considerations for activating Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/next-experience-adoption-paths.md).

Agents can use the ServiceNow Otto panel standard chat to interact with and get assistance from generative AI. On the ServiceNow Otto panel standard chat, you can increase your productivity and efficiency by using the generative AI experience to summarize a chat, case, incident, or generate resolution notes.

Conversational aspects of the panel, such as skill detection, are powered by Now LLM Service.

**Note:** ServiceNow Otto skills must be enabled to appear on the ServiceNow Otto panel standard chat. For more information, see [ServiceNow Otto skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skills/now-assist-skills.md).

Let's get started by selecting the ServiceNow Otto icon \[Omitted image "bus-ai-otto.svg"\] Alt text: to display the ServiceNow Otto panel standard chat.\[Omitted image "otto-panel-icon.png"\] Alt text:

If a number in a square appears, it indicates how many messages you missed when the ServiceNow Otto panel standard chat was closed.

\[Omitted image "now-assist-panel-screenshot-2.png"\] Alt text: ServiceNow Otto panel standard chat with callouts.

\[Omitted image "now-assist-panel-chats.png"\] Alt text: ServiceNow Otto panel standard chat showing active chats, updates, and closed chats.

The ServiceNow Otto panel standard chat includes:

<table id="table_yzf_wkw_hzb"><thead><tr><th>

Item number

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 - Enter modal button

</td><td>

Expands the chat into a 90% screen-size window.

</td></tr><tr><td>

2 - \[Omitted image "now-assist-panel-pushpin.png"\] Alt text: Pushpin icon

</td><td>

Positions, or pins, the ServiceNow Otto panel standard chat to the screen.

</td></tr><tr><td>

3 - Display chats button

</td><td>

Displays the Chats window.

</td></tr><tr><td>

4 - Option buttons

</td><td>

Displays the available options.

</td></tr><tr><td>

5 - Copy message button

</td><td>

Copies the ServiceNow Otto panel standard chat message.

</td></tr><tr><td>

6 - Reply to ServiceNow Otto panel... field

</td><td>

Enter actions.

</td></tr><tr><td>

Voice Input

 \[Omitted image "now-assist-panel-voice-input.png"\] Alt text: Voice input microphone on the panel.

</td><td>

If Voice Input is activated, select the microphone icon or the keyboard shortcut to use your voice to interact with the ServiceNow Otto panel standard chat. After you speak, there’s a pause while the system transcribes the text and then displays it on the screen. See [Enable voice input](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-voice-input-for-now-assist-panel.md) for information on enabling Voice Input. See [Next Experience keyboard shortcuts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/next-experience-keyboard-shortcuts.md) for the ServiceNow Otto menu \(Voice Input mode\) shortcuts for Microsoft and macOS.

</td></tr><tr><td>

8 - Active chats

</td><td>

All active chats display in the Active chats section. in the Active chats section of the ServiceNow Otto panel standard chat. You can create additional chats by selecting the + icon in the heading.

</td></tr><tr><td>

9 - Updates

</td><td>

Displays important updates and reminders.

</td></tr><tr><td>

10 - Closed chats

</td><td>

Displays all closed chats. If you select one of the closed chats, you can see that chat's history.

</td></tr></tbody>
</table>ServiceNow Otto panel standard chat is available on Next Experience and ServiceNow Studio. The following screenshots show the ServiceNow Otto panel standard chat in a workspace and on Core UI screens under Next Experience.

<table id="table_smr_n2b_xyb"><tbody><tr><td>

Next Experience

</td><td>

Core UI

</td></tr><tr><td>

\[Omitted image "now-assist-panel-overview-example.png"\] Alt text: ServiceNow Otto panel standard chat on Next Experience.

</td><td>

\[Omitted image "now-assist-panel-overview-ui16-example.png"\] Alt text: ServiceNow Otto panel standard chat on a Core UI incident form.

</td></tr></tbody>
</table>## Navigating from the ServiceNow Otto panel standard chat

Navigate from the ServiceNow Otto panel standard chat without leaving the current conversation by entering a navigation request in the **Ask ServiceNow Otto to...** field. If you enter "navigate me to active incidents," the ServiceNow Otto panel standard chat displays a button that enables you to view the active incidents.

## Chat summarization

Quickly learn the details of a chat by reading a chat summarization. The chat summarization gives you enough details about the chat so that your requester doesn't have to repeat the same information to you.

To generate a chat summarization from the ServiceNow Otto panel standard chat, select **Chat Summarization** or enter `summarize chat` in the **Ask ServiceNow Otto to** field.

**Note:** You can also generate a chat summarization by using the `/summarize` quick action in Agent Chat.

## Case or incident summarization

Quickly learn the details of a case or incident by reading a case summarization. The summarization gives you enough details about the interaction so that your requester doesn't have to repeat the same information to you.

You can generate a case or incident summarization from the ServiceNow Otto panel standard chat for ServiceNow Otto for CSM, ServiceNow Otto for HRSD, or ServiceNow Otto for ITSM:

-   For ServiceNow Otto for CSM, select **Summarize record** or enter `summarize a record` in the **Ask ServiceNow Otto to** field.
-   For ServiceNow Otto for HRSD, select **Summarize record** or enter `summarize a record` in the **Ask ServiceNow Otto to** field.
-   For ServiceNow Otto for ITSM, select **Summarize incident** or enter `summarize an incident` in the **Ask ServiceNow to** field.

## Conversation Help

Get specific and accurate answers to your queries by using the Get Help skill option on the ServiceNow Otto panel standard chat. This skill is available to everyone entitled to ServiceNow Otto capabilities.

For more information about the ServiceNow Otto Conversational Help skill which represents as Get Help on the ServiceNow Otto panel standard chat, see [Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skills/conversational-help-skills.md).

## Resolution notes generation

Quickly learn the details of how an interaction was resolved by generating and reading resolution notes.

To generate resolution notes from the ServiceNow Otto panel standard chat, select **Generate resolutions notes** or enter `generate resolutions notes` in the **Ask ServiceNow Otto to** field.

## Streaming responses

After you enter a question or request on the ServiceNow Otto panel standard chat, ServiceNow Otto gathers information from multiple sources. These sources may include Knowledge Base articles, external content, product documentation, catalog items, and workflows and combines them into a synthesized, comprehensive answer. Instead of waiting for the entire message to render, the synthesized response streams in real time and stops streaming after the entire message has been delivered. An animated sparkle icon \(\[Omitted image "bus-ai-otto.svg"\] Alt text:\) appears while the response is generated and changes to the static sparkle icon after the response has fully loaded.

**Parent Topic:**[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-panel-overview.md)

