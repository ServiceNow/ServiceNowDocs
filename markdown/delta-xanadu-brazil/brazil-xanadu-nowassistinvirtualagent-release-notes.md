---
title: Combined Now Assist in Virtual Agent release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Now Assist in Virtual Agent from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-nowassistinvirtualagent-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 25
breadcrumb: [Products combined by family]
---

# Combined Now Assist in Virtual Agent release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Now Assist in Virtual Agent from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist in Virtual Agent release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist in Virtual Agent to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Now Assist in Virtual Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Use enhanced chat](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&family=xanadu&ft:locale=en-US)**

Enhanced chat is a conversational support experience within a resizable and moveable window that also includes the ability to have multiple active conversations and superior search capabilities. Using enhanced chat's full-page experience further intertwines chat and search capabilities by redirecting users into a full-page chat after entering a query into a portal's search bar.

-   **[View inline citations](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&family=xanadu&ft:locale=en-US)**

View the expanded list of inline citations for standard and enhanced chat:

    -   Catalog
    -   Topic, subflows, or actions
    -   Q&amp;A Knowledge Base articles
    -   External content connections

**Note:** External content connections now include the following connection types:

        -   Microsoft SharePoint
        -   Confluence
        -   Atlassian Jira Cloud
        -   Google Drive
        -   Microsoft Teams
        -   Predefined web sources
        -   ServiceNow® documentation
        -   Slack
    -   People

**Note:** If Knowledge Graph is turned on, you can view information about a person. The people information in the Virtual Agent response typically includes their title, department, location, and email address. The people popover shows additional information.

