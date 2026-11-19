---
title: Using ServiceNow Otto for Virtual Agent
description: ServiceNow Otto for Virtual Agent enhances the user experience by combining AI Search with generative or agentic AI chat skills. These skills can speed up issue resolution and reduce deflection to a live agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/using-now-assist-in-va.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [Using, Now Assist, Virtual Agent, AI Search, enhanced chat, dynamic window, full-page experience, full page experience, standard chat, genius results, generative AI]
breadcrumb: [ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Using ServiceNow Otto for Virtual Agent

ServiceNow® Otto for Virtual Agent enhances the user experience by combining AI Search with generative or agentic AI chat skills. These skills can speed up issue resolution and reduce deflection to a live agent.

## Standard, enhanced, and premium chat

During the ServiceNow Otto for Virtual Agent guided setup, you may be presented with three user experiences to select from:

-   Standard chat
-   Enhanced chat
-   Premium chat

Standard chat is a conversational support experience within a static chat widget. Enhanced and premium chat are conversational experiences within a resizable and movable chat window that includes the ability to have multiple active conversations. Enhanced and premium chat enable users to choose their way of engaging with ServiceNow Otto on their ServiceNow portals from a variety of entry points.

When choosing enhanced chat from the guided setup, if you also have AI Search enabled on your portal, you're presented with the **Allow the search bar to open into a full-page chat experience** option. If you select this option, your conversational and search experience appears as a full page inside the portal. The conversational fluidity and citation behavior between the enhanced chat and full-page experience remains the same regardless of which chat experience you choose. You can still access enhanced chat's resizable and moveable chat window when you have full-page experience turned on. Turning on the enhanced chat full-page experience further combines chat and search capabilities by redirecting you into a full-page chat after entering a query into a portal's search bar. For more information about enhanced chat's full-page experience, see [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md).

Premium chat automatically comes with a full-page chat experience option where conversational and search experiences are more intertwined and present a seamless display. When you enter a query or request from the portal's search bar, you're automatically brought into a full-page conversational search experience. Premium chat is the latest version of the ServiceNow® Otto for Virtual Agent conversational experience. It's a redesigned chat interface powered by the AI Services architecture. It moves agentic orchestration and conversations to an AI-native technology infrastructure that supports more continuous feature releases and interactive experiences.

**Note:** For more information about selecting a chat experience in the admin guided setup, see [Display your assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/display-assistant-portal-channel.md).

The types of citations that appear in synthesized responses are the same between standard, enhanced, or premium chat, but their formatting differs. The following citations may appear in your synthesized results:

-   Catalog
-   Topic, subflows, or actions
-   Q&amp;A Knowledge Base articles
-   External content connections
-   People

For more information on these citations, see their respective sections in [Standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/nava-standard-chat.md), [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md), or [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/nava-integrated-chat.md).

The appearance of the default chat widget button varies depending on whether you have standard, enhanced, or premium chat turned on. The default standard chat button displays as a traditional message icon and the default enhanced chat or premium chat button displays as the universal ServiceNow Otto icon. This button is only accessible through portal pages. While in enhanced or premium chat's full-page experience, you're unable to access the chat widget button.

\[Omitted image "NAVA-FAB.png"\] Alt text: Standard chat widget button displayed as a traditional message icon.

\[Omitted image "NASS-dynamic-window-FAB.png"\] Alt text: Enhanced chat or premium chat widget button displayed as the universal Otto icon.

**Warning:** Do not modify or remove the default AI disclaimer. If you modify or remove the default AI disclaimer, you're responsible for communicating to end users that they are interacting with an AI system and any associated risks. ServiceNow is not responsible for the effects of any changes made.

## Differences between display experiences

The following list includes benefits of premium chat:

-   Faster responses
-   Real-time personalization through dynamic experience generation
-   Open-source widget ecosystem with customizable UI components
-   Rich content generation, such as charts, visualizations, and interactive elements
-   AI Services foundation for large language model \(LLM\) orchestration

The following tables outline feature differences between standard, enhanced, and premium chat.

|Feature|Standard chat|Enhanced chat|Premium chat|
|-------|-------------|-------------|------------|
|Movable or resizable interface|No|Yes|Yes|
|Full-screen experience|No|Yes|Yes|
|Portal's search bars redirect to include chat capabilities or directly into chat|No|Yes|Yes|
|Mobile-optimized interface|Yes|Yes|Yes|
|Customizable widgets|No|No|Yes|
|Interactive view|No|Yes|Yes|
|Dark mode|No|Limited|Yes|
|Personalized greeting message|Yes|Yes|Yes|
|Prompt library|No|No|Yes|
|Guest user elevation|Yes|Yes|Limited|
|View all topics/Show all options|Yes|Yes|Yes|
|Virtual Agent Notifications|Yes|Yes|No|
|Post-chat survey|Yes|Yes|No|

|Feature|Standard chat|Enhanced chat|Premium chat|
|-------|-------------|-------------|------------|
|Portal knowledge search|Yes|Yes|Yes|
|Unified search with internal and external sources|No|Yes|Yes|
|Web search integration|Yes|Yes|Yes|
|Suggestive search results|No|Limited|Yes|
|Catalog search integration|Yes|Yes|Yes|

|Feature|Standard chat|Enhanced chat|Premium chat|
|-------|-------------|-------------|------------|
|Basic text chat|Yes|Yes|Yes|
|AI-powered responses|Yes|Yes|Yes|
|Generative AI based on large language models \(LLMs\)|Yes|Yes|Yes|
|Response streaming|Yes|Yes|Yes|
|Conversation history|Yes|Yes|Yes|
|Multiple concurrent conversations|No|Yes|Yes|
|Conversations remain active after task completion|No|Yes|Yes|
|AI agents support|Yes|Yes|Yes|
|Topics support|Yes|Yes|Yes|
|Subflows support|Yes|Yes|Yes|
|Actions support|Yes|Yes|Yes|
|Custom skills support|Yes|Yes|Yes|
|Agentic processing stop capabilities|Yes|Yes|No|
|Tone, response length, and persona settings|No|Yes|Yes|
|Post-chat survey|Yes|Yes|No|

<table id="table_j35_l3k_xkc"><thead><tr><th>

Feature

</th><th>

Standard chat

</th><th>

Enhanced chat

</th><th>

Premium chat

</th></tr></thead><tbody><tr><td>

Multilingual UI

</td><td>

Yes

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Multilingual responses

</td><td>

Limited

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Dynamic language detection

</td><td>

Yes

</td><td>

Yes

</td><td>

Limited **Note:** Only tier 1 languages are supported.

</td></tr></tbody>
</table>|Feature|Standard chat|Enhanced chat|Premium chat|
|-------|-------------|-------------|------------|
|Virtual Agent in Employee Center \(portal\)|Yes|Yes|Yes|
|Third-party website|No|Yes|No|
|Now Assist panel \(workspace\)|Yes|Yes|Yes|
|Microsoft Teams integration|Yes|No|Yes|
|Slack integration|Yes|No|No|
|Mobile-optimized web interface|Yes|Yes|Yes|
|Google Chat integration|Yes|No|No|
|Microsoft Copilot integration|Yes|No|No|
|WhatsApp integration \(Twilio\)|Yes|No|No|
|SMS integration \(Twilio\)|Yes|No|No|
|Cisco Webex integration|No|No|No|

|Feature|Standard chat|Enhanced chat|Premium chat|
|-------|-------------|-------------|------------|
|Conversation count|Yes|Yes|Yes|
|User engagement metrics|Yes|Yes|Yes|
|Resolution rate|Yes \(manual\)|Yes \(manual\)|Yes \(automated\)|
|AI response quality scoring|No|No|Yes|
|Conversation satisfaction \(CSAT\)|Yes \(manual\)|Limited|Yes|

|Feature|Standard chat|Enhanced chat|Premium chat|
|-------|-------------|-------------|------------|
|Custom styling \(chat header, logo, and menu\)|Yes|Yes|Yes|
|Full agentic AI support|Yes|Yes|Yes|
|Branding and personalization|Yes|Yes|Yes|

## Prerequisite requirements for standard and enhanced chat

Standard and enhanced chat require the ServiceNow default chat widget button to be turned on. Complete the following actions for enhanced chat to display a synthesized response after entering a search query through the portal:

-   [Configure the portal's AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/configuring-ais.md).
-   Turn on the ServiceNow default Search page widget.
-   Turn on the ServiceNow default chat widget button.

Complete the following actions for enhanced chat to display a synthesized response in the full-page experience after entering a search query through the portal's search bar:

-   Configure the portal's AI Search.
-   Turn on the ServiceNow default Search page widget.
-   Turn on the ServiceNow default chat widget button.
-   Turn on the ServiceNow default Search Typeahead widget.

For information about premium chat prerequisite requirements, see [Prerequisites for premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/premium-chat-prereqs.md).

## More information

Want to learn more? Visit these resources.

-   For more information on enhanced chat, see [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md).
-   For more information on enhanced chat in Employee Center, see [Enhanced chat in Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/nass-now-assissist-self-service.md).
-   For more information on enhanced chat in self-service portals, see [Now Assist conversational experience in self-service portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/nass-portal.md).
-   For more information on premium chat, see [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/nava-integrated-chat.md).
-   For more information about third-party AI model providers, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)
-   For more information about model provider support, see [Model Provider support availability for ServiceNow Otto skills and AI Agents](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2222333).
-   For more information on turning on a chat display, see [Display your assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/display-assistant-portal-channel.md).
-   For more information on ServiceNow Otto, see [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md).
-   For more information on ServiceNow Otto for AI Search, see [ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-ais.md).
-   For more information on language support, see [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/translation-for-now-assist.md).
-   For more information on ServiceNow Otto for Virtual Agent analytics, see [Analyzing assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/ai-engagement-analytics.md).

