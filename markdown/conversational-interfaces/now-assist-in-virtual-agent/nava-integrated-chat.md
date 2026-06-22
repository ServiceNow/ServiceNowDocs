---
title: Premium chat
description: Now Assist in Virtual Agent premium chat is a contextual chat experience that appears throughout the platform, adapting its behavior and interface based on where users are and what they're doing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/nava-integrated-chat.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-01-23"
reading_time_minutes: 17
breadcrumb: [Using Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Premium chat

Now Assist in Virtual Agent premium chat is a contextual chat experience that appears throughout the platform, adapting its behavior and interface based on where users are and what they're doing.

To access the Now Assist in Virtual Agent premium chat screen, select the Now Assist icon or enter text in the omnibar. \[Omitted image "nava-portal-screen.png"\] Alt text:

After the premium chat screen appears, begin entering a prompt in the chat input box. You can enter the entire prompt or select one of the recommended prompts that displays below the chat input box. Recommended prompts may include:

-   Related workflows and actions
-   Keyword-based prompts
-   Direct links to relevant content

**Note:** For more information about how Now Assist in Virtual Agent and Now Assist in AI Search combine to include recommended prompts, see [Auto-complete suggestion types included with Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-search/auto-complete-suggestion-types-na-ais.md).

## Chat input box features

\[Omitted image "nava-premium-callouts-screen.png"\] Alt text:

The chat input box has these features:

-   **Multi-line input**

    The chat input box starts as a single-line field and automatically expands to multi-line mode when text exceeds the available width.

-   **Plus sign icon**

    Select the plus sign \(+\) icon to access additional options including web search and file upload.\[Omitted image "nava-premium-chat-add-files.png"\] Alt text:

-   **Web search**

    When you select the plus sign icon, the **Web search** toggle appears. You can toggle the **Web search** option on to receive responses that combine both internal knowledge base results and web search results. You can toggle the web search on or off at any time during a conversation.

-   **File upload**

    You can upload files by selecting the file upload icon or by dragging and dropping files directly into the chat input box. The premium chat screen displays thumbnails for the first three uploaded files and you can upload up to 20 files in a single interaction.


## Navigating the chat window resizing options and controls toolbar

The Now Assist sub-header consists of four elements. The following figure and table shows an example and description of those elements.

\[Omitted image "nava-premium-window-controls.png"\] Alt text:

<table id="table_lgz_t33_33c"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Chats \(\[Omitted image "list-hamburger-icon.png"\] Alt text: Chats icon.\)

</td><td>

All chats appear.

 Chats are organized with the most recent conversations at the top. Selecting a chat opens the chat in the conversation area. If there are unread chats or notifications, a badge number appears on the Chats icon \(\[Omitted image "list-hamburger-icon.png"\] Alt text: Chats icon.\). Any unread chat or notification appears with a red dot next to it and the chat title appears in bold. Additionally, if you switch to a new chat while another active chat is ongoing, a pop-up message on the Chats icon \(\[Omitted image "list-hamburger-icon.png"\] Alt text: Chats icon.\) appears: `Your previous chat was saved. You can revisit all of your past chats and continue ones that are still active.` The following list includes the chat sections that you may see in the chats area.

 -   Active: Chats where you can continue the conversation. If applicable, active chats move to the Closed chats section after two hours of inactivity. This 2 hour time limit can be configured within the Messaging Channels \{sys\_cs\_channel.list\} table. To change the inactivity time limit, from the Messaging Channels \{sys\_cs\_channel.list\} table, select the **NASS** record and populate the **Conversation Idle Timeout** field with your preferred active chat time limit. If you have no active chats, `No chatter at the moment` is displayed. If more than 12 active chats are running, a **Show more** link appears to view more chats. Selecting **Show more** displays an additional 10 chats.
-   Updates: Updates for important notifications and reminders can be configured to display. When **sn\_nowassist\_va.nass\_notification\_enabled** is set to `true` \(the default\), simple \(nonactionable\) Virtual Agent notifications appear on your portal home page. After selecting a notification, you’re redirected to this Updates section. If you have no updates, `You're all caught up` is displayed. If more than four updates are available, a **Show more** link appears to view more updates. Selecting **Show more** displays an additional 10 updates.

**Note:** If **sn\_nowassist\_va.nass\_notification\_enabled** is set to `false`, the Updates section doesn't appear.

-   Closed: Closed chats can be configured to display. You know that a message has closed when the designated time has passed \(2 hours of inactivity\) or you receive the following response in the chat: `It looks like you're finished with this chat, so I'll go ahead and close it.` Turn on closed chats by selecting the **Show closed chats** check box within **Conversational Interfaces** &gt; **Assistants** &gt; **\[Selected Assistant Name\]** &gt; **Chat experience** &gt; **Closed chats**. After being turned on, closed chats are displayed for as long as they’re available within the Conversations \(sys\_cs\_conversation\) table. Closed chats appear in a read-only mode and can’t become active again. If more than four closed chats are available, a **Show more** link appears to view more closed chats. Selecting **Show more** displays an additional 10 closed chats. After a conversation has closed, you can’t reopen it.Hovering over a closed chat displays the delete icon \(\[Omitted image "delete-agent.png"\] Alt text: Delete icon\). Confirm the chat deletion on the Delete this chat? modal to permanently delete the chat from the interface.

</td></tr><tr><td>

2. \[Chat name\]

</td><td>

The name of the conversation.

 If you select a promoted asset or query, that asset's title appears as the chat name. If instead you enter an utterance into the **Reply to Now Assist** field, your initial utterance becomes the chat name. The chat name appears in both the Now Assist subheader and **Chats list** &gt; **Active** section.

</td></tr><tr><td>

3. New chat \(\[Omitted image "nass-new-chat-icon.png"\] Alt text: New chat icon.\)

</td><td>

A new conversation begins.

 You may be prompted with a greeting message along with any promoted conversational assets such as topics, subflows, and/or actions, or suggested queries.

</td></tr><tr><td>

4. Support and settings \(\[Omitted image "ellipsis-vertical-outline-24.svg"\] Alt text: Support and settings icon.\)

</td><td>

Support contact information such as phone numbers and email addresses are listed. If live agents are available, an active **Contact Live Agent** button is displayed. Although multiple active conversations are possible, you can only have one live agent conversation at a time. Selecting **Contact Live Agent** begins a chat with a live agent. After a live agent enters the chat, the **Contact Live Agent** button becomes inactive. If live agents are unavailable, an inactive **No live agents currently available** button is displayed.

 Settings toggles for Audio notifications and Notifications appear. By default, audio notifications are turned on and notifications are turned off. If admins have enabled notifications within the guided setup, users can turn on the notifications.

</td></tr><tr><td>

5. Interactive view \(\[Omitted image "nass-close-interactive-view-icon.png"\] Alt text: or \[Omitted image "nass-open-interactive-view-icon.png"\] Alt text:\)

</td><td>

**Note:** This icon only appears in the sub-header whenever the interactive view is available.

 Open or close the interactive view. The interactive view appears towards the right of the conversational chat area. Interactive view is available whenever an organizational chart is an available option in a people citation popover. If multiple interactive views are available in the same conversation, for example, you opened multiple people's org charts in a conversation, a drop-down is available to switch between the different interactive views' tabs.

</td></tr></tbody>
</table>## Chatting with Virtual Agent

After the user enters an utterance and a search result is found, a synthesized response may appear. A synthesized response includes a brief summary of the requested information and search results along with Genius Results. For more information on how these search results are found, see [Now Assist Actions Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-search/now-assist-catalog-ordering-gr.md) and [Now Assist Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-search/now-assist-qna-genius-results.md).

If multiple results are found, you can follow inline citations to either begin an action or learn more. The option to **Show sources** appears at the end of the synthesized response for internal and external Knowledge Base articles. Virtual Agent can only return available catalog items that match a user's request when the Now Assist Multi-Turn Catalog Ordering skill is enabled.

**Note:** For full catalog functionality, enable the generative AI experience for catalog item request submissions. For more information, see [Configure Now Assist in Conversational Catalog Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/configure-gen-ai-catalog-item.md).

Whenever only a single search result for topics is found, the synthesized response and options are bypassed by default and users are brought directly into that action's flow. You may consider bypassing the synthesized response and options by automatically launching catalog items, too. For more information on automatically launching single search result actions, search for the **sn\_nowassist\_va.synthesized\_autostart\_items** system property in [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/r_AvailableSystemProperties.md).

You can create a new query from within a Now Assist conversation using mid-topic discovery. For more information, see [Mid-topic switching during Now Assist in Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/intent-switching-na-va.md).

If Now Assist Guardian is enabled and your request contains profane content, the Virtual Agent responds with a message prompting you to re-enter an appropriate request without profanity or offensive content.If your request is too ambiguous on the portal search, a synthesized response appears along with an **Ask a follow up** option. Selecting the **Ask a follow up** option redirects you to a Virtual Agent chat. In the Virtual Agent chat, you can submit your follow-up question or request, but the synthesized response links are only available to select on the portal page and are unavailable to select in the chat window. If your follow-up question or request is too ambiguous in the Virtual Agent chat, Virtual Agent asks a clarifying question and displays the go to search results icon \(\[Omitted image "nass-search-result-icon.png"\] Alt text: Go to search results icon.\) in the feedback panel.

Each Virtual Agent response includes a feedback icons panel. The feedback icons panel appears on the latest Virtual Agent response and whenever you hover over any Virtual Agent response. You can indicate if the response was helpful by selecting the like thumbs up icon \(\[Omitted image "llm-thumbs-up-like.png"\] Alt text: Thumbs up icon.\). If the response wasn't helpful, select the dislike thumbs down icon \(\[Omitted image "llm-thumbs-down-dislike.png"\] Alt text: Thumbs down icon.\). When you select the thumbs up or thumbs down icon, you are prompted to provide detailed feedback by selecting one or more reason check boxes. You can also select **Other** to add comments or suggestions \(up to 300 characters\). After making your selection, select **Submit** to submit your feedback or select **X** to close the dialog without submitting feedback. All submitted feedback is captured, stored, and made available through analytic dashboards.

\[Omitted image "feedback-panel-granular.png"\] Alt text: Thumbs down granular feedback dialog.

Depending on the context of the response, an additional go to search results icon \(\[Omitted image "nass-search-result-icon.png"\] Alt text: Go to search results icon.\) may appear in the feedback icons panel. This icon appears alongside synthesized responses in Virtual Agent, clarifying questions in Virtual Agent, and regular search results or Virtual Agent fallback topics whenever a synthesized response is unavailable. Selecting the go to search results icon \(\[Omitted image "nass-search-result-icon.png"\] Alt text: Go to search results icon.\) redirects you to the search results page and begins a search query using the last five chat utterances you entered.Additionally, a copy message icon \(\[Omitted image "dw-feedback-copy-message-icon.png"\]\) appears on received Virtual Agent responses.

\[Omitted image "nava-premium-feedback-panel.png"\] Alt text:

Responses generated in Now Assist in Virtual Agent can come from a combination of catalog items, Virtual Agent topics, subflows and actions, knowledge articles, attachments, external content sources, and people citations. Inline citations appear at the end of the relevant synthesized response sentence. Selecting an inline citation results in a popover containing either a link to an article or source, or a description and action to start the action. The following options may appear as synthesized response in-line citations depending on what search results are returned:

-   Catalog
-   Topic, subflows, or actions
-   Q&amp;A Knowledge Base articles
-   External content connections
-   People
-   Extended entities and additional records

**Note:** Q&amp;A Knowledge Base and external content connection citations also appear within the expandable **Show sources** option.

## Response feedback

Each Virtual Agent response includes a feedback icons panel. The feedback icons panel appears on the latest Virtual Agent response and whenever you hover over any Virtual Agent response. You can indicate if the response was helpful by selecting the like thumbs up icon \(\[Omitted image "llm-thumbs-up-like.png"\] Alt text: Thumbs up icon.\). If the response wasn't helpful, select the dislike thumbs down icon \(\[Omitted image "llm-thumbs-down-dislike.png"\] Alt text: Thumbs down icon.\). When you select the thumbs up or thumbs down icon, you are prompted to provide detailed feedback by selecting one or more reason check boxes. You can also select **Other** to add comments or suggestions \(up to 300 characters\). After making your selection, select **Submit** to submit your feedback or select **X** to close the dialog without submitting feedback. All submitted feedback is captured, stored, and made available through analytic dashboards.

\[Omitted image "feedback-panel-granular.png"\] Alt text: Thumbs down granular feedback dialog.

Depending on the context of the response, an additional go to search results icon \(\[Omitted image "nass-search-result-icon.png"\] Alt text: Go to search results icon.\) may appear in the feedback icons panel. This icon appears alongside synthesized responses in Virtual Agent, clarifying questions in Virtual Agent, and regular search results or Virtual Agent fallback topics whenever a synthesized response is unavailable. Selecting the go to search results icon \(\[Omitted image "nass-search-result-icon.png"\] Alt text: Go to search results icon.\) redirects you to the search results page and begins a search query using the last five chat utterances you entered.Additionally, a copy message icon \(\[Omitted image "dw-feedback-copy-message-icon.png"\]\) appears on received Virtual Agent responses.

## Extended entities and view records

Extended entity information can be found if you have activated Knowledge Graph.

**Note:** To enable the Knowledge Graph natural language query \(NLQ\) schema, configure this schema for the assistant. To configure the schema for an assistant, see [Assign search sources to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/add-info-sources-assistant.md).

These extended entities that come from the additional custom tables associated with the Knowledge Graph natural language query \(NLQ\) schema can include:

-   Assets
-   Incidents
-   Recently viewed knowledge base articles
-   Requests
-   Tasks

Select an entity in-line citation to view that entity record in a new tab, or select **View records** to view a list of additional entities. Selecting a link from the **View records** pop-up opens a new tab with that entity table's data.

## Chatting with a live agent in Virtual Agent

You can chat with a live agent if you need more support. Select the **Contact Live Agent** button found in the Support and settings \(\[Omitted image "ellipsis-vertical-outline-24.svg"\] Alt text: Support and settings icon.\) option, enter a request such as `Chat with live agent` into the chat, or select the **Request a live agent** fallback option. After an agent has accepted your chat, the agent's name and avatar appears at the top of the chat in a banner. Only one live agent chat at a time is permitted. To exit the live chat, select **End live chat**. The chat history then moves to the Closed chat section.

\[Omitted image "dw-end-live-chat-yp6.png"\] Alt text: End live chat button appears in a banner at the top of the chat.

## Submitting catalog requests

You can submit catalog requests directly from Now Assist in Virtual Agent premium chat without leaving the chat experience.

To submit a catalog request:

1.  Open Now Assist in Virtual Agent premium chat.
2.  Find a catalog item through chat.
3.  Select the item and a catalog form opens inline in the interactive view.
4.  Complete the required form fields.
5.  Select **Submit**. A confirmation message appears and your request record is created.

## Catalog submission confirmation

After you successfully submit a catalog item, a confirmation message appears with a **View Details** button that opens your submitted request record.

The **View Details** button behaves in the following ways:

-   In Virtual Agent portals: Select **View Details** to open the submitted request record in a new browser tab. The Virtual Agent chat window shrinks to floating mode.
-   In pop-out windows: If you select the pop-out icon on a submitted catalog form, the new window displays the submission confirmation page with your request details, not a blank form to start over.

## Fallback options

**Note:** For more information about where and how to enable fallback options, see [Manage an assistant chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/manage-assistant-chat-experience.md).

A fallback state can occur whenever search results are unavailable. Scenarios where search results are unavailable include the Virtual Agent didn't understand the query, complaint small talk was found, or an error occurred. When search results are unavailable, a single or multiple fallback options may appear. These fallback options include:

-   **Request a live chat**: Triggers live agent mode and routes you to a human support representative.
-   **Search the web**: Triggers web search mode and uses the internet to search for the results.

    **Note:** Only the last query entered into the conversation is considered when entering web search mode via this **Search the web** fallback option.

-   **Create a generic ticket**: Creates a record.
-   **Custom fallback option**: Presents a fallback Virtual Agent topic.

Select a fallback option to launch that mode or action.

\[Omitted image "dw-web-search-fallback-example.png"\] Alt text: Search the web and Create a generic ticket buttons are fallback options for end users.

When you're using premium chat and you enter a search query through your portal's search bar, you’re redirected to the portal's search results page. At the top of the search results page, you see Genius Results in a synthesized response generated by Now Assist. This synthesized response answer provides inline citations that appear at the end of each sentence. You can select citations and if applicable, such as for conversational catalog items, select whether to \[Omitted image "nass-open-new-tab-icon.png"\] Alt text: Request with form icon.**Request with form** or \[Omitted image "nass-chat-bubble-icon.png"\] Alt text: Request in chat icon.**Request in chat**. Similar options also appear in the regular search results area, as indicated by the request in chat icon \( \[Omitted image "nass-chat-bubble-icon.png"\] Alt text: Request in chat icon.\) and request with form icon \(\[Omitted image "nass-open-new-tab-icon.png"\] Alt text: Request in form icon.\). Depending on your selection, the catalog request flow launches within either the Virtual Agent chat or a form.

\[Omitted image "dw-synthesized-response-search-bar.png"\] Alt text: A synthesized response appears at the top of the search results after a search query for request laptop was made.

You can start the chat experience either through the chat icon on the portal's search results page or through the portal's chat widget button.

\[Omitted image "dw-syntheszied-response-search-bar-request-variations.png"\] Alt text: Portal search page results with entry points into chat.

\[Omitted image "nava-chat-widget-button-portal.png"\] Alt text:

After selecting the chat widget button on the portal, the floating chat window opens and replaces the chat button. A greeting message appears, and a chat is created only after you have entered an initial utterance. If you have an active chat ongoing, the current active chat appears instead of a greeting message. You can select a predefined action, topic, suggested search query, start a new conversation, or view all options, if applicable. The **View all options** link only shows if more than one suggested search query or promoted topic is available.

**Note:** Any search query entered into the portal’s search bar or Virtual Agent is incorporated into the greeting topic for future conversations as a suggested search query. Suggested search queries can be viewed in the Search Suggestions \[sys\_search\_suggestion.list\] table. For more information on how to enable suggested search queries, see [Now Assist in Virtual Agent system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/nava-sys-props.md).

If language detection is turned on and the initial utterance entered into the portal's search bar or chat differs from the user's profile language preference, the conversational language automatically switches to the detected language. For more information and examples of language detection in premium chat conversations, see [Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/dynamic-lang-detection-translation-enhanced-chat.md).

