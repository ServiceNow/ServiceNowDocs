---
title: Virtual Agent release notes
description: The ServiceNow Virtual Agent application provides user assistance through a conversational messaging interface so that you can design and build automated conversations that help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
---

# Virtual Agent release notes

The ServiceNow® Virtual Agent application provides user assistance through a conversational messaging interface so that you can design and build automated conversations that help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Xanadu release.

## Virtual Agent highlights for the Xanadu release

[Xanadu Patch 9](../quality/xanadu-patch-9.md)

-   View people information in the synthesized response along with people citation when you search a person in Microsoft Teams chat.
-   AI agent support for Virtual Agent.
-   View AI agents in Virtual Agent Designer.

-   Integrate ServiceNow® Now Assist for Virtual Agent with Microsoft Copilot to enable making IT-related calls and resolve tasks without having to leave the Microsoft Teams tenant.
-   Enable Now LLM Service support for Virtual Agent conversations in Conversational Integration with Microsoft Teams and Conversational Integration with Slack.
-   Review and test large language model \(LLM\) topic descriptions against existing Natural Language Understanding \(NLU\) utterances, migrate Virtual Agent notifications and Proactive Triggers, and migrate NLU vocabulary sources in the NLU to LLM topic migration workflow.
-   Configure One Extend Rate Limit for incoming requests for providers.
-   Now Assist conversational experience using Now Virtual Agent bot and Self-configured bots within Microsoft Copilot.

Xanadu Patch 3

-   Use an updated Virtual Agent Designer list-based home page that includes conversational subflows and actions.
-   Work with conversations associated to primary and secondary assistants in Virtual Agent Designer.
-   Use language detection and engage in small talk within LLM conversations.
-   Receive a synthesized response for Now Assist in Virtual Agent users.

See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) for more information.

**Note:** Performance and the user experience are improved by tracking aggregate in-app activity, including interaction with the app. This tracking is focused on aggregated technical information rather than personal information.

## New in the Xanadu release

