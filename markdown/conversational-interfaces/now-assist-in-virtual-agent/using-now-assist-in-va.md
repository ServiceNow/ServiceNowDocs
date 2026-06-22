---
title: Using Now Assist in Virtual Agent
description: Now Assist in Virtual Agent enhances the user experience by combining AI Search with generative AI chat skills. These skills can speed up issue resolution and reduce deflection to a live agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/now-assist-in-virtual-agent/using-now-assist-in-va.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
keywords: [Using, Now Assist, Virtual Agent, AI Search, enhanced chat, dynamic window, full-page experience, full page experience, standard chat, genius results, generative AI]
breadcrumb: [Now Assist in Virtual Agent, Conversational Interfaces]
---

# Using Now Assist in Virtual Agent

Now Assist in Virtual Agent enhances the user experience by combining AI Search with generative AI chat skills. These skills can speed up issue resolution and reduce deflection to a live agent.

## Standard, enhanced, and premium chat

During the Now Assist in Virtual Agent guided setup, you may be presented with three user experiences to select from: standard chat, enhanced chat, or premium chat. Standard chat is a conversational support experience within a static chat widget. Enhanced chat and premium chat are conversational experiences within a resizable and movable chat window that include the ability to have multiple active conversations. Enhanced and premium chat enable users to choose their way of engaging with Now Assist on their ServiceNow portals from a variety of entry points. When choosing enhanced or premium chat from the guided setup, if you also have AI Search enabled on your portal, you’re presented with the **Allow the search bar to open into a full-page chat experience** option. If you select this option, your conversational and search experience appears as a full page inside the portal. The conversational fluidity and citation behavior between the enhanced or premium chat and the chat's full-page experience remains the same regardless of which chat experience you choose. You can still access enhanced or premium chat's resizable and moveable chat window when you have full-page experience turned on and are on screens other than the full-page experience itself. Turning on enhanced or premium chat's full-page experience further combines chat and search capabilities by redirecting you into a full-page chat after entering a query into a portal's search bar.

**Note:** For more information about selecting a chat experience in the admin guided setup, see [Display your chat assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/display-assistant-portal-channel.md).

The following table outlines feature differences between standard, enhanced, and premium chat.

|Feature|Standard chat|Enhanced chat|Premium chat|
|-------|-------------|-------------|------------|
|Portal's search bars redirect to include chat capabilities or directly into chat|No|Yes|Yes|
|Chat window resizable and moveable|No|Yes|Yes|
|Interactive view|No|Yes|Yes|
|Multiple active conversations|No|Yes|Yes|
|Conversations remain active after task completion|No|Yes|Yes|
|View all topics/Show all options|Yes|Yes|Yes|

The types of citations that appear in synthesized responses are the same between standard and enhanced or premium chat, but their formatting differs. The following citations may appear in your synthesized results:

-   Catalog
-   Topic, subflows, or actions
-   Q&amp;A Knowledge Base articles
-   External content connections
-   People

For more information on these citations, see their respective sections in [Standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-standard-chat.md), [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md), or [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-integrated-chat.md).

The appearance of the default chat widget button varies depending on whether you have standard, enhanced, or premium chat turned on. The default standard chat button displays as a traditional message icon and the default enhanced chat or premium chat button displays as the universal AI-generated sparkle icon. This button is only accessible through portal pages. While in enhanced or premium chat's full-page experience, you’re unable to access the chat widget button.

\[Omitted image "NAVA-FAB.png"\] Alt text: Chat bubble button.

\[Omitted image "NASS-dynamic-window-FAB.png"\] Alt text: Sparkle button.

## Enhanced or premium chat's full-page experience

Where your users learn about search results differs between the enhanced or premium chat and enhanced or premium chat's full-page experience. For enhanced or premium chat, when you enter a search query through your portal's search bar, you’re redirected to the portal's search results page. At the top of the search results page, you see Genius Results in a synthesized response generated by Now Assist. When you're using enhanced or premium chat's full-page experience and you enter a search query through one of the portal's search bars, you’re redirected to the full-page experience's chat tab. Within the chat tab, you may see a synthesized response generated by Now Assist within a conversation depending on your utterance. You continue the conversation within the chat tab.

\[Omitted image "nass-full-page-now-assist-tab-zp4.png"\] Alt text: A synthesized response appears for an order a laptop prompt in the Now Assist tab.

The conversational fluidity and citation behavior between the enhanced or premium chat and enhanced or premium chat's full-page experience remains the same regardless of which chat experience you use. The conversations that you have either through the enhanced or premium chat's window or full-page experience remain in synchronization, and the conversational history is retained in both mediums. For example, if you enter `Order a loaner laptop` the conversational fluidity and citations that appear are the same whether in enhanced or premium chat or enhanced or premium chat's full-page experience. If you begin the laptop catalog request in the full-page experience, you can still view and continue the conversation in the enhanced or premium chat's window because the chat experiences remain in synchronization with one another. For more information about conversational behavior and citations, see [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md) or [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-integrated-chat.md).

