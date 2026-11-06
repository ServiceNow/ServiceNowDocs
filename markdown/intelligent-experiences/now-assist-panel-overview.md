---
title: ServiceNow Otto panel
description: With the ServiceNow Otto panel, you can get assistance from generative AI experiences to solve customer issues faster. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information more quickly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-panel-overview.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
keywords: [Now Assist panel, Gen AI, Generative AI, Next Experience, chat summarization, Incident summarization]
breadcrumb: [ServiceNow Otto Experiences, Exploring AI Admin Hub, AI Admin Hub, Generative AI skills, Enable AI Experiences]
---

# ServiceNow Otto panel

With the ServiceNow Otto panel, you can get assistance from generative AI experiences to solve customer issues faster. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information more quickly.

You must fulfill the following conditions to use the ServiceNow Otto panel:

-   Next Experience must be enabled. For more information, see [Considerations for activating Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-adoption-paths.md).
-   You must have the now\_assist\_panel\_user role.
-   Your role must be applied to at least one active ServiceNow Otto skill to use skills in the ServiceNow Otto panel.

There are three versions of ServiceNow Otto panel chats: standard, enhanced, and premium. Select one of the versions to learn more:

-   [Standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-panel-standard.md) - provides conversational support assistance within a standard, static chat window. To activate the ServiceNow Otto panel standard chat, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/activate-now-assist-panel.md).
-   [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-panel-enhanced.md) - provides conversational support assistance within a dynamic window that gives a more intuitive and personalized experience. You must activate the ServiceNow Otto panel enhanced chat and configure your ServiceNow Otto instance to use the enhanced chat. See [Activate the ServiceNow Otto panel enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-panel-enhanced-activate.md) for more information.
-   [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-panel-premium.md) - provides conversational support assistance within a fully agentic chat experience that enables the assistant to reason across multiple sources and execute complex workflows without leaving the conversation. You must activate the ServiceNow Otto panel premium chat and configure your ServiceNow Otto instance to use the premium chat. See [Display your assistant on Platform or ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/display-nap-assistant.md) for more information.

If you want to use assistants, you must activate them. See [Configure assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md) for information on activating assistants.

**Note:** Voice dictation is automatically activated when you activate the ServiceNow Otto panel. As of the Zurich Patch 4 release, voice dictation is configured in the [Configure Next Experience accessibility preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-accessibility-preferences.md).

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
|Context-aware suggestions|No|No|Limited|
|Response streaming|Yes|Yes|Yes|
|Conversation history|Yes|Yes|Yes|
|Multiple concurrent conversations|No|Yes|Yes|
|Conversations remain active after task completion|No|Yes|Yes|
|AI agents support|Yes|Yes|Yes|
|Tone, response length, and persona settings|No|Yes|Yes|

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
|File upload|Limited|Yes|Yes|
|PDF upload and question answering|No|Yes|Yes|
|Image upload|No|Limited|Yes|
|Text file analysis|No|Yes|Yes|
|File generation|No|No|Yes|

|Feature|Standard chat|Enhanced chat|Premium chat|
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
|Full agentic AI support|Yes|Yes|Yes|
|Branding and personalization \(chat header, logo\)|No|No|Yes|

For help with installation, see [Solving installation and configuration issues with ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-install-config-checklist.md).

-   **[Standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-panel-standard.md)**  
With the ServiceNow Otto panel standard chat, you can get assistance from generative AI experiences to solve customer issues faster. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information more quickly.
-   **[Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-panel-enhanced.md)**  
ServiceNow Otto panel enhanced chat is a conversational support experience within a dynamic window that also includes the ability to have multiple active conversations and superior search capabilities. Use ServiceNow Otto panel enhanced chat to improve your productivity and efficiency by leveraging generative AI to perform tasks such as summarize a chat, case, or incident, request help, generate resolution notes, among others.
-   **[Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-panel-premium.md)**  
ServiceNow Otto panel premium chat is an AI chat experience built into your ServiceNow environment. Ask questions, get answers from your organization's knowledge, and take action on records. It supports file uploads, web search, and multistep agentic tasks, so you can handle more complex requests without leaving the panel.

**Parent Topic:**[ServiceNow Otto Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-experiences.md)