-   **[AI agents in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    View AI agents created in AI Agent Studio in Virtual Agent Designer.


-   **Quick start tests for [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Virtual Agent works as expected. If you customized Virtual Agent, copy the quick start tests and configure them for your customizations.

-   **Rich text for Static and Dynamic Choice controls: [Static Choice user input control](https://www.servicenow.com/docs/access?context=va-static-choicelist&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) and [Dynamic Choice user input control](https://www.servicenow.com/docs/access?context=va-reference-choicelist&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Use rich text options when creating Static and Dynamic Choice nodes in ServiceNow® Virtual Agent Designer.

-   **Virtual Agent Web Client branding: [Set up your Virtual Agent bot's branding](https://www.servicenow.com/docs/access?context=ac-configure-chat-branding&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Customize colors in the New Messages Above and New Messages Below banners in the chat window.

-   **LLM topic type association: [Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Associate LLM Assistants to Setup topics, Topic blocks, and Custom controls.

-   **[LLM topic testing](https://www.servicenow.com/docs/access?context=test-llm-topics&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Define an assistant on the Virtual Agent \(VA\) testing panel, when selecting Test All Active Topics with selecting an assistant.

-   **[LLM Text bot response control](https://www.servicenow.com/docs/access?context=va-ai-response&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Use the LLM Text bot response control to generate messages in conversations using LLM topic discovery.

-   **[Conversational Analytics dashboard in Platform Analytics experience](https://www.servicenow.com/docs/access?context=VA-dashboard-landing-page-pae&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    The Conversational Analytics dashboard in the ServiceNow® Platform Analytics experience meets the compliance requirements of data regulated market environments, for example, Government Community Cloud \(GCC\). The dashboard contains indicators and breakdowns for rich visualizations and detailed analysis. You can access the dashboard by navigating to **All** &gt; **Conversational Interfaces** &gt; **Analytics**.

-   **[New system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Determine whether actions for Virtual Agent notifications and Proactive Triggers are created after completing the full topic migration workflow via the **com.glide.cs.notification.create\_llm\_actions\_after\_topic\_migration** and **com.glide.cs.proactive\_trigger.create\_llm\_actions\_after\_topic\_migration** system properties.

-   **[NLU to LLM topic migration enhancements](https://www.servicenow.com/docs/access?context=llm-topic-migration&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**
    -   Migrate Virtual Agent notifications and Proactive Triggers actions on the Review connections step after publishing the newly migrated LLM topics in the NLU to LLM topic migration workflow.
    -   Review, edit, and test LLM topic descriptions against existing NLU utterances, if available, in the Review descriptions step. The Review descriptions step occurs after migration but before publication in the NLU to LLM topic migration workflow.
    -   Migrate NLU vocabulary sources automatically into either Dynamic Choice or Static Choice nodes, depending on the vocabulary sources setup in NLU.
-   **[Max wait time queue allows LLM topic selection](https://www.servicenow.com/docs/access?context=awa-create-queue-triggers&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Select LLM topics to be chosen after the max wait time is met during a Now Assist in Virtual Agent conversation. ServiceNow® Advanced Work Assignment queue triggers support LLM topics whenever the **Trigger Type** field's value is **Max Wait** and you’re prompted to select a Virtual Agent topic.

-   **[Catalogs for Virtual Agent](https://www.servicenow.com/docs/access?context=va-catalogs&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Search for and order services or products from catalog macroponents in Virtual Agent chat by using plain language. Customize the appearance of your catalogs to match your business’ branding.

-   **[Integrating Now Assist in Virtual Agent with Microsoft Copilot](https://www.servicenow.com/docs/access?context=ms-copilot-na-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Use your Self-configured bot to connect with Microsoft Copilot. The process of integrating the Self-configured bot with Microsoft Copilot is similar to that of integrating the Self-configured bot with Microsoft Teams.

    You can @-mention the bot name to initiate a chat within Copilot and Copilot provides you the response based on your utterance.

    Microsoft Copilot, when integrated with Now Assist in Virtual Agent, understands the ServiceNow context and routes users to Now Assist to conduct ServiceNow -related questions and tasks within Microsoft Teams.

    Use your Now Virtual Agent bot to connect with Microsoft Copilot by @-mentioning the bot name.

    Support for using declarative agents with Self-configured bots and transferring to live agents is available.

    Support for the default Now Virtual Agent bot plugin is available on the Microsoft Teams Store.

-   **[Integrating Virtual Agent with enterprise messaging apps](https://www.servicenow.com/docs/access?context=integ-va-enterprise-apps&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Now LLM Service support for channels enables LLM-based conversations with Now Assist in Conversational Integration with Microsoft Teams and Conversational Integration with Slack.

    The Now LLM Service support also provides new ServiceNow AI Search experience in channels with the following features:

    -   Legal disclaimers
    -   Pagination
    -   Search
    -   Generative AI Q&amp;A card
-   **[Configure rate limiting for providers](https://www.servicenow.com/docs/access?context=configure-rate-limit&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Configure rate limiting at the provider level to control the request flow for requests made within a stipulated time.


-   **[Primary and secondary assistants are honored in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=llm-assistants&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    View which conversational assets are applicable to primary or secondary assistants.

-   **Language detection for LLM conversations**

    For Now Assist in Virtual Agent users, use language detection for your LLM conversations to improve your user's experience.

-   **[Synthesized response](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    For Now Assist in Virtual Agent users, a synthesized response can appear. A synthesized response includes a brief summary of the requested information and search results along with Genius Results. Mid-topic switching can occur during a conversation with synthesized response. Users can continue with their original request or switch the conversation's focus.

-   **[New system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The following system property was added to increase flexibility of the search results and response:

    -   **sn\_nowassist\_va.synthesized\_autostart\_items**: When synthesized response only returns a singular action, configure whether to directly launch into that action. By default, whenever synthesized response returns a single Virtual Agent topic, that action is auto-launched. The following actions can be configured to auto-launch:
        -   Synthesized response returns a single conversational catalog item.
        -   Synthesized response returns a single Virtual Agent topic, along with Knowledge Base information.
        -   Synthesized response returns a single conversational catalog item, along with Knowledge Base information.

## UI changes

-   **[UI chat updates](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**
    -   The `New messages below` button in Virtual Agent was replaced with a simplified down-arrow indicator.
    -   The `New messages above` button was deprecated because Virtual Agent now auto-scrolls to the top of the oldest new message.
    -   Input text bar was updated to a more modern look and feel.
    -   The start a new conversation icon was updated.
-   **Virtual Agent Designer Topic testing window: [Testing LLM topics](https://www.servicenow.com/docs/access?context=test-llm-topics&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Various UI updates to field descriptions for controls.

    -   Modify conditions and scripts for additional instructions when testing LLM topics.
    -   Messages with potentially inappropriate content are now flagged in the **Modify Instructions** \(formerly **Prompt Discovery**\) tab when testing LLM Virtual Agent topics.
-   **[NLU to LLM topic migration workflow](https://www.servicenow.com/docs/access?context=llm-topic-migration&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Changed the Review topic blocks step label to Review connections and added the new Review descriptions step prior to the Publish step in the NLU to LLM workflow.


-   **[Virtual Agent Designer home page](https://www.servicenow.com/docs/access?context=vad-topics-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    For Now Assist in Virtual Agent users, a new list-based Virtual Agent Designer home page appears for users who have activated Now Assist in Virtual Agent and the Agent assist Topics skill. The card-based UI is still available for those who use only NLU/keyword or Virtual Agent Lite.

-   **[Virtual Agent Designer user input controls](https://www.servicenow.com/docs/access?context=va-user-inputs&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    For Now Assist in Virtual Agent users, updates to LLM user inputs include:

    -   Use the Validation toggle in the Advanced section of User Inputs to confirm user input values by scripts.
    -   Use the Allow slot filling toggle on User Inputs to switch between static \(single field\) and dynamic \(define with scripts or data pill picker\) detail description modes.
    -   Get a message that a mandatory field cannot be skipped when you attempt to skip a user input with conditions not set to be skippable.
-   **[Small talk for LLM conversations](https://www.servicenow.com/docs/access?context=create-small-talk&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    For Now Assist in Virtual Agent users, use small talk in LLM conversations for greetings and farewells along with gratitude and complaint statements. A Semantic Filtering Framework \(SFF\) detects small talk and generates an appropriate response.

-   **[Primary and secondary assistants within topic migration](https://www.servicenow.com/docs/access?context=migrate-nlu-llm&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    View whether assistants are primary or secondary assistants in the Settings step of topic migration.

-   **[AI generated topic description message within topic migration](https://www.servicenow.com/docs/access?context=migrate-nlu-llm&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    For Now Assist in Virtual Agent users, a `Topic description generated by Now Assist` message now appears near the **Topic Description** field during the topic migration's Review descriptions step.


## Deprecations

-   Starting with the Xanadu release, the Conversational Analytics dashboard is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Virtual Agent is a ServiceNow AI Platform feature that is available with activation of the Glide Virtual Agent plugin \(com.glide.cs.chatbot\), which requires a separate subscription. For details, see [Activate Virtual Agent](https://www.servicenow.com/docs/access?context=activate-virtual-agent&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

**Note:** The Glide Virtual Agent plugin initially installs the Topic Recommendations and Conversational Analytics apps. Subsequent updates to these apps must be installed from the ServiceNow Store.

ServiceNow® Virtual Agent Lite is a subset of the Virtual Agent platform that is available to ServiceNow® IT Service Management \(ITSM\) customers. It doesn't require activation and works with ITSM Virtual Agent Lite conversations, which are also available to ITSM customers.

## Browser requirements

Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Localization information

The ServiceNow® Localization Framework is integrated in Virtual Agent.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Conversational Interfaces Console](https://www.servicenow.com/docs/access?context=ci-console&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    The ServiceNow® Conversational Interfaces Console enables you to install, manage, and monitor your virtual and live agents to support your users through chat.

-   **[Prebuilt Virtual Agent topics, topic blocks, and ServiceNow NLU models](https://www.servicenow.com/docs/access?context=prebuilt-topics-ITSM&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    The following ServiceNow business applications provide prebuilt Virtual Agent conversation topics, NLU models, and, in some cases, topic blocks as reusable components:

    -   ServiceNow® Customer Service Management
    -   ServiceNow® Field Service Management
    -   ServiceNow® HR Service Delivery
    -   ServiceNow® Instance Security Center
    -   ServiceNow® IT Service Management
    -   ServiceNow® Project Portfolio Management
    -   ServiceNow® Universal Request
-   **[Natural Language Understanding](https://www.servicenow.com/docs/access?context=nlu-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Virtual Agent integrates with the Natural Language Understanding \(NLU\) application, which provides the NLU Workbench for creating NLU models. Virtual Agent uses these models to recognize and process user utterances, intents, and entities in bot conversations.


**Parent Topic:**[Conversational Interfaces release notes](../conversational-interfaces/conversational-interfaces-rn-landing.md)

