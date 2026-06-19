---
title: Premium chat
description: Now Assist panel premium chat is an AI chat experience built into your ServiceNow environment that lets you ask questions, get answers from your organization's knowledge, and take action on records — all in one place. It supports file uploads, web search, and multi-step agentic tasks, so you can handle more complex requests without leaving the panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/now-assist-panel-premium.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 21
breadcrumb: [Now Assist panel, Now Assist Experiences, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Premium chat

Now Assist panel premium chat is an AI chat experience built into your ServiceNow environment that lets you ask questions, get answers from your organization's knowledge, and take action on records — all in one place. It supports file uploads, web search, and multi-step agentic tasks, so you can handle more complex requests without leaving the panel.

**Important:**

-   Next Experience must be enabled to use the Now Assist panel. For more information, see .
-   Now Assist panel premium chat must be activated before you can use it. See  for more information.
-   If you want to use assistants, you must activate them. See  for information on activating assistants.
-   To use the full capabilities of Now Assist panel premium chat, AI Search must be enabled for your portal. Without it, Now Assist panel premium chat functions in a limited capacity. Basic interactions such as predefined topic flows and simple questions and answers are available, but knowledge article retrieval, AI responses grounded in instance content, and semantic search capabilities require AI Search. For more information, see .
-   Now Assist skills must be enabled to appear on the Now Assist panel. For more information, see [Activate a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configure-a-now-assist-skill.md).
-   Conversational aspects of the Now Assist panel, such as skill detection, are powered by Now LLM Service.

To begin, select the Now Assist icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: Now Assist sparkle icon to display the Now Assist panel.

\[Omitted image "na-panel-screenshot-example-premium.png"\] Alt text: Now Assist panel premium chat.

The Now Assist panel includes:

<table id="table_yzf_wkw_hzb"><thead><tr><th>

Item number

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 - Expand \[Omitted image "premium-chat-arrows-icon.png"\]

</td><td>

Expands the chat into a 90% screen-size window. The 90% screen-size window can’t be resized or moved. Selecting the icon again resizes the chat back into the floating window. You can also resize the chat window using the window's edges.

</td></tr><tr><td>

2 - Pin \[Omitted image "premium-chat-pin-icon.png"\] Alt text:

</td><td>

Positions, or pins, the Now Assist panel to the screen.

</td></tr><tr><td>

3 - Close \[Omitted image "premium-chat-down-arrow-icon.png"\] Alt text:

</td><td>

Closes the Now Assist panel.

</td></tr><tr><td>

4 - Chat history \[Omitted image "premium-chat-three-lines-icon.png"\] Alt text:

 Chat history with unread chats \[Omitted image "premium-chat-history-red-dot-icon.png"\] Alt text:

</td><td>

Displays the Chat History window. A red dot appears on the icon if you have any unread chats.

</td></tr><tr><td>

5 - New conversation \[Omitted image "premium-chat-pencil-icon.png"\] Alt text:

</td><td>

Starts a new Now Assist panel conversation.

</td></tr><tr><td>

6 - Input bar

</td><td>

Enter your prompt or request.

</td></tr><tr><td>

7 - Voice input \[Omitted image "premium-chat-microphone-icon.png"\] Alt text:

</td><td>

If voice input is enabled, select the microphone icon and speak your message. Your speech is transcribed and appears in the input bar in real time.

**Note:** Voice input must be enabled by an administrator before it is available. Administrators can enable or disable voice input at the instance level. Individual users can also turn voice input on or off.

</td></tr><tr><td>

8 - Add files &amp; images/Include Web

 \[Omitted image "na-panel-premium-plus-icon.png"\] Alt text: Add files and images and Include Web options.

</td><td>

Add files and images

 Upload files during conversations to help the assistant understand your request. The assistant reads uploaded files and uses that content to fill required fields and answer questions.

 You can also upload images to help the assistant understand a visual situation. The assistant analyzes the uploaded content and can answer natural-language questions about it, generate summaries, and recommend or execute actions based on what it sees. For example:

-   Upload a screen shot of an error message and ask, "What error is shown here?"
-   Upload a photo of a damaged device and ask Now Assist to create an incident

When referencing visual content, the assistant can identify specific image regions in its response.

 Uploaded files are retained only during your active session and cleared automatically when the session ends. Supported file formats are:

-   PDF
-   JPEG
-   TXT
-   CSV
-   PNG

You can upload a maximum of 5 files per conversation. You can change the model provider at the instance level by navigating to **Now Assist Admin** &gt; **Skills** &gt; **Settings**. If the provider is set to anything other than Azure, the Add files &amp; images option will not be visible.

 Include Web

 If you select the Include Web option, the assistant's search is expanded to include internet results alongside internal knowledge base articles and catalog items. Your prior conversation context carries over when Include Web is enabled, though sensitive personal information such as your name, email address, and phone number is removed before being shared externally. To help answer location-aware or company-specific questions, publicly available information such as your location and company name may be included in the web search. Responses indicate which parts of the answer come from web sources, and citations for web results show the page title and web link. The Include Web setting is preserved if you return to a past conversation that had it enabled.

</td></tr><tr><td>

9 - Previously used prompts

</td><td>

Prompts that you've previously entered.

</td></tr><tr><td>

10 - Now Assist message

</td><td>

Indicates that the answers are generated by AI.

</td></tr></tbody>
</table>If you select the Chat History icon \[Omitted image "premium-chat-three-lines-icon.png"\] Alt text:, the Chat History window appears:

\[Omitted image "na-panel-closed-chat-premium.png"\] Alt text: Now Assist panel premium chat showing new chat, active and closed chats.

The Chat History panel displays the following:

<table id="table_s4m_r1r_53c"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

A - New Chat

 \[Omitted image "premium-chat-pencil-icon.png"\] Alt text:

</td><td>

Start a new conversation.

 You may be prompted with a greeting message along with any promoted conversational assets such as topics, subflows, and actions, or suggested queries. If more than 6 promoted topics are enabled, the first 6 topics appear along with a View all topics option that displays the complete list.

</td></tr><tr><td>

This record

</td><td>

Conversations related to the current record you're viewing.

 This section appears only when you're viewing a specific record, such as an incident or case. When you open the Now Assist panel while on a record, the most recent conversation associated with that record is automatically displayed. Conversations in this section are identified by the record number prefix in the conversation title—for example, INC0012345 — My laptop won't turn on. The same conversation may appear in both This record and Active sections if it's still in progress. When you navigate to a different record, the This record section updates to show conversations for the new record. When you navigate to a home page or list view, this section is hidden.

</td></tr><tr><td>

B - Active

</td><td>

Chats where you can continue the conversation.

 Unread chats are indicated with a red dot. Active chats include both record-specific conversations and general conversations. Record-specific conversations may also appear in the This record section if you're currently viewing that record. Active chats move to the Closed chats section after two hours of inactivity. Configure this 2-hour time limit in the Messaging Channels \[sys\_cs\_channel\] table. To change the inactivity time limit, select the **NASS** record from the Messaging Channels \[sys\_cs\_channel\] table and populate the **Conversation Idle Timeout** field. If more than 12 active chats are running, a **Show more** link appears. Selecting **Show more** displays an additional 10 chats.

 When you navigate to a record page, the panel displays the most recent conversation associated with that record in the This record section of Chat History. If you navigate away and return to the same record, the panel restores that conversation automatically. If you switch to a different record, the This record section updates to show conversations for the new record. Conversations tied to a specific record are identified by the record number prefix in the conversation title — for example, INC0012345 — My laptop won't turn on.

</td></tr><tr><td>

C - Closed

</td><td>

A message closes when the designated time passes \(2 hours of inactivity\) or you receive this response: `It looks like you're finished with this chat, so I'll go ahead and close it.` Turn on closed chats by selecting the **Show closed chats** check box in **Conversational Interfaces** &gt; **Assistants** &gt; **\[Selected Assistant Name\]** &gt; **Chat experience** &gt; **Closed chats**. After being turned on, closed chats are displayed for as long as they're available in the Conversations \[sys\_cs\_conversation\] table. If more than four closed chats are available, a **Show more** link appears. Selecting **Show more** displays an additional 10 closed chats. Closed chats cannot be reopened.Hovering over a closed chat displays the delete icon.

</td></tr></tbody>
</table>The Now Assist feedback icons panel consist of these elements:

\[Omitted image "na-panel-premium-feedback-icons.png"\] Alt text: Feedback icons on Now Assist panel premium chat.

\[Omitted image "na-panel-premium-feedback-icons-2.png"\] Alt text: More feedback icons on Now Assist panel premium chat.

**Note:** If search results involve personalized or user-specific information, you will not be able to access more than 10 results even if they're available.

<table id="table_qzq_r2c_qfc"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1 - \[Chat name\]

</td><td>

The name of the conversation.

 If you select a promoted asset or query, that asset's title becomes the chat name. If instead you enter a prompt into the **Reply to Now Assist** field, your initial prompt becomes the chat name. The chat name appears in both the Now Assist subheader and **Chats list** &gt; **Active** section.

</td></tr><tr><td>

2 - Thumbs up \(like\) \[Omitted image "nap-thumbs-up.png"\] Alt text:

 Thumbs down \(dislike\) \[Omitted image "nap-thumbs-down.png"\] Alt text:

</td><td>

Select the thumbs up icon if the response was helpful, or the thumbs down icon if it wasn't.

</td></tr><tr><td>

3 - Copy \[Omitted image "nap-copy-icon.png"\] Alt text:

</td><td>

Copy the response.

</td></tr><tr><td>

4 - Download

 \[Omitted image "na-panel-premium-download.png"\] Alt text: Download options.

</td><td>

Displays a menu with options to download the conversation as a PDF or DOC file.

</td></tr><tr><td>

5 - Sources and more \[Omitted image "na-panel-premium-sources.png"\] Alt text: Sources and more option.

</td><td>

Opens a panel showing the sources used to generate the response, along with related content. From the panel you can select **View all results** to navigate to the global search page.

</td></tr></tbody>
</table>Now Assist panel is available on Next Experience and ServiceNow Studio. The following screenshots show the Now Assist panel in a workspace and on Core UI screens under Next Experience.

<table id="table_smr_n2b_xyb"><tbody><tr><td>

Next Experience

</td><td>

Core UI

</td></tr><tr><td>

\[Omitted image "na-panel-overview-example-premium.png"\] Alt text: Screen with Now Assist panel premium chat.

</td><td>

\[Omitted image "now-assist-panel-overview-ui16-example.png"\] Alt text: Now Assist panel on a Core UI incident form.

</td></tr></tbody>
</table>## Response feedback

Each Virtual Agent response includes a feedback icons panel. The feedback icons panel appears on the latest Virtual Agent response and whenever you hover over any Virtual Agent response. You can indicate if the response was helpful by selecting the like thumbs up icon \[Omitted image "nap-thumbs-up.png"\] Alt text:. If the response wasn't helpful, select the dislike thumbs down icon \[Omitted image "nap-thumbs-down.png"\] Alt text:. When you select the thumbs up or thumbs down icon, you are prompted to provide detailed feedback by selecting one or more reason check boxes. You can also select **Other** to add comments or suggestions \(up to 300 characters\). After making your selection, select **Submit** to submit your feedback, or select **X** to close the dialog without submitting feedback. All submitted feedback is captured, stored, and made available through analytic dashboards.

\[Omitted image "feedback-panel-granular.png"\] Alt text: Thumbs down granular feedback dialog.

Depending on the context of the response, an additional go to search results icon \[Omitted image "nass-search-result-icon.png"\] may appear in the feedback icons panel. This icon appears alongside synthesized responses in Virtual Agent, clarifying questions in Virtual Agent, and regular search results or Virtual Agent fallback topics whenever a synthesized response is unavailable. Selecting the go to search results icon \[Omitted image "nass-search-result-icon.png"\] redirects you to the search results page and begins a search query using the last five chat utterances you entered.Additionally, a copy message icon \(\[Omitted image "dw-feedback-copy-message-icon.png"\]\) appears on received Virtual Agent responses.

## Multi-intent requests

When your request combines information from both internal and external sources, Now Assist breaks it into steps and handles each part separately before delivering a combined response. For example, if you ask Now Assist to find a product online and then order it through your company's catalog, Now Assist searches the web for the product information and executes the catalog item as separate steps, then combines the results into a single cohesive answer. You receive on-screen processing messages as each step completes.

## Agentic conversations

Admins must first enable AI agents before end users can experience agentic conversations. Now Assist panel discovers and executes agentic workflows. For more information on agentic workflows, see [Now Assist agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/sn-aia-use-cases-list.md) and [Multiple conversations in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/multiple-conversations-aia.md).

When you ask a question to the Now Assist panel premium chat, the agent understands the query and begins a flow. When you submit a message with multiple questions or requests, Now Assist panel premium chat answers them consecutively. It can reason, plan, and execute across AI agents, Now Assist panel topics, conversational actions and subflows, catalogs, Knowledge Base articles, custom skills, and any Now Assist supported skills to help you. You receive on-screen messages showing where the agent is in the agentic processing flow prior to receiving the response. After the processing completes, a View AI Steps section header appears where you can expand and view the processing flow steps. You can stop the agentic processing flow at any time by selecting the End flow icon \(\[Omitted image "agentic-end-flow-icon.png"\] Alt text: End flow icon.\). After an action starts, it can't be stopped. Selecting the End flow icon only stops the subsequent processing steps.

If your question is unclear or could apply to multiple topics, Now Assist evaluates your request and may ask for clarification before responding. This helps you receive a focused, relevant answer rather than an overwhelming list of results. If the assistant is confident it understands your intent, it responds immediately without asking for clarification. If no relevant answer is found, the assistant displays a message and suggests an alternative, such as contacting support.

You can explore a response in more depth without asking your original question again. Follow-up requests such as "show more detail," "compare sources," "summarize by theme," or "what's missing?" remain anchored to the same retrieved context. The context resets when you start a new conversation. You can also start a follow-up conversation in the Now Assist panel directly from a search result in workspace. When viewing a search result, select the follow-up option to open the Now Assist panel with the result as context for your next question.

Processing messages are short status updates that appear on-screen while Now Assist works on your request. They reflect what Now Assist is actively doing at each step, such as searching for information or analyzing a document, and update as each step completes. Processing messages don’t appear for simple interactions such as greetings, which are handled instantly.

When an agentic workflow requires your input before it can continue, the processing messages pause and no loading indicator is displayed. After you provide the requested input, a new processing message appears to indicate that Now Assist has resumed processing your request.

When you view search results in a workspace, you can continue exploring a topic by asking a follow-up question in the Now Assist panel. Select **Ask a follow-up** from the search result to open the Now Assist panel and then enter your follow-up question in the input bar.

## Navigating from the Now Assist panel

You can navigate from the Now Assist panel without leaving the current conversation by entering a navigation request in the **Ask Now Assist to...** field. If you enter "navigate me to active incidents," Now Assist displays a button that enables you to view the active incidents.

## Chat summarization

Quickly learn the details of a chat by reading a chat summarization. The chat summarization gives you enough details about the chat so that your requester doesn't have to repeat the same information.

To generate a chat summarization from the Now Assist panel, select **Chat Summarization** or enter `summarize chat` in the **Ask Now Assist to** field. You can also generate a chat summarization by using the `/summarize` quick action in Agent Chat.

## Case or incident summarization

Quickly learn the details of a case or incident by reading a case summarization. The summarization gives you enough details about the interaction so that your requester doesn't have to repeat the same information.

You can generate a case or incident summarization from the Now Assist panel for Now Assist for CSM, Now Assist for HRSD, or Now Assist for ITSM:

-   For Now Assist for CSM, select **Summarize record** or enter `summarize a record` in the **Ask Now Assist to** field.
-   For Now Assist for HRSD, select **Summarize record** or enter `summarize a record` in the **Ask Now Assist to** field.
-   For Now Assist for ITSM, select **Summarize incident** or enter `summarize an incident` in the **Ask Now Assist to** field.

## Resolution notes generation

Quickly learn the details of how an interaction was resolved by generating and reading resolution notes.

To generate resolution notes from the Now Assist panel, select **Generate resolutions notes** or enter `generate resolutions notes` in the **Ask Now Assist to** field.

## Streaming responses

After you enter a question or request on the Now Assist panel, Now Assist gathers information from Knowledge Base articles, external content, product documentation, catalog items, and workflows and combines them into a synthesized, comprehensive answer. Instead of waiting for the entire message to render, the synthesized response streams in real time and stops streaming after delivery. An animated sparkle icon \(\[Omitted image "icon-ai-sparkle.png"\] Alt text: Now Assist sparkle icon\) appears while the response is generated and changes to the static sparkle icon after the response has fully loaded. Synthesized responses include inline citations that identify the sources used to generate the answer. Up to three inline citations appear within the response. Select a citation to open the source in a new browser tab. To view all sources and related results, select **Sources and more**. External links, such as those from web search results, open in a new browser tab. Your current tab and Now Assist conversation are not affected.

## Single search results

When your request returns a single result, Now Assist displays a card with the most relevant fields for that record and fields with no information are hidden automatically. Fields with no information are hidden automatically to keep the response easy to read. The fields displayed are either configured by your administrator or determined automatically based on your query.

-   People results: The card includes available contact and profile details. Select **View profile** to open the full profile in interactive view or select the org chart icon to view the person's position in the org chart.
-   Records \(such as incidents or assets\): Select the link in the card to open the full record. The record opens in the current tab and the Now Assist panel automatically collapses to pinned mode. If the record can't open in the current tab, it opens in a new browser tab instead.
-   Actions and topics: Select the card to launch the corresponding action or topic directly in the chat.
-   Catalog items: Select the card to open the catalog form. To open the form in the current tab, select the pop-out icon. The Now Assist panel collapses to pinned mode. If the form can't open in the current tab, it opens in a new browser tab instead. If the catalog form contains links to additional content, selecting those links loads the new content within the same interactive view and a back button appears. Select the back button to return to the previously viewed content.
-   Knowledge Base articles: Select the card to open the article. To open the article in the current tab, select the pop-out icon. The Now Assist panel collapses to pinned mode. If the article can't open in the current tab, it opens in a new browser tab instead. This works for both internal and external knowledge base sources. If the article contains links to additional content, selecting those links loads the new content within the same interactive view and a back button appears. Select the back button to return to the previously viewed content.

When only one result is found, the **View all** link does not appear at the end of the response. Records displayed in the response are not shown as citations in the sources panel.

## Switching between interactive views

When a conversation contains more than one interactive view — for example, a Knowledge Base article and a catalog form opened during the same conversation — you can switch between them using the drop-down selector in the interactive view header. The header always displays the name of the most recently opened interactive view. The first time you open a second interactive view in a conversation, a message appears letting you know you can use the drop-down selector to switch between views. Each interactive view in the conversation is represented by a thumbnail card in the chat. The thumbnail card for the currently visible view shows Hide. Selecting a different view from the drop-down selector updates the thumbnail card statuses accordingly — the newly visible view shows Hide, and the previous view shows Show.

## Submitting catalog requests

You can submit catalog requests directly from the Now Assist panel without leaving the chat experience.

To submit a catalog request:

1.  Open the Now Assist panel.
2.  Find a catalog item through chat.
3.  Select the item and a catalog form opens inline in the interactive view.
4.  Complete the required form fields.
5.  Select **Submit**. A confirmation message appears and your request record is created.

## Catalog submission confirmation

After you successfully submit a catalog item, a confirmation message appears with a **View Details** button that opens your submitted request record.

The **View Details** button behaves in the following ways:

-   In Now Assist panel: Select **View Details** to open the submitted request record in the current tab. The Now Assist panel automatically shrinks to pinned mode.
-   In pop-out windows: If you select the pop-out icon on a submitted catalog form, the new window displays the submission confirmation page with your request details, not a blank form to start over.

## Unsaved catalog form changes

If you start filling out a catalog form in the Now Assist panel and navigate to other content before submitting, such as selecting another catalog item or knowledge article, a confirmation modal appears asking whether you want to stay or leave without saving.

-   To continue working on the catalog form, select Stay. The modal closes, and you return to the catalog form with your progress intact.
-   To discard changes and view new content, select Leave without saving. The form closes, your unsaved data is discarded, and the content you selected appears in the interactive view.

**Note:** The discard warning modal does not appear when you switch conversations using Chat History. It only appears when navigating to different content within the same conversation.

## Multiple search results

When your request returns multiple results from Knowledge Graph, Now Assist displays them in a table. Empty columns are hidden automatically to keep the table easy to read. The columns displayed are determined automatically based on your query.

-   People results: Use the horizontal and vertical scrollbars to view additional rows or columns. Select a person's name to open their profile in interactive view or select the org chart icon to view their position in the org chart.
-   Record results \(such as incidents or assets\): Select a record number to open the full record in the current tab. The Now Assist panel automatically reverts to pinned mode. If the record can't open in the current tab, it opens in a new browser tab instead.

A **View all** link appears at the end of the response. Selecting it opens a summary page showing all records in the current tab and the Now Assist panel reverts to pinned mode. If the records can't open in the current tab, they open in a new browser tab instead.

If your results include more than one type of record \(for example, people and incidents\), a separate **View all** link appears for each record type. Records displayed in the response are not shown as citations in the sources panel. When results include a mix of records and text content \(such as knowledge base articles\), Now Assist may display both a table and bullet points or text in the same response and related records appear above the Sources and more link. Select a record group — such as users or assets — to open the corresponding list in the current tab.

**Note:** If you're using Now Assist in a portal, records and View all results open in a new portal tab.

## Fallback options

A fallback state can occur whenever search results are unavailable. Scenarios where search results are unavailable include when Now Assist didn't understand the query, complaint small talk was found, or an error occurred. When search results are unavailable, the **Search the web** fallback option may appear. If you select the **Search the web** fallback option, the web search mode is triggered and uses the internet to search for the results. Only the last query entered into the conversation is considered when entering web search mode via this **Search the web** fallback option. For more information about where and how to enable fallback options, see .

If Now Assist can't find relevant results for your query, or if an answer is based on limited evidence, Now Assist displays a message to let you know. It may also suggest ways to improve your results, such as rephrasing your query, broadening your search scope, or specifying a time frame or source.

If Now Assist can't find relevant results in your organization's internal content, an **Include the Web** button appears in the chat. Selecting it reruns your query with web results included and turns on Include Web mode for the rest of the conversation. Unlike the Search the web fallback option, which only applies to your most recent query, selecting **Include the Web** expands all subsequent responses to include web results.

\[Omitted image "na-panel-premium-chat-fallback.png"\] Alt text: Search the web fallback option screen.

**Parent Topic:**[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/now-assist-panel-overview.md)

