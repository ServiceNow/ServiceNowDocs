---
title: ServiceNow Otto for Virtual Agent release notes
description: The ServiceNow Otto for Virtual Agent application uses large language models \(LLMs\) to create a natural-language conversational experience that can improve the success of your self-service workflows. See the following sections for release notes by version.The ServiceNow Virtual Agent application provides user assistance through a conversational interface to help users quickly obtain information and perform common work tasks. Virtual Agent was enhanced and updated in the Brazil release.The September 2026 release deprecated Virtual Agent for NLU and keywords and added several features including upload file size improvements and embed enhanced chat capabilities.HEIDI BETH FEEL FREE TO UPDATE AS WELL. THIS MIMICS OLD HIGHLIGHTS SECTION.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/virtual-agent-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Conversational Interfaces release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow Otto for Virtual Agent release notes

The ServiceNow® Otto for Virtual Agent application uses large language models \(LLMs\) to create a natural-language conversational experience that can improve the success of your self-service workflows. See the following sections for release notes by version.

## About ServiceNow Otto for Virtual Agent

-   Use a conversation designer to build and test conversations without scripting or advanced skills.
-   Empower users to self-serve with AI agents, enhanced or premium chat with AI Search, conversational catalog skills, and more.
-   Seamlessly transfer the entire conversation history and context to the right human agent so they can quickly address any escalations and resolve user issues.

See  for more information.

## Activation and other requirements

**Note:** ServiceNow Otto for Virtual Agent is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Virtual Agent is available with activation of the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) if you have the admin role. For details, see Activate Virtual Agent. Once activated, you can install ServiceNow Otto for Virtual Agent by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    You can upgrade ServiceNow Otto for Virtual Agent from the ServiceNow Store.

-   **Browser requirements**

    Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/browser-support.md).

-   **Additional requirements**

    ServiceNow Otto for Virtual Agent requires at least one ServiceNow Otto product or the Requestor Agents - Foundation plugin.


## Accessibility and localization

-   **Localization information**

    Dynamic Translation is supported for non-streaming ServiceNow Otto for Virtual Agent conversations. For more information, see .


**Parent Topic:**[Conversational Interfaces release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/conversational-interfaces-rn-landing.md)

## October 2026

The ServiceNow® Virtual Agent application provides user assistance through a conversational interface to help users quickly obtain information and perform common work tasks. Virtual Agent was enhanced and updated in the Brazil release.

### What's new



-   **Cancel live agent request**

    In premium chat, select the **Cancel** button on the banner while a live agent request is in process to cancel the request. After the request is cancelled or the live agent connects to the chat, the banner disappears from chat.

-   ****

    Turn voice dictation on or off for an assistant on the **Voice experience** page. For ServiceNow Otto for Virtual Agent assistants, voice dictation is only available for premium chat. For ServiceNow Otto panel – Platform assistant, voice dictation is available for all chat experiences.

    **Note:** Voice dictation was previously known as voice input, which was enabled from within .

-   ****

    For eligible new customers, premium chat is the default and the only available chat experience. If the assistant uses the Now LLM provider, the premium chat option isn't available.

-   **Non-English language recognition for voice input**

    When you speak in the default language selected in your profile, even if this language is non-English, your speech is transcribed into text in that same language.

-   ****

    Measure the quality of your conversational assistant at scale with automated evaluations in Assistant Designer. Choose the metrics that define success for you, such as conversation success, conversation fluency, faithfulness, skill selection accuracy, and turn count. You can run them against your own test data set and ground truth.


### What's changed

-   ****

    The **Prioritize AI agents during skills discovery** option is available when configuring additional chat features. Because all assistants now use agentic orchestration by default, AI agent skills are available during skills discovery. Turning on this option gives AI agents priority over other assets \(such as knowledge bases and Q&amp;A modules\) when the assistant discovers skills. If your assistant has overlapping skills \(for example, a knowledge base article and an AI agent that both answer the same question\), this setting lets you decide which one is prioritized, so you can steer users toward the AI agent experience instead of a static article.

-   ****

    The **sn\_nowassist\_va.assistant\_personalization** system property is removed from the admin experience. This property previously let admins show or hide chat personalization options \(agent persona, tone, and response length\) when branding an assistant. By default, all settings are shown.


### What's deprecated or removed

-   **Agentic support page**

    The **Agentic support** page has been deprecated for ServiceNow Otto for Virtual Agent and ServiceNow Otto panel - Platform. There is no loss of functionality previously provided by the **Agentic support** page. By default, all existing assistants operate in agentic mode. The **Prioritize AI agents during skills discovery** option is available when configuring additional chat features.


