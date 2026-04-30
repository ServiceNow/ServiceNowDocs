---
title: Premium chat
description: Now Assist panel premium chat is an AI chat experience built into your ServiceNow environment that lets you ask questions, get answers from your organization's knowledge, and take action on records — all in one place. It supports file uploads, web search, and multi-step agentic tasks, so you can handle more complex requests without leaving the panel.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 10
breadcrumb: [Now Assist panel, Now Assist Experiences, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Premium chat

Now Assist panel premium chat is an AI chat experience built into your ServiceNow environment that lets you ask questions, get answers from your organization's knowledge, and take action on records — all in one place. It supports file uploads, web search, and multi-step agentic tasks, so you can handle more complex requests without leaving the panel.

Note these important considerations:

-   Next Experience must be enabled to use the Now Assist panel. For more information, see [Considerations for activating Next Experience](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
-   Now Assist panel premium chat must be activated before you can use it. See [Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for more information.
-   If you want to use assistants, you must activate them. See [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for information on activating assistants.
-   To use the full capabilities of Now Assist panel premium chat, AI Search must be enabled for your portal. Without it, Now Assist panel premium chat functions in a limited capacity. Basic interactions such as predefined topic flows and simple questions and answers are available, but knowledge article retrieval, AI responses grounded in instance content, and semantic search capabilities require AI Search. For more information, see [Enable and configure AI Search in Service Portal](https://www.servicenow.com/docs/access?context=enable-ais-sp&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
-   Now Assist skills must be enabled to appear on the Now Assist panel. For more information, see [Now Assist skills](../../now-assist-skills/concept/now-assist-skills.md).
-   Conversational aspects of the Now Assist panel, such as skill detection, are powered by Now LLM Service.

The following sections describe how to use the key features of Now Assist panel premium chat. To begin, select the Now Assist icon ![Now Assist sparkle icon](../../../common/image/icon-ai-sparkle.png) to display the Now Assist panel.

![Now Assist panel premium chat.](../images/na-panel-screenshot-example-premium.png "Now Assist panel")

The Now Assist panel includes:

<table id="table_yzf_wkw_hzb"><thead><tr><th>

Item number

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 - Expand

 ![](../images/premium-chat-arrows-icon.png)

</td><td>

Expands the chat into a 90% screen-size window. The 90% screen-size window can’t be resized or moved. Selecting the icon again resizes the chat back into the floating window. You can also resize the chat window using the window's edges.

</td></tr><tr><td>

2 - Pin

 ![](../images/premium-chat-pin-icon.png)

</td><td>

Positions, or pins, the Now Assist panel to the screen.

</td></tr><tr><td>

3 - Close

 ![](../images/premium-chat-down-arrow-icon.png)

</td><td>

Closes the Now Assist window.

</td></tr><tr><td>

4 - Chat history

 ![](../images/premium-chat-three-lines-icon.png)

 Chat history with unread chats

 ![](../images/premium-chat-history-red-dot-icon.png)

</td><td>

Displays the Chat History window. A red dot appears on the icon if you have any unread chats.

</td></tr><tr><td>

5 - New conversation

 ![](../images/premium-chat-pencil-icon.png)

</td><td>

Starts a new Now Assist panel conversation.

</td></tr><tr><td>

6 - Input bar

</td><td>

Enter your prompt or request.

</td></tr><tr><td>

7 - Voice input

 ![](../images/premium-chat-microphone-icon.png)

</td><td>

If voice input is enabled, select the microphone icon to activate voice input and transcribe your speech to text in real time. The transcribed text appears in the input bar and is sent to the assistant as a prompt.

</td></tr><tr><td>

8 - Add files &amp; images/Include Web

 ![Add files and images and Include Web options.](../images/na-panel-premium-plus-icon.png)

</td><td>

Add files &amp; images or include web information in results.

 Upload files during conversations to help the assistant understand your request. The assistant reads uploaded files and uses that content to fill required fields and answer questions. Uploaded files are retained only during your active session and cleared automatically when the session ends. Supported file formats are PDF, JPEG, TXT, and CSV and you can upload a maximum of 5 files per conversation. You can change the model provider at the instance level by navigating to **Now Assist Admin** &gt; **Skills** &gt; **Settings**. If the provider is set to anything other than Azure, the Add files &amp; images option will not be visible.

 If you select the Include Web option, the assistant's search is expanded to include internet results alongside internal knowledge base articles and catalog items.

</td></tr><tr><td>

9 - Previously used prompts.

</td><td>

Prompts that you've previously entered.

</td></tr><tr><td>

10 - Now Assist message

</td><td>

Indicates that the answers are generated by AI.

</td></tr></tbody>
</table>![Now Assist panel premium chat showing new chat, active and closed chats.](../images/na-panel-closed-chat-premium.png "Now Assist Chat History window")

The Chat History panel displays the following:

<table id="table_s4m_r1r_53c"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

A - New Chat

 ![](../images/premium-chat-pencil-icon.png)

</td><td>

Start a new conversation.

 You may be prompted with a greeting message along with any promoted conversational assets such as topics, subflows, and actions, or suggested queries.

</td></tr><tr><td>

B - Active

</td><td>

Chats where you can continue the conversation. Unread chats are indicated with a red dot. Active chats move to the Closed chats section after two hours of inactivity. Configure this 2-hour time limit in the Messaging Channels \[sys\_cs\_channel\] table. To change the inactivity time limit, select the **NASS** record from the Messaging Channels \[sys\_cs\_channel\] table and populate the **Conversation Idle Timeout** field. If more than 12 active chats are running, a **Show more** link appears. Selecting **Show more** displays an additional 10 chats.

</td></tr><tr><td>

C - Closed

</td><td>

A message closes when the designated time passes \(2 hours of inactivity\) or you receive this response: `It looks like you're finished with this chat, so I'll go ahead and close it.` Turn on closed chats by selecting the **Show closed chats** check box in **Conversational Interfaces** &gt; **Assistants** &gt; **\[Selected Assistant Name\]** &gt; **Chat experience** &gt; **Closed chats**. After being turned on, closed chats are displayed for as long as they're available in the Conversations \[sys\_cs\_conversation\] table. If more than four closed chats are available, a **Show more** link appears. Selecting **Show more** displays an additional 10 closed chats. Closed chats cannot be reopened.Hovering over a closed chat displays the delete icon.

</td></tr></tbody>
</table>The Now Assist feedback icons consists of these elements:

![Feedback icons on Now Assist panel premium chat.](../images/na-panel-premium-feedback-icons.png)

![More feedback icons on Now Assist panel premium chat.](../images/na-panel-premium-feedback-icons-2.png)

**Note:** If search results involve personalized or user-specific information, you will not be able to access more than 10 results even if they're available.

<table id="table_qzq_r2c_qfc"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 - \[Chat name\]

</td><td>

The name of the conversation.

 If you select a promoted asset or query, that asset's title becomes the chat name. If instead you enter an prompt into the **Reply to Now Assist** field, your initial prompt becomes the chat name. The chat name appears in both the Now Assist subheader and **Chats list** &gt; **Active** section.

</td></tr><tr><td>

2 - Thumbs up \(like\) ![](../images/nap-thumbs-up.png)

 Thumbs down \(dislike\) ![](../images/nap-thumbs-down.png)

</td><td>

Select the thumbs up icon if the response was helpful, or the thumbs down icon if it wasn't.

</td></tr><tr><td>

3 - Copy ![](../images/nap-copy-icon.png)

</td><td>

Copy the response.

</td></tr><tr><td>

4 - Download ![Download options.](../images/na-panel-premium-download.png)

</td><td>

Displays a menu with options to download the conversation as a PDF or DOC file.

</td></tr><tr><td>

5 - Sources and more ![Sources and more option.](../images/na-panel-premium-sources.png)

</td><td>

Opens a panel showing the sources used to generate the response, along with related content. From the panel you can select **View all results** to navigate to the global search page.

</td></tr></tbody>
</table>Now Assist panel is available on Next Experience and ServiceNow Studio. The following screenshots show the Now Assist panel in a workspace and on Core UI screens under Next Experience.

<table id="table_smr_n2b_xyb"><tbody><tr><td>

Next Experience

</td><td>

Core UI

</td></tr><tr><td>

![Screen with Now Assist panel premium chat.](../images/na-panel-overview-example-premium.png)

</td><td>

![Now Assist panel on a Core UI incident form.](../images/now-assist-panel-overview-ui16-example.png)

</td></tr></tbody>
</table>## Agentic conversations

**Note:** Admins must first enable AI agents before end users can experience agentic conversations. Now Assist panel discovers and executes agentic workflows. For more information on agentic workflows, see [Now Assist agentic workflows](../../now-assist-ai-agents/concept/sn-aia-use-cases-list.md) and [Multiple conversations in Now Assist AI agents](../../now-assist-ai-agents/concept/multiple-conversations-aia.md).

When you ask a question to the Now Assist panel premium chat, the agent understands the query and begins a flow. When you submit a message with multiple questions or requests, Now Assist panel premium chat answers them consecutively. It can reason, plan, and execute across AI agents, Now Assist panel topics, conversational actions and subflows, catalogs, Knowledge Base articles, custom skills, and any Now Assist supported skills to help you. You receive on-screen messages showing where the agent is in the agentic processing flow prior to receiving the response. After the processing completes, a View AI Steps section header appears where you can expand and view the processing flow steps. You can stop the agentic processing flow at any time by selecting the End flow icon \(![End flow icon.](../images/agentic-end-flow-icon.png)\). After an action starts, it can't be stopped. Selecting the End flow icon only stops the subsequent processing steps.

If your question is unclear or could apply to multiple topics, Now Assist evaluates your request and may ask for clarification before responding. This helps you receive a focused, relevant answer rather than an overwhelming list of results. If the assistant is confident it understands your intent, it responds immediately without asking for clarification. If no relevant answer is found, the assistant displays a message and suggests an alternative, such as contacting support.

Processing messages are short status updates that appear on-screen while Now Assist works on your request. They reflect what Now Assist is actively doing at each step, such as searching for information or analyzing a document, and update as each step completes. Processing messages don’t appear for simple interactions such as greetings, which are handled instantly.

## Navigating from the Now Assist panel

You can navigate from the Now Assist panel without leaving the current conversation by entering a navigation request in the **Ask Now Assist to...** field. If you enter "navigate me to active incidents," Now Assist displays a button that enables you to view the active incidents.

## Chat summarization

Quickly learn the details of a chat by reading a chat summarization. The chat summarization gives you enough details about the chat so that your requester doesn't have to repeat the same information.

To generate a chat summarization from the Now Assist panel, select **Chat Summarization** or enter `summarize chat` in the **Ask Now Assist to** field.

**Note:** You can also generate a chat summarization by using the `/summarize` quick action in Agent Chat.

## Case or incident summarization

Quickly learn the details of a case or incident by reading a case summarization. The summarization gives you enough details about the interaction so that your requester doesn't have to repeat the same information.

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

After you enter a question or request on the Now Assist panel, Now Assist gathers information from Knowledge Base articles, external content, product documentation, catalog items, and workflows and combines them into a synthesized, comprehensive answer. Instead of waiting for the entire message to render, the synthesized response streams in real time and stops streaming after delivery. An animated sparkle icon \(![Now Assist sparkle icon](../../../common/image/icon-ai-sparkle.png)\) appears while the response is generated and changes to the static sparkle icon after the response has fully loaded.

## Fallback options

**Note:** For more information about where and how to enable fallback options, see [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

A fallback state can occur whenever search results are unavailable. Scenarios where search results are unavailable include when Now Assist didn't understand the query, complaint small talk was found, or an error occurred. When search results are unavailable, the **Search the web** fallback option may appear. If you select the **Search the web** fallback option, the web search mode is triggered and uses the internet to search for the results.

**Note:** Only the last query entered into the conversation is considered when entering web search mode via this **Search the web** fallback option.

![Search the web fallback option screen.](../images/na-panel-premium-chat-fallback.png "Example of Search the web fallback option")

**Parent Topic:**[Now Assist panel](now-assist-panel-overview.md)

