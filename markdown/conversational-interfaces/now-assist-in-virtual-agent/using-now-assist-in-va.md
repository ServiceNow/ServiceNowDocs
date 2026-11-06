---
title: Using ServiceNow Otto for Virtual Agent
description: ServiceNow Otto for Virtual Agent enhances the user experience by combining AI Search with generative or agentic AI chat skills. These skills can speed up issue resolution and reduce deflection to a live agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/now-assist-in-virtual-agent/using-now-assist-in-va.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
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

When choosing enhanced chat from the guided setup, if you also have AI Search enabled on your portal, you're presented with the **Allow the search bar to open into a full-page chat experience** option. If you select this option, your conversational and search experience appears as a full page inside the portal. The conversational fluidity and citation behavior between the enhanced chat and full-page experience remains the same regardless of which chat experience you choose. You can still access enhanced chat's resizable and moveable chat window when you have full-page experience turned on. Turning on the enhanced chat full-page experience further combines chat and search capabilities by redirecting you into a full-page chat after entering a query into a portal's search bar. For more information about enhanced chat's full-page experience, see [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md).

Premium chat automatically comes with a full-page chat experience option where conversational and search experiences are more intertwined and present a seamless display. When you enter a query or request from the portal's search bar, you're automatically brought into a full-page conversational search experience. Premium chat is the latest version of the ServiceNow® Otto for Virtual Agent conversational experience. It's a redesigned chat interface powered by the AI Services architecture. It moves agentic orchestration and conversations to an AI-native technology infrastructure that supports more continuous feature releases and interactive experiences.

**Note:** For more information about selecting a chat experience in the admin guided setup, see [Display your assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/display-assistant-portal-channel.md).

The types of citations that appear in synthesized responses are the same between standard, enhanced, or premium chat, but their formatting differs. The following citations may appear in your synthesized results:

-   Catalog
-   Topic, subflows, or actions
-   Q&amp;A Knowledge Base articles
-   External content connections
-   People

For more information on these citations, see their respective sections in [Standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/nava-standard-chat.md), [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md), or [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/nava-integrated-chat.md).

The appearance of the default chat widget button varies depending on whether you have standard, enhanced, or premium chat turned on. The default standard chat button displays as a traditional message icon and the default enhanced chat or premium chat button displays as the universal ServiceNow Otto icon. This button is only accessible through portal pages. While in enhanced or premium chat's full-page experience, you're unable to access the chat widget button.

\[Omitted image "NAVA-FAB.png"\] Alt text: Standard chat widget button displayed as a traditional message icon.

\[Omitted image "NASS-dynamic-window-FAB.png"\] Alt text: Enhanced chat or premium chat widget button displayed as the universal Otto icon.

**Warning:** Do not modify or remove the default AI disclaimer. If you modify or remove the default AI disclaimer, you're responsible for communicating to end users that they are interacting with an AI system and any associated risks. ServiceNow is not responsible for the effects of any changes made.

## Differences between display experiences

The following tables outline feature differences between standard, enhanced, and premium chat.

|Feature|Standard chat|Enhanced chat|Premium chat|
|-------|-------------|-------------|------------|
|Portal's search bars redirect to include chat capabilities or directly into chat|No|Yes|Yes|
|Chat window resizable and moveable|No|Yes|Yes|
|Interactive view|No|Yes|Yes|
|Multiple active conversations|No|Yes|Yes|
|Conversations remain active after task completion|No|Yes|Yes|
|View all topics/Show all options|Yes|Yes|Yes|

## Prerequisite requirements for standard and enhanced chat

Standard and enhanced chat require the ServiceNow default chat widget button to be turned on. Complete the following actions for enhanced chat to display a synthesized response after entering a search query through the portal:

-   [Configure the portal's AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configuring-ais.md).
-   Turn on the ServiceNow default Search page widget.
-   Turn on the ServiceNow default chat widget button.

Complete the following actions for enhanced chat to display a synthesized response in the full-page experience after entering a search query through the portal's search bar:

-   Configure the portal's AI Search.
-   Turn on the ServiceNow default Search page widget.
-   Turn on the ServiceNow default chat widget button.
-   Turn on the ServiceNow default Search Typeahead widget.

For information about premium chat prerequisite requirements, see [Prerequisites for premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/premium-chat-prereqs.md).

## More information

Want to learn more? Visit these resources.

-   For more information on enhanced chat, see [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md).
-   For more information on enhanced chat in Employee Center, see [Enhanced chat in Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/nass-now-assissist-self-service.md).
-   For more information on enhanced chat in self-service portals, see [ServiceNow Otto conversational experience in self-service portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/nass-portal.md).
-   For more information on premium chat, see [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/nava-integrated-chat.md).
-   For more information about third-party AI model providers, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)
-   For more information about model provider support, see [Model Provider support availability for ServiceNow Otto skills and AI Agents](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2222333).
-   For more information on turning on a chat display, see [Display your assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/display-assistant-portal-channel.md).
-   For more information on ServiceNow Otto, see [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).
-   For more information on ServiceNow Otto for AI Search, see [ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/now-assist-ais.md).
-   For more information on language support, see [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/translation-for-now-assist.md).
-   For more information on ServiceNow Otto for Virtual Agent analytics, see [Analyzing assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/ai-engagement-analytics.md).

