---
title: Enhanced chat
description: Now Assist panel enhanced chat is a conversational support experience within a dynamic window that also includes the ability to have multiple active conversations and superior search capabilities. Use Now Assist panel enhanced chat to improve your productivity and efficiency by leveraging generative AI to perform tasks such as summarize a chat, case, or incident, request help, generate resolution notes, among others.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Now Assist panel, Now Assist Experiences, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Enhanced chat

Now Assist panel enhanced chat is a conversational support experience within a dynamic window that also includes the ability to have multiple active conversations and superior search capabilities. Use Now Assist panel enhanced chat to improve your productivity and efficiency by leveraging generative AI to perform tasks such as summarize a chat, case, or incident, request help, generate resolution notes, among others.

Agents can use the Now Assist panel enhanced chat to interact with and get assistance from generative AI. You can move the chat window by selecting the header and dragging the chat window to the desired location. You can resize the chat window by using the window's edges to resize to your desired size or use the toolbar icons.

Conversational aspects of the Now Assist panel, such as skill detection, are powered by Now LLM Service.

**Note:** To use the full capabilities of Now Assist panel enhanced chat, AI Search must be enabled for your portal. Without it, Now Assist panel enhanced chat functions in a limited capacity. Basic conversational interactions such as predefined topic flows and simple questions and answers are available, but knowledge article retrieval, AI responses grounded in instance content, and semantic search capabilities require AI Search. For more information, see [Enable and configure AI Search in Service Portal](https://www.servicenow.com/docs/access?context=enable-ais-sp&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

## Prerequisites

You must fulfill the following conditions before using the Now Assist panel enhanced chat:

-   Next Experience must be enabled. For more information, see [Considerations for activating Next Experience](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).
-   You must have the now\_assist\_panel\_user role.
-   Your role must be applied to at least one active Now Assist skill to use skills in the Now Assist panel.
-   Now Assist panel enhanced chat must be activated before you can use it. See [Activate Now Assist panel enhanced chat](../task/now-assist-panel-enhanced-activate.md) for more information.
-   Now Assist skills must be enabled to appear on the Now Assist panel. For more information, see [Now Assist skills](../../now-assist-skills/concept/now-assist-skills.md).
-   If you want to use assistants, you must activate them. See [Activate Now Assist panel assistants](../task/now-assist-panel-activate-assistant.md) for information on activating assistants.
-   If you want to use voice input, you have to enable voice input [Enable voice input for Now Assist panel](../../now-assist-admin/task/enable-voice-input-for-now-assist-panel.md).

    **Note:** Voice input is automatically activated when you activate the Now Assist panel. As of the Zurich Patch 4 release, voice input is configured in the [Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).


## Now Assist panel enhanced chat overview

Let's get started by selecting the Now Assist icon ![Now Assist sparkle icon](../../../common/image/icon-ai-sparkle.png) to display the Now Assist panel.

![Now Assist panel - enhanced chat](../images/na-panel-screenshot-example-enhanced.png "Now Assist panel")

![Now Assist panel - enhanced chat showing active and closed chats.](../images/na-panel-closed-chat-enhanced.png)

The Now Assist panel includes:

<table id="table_yzf_wkw_hzb"><thead><tr><th>

Item number

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 - ![Expand icon.](../images/na-panel-expand-icon.png)

</td><td>

Expands the chat into a 90% screen-size window. The 90% screen-size window can’t be resized or moved. Selecting the icon again resizes the chat back into the floating window.

</td></tr><tr><td>

2 - ![Pushpin icon.](../images/na-panel-pin-enhanced.png)

</td><td>

Positions, or pins, the Now Assist panel to the screen.

</td></tr><tr><td>

3 - Option buttons

</td><td>

Displays the available options.

</td></tr><tr><td>

4 - Reply to Now Assist...

</td><td>

Enter actions.

</td></tr><tr><td>

5 - Now Assist message

</td><td>

Indicates that the answers are generated by AI.

</td></tr><tr><td>

6 - Active chats

</td><td>

All active chats display in the Active chats section. in the Active chats section of the Now Assist. You can create additional chats by selecting the + icon in the heading.

</td></tr><tr><td>

7 - Closed chats

</td><td>

Displays all closed chats. If you select a closed chat, the chat's history displays.

</td></tr></tbody>
</table>The Now Assist subheader consists of these elements:

![Chat window controls include New Chat, Chats, Support, and Settings.](../images/na-panel-chat-controls-enhanced.png)

<table id="table_qzq_r2c_qfc"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Chats \(![Chats icon.](../images/na-panel-hamburger-icon.png)\)

</td><td>

All chats appear.

 Chats are organized with the most recent conversations at the top. Selecting a chat opens the chat in the conversation area. If there are unread chats or notifications, a badge number appears on the Chats icon \(![List icon.](../images/na-panel-hamburger-icon.png)\). Any unread chat or notification appears with a red dot next to it and the chat title appears in bold. Additionally, if you switch to a new chat while another active chat is ongoing, a pop-up message on the Chats icon \(![List icon.](../images/na-panel-hamburger-icon.png)\) appears: `Your previous chat was saved. You can revisit all of your past chats and continue ones that are still active.` The following list includes the chat sections that you may see in the chats area.

 -   Active: Chats where you can continue the conversation. If applicable, active chats move to the Closed chats section after two hours of inactivity. This 2 hour time limit can be configured within the Messaging Channels \{sys\_cs\_channel.list\} table. To change the inactivity time limit, from the Messaging Channels \{sys\_cs\_channel.list\} table, select the **NASS** record and populate the **Conversation Idle Timeout** field with your preferred active chat time limit. If you have no active chats, `No chatter at the moment` is displayed. If more than 12 active chats are running, a **Show more** link appears to view more chats. Selecting **Show more** displays an additional 10 chats.
-   Updates: Updates for important notifications and reminders can be configured to display. When **sn\_nowassist\_va.nass\_notification\_enabled** is set to `true` \(the default\), simple \(nonactionable\) Now Assist panel notifications appear on your portal home page. After selecting a notification, you’re redirected to this Updates section. If you have no updates, `You're all caught up` is displayed. If more than four updates are available, a **Show more** link appears to view more updates. Selecting **Show more** displays an additional 10 updates.

**Note:** If **sn\_nowassist\_va.nass\_notification\_enabled** is set to `false`, the Updates section doesn't appear.

-   Closed: Closed chats can be configured to display. A message closes when the designated time has passed \(2 hours of inactivity\) or you receive the following response in the chat: `It looks like you're finished with this chat, so I'll go ahead and close it.` Turn on closed chats by selecting the **Show closed chats** check box within **Conversational Interfaces** &gt; **Assistants** &gt; **\[Selected Assistant Name\]** &gt; **Chat experience** &gt; **Closed chats**. After being turned on, closed chats are displayed for as long as they’re available within the Conversations \(sys\_cs\_conversation\) table. Closed chats appear in a read-only mode and can’t become active again. If more than four closed chats are available, a **Show more** link appears to view more closed chats. Selecting **Show more** displays an additional 10 closed chats. After a conversation has closed, you can’t reopen it.Hovering over a closed chat displays the delete icon \(\). Confirm the chat deletion on the Delete this chat? modal to permanently delete the chat from the interface.

</td></tr><tr><td>

2. \[Chat name\]

</td><td>

The name of the conversation.

 If you select a promoted asset or query, that asset's title appears as the chat name. If instead you enter an utterance into the **Reply to Now Assist** field, your initial utterance becomes the chat name. The chat name appears in both the Now Assist subheader and **Chats list** &gt; **Active** section.

</td></tr><tr><td>

3. New chat \(![New chat icon.](../images/na-panel-new-chat-icon.png)\)

</td><td>

A new conversation begins.

 You may be prompted with a greeting message along with any promoted conversational assets such as topics, subflows, and/or actions, or suggested queries.

</td></tr><tr><td>

4. Feedback icons panel

</td><td>

You can indicate if the response was helpful by selecting the like thumbs up icon ![](../images/nap-thumbs-up.png) or if the response wasn't helpful, you can select the dislike thumbs down icon ![](../images/nap-thumbs-down.png). You can also copy the response by selecting the copy message icon ![](../images/nap-copy-icon.png).

</td></tr></tbody>
</table>Now Assist panel is available on Next Experience and ServiceNow Studio. The following screenshots show the Now Assist panel in a workspace and on Core UI screens under Next Experience.

<table id="table_smr_n2b_xyb"><tbody><tr><td>

Next Experience

</td><td>

Core UI

</td></tr><tr><td>

![Now Assist panel enhanced chat on Next Experience](../images/na-panel-overview-example-enhanced.png)

</td><td>

![Now Assist panel on a Core UI incident form.](../images/now-assist-panel-overview-ui16-example.png)

</td></tr></tbody>
</table>## Response feedback

Each Virtual Agent response includes a feedback icons panel. The feedback icons panel appears on the latest Virtual Agent response and whenever you hover over any Virtual Agent response. You can indicate if the response was helpful by selecting the like thumbs up icon \(![image.llm-thumbs-up-like]\). If the response wasn't helpful, select the dislike thumbs down icon \(![image.llm-thumbs-down-dislike]\). When you select the thumbs up or thumbs down icon, you are prompted to provide detailed feedback by selecting one or more reason check boxes. You can also select **Other** to add comments or suggestions \(up to 300 characters\). After making your selection, select **Submit** to submit your feedback or select **X** to close the dialog without submitting feedback. All submitted feedback is captured, stored, and made available through analytic dashboards.

![Thumbs down granular feedback dialog.](../../now-assist-in-va/image/feedback-panel-granular.png "Example of additional feedback panel from thumbs down icon")

Depending on the context of the response, an additional go to search results icon \(![Go to search results icon.](../../now-assist-in-va/image/nass-search-result-icon.png)\) may appear in the feedback icons panel. This icon appears alongside synthesized responses in Virtual Agent, clarifying questions in Virtual Agent, and regular search results or Virtual Agent fallback topics whenever a synthesized response is unavailable. Selecting the go to search results icon \(![Go to search results icon.](../../now-assist-in-va/image/nass-search-result-icon.png)\) redirects you to the search results page and begins a search query using the last five chat utterances you entered.Additionally, a copy message icon \(![](../../now-assist-in-va/image/dw-feedback-copy-message-icon.png)\) appears on received Virtual Agent responses.

## Agentic conversations

**Note:** Admins must first enable AI agents before end users can experience agentic conversations. Now Assist panel discovers and executes agentic workflows. For more information on agentic workflows, see [Now Assist agentic workflows](../../now-assist-ai-agents/concept/sn-aia-use-cases-list.md) and [Multiple conversations in Now Assist AI agents](../../now-assist-ai-agents/concept/multiple-conversations-aia.md).

When you ask a question to the Now Assist panel enhanced chat, the agent understands the query and begins a flow. When you submit a message with multiple questions or requests, Now Assist panel enhanced chat answers the multiple questions consecutively in its response. It can reason, plan, and execute across AI agents, Now Assist panel topics, conversational actions and subflows, catalogs, Knowledge Base articles, custom skills, and any Now Assist supported skills to help you. You receive on-screen messages to let you know where the agent is in the agentic processing flow prior to receiving the response. After the processing has completed its flow, a View AI Steps section header appears, where the processing flow steps can be expanded and viewed. You can stop the agentic processing flow at any time by selecting the End flow icon \(![End flow icon.](../../now-assist-in-va/image/agentic-end-flow-icon.png)\). After an action starts, it can't be stopped. Selecting the End flow icon only stops the proceeding processing steps.

## Navigating from the Now Assist panel

You can navigate from the Now Assist panel without leaving the current conversation by entering a navigation request in the **Ask Now Assist to...** field. If you enter "navigate me to active incidents," Now Assist displays a button that enables you to view the active incidents.

## Chat summarization

Quickly learn the details of a chat by reading a chat summarization. The chat summarization gives you enough details about the chat so that your requester doesn't have to repeat the same information to you.

To generate a chat summarization from the Now Assist panel, select **Chat Summarization** or enter `summarize chat` in the **Ask Now Assist to** field.

**Note:** You can also generate a chat summarization by using the `/summarize` quick action in Agent Chat.

## Case or incident summarization

Quickly learn the details of a case or incident by reading a case summarization. The summarization gives you enough details about the interaction so that your requester doesn't have to repeat the same information to you.

You can generate a case or incident summarization from the Now Assist panel for Now Assist for CSM, Now Assist for HRSD, or Now Assist for ITSM:

-   For Now Assist for CSM, select **Summarize record** or enter `summarize a record` in the **Ask Now Assist to** field.
-   For Now Assist for HRSD, select **Summarize record** or enter `summarize a record` in the **Ask Now Assist to** field.
-   For Now Assist for ITSM, select **Summarize incident** or enter `summarize an incident` in the **Ask Now Assist to** field.

## Conversation Help

Get specific and accurate answers to your queries by using the Get Help skill option on the Now Assist panel. This skill is available to everyone entitled to Now Assist capabilities.

For more information about the Now Assist Conversational Help skill that represents as Get Help on the Now Assist panel, see [Now Assist Conversational Help](../../now-assist-skills/concept/conversational-help-skills.md).

## Resolution notes generation

Quickly learn the details of how an interaction was resolved by generating and reading resolution notes.

To generate resolution notes from the Now Assist panel, select **Generate resolutions notes** or enter `generate resolutions notes` in the **Ask Now Assist to** field.

## Streaming responses

After you enter a question or request on the Now Assist panel, Now Assist gathers information from Knowledge Base articles, external content, product documentation, catalog items, and workflows and combines them into a synthesized, comprehensive answer. Instead of waiting for the entire message to render, the synthesized response streams in real time and stops streaming after the entire message has been delivered. An animated sparkle icon \(![Now Assist sparkle icon](../../../common/image/icon-ai-sparkle.png)\) appears while the response is generated and changes to the static sparkle icon after the response has fully loaded.

## Fallback options

**Note:** For more information about where and how to enable fallback options, see [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

A fallback state can occur whenever search results are unavailable. Scenarios where search results are unavailable include when Now Assist didn't understand the query, complaint small talk was found, or an error occurred. When search results are unavailable, the **Search the web** fallback option may appear. If you select the **Search the web** fallback option, the web search mode is triggered and uses the internet to search for the results.

**Note:** Only the last query entered into the conversation is considered when entering web search mode via this **Search the web** fallback option.

![](../images/nap-search-web-fallback.png "Example of Search the web fallback option")

**Parent Topic:**[Now Assist panel](now-assist-panel-overview.md)