## September 2026 \| Early Availability

The September 2026 release deprecated Virtual Agent for NLU and keywords and added several features including upload file size improvements and embed enhanced chat capabilities.

### What's new

-   ****

    For eligible new customers, premium chat is the default and the only available chat experience. If the assistant uses the Now LLM Service provider, the premium chat option isn't available.

-   **Embed on third-party sites for enhanced chat**

    Embed the chat widget for enhanced chat on third-party websites.

-   **View all topics on the premium chat greeting screen**

    Select **View all topics** on the chat’s greeting screen to show all promoted topics in premium chat.


### What's changed

-   ****

    Role-based configuration is no longer stored or managed within Assistant Designer.

-   **Upload files improvements**

    Upload up to 10 files or 50 MB for the following file types: PDF native, PDF OCR, Word, PPTX, Excel, CSV, TXT, JPEG, PNG for premium chat in ServiceNow Otto for Virtual Agent and Otto panel.

-   **Updated ServiceNow Otto processing animation**

    View an updated ServiceNow Otto processing animation.


### What's deprecated or removed

-   **Deprecation of Virtual Agent for NLU and keywords**

    Starting with the Brazil release, Virtual Agent for NLU and Virtual Agent Lite are being prepared for future deprecation. They will eventually be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

-   **Deprecation of Virtual Agent channel integrations applications**

    Starting with the Brazil release, the following Virtual Agent channel integration applications are being prepared for future deprecation:

    -   Conversational Integration with Alexa
    -   Conversational IVR with Amazon Connect
    -   IBM Watson Assistant conversations
    They will eventually be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-llm-model-updates.md)**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


### Plugin information

-   **Plugins planned for deprecation**

    Conversational Analytics \(com.sn.conversational.analytics\): Replace with Assistant Analytics.

    Conversational Integration with Alexa \(com.sn.va.alexa\): There is no replacement for this plugin.

    Conversational IVR with Amazon Connect \(com.sn\_va\_amz.connect\): There is no replacement for this plugin.

    Glide Virtual Agent Lite \(com.glide.cs.chatbot.lite\): Replace with Requestor Agents - Foundation \(direct migration options\), EmployeeWorks - User, EmployeeWorks for GovCloud - User.

    HR Service Delivery NLU Model for Virtual Agent Conversations \(com.sn\_hr\_nlu\_model\): There is no replacement for this plugin.

    HR Service Delivery Virtual Agent Conversations \(com.sn\_hr\_virtual\_agent\): There is no replacement for this plugin.

    IBM Watson integration \(com.glide.cs.ibm.watson.assistant, com.glide.nlu.ibmwatson.intent.discovery, com.glide.cs.ibm.watson.assistant.topic, com.glide.cs.ibm.watson.assistant.topicV2\): There is no replacement for these plugins.

    Intent Discovery \(sn\_nlu\_discovery\): There is no replacement for this plugin.

    Issue Auto Resolution \(com.glide.cs.auto\_resolution\): There is no replacement for this plugin.

    Issue Auto resolution for HR \(com.snc.hr.issue\_auto\_resolution\): There is no replacement for this plugin.

    ITSM Virtual Agent Conversation Topics Lite \(com.snc.itsm.virtualagent.lite\): There is no replacement for this plugin.

    NLU Workbench-Advanced Features \(com.snc.nlu.workbench.advanced\): There is no replacement for this plugin.

    Topic Recommendations \(com.sn\_topic\_recommend\): There is no replacement for this plugin.

-   **Renamed or changed plugins**

    Conversational Integration with Apple Messages for Business \(com.sn.va.abc.adapter\): Deprecation of NLU functionality and migration to LLM support.

    Conversational Integration with AWS End User Messaging \(com.sn\_sms\_aws\_adapter\): Deprecation of Virtual Agent NLU functionality and migration to LLM support.

    Conversational Integration with Facebook Messenger \(com.sn.va.fb.messenger\): Deprecation of Virtual Agent NLU functionality and migration to LLM support.

    Conversational Integration with LINE \(com.sn.va.line\): Deprecation of NLU functionality and migration to LLM support.

    Conversational Interfaces - Diagnostics \(com.sn.ci.diagnostics\): Deprecation of Virtual Agent NLU functionality. There is no replacement.

    Omnichannel Callback for Customer Service Management \(com.sn\_omnichannel\_callback\): Deprecation of NLU functionality and migration to LLM support.

    Virtual Agent NLU \(com.glide.cs.chatbot\): Deprecation of Virtual Agent NLU functionality. Migrate NLU topics to LLM.