Each Virtual Agent response includes a feedback icons panel. The feedback icons panel appears on the latest Virtual Agent response and whenever you hover over any previous Virtual Agent response. You can indicate if the response was helpful by selecting the like thumbs up icon \(\[Omitted image "llm-thumbs-up-like.png"\] Alt text: Thumbs up icon.\). If the response wasn't helpful, select the dislike thumbs down icon \(\[Omitted image "llm-thumbs-down-dislike.png"\] Alt text: Thumbs down icon.\). This feedback is used to train the LLM model and improve responses over time. Depending on the context of the response, an additional go to search results icon \(\[Omitted image "nass-search-result-icon.png"\] Alt text: Go to search results icon.\) may appear in the feedback icons panel. This icon appears alongside synthesized responses in Virtual Agent, clarifying questions in Virtual Agent, and fallback topics whenever a synthesized response is unavailable but there are regular search results available. When the full-page experience is on and you select the go to search results icon \(\[Omitted image "nass-search-result-icon.png"\] Alt text: Go to search results icon.\), you’re redirected to the **Search** tab. After redirecting to the **Search** tab, a search query using the last five chat utterances you entered begins.Additionally, a copy message icon \(\[Omitted image "dw-feedback-copy-message-icon.png"\]\) appears on received Virtual Agent responses.

The Now Assist sub-header consists of four elements. The following figure and table shows an example and description of those elements.

\[Omitted image "nass-full-page-now-assist-tab-figure-zp4.png"\] Alt text: Chat window controls include New Chat, Chats, Support, and Settings.

<table id="table_qzq_r2c_qfc"><thead><tr><th>

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
</table>While in the full-page experience, you can select the **Search** tab. Selecting the **Search** tab auto-populates the search bar with the first utterance found in the chat tab, but a search query doesn’t begin. The chat and **Search** tabs are otherwise independent of the other, so running a search doesn’t impact your existing chats nor does starting new chats impact your existing search results. You must enter text into the search bar so that the search bar becomes active and then you can submit your search. The search results that appear in the **Search** tab resemble the search results found on the portal page, excluding the Genius Results synthesized response. Two icons may appear next to the search results:

-   \[Omitted image "nass-chat-bubble-icon.png"\] Alt text: Request in Chat icon. \(Request in Chat\)

    The \[Omitted image "nass-chat-bubble-icon.png"\] Alt text: Request in Chat icon. \(Request in Chat\) icon opens the conversational catalog into a new chat.

-   \[Omitted image "nass-open-new-tab-icon.png"\] Alt text: Open in New Tab icon. \(Open in New Tab\)

    The \[Omitted image "nass-open-new-tab-icon.png"\] Alt text: Open in New Tab icon. \(Open a New Tab\) icon redirects you to either complete a catalog form or view content in a new tab.


\[Omitted image "nass-full-page-search-tab-zp4.png"\] Alt text: Order a laptop search results appear in the Search tab of the full-page experience.

The following table outlines the preceding feature differences between enhanced chat window and enhanced chat full-page experience.

<table id="table_tn4_mfp_s2c"><thead><tr><th>

Feature

</th><th>

Enhanced chat

</th><th>

Enhanced chat full-page experience

</th></tr></thead><tbody><tr><td>

Entry points

</td><td>

-   Entering an utterance into the chat through the chat widget button.
-   The portals search results page's synthesized response via chat icon \(\[Omitted image "nass-chat-bubble-icon.png"\] Alt text: Request in Chat icon.\) or Request in chat link from popover.
-   Notifications

</td><td>

-   Entering an utterance into the portal's search bar.
-   The go to search results icon \(\[Omitted image "nass-search-result-icon.png"\] Alt text: Go to search results icon.\) from an enhanced chat's chat window response.

</td></tr><tr><td>

Portal search bar results

</td><td>

Redirects to the portal's search page results.

</td><td>

Redirects into the full-page experience's chat tab.

</td></tr></tbody>
</table>## Prerequisite requirements for standard, enhanced, and premium chat

Standard, enhanced, and premium chat require the ServiceNow default chat widget button to be turned on. The following actions must be completed for enhanced or premium chat to display a synthesized response after entering a search query through the portal:

-   [Configure the portal's AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-ais.md)
-   Turn on the ServiceNow default Search page widget.
-   Turn on the ServiceNow default chat widget button.

The following actions must be completed for enhanced or premium chat to display a synthesized response in the full-page experience after entering a search query through the portal's search bar:

-   Configure the portal's AI Search configured
-   Turn on the ServiceNow default Search page widget.
-   Turn on the ServiceNow default chat widget button.
-   Turn on the ServiceNow default Search Typeahead widget.

## More information

Want to learn more? Visit these resources.

-   For more information on enhanced chat, see [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md).
-   For more information on enhanced chat in Employee Center, see [Enhanced chat in Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/nass-now-assissist-self-service.md).
-   For more information on enhanced chat in self-service portals, see [Now Assist conversational experience in self-service portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/nass-portal.md).
-   For more information on premium chat, see [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-integrated-chat.md).
-   For more information on Now Assist, see [Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/platform-now-assist-landing.md).
-   For more information on Now Assist in AI Search, see [Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-ais.md).
-   For more information on language support, see [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/translation-for-now-assist.md).
-   For more information on Now Assist in Virtual Agent analytics, see .