-   **[Use suggested actions](https://www.servicenow.com/docs/access?context=suggested-actions&family=xanadu&ft:locale=en-US)**

View suggested actions that were related to your prior conversation and that you consider doing next. After completing a conversational catalog request, conversational subflow, or Virtual Agent topic, two suggested actions appear after a `Here's what you can do next` header.

-   **[Stream enhanced chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&family=xanadu&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Use language detection to automatically switch the conversational language for enhanced chat conversations](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation-enhanced-chat&family=xanadu&ft:locale=en-US)**

Automatically switch the conversational language to the user's detected language during LLM enhanced chat conversations when language detection is turned on. This automatic switch can occur when a user enters an utterance at the start of a new conversation or within the portal home page’s search field.

-   **[Recognize the Boolean user input control during dynamic translation](https://www.servicenow.com/docs/access?context=multi-language-options-va&family=xanadu&ft:locale=en-US)**

Recognize the Boolean user input control in chat conversations during dynamic translation.

-   **[Adjust Shorten responses toggle to impact Show more option in chat](https://www.servicenow.com/docs/access?context=va-text-response&family=xanadu&ft:locale=en-US)**

For bot text responses, adjust the **Shorten responses** toggle in Virtual Agent Designer to turn off the **Show more** option on the user side. When **Shorten responses** is turned off, the **Show more** option does not appear in the chat to the user and the full answer is displayed rather than a truncated response.

-   **[Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

In addition to configuring Now Assist in Virtual Agent assistants, admins can configure the default Now Assist panel assistants. Options may vary for Now Assist panel assistants.

[Create an assistant](https://www.servicenow.com/docs/access?context=create-assistant&family=xanadu&ft:locale=en-US)

    -   If multiple assistants are created, users can chat simultaneously with multiple assistants. Conversations are independent from each other.
    -   Turn on or off Now Assist panel \(agent or creator\) assistant. Contact support to configure Now Assist panel assistants.
[Assign Now Assist skills to an assistant](https://www.servicenow.com/docs/access?context=assign-na-skills-assistant&family=xanadu&ft:locale=en-US)

    -   Now Assist Topic skill must be turned on at the assistant level for document uploads to be activated when managing the chat experience. For more information, see [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&family=xanadu&ft:locale=en-US).
    -   Create and manage agentic workflows in Now Assist AI Agents Studio and assign the workflows to the assistant.
[Display your assistant on a portal or channel](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&family=xanadu&ft:locale=en-US)

    -   Display Now Assist in Virtual Agent enhanced chat, with or without the full-page experience, on your portal or mobile app. This dynamic window includes the ability to have multiple active conversations and search capabilities. To use enhanced chat, portals and mobile apps require AI Search to be enabled. For more information on the prerequisites, see [Portal prerequisites for enhanced chat](https://www.servicenow.com/docs/access?context=prerequisites-enhanced-chat&family=xanadu&ft:locale=en-US) and [Mobile app prerequisites for enhanced chat](https://www.servicenow.com/docs/access?context=mobile-prereqs-enhanced-chat&family=xanadu&ft:locale=en-US).
[Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&family=xanadu&ft:locale=en-US)

    -   Upload documents to Now Assist in Virtual Agent standard chat or enhanced chat experience. The Now Assist topics skill must be enabled in Now Assist skills. For more information on file formats, see [Upload documents in Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&family=xanadu&ft:locale=en-US).
[Review assistant settings](https://www.servicenow.com/docs/access?context=review-assistant-settings&family=xanadu&ft:locale=en-US)

    -   Document uploads appear as active if it's turned on when managing the chat experience.
-   **[Upload documents in Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&family=xanadu&ft:locale=en-US)**

Upload or drag and drop files to Now Assist in Virtual Agent \(standard chat or enhanced chat\). The assistant analyzes and understands the content of the files, and a user can ask questions about the content of the files or get a summary.

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&family=xanadu&ft:locale=en-US)**

Enable suggested actions in Now Assist in Virtual Agent so that users are offered options for what they can do after completing a prior action. Suggested actions is applicable to standard and enhanced chat, mobile, and Microsoft Teams.


-   **[Stream chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&family=xanadu&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.


-   **[Use Now Assist to call Microsoft Active Directory v2 actions](https://www.servicenow.com/docs/access?context=ms-ad-v2-spoke&family=xanadu&ft:locale=en-US)**

Install Now Assist for Conversational Spokes plugin and start utilizing the conversational ability of the Look up User spoke action. You can call this action from a conversational interface like Now Assist.

-   **[Run an action from a conversation](https://www.servicenow.com/docs/access?context=conversational-actions&family=xanadu&ft:locale=en-US)**

Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational action from Workflow Studio. View and edit conversational actions within Virtual Agent Designer.

-   **[Run a subflow from a conversation](https://www.servicenow.com/docs/access?context=conversational-subflows&family=xanadu&ft:locale=en-US)**

Run a Workflow Studio subflow from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio. View and edit conversational subflows within Virtual Agent Designer.

-   **[AI generated topic description message within topic migration](https://www.servicenow.com/docs/access?context=migrate-nlu-llm&family=xanadu&ft:locale=en-US)**

A `Topic description generated by Now Assist` message now appears near the **Topic Description** field during the topic migration's Review descriptions step.

-   **[Small talk for LLM conversations](https://www.servicenow.com/docs/access?context=create-small-talk&family=xanadu&ft:locale=en-US)**

Use small talk in LLM conversations for greetings and farewells along with gratitude and complaint statements. A Semantic Filtering Framework \(SFF\) detects small talk and generates an appropriate response.

-   **[Language detection for LLM conversations](https://www.servicenow.com/docs/access?context=multi-language-options-va&family=xanadu&ft:locale=en-US)**

Use language detection for your LLM conversations to improve your user's experience.

-   **[Virtual Agent Designer Topics home page](https://www.servicenow.com/docs/access?context=vad-topics-page&family=xanadu&ft:locale=en-US)**

A new list-based Virtual Agent Designer home page appears for users who have activated Now Assist in Virtual Agent and the Agent assist Topics skill. The card-based UI is still available for those users who use only NLU/keyword or Virtual Agent Lite.

-   **[Virtual Agent Designer user input controls](https://www.servicenow.com/docs/access?context=va-user-inputs&family=xanadu&ft:locale=en-US)**

Updates to LLM user inputs include:

    -   Use the Validation toggle in the Advanced section of User Inputs to confirm user input values by scripts.
    -   Use the Allow slot filling toggle on User Inputs to switch between static \(single field\) and dynamic \(define with scripts or data pill picker\) detail description modes.
    -   Get a message that a mandatory field cannot be skipped when you attempt to skip a user input with conditions not set to be skippable.
-   **[Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Updates to the admin guided setup include:

    -   Enhance functionality and efficiency of your Virtual Agent by linking primary assistants to secondary assistants, enabling a primary assistant to use search sources from secondary assistants.
    -   View the relationship between primary and secondary assistants within a map view.
    -   Select portals and mobile applications to display Virtual Agents.
    -   Create conversational subflows and actions by launching Workflow Studio to make conversational subflows and actions available to the assistant.
-   **[Synthesized response](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&family=xanadu&ft:locale=en-US)**

For Now Assist in Virtual Agent users, a synthesized response can appear. A synthesized response includes a brief summary of the requested information and search results along with Genius Results. Mid-topic switching can occur during a conversation with synthesized response. Users can continue with their original request or switch the conversation's focus.

-   **[New system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=xanadu&ft:locale=en-US)**

The following system property was added to increase flexibility of the search results and response:

    -   **sn\_nowassist\_va.synthesized\_autostart\_items**: When synthesized response only returns a singular action, configure whether to directly launch into that action. By default, whenever synthesized response returns a single Virtual Agent topic, that action is auto-launched. The following actions can be configured to auto-launch:
        -   Synthesized response returns a single conversational catalog item.
        -   Synthesized response returns a single Virtual Agent topic, along with Knowledge Base information.
        -   Synthesized response returns a single conversational catalog item, along with Knowledge Base information.

-   **[Delete virtual agents](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Delete a Virtual Agent from the assistants list.

-   **[Support virtual agents on a portal](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Allow public availability of an LLM-based Virtual Agent on a portal.

-   **[Display a virtual agent in a channel](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Integrate your preferred messaging channels to display your Virtual Agent.

-   **[Install proactive triggers](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Install Proactive Triggers from within the Review page.

-   **[Support notifications in virtual agents](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Support actionable and non-actionable notifications for LLM conversations in Virtual Agent.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Select continue or move to next task button](https://www.servicenow.com/docs/access?context=nava-standard-chat&family=yokohama&ft:locale=en-US)**

The **Continue to next task** button appears in the new **Ready to move on to your next task** card whenever multiple questions are found in a single standard chat user's message. The **Move on to the next task** citation appears at the end of an enhanced chat's synthesized response whenever multiple questions or requests are found along with an action in the user's single message. Whenever either **Continue to next task** \(standard chat\) or **Move on to the next task** \(enhanced chat\) is selected, the second question or request is reviewed and a synthesized response is sent back regarding the user's second question or request.

-   **[Multiple questions in a single user message are answered consecutively](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&family=yokohama&ft:locale=en-US)**

Virtual Agent can answer multiple questions that were submitted in a single message query. Now Assist panel or Now Assist in Virtual Agent answers the multiple questions consecutively in a response.

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&family=yokohama&ft:locale=en-US)**

Use **sn\_aia.use\_agents\_in\_planner** to configure AI agent discovery behavior. The default value is `true`, preferring AI agents over assets including catalogs, topics, Q&amp;A knowledge base articles, workflows, and sub-workflows. When set to `false`, there’s no preference for AI agents. AI agents and assets are treated the same.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Clarifying questions for unclear requests](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=zurich&ft:locale=en-US)**

Get precise, relevant answers from Now Assist in Virtual Agent premium chat even when your request is unclear, as the assistant asks you a targeted clarifying question before responding instead of returning an overwhelming list of results. When the assistant is confident that it understands your request, it responds immediately without interrupting the conversation.

-   **[Upload documents](https://www.servicenow.com/docs/access?context=nava-integrated-chat&family=zurich&ft:locale=en-US)**

Upload documents directly into a Now Assist in Virtual Agent conversation during topic, skill, catalog, or agent execution, and let the assistant extract information from them to automatically fill in required fields, answer questions, and keep the conversation moving. Uploaded document context is retained for the duration of the session and cleared when the session ends to protect your data.

-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=zurich&ft:locale=en-US)**

For new and upgrading customers, Now Assist panel - Platform assistant comes with the option to opt into premium chat if your instance meets certain criteria. For more information, see [Premium chat](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=zurich&ft:locale=en-US) and [Display assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&family=zurich&ft:locale=en-US).

-   **[Display assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&family=zurich&ft:locale=en-US)**

If you're a new or upgrading customer and you have opted into the premium chat experience, legacy messages \(formerly chat messages\) and legacy fallbacks \(formerly chat fallbacks\) settings aren't automatically migrated. You must review, configure, and customize them in premium messages and premium fallbacks.

**Note:** ServiceNow performs a set of readiness checks to confirm that your instance is eligible for premium chat. If your instance doesn’t meet the requirements, you can continue using your existing standard or enhanced chat experience. After an upgrade, there may be a delay before premium chat is available to choose from.

-   **[Brand and personalize an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&family=zurich&ft:locale=en-US)**

Brand your Now Assist panel – Platform assistant's chat header and chat logo, if you have premium chat set up.

-   **[Manage chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&family=zurich&ft:locale=en-US)**

Now Assist panel – Platform assistant has premium messages and premium fallback capabilities.

**Note:** For premium fallbacks, web search fallback is dependent on your web search mode setting in [Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&family=zurich&ft:locale=en-US). If web search mode is turned off, web search fallback is unavailable. If web search mode is turned on, web search fallback is available where you can turn it on or off.

Feedback surveys are supported in both standard chat and enhanced chat experiences. When enhanced chat is enabled, the survey is automatically triggered when the user indicates that they are finished chatting, based on the assistant’s survey configuration.

-   **[Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&family=zurich&ft:locale=en-US)**

Edit an assistant to turn response feedback on or off. For more information, see [Manage response feedback](https://www.servicenow.com/docs/access?context=manage-sentiment-survey&family=zurich&ft:locale=en-US).

-   **[ServiceNow Otto for Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&family=zurich&ft:locale=en-US)**

Turn premium chat on or off for the Now Assist panel – Platform assistant using the **sn\_nowassist\_va.enable\_nap\_aix\_experience** system property. The default value is set to `false`. When the system property is set to `false`, you can switch back to your previous state \(standard chat or enhanced chat\) from the Assistant Designer chat experience modal. When the system property is set to `true`, you won't have the option to make edits to the chat experience. Premium chat is only available if your instance meets all requirements.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Now Assist in Virtual Agent features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Standard chat](https://www.servicenow.com/docs/access?context=nava-standard-chat&family=xanadu&ft:locale=en-US)**

The existing Now Assist in Virtual Agent LLM conversational behavior received a terminology update and is now referred to as standard chat.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Agentic conversation processing messages for Now Assist panel and Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&family=yokohama&ft:locale=en-US)**

Before receiving a response, you receive acknowledgment messages from the Virtual Agent and on-screen processing messages to let you know where the agent is at in the agentic processing flow. The on-screen processing messages appear in present tense until the processing flow is complete. After the processing flow is complete, then the on-screen messages change to past tense and a View AI Steps section header appears above the processed messages. You can expand the collapsed View AI Steps section header to view the processed messages.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Now Assist in Virtual Agent features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Now Assist in Virtual Agent features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   In Patch 6, Bing support for the searching and scraping search result type is no longer supported when adding a web search tool in Now Assist Skill Kit.
-   In Patch 4, support for Now Assist in Conversational IVR was removed.

</td></tr><tr><td>

Zurich

</td><td>

-   In Patch 4, the **sn\_aia.use\_agents\_in\_planner** system property has been removed. The system property was used for configuring AI agent discovery behavior.
-   In Patch 4, the Now Assist skills page in the assistant admin guided setup has been removed due to the skills being turned on by default.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Now Assist in Virtual Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&family=xanadu&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&family=xanadu&ft:locale=en-US)
-   [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&family=xanadu&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&family=xanadu&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&family=xanadu&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for PSDS](https://www.servicenow.com/docs/access?context=now-assist-for-psds&family=xanadu&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&family=xanadu&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&family=xanadu&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&family=xanadu&ft:locale=en-US)

For more information, see [Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

**Note:** When you upgrade to Yokohama Patch 8 or later, agentic AI is the primary orchestration in Virtual Agent. For more information about agentic AI, see [Agentic conversations in Virtual Agent](https://www.servicenow.com/docs/access?context=agentic-conversations-vad&family=yokohama&ft:locale=en-US).

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following products are available:

    -   [ServiceNow Otto for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&family=yokohama&ft:locale=en-US)
    -   [Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&family=yokohama&ft:locale=en-US)
    -   [Now Assist for CWM](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&family=yokohama&ft:locale=en-US)
    -   [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Employee Experience](https://www.servicenow.com/docs/access?context=now-assisit-employee-exp&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&family=yokohama&ft:locale=en-US)
    -   [Now Assist](https://www.servicenow.com/docs/access?context=now-assist-for-esg&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&family=yokohama&ft:locale=en-US)
    -   [Now Assist](https://www.servicenow.com/docs/access?context=now-assist-for-irm&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for ITOM](https://www.servicenow.com/docs/access?context=now-assist-itom&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&family=yokohama&ft:locale=en-US)
    -   [Operational Technology \(OT\) Manager Foundation](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for PSDS](https://www.servicenow.com/docs/access?context=now-assist-for-psds&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Security Incident Response \(SIR\)](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Strategic Portfolio Management](https://www.servicenow.com/docs/access?context=now-assist-spm&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&family=yokohama&ft:locale=en-US)
    -   [Now Assist](https://www.servicenow.com/docs/access?context=now-assist-tprm&family=yokohama&ft:locale=en-US)
    -   [Now Assist for WSD](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&family=yokohama&ft:locale=en-US)
    -   [ServiceNow Otto for Unified Security Exposure Management](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&family=yokohama&ft:locale=en-US)
For more information, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

**Note:** When you upgrade to Zurich Patch 2 or later, agentic AI is the primary orchestration in Virtual Agent. For more information about agentic AI, see [Agentic conversations in Virtual Agent](https://www.servicenow.com/docs/access?context=agentic-conversations-vad&family=zurich&ft:locale=en-US).

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following products are available:

    -   For more information, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist in Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&family=xanadu&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Additional requirements**

[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&family=yokohama&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.


</td></tr><tr><td>

Zurich

</td><td>

-   **Additional requirements**

[ServiceNow Otto for Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&family=zurich&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist in Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Now Assist in Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Browser requirements**

Now Assist in Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Browser requirements**

Now Assist in Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](https://www.servicenow.com/docs/access?context=browser-support&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Now Assist in Virtual Agent, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist in Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&family=xanadu&ft:locale=en-US) is supported in Now Assist Virtual Agent conversations. For details, see [Enable translation for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&family=xanadu&ft:locale=en-US) and [Localization options for Virtual Agent](https://www.servicenow.com/docs/access?context=multi-language-options-va&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Localization information**

[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&family=yokohama&ft:locale=en-US) is supported for non-streaming Now Assist Virtual Agent conversations. For details, see [Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&family=yokohama&ft:locale=en-US) and [Using language detection and dynamic machine translation in Virtual Agent](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Localization information**

[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&family=zurich&ft:locale=en-US) is supported for non-streaming Now Assist Virtual Agent conversations. For details, see [Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&family=zurich&ft:locale=en-US), [Language detection and dynamic translation in enhanced chat](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation-enhanced-chat&family=zurich&ft:locale=en-US), and [Language detection and dynamic translation in standard chat](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation-standard-chat-nlu&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist in Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

[Xanadu Patch 9](https://www.servicenow.com/docs/access?context=xanadu-patch-9&family=xanadu&ft:locale=en-US)

-   Use enhanced chat to provide users with a conversational experience within a resizable and movable chat window that includes the ability to have multiple active conversations. Enhanced chat enables users to choose their way of engaging with Now Assist on their ServiceNow portals from a variety of entry points. Enhanced chat includes synthesized responses after entering a search query into a portal's search bar. If Now Assist in AI Search is turned on, enhanced chat also offers an optional full-page experience where your users can enter into a full-page chat experience after entering a search query into a portal's search bar. Enhanced chat also offers an updated, modern look and feel along with chat controls to resize and move the chat window.
-   View an expanded list of inline citations for both standard and enhanced chat. New inline citations for external content and people searches are available.
-   View and work with suggested actions after completing an action in Now Assist in Virtual Agent.
-   Stream responses for Now Assist LLM - enhanced chat conversations.
-   Upload or drag documents and images into a standard or enhanced chat.
-   Automatically switch to the user's detected language in enhanced chat conversations when language detection is turned on.
-   Enable pinning a chat window on a portal by using the **sn\_nowassist\_va.enhanced\_chat\_pin\_enabled.&lt;portal-url&gt;** system property.

 [Xanadu Patch 7](https://www.servicenow.com/docs/access?context=xanadu-patch-7&family=xanadu&ft:locale=en-US)

-   Stream responses for Now Assist LLM chat conversations.

 [Xanadu Patch 3](https://www.servicenow.com/docs/access?context=xanadu-patch-3&family=xanadu&ft:locale=en-US)

-   Run actions from a conversation.
-   Run subflows from a conversation.
-   Use an updated Virtual Agent Designer list-based home page that includes conversational subflows and actions.
-   Use language detection and engage in small talk within LLM conversations.
-   Link primary assistants with secondary assistants to use search sources from secondary assistants.
-   Use language detection and engage in small talk within LLM conversations.
-   Receive a synthesized response for Now Assist in Virtual Agent users.

 [Xanadu Patch 1](https://www.servicenow.com/docs/access?context=xanadu-patch-1&family=xanadu&ft:locale=en-US)

-   Enhancements to the Now Assist in Virtual Agent admin guided setup.

See [Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&family=xanadu&ft:locale=en-US) for more information.


</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   View a people citation's org chart in the interactive view. The interactive view opens to the right of the chat conversation area.
-   Notice several UI improvements to enhanced chat and enhanced chat's full-page experience, including an updated input bar, gradient borders, copy message icon for received messages, and more.
-   Enable voice input to allow users to use a microphone to type the input. Voice input is only available for Now Assist panel Platform assistant.

 [Yokohama Patch 6](https://www.servicenow.com/docs/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Use agentic conversations and view agentic conversational processing flow steps.
-   View extended entities and records in standard and enhanced chat conversations if they’re associated with the Knowledge Graph natural language query \(NLQ\) schema.
-   View suggested search queries previously performed in the portal's search bar within enhanced chat conversations.
-   Work with the simplified subheader of enhanced chat.
-   Delete closed enhanced chat conversations.
-   Expand the fallback options.
-   Enter into web search mode manually via the input bar.

 [Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   Use enhanced chat to provide users with a conversational experience within a resizable and movable chat window that includes the ability to have multiple active conversations. Enhanced chat enables users to choose their way of engaging with Now Assist on their ServiceNow portals from a variety of entry points. Enhanced chat includes synthesized responses after entering a search query into a portal's search bar. If Now Assist in AI Search is turned on, enhanced chat also offers an optional full-page experience where your users can enter into a full-page chat experience after entering a search query into a portal's search bar. Enhanced chat also offers an updated, modern look and feel along with chat controls to resize and move the chat window.
-   View an expanded list of inline citations for both standard and enhanced chat. New inline citations for external content and people searches are available.
-   View and work with suggested actions after completing an action in Now Assist in Virtual Agent.
-   Stream responses for Now Assist LLM - enhanced chat conversations.
-   Upload or drag documents and images into a standard or enhanced chat.
-   Automatically switch to the user's detected language in enhanced chat conversations when language detection is turned on.
-   Use the Web Search custom skill to search for an answer on the internet.

 [Yokohama Patch 1](https://www.servicenow.com/docs/access?context=yokohama-patch-1&family=yokohama&ft:locale=en-US)

-   Stream responses for Now Assist LLM chat conversations.

 See [Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 12](https://www.servicenow.com/docs/access?context=zurich-patch-12&family=zurich&ft:locale=en-US)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Virtual Agent and ServiceNow Otto panel. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 [Zurich Patch 11](https://www.servicenow.com/docs/access?context=zurich-patch-11&family=zurich&ft:locale=en-US)

-   Prompts help users ask better questions and get more accurate answers. Admins can turn prompt library on or off and further configure the default recommended prompts for users.

 [Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US)

-   Opt into premium chat for your Now Assist in Virtual Agent assistants.
-   Enable voice input for Now Assist in Virtual Agent assistants \(premium chat\), and for the Now Assist panel - Platform assistant \(standard, enhanced, or premium chat\).
-   Personalize your assistant's tone, response length, and persona.

 [Zurich Patch 9](https://www.servicenow.com/docs/access?context=zurich-patch-9&family=zurich&ft:locale=en-US)

-   Use Now Assist in Virtual Agent on your mobile device.
-   The default Employee Slate assistant comes with premium chat. Premium chat is a contextual chat experience that appears throughout the platform, adapting its behavior and interface based on where users are and what they’re doing.

 [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US)

-   Use the Now Assist in Virtual Agent clarification feature to get direct answers to ambiguous requests. If your question can apply to multiple topics, the assistant asks a follow-up question to narrow down your intent before responding.
-   Opt into premium chat for your Now Assist panel - Platform assistant. Your instance must first meet certain prerequisites. Premium chat is an AI chat experience built into your ServiceNow environment that lets you ask questions, get answers from your organization's knowledge, and take action on records — all in one place. It supports file uploads, web search, and multi-step agentic tasks, so that you can handle more complex requests without leaving the panel.
-   Brand your Now Assist panel – Platform assistant, if you have premium chat set up.

 [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Start a Now Assist in Virtual Agent conversation from anywhere in the Employee Hub.
-   Provide response feedback to Now Assist in Virtual Agent responses.
-   Use natural-language questions and receive concise, synthesized answers.

 [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Japanese language support for voice assistants enables Japanese-speaking users to experience natural, culturally appropriate interactions with AI voice agents.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   View a people citation's org chart in the interactive view. The interactive view opens next to the chat conversation area.
-   Notice several UI improvements to enhanced chat and enhanced chat's full-page experience, including an updated input bar, gradient borders, copy message icon for received messages, and more.
-   Turn on voice input to enable users to use a microphone to enter the input. Voice input is only available for Now Assist panel Platform assistant.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Use agentic conversations and view agentic conversational processing flow steps.
-   View extended entities and records in standard and enhanced chat conversations if they’re associated with the Knowledge Graph Natural Language Query \(NLQ\) schema.
-   View suggested search queries previously performed in the portal's search bar within enhanced chat conversations.
-   Work with the simplified subheader of enhanced chat.
-   Delete closed enhanced chat conversations.
-   Expand the fallback options.
-   Enter into web search mode manually via the input bar.

 See [ServiceNow Otto for Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

