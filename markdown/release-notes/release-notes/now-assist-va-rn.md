---
title: Now Assist in Virtual Agent release notes
description: The ServiceNow Now Assist in Virtual Agent application uses generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses large language models \(LLMs\) to create a natural-language conversational experience that can improve the success of your self-service workflows. Now Assist in Virtual Agent was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 29
---

# Now Assist in Virtual Agent release notes

The ServiceNow® Now Assist in Virtual Agent application uses generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses large language models \(LLMs\) to create a natural-language conversational experience that can improve the success of your self-service workflows. Now Assist in Virtual Agent was enhanced and updated in the Zurich release.

## Now Assist in Virtual Agent highlights for the Zurich release

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Use the Now Assist in Virtual Agent clarification feature to get direct answers to ambiguous requests. If your question can apply to multiple topics, the assistant asks a follow-up question to narrow down your intent before responding.
-   Opt into premium chat for your Now Assist panel - Platform assistant. Your instance must first meet certain prerequisites. Premium chat is an AI chat experience built into your ServiceNow environment that lets you ask questions, get answers from your organization's knowledge, and take action on records — all in one place. It supports file uploads, web search, and multi-step agentic tasks, so you can handle more complex requests without leaving the panel.
-   Brand your Now Assist panel – Platform assistant, if you have premium chat set up.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Start a Now Assist in Virtual Agent conversation from anywhere in the Employee Hub.
-   Provide response feedback to Now Assist in Virtual Agent responses.
-   Use natural-language questions and receive concise, synthesized answers.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.
-   Japanese language support for voice assistants enables Japanese-speaking users to experience natural, culturally appropriate interactions with AI voice agents.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   View a people citation's org chart in the interactive view. The interactive view opens to the right of the chat conversation area.
-   Notice several UI improvements to enhanced chat and enhanced chat's full-page experience, including an updated input bar, gradient borders, copy message icon for received messages, and more.
-   Enable voice input to allow users to use a microphone to type the input. Voice input is only available for Now Assist panel Platform assistant.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Use agentic conversations and view agentic conversational processing flow steps.
-   View extended entities and records in standard and enhanced chat conversations if they’re associated with the Knowledge Graph Natural Language Query \(NLQ\) schema.
-   View suggested search queries previously performed in the portal's search bar within enhanced chat conversations.
-   Work with the simplified subheader of enhanced chat.
-   Delete closed enhanced chat conversations.
-   Expand the fallback options.
-   Enter into web search mode manually via the input bar.

See [Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for more information.

## New in the Zurich release

-   **[Clarifying questions for unclear requests](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Get precise, relevant answers from Now Assist in Virtual Agent premium chat even when your request is unclear, as the assistant asks you a targeted clarifying question before responding instead of returning an overwhelming list of results. When the assistant is confident it understands your request, it responds immediately without interrupting the conversation.

-   **[Upload documents](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Upload documents directly into a Now Assist in Virtual Agent conversation during topic, skill, catalog, or agent execution, and let the assistant extract information from them to automatically fill in required fields, answer questions, and keep the conversation moving. Uploaded document context is retained for the duration of the session and cleared when the session ends to protect your data.

-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    For new and upgrading customers, Now Assist panel - Platform assistant comes with the option to opt into premium chat if your instance meets certain criteria. For more information, see [Premium chat](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and .

-   **[Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    If you're a new or upgrading customer and you have opted into the premium chat experience, legacy messages \(formerly chat messages\) and legacy fallbacks \(formerly chat fallbacks\) settings aren't automatically migrated. You must review, configure, and customize them in premium messages and premium fallbacks.

    **Note:** ServiceNow performs a set of readiness checks to confirm that your instance is eligible for premium chat. If your instance doesn’t meet the requirements, you can continue using your existing standard or enhanced chat experience. After an upgrade, there may be a delay before premium chat is available to choose from.

-   **[Brand an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Brand your Now Assist panel – Platform assistant's chat header and chat logo, if you have premium chat set up.

-   **[Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Now Assist panel – Platform assistant has premium messages and premium fallback capabilities.

    **Note:** For premium fallbacks, web search fallback is dependent on your web search mode setting in [Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US). If web search mode is turned off, web search fallback is unavailable \(grayed out\). If web search mode is turned on, web search fallback is available where you can turn it on or off.

    Feedback surveys are supported in both standard chat and enhanced chat experiences. When enhanced chat is enabled, the survey is automatically triggered when the user indicates that they are finished chatting, based on the assistant’s survey configuration.

-   **[Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Edit an assistant to turn response feedback on or off. For more information, see [Manage response feedback](https://www.servicenow.com/docs/access?context=manage-sentiment-survey&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Turn premium chat on or off for Now Assist panel – Platform assistant using the **sn\_nowassist\_va.enable\_nap\_aix\_experience** system property. The default value is set to `false`. When the system property is set to `false`, you can switch back to your previous state \(standard chat or enhanced chat\) from the Assistant Designer chat experience modal. When the system property is set to `true`, you won't have the option to make edits to the chat experience. Premium chat is only available if your instance meets all requirements.


-   **[Start NAVA conversations from anywhere](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Start a Now Assist in Virtual Agent premium chat from any page in the Employee Hub with a single click, without interrupting existing workflows. You can upload files, toggle web search on or off, and receive a personalized greeting with promoted topics when opening a new conversation.

-   **[Response feedback](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Provide more detailed feedback on Now Assist in Virtual Agent responses by selecting thumbs up or thumbs down, then choosing from configurable checkbox options or adding your own comments to explain exactly what was helpful or what fell short. Your feedback is captured and made available through analytics dashboards, helping admins continuously improve the quality of responses you receive.

-   **[Use natural-language questions](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Enable users to ask natural-language questions and receive concise, synthesized answers while maintaining transparency, trust, and efficient task completion.

-   **[New building block framework](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Provide a consistent, reusable building block framework for the NextWave web experience using primitives and widgets.

-   **[New Include Web results button](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Enable a web search experience that includes a "Include Web results" button in the input box that includes internal and external web results.

-   **[Test voice agents](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Test voice agents directly in Assistant Designer with live transcription, tool execution tracking, and conversation logs.

-   **[Dutch and Thai language support](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Dutch and Thai language support for voice assistants enables users to experience natural pronunciation and culturally appropriate interactions with AI voice agents.


-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library, and Analytics.

    [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Access the **Assistants** tab within [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) by navigating to **All** &gt; **Assistant Designer**. The **Assistants** tab is only available for customers who have the Now Assist license. NLU-only customers don't have access to [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
    [View assistants](https://www.servicenow.com/docs/access?context=view-assistants&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   View chat and voice assistants within the **Assistants** tab of [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
        -   The card view is the default view for the assistants.
        -   An inactive \(gray\) or active \(green\) label is shown for each assistant.
        -   Activate, deactivate, test, edit, or delete an assistant.
        -   A display experience label is shown on each chat assistant card.
        -   A domain label is shown on assistant cards if an assistant is created outside of the global domain. If assistants are only created within the global domain, the label isn’t shown.
        -   The ability to view or edit an assistant depends on the domain that the admin has access to.
        -   The name and date are shown for when the assistant was last updated.
        -   Voice assistants show a voice icon and label on the card. Voice assistants can't be tested within Assistant Designer.
        -   The map view shows the assistant hierarchy where you can open, turn on or off, or delete an assistant.
    -   View the side panel for quick access to **Pick up where you left off**, **Recent activity**, and **Resources**.
    [Create a voice assistant](https://www.servicenow.com/docs/access?context=configure-voice-assistants&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Start creating an AI voice assistant by providing a name and description. Tag to a business unit to analyze your voice assistant.
    -   Power your voice assistant with agentic experience by adding AI agents.
    -   Personalize your voice assistant by choosing a language, adding a welcome message, and an AI voice persona.

        **Note:** The supported languages are:

        -   English
        -   German
        -   Spanish
    -   Secure the voice interactions by setting up caller authentication methods and safeguards.
    [Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Add basic details such as a name and description for your chat assistant, and set your assistant as a primary assistant. The Basic details page within the UI has replaced the Overview page.
    -   Now Assist panel – Platform \(default\) assistant can be set as a primary assistant and linked to secondary assistants. Now Assist panel – Developer assistant doesn't have this option.
    -   The name and description of the Now Assist panel assistants can't be changed.
    [Use agentic support for a chat assistant](https://www.servicenow.com/docs/access?context=use-agentic-support&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Let the assistant use AI agent skills and agentic orchestration. Admins can choose between agentic or standard \(Q&amp;A\) modes depending on business needs and user experience goals. Turn on or off the **Prioritize AI agents during skills discovery** feature.
    [Assign search sources to a chat assistant](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Restore search sources back to the default \(Now Assist Multi-Turn Catalog Ordering and Now Assist Q&amp;A\).
    -   Now Assist panel - Platform \(default\) assistant now has the option to copy an existing search configuration.
    -   Dynamic global search configuration has been added to the list of search application configurations.
    -   Create or configure additional search sources by selecting the **External Content Connectors** link. This replaces a card view.
    -   Manage knowledge articles by selecting the **Knowledge Center** link.
    -   In edit mode, search sources are found within the Information Sources sub-tab.
    [Add a Knowledge Graph schema to a chat assistant](https://www.servicenow.com/docs/access?context=add-kg-schema-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Adding a Knowledge Graph schema has moved from the Information sources page to its own page.
    -   Add a Knowledge Graph schema is now available for the Now Assist panel - Platform \(default\) assistant. For the NLQ schema, if Global Graph or Global Graph Mini is selected, you have the option to select tags for specific workspaces that are active on the instance.
    -   Define the mapping relationship between individual workspaces on the instance and predefined Knowledge Graph tags when Global Schema is selected for NLQ.
    -   In edit mode, Knowledge Graph is found within the Information Sources sub-tab.
    [Add assets to a chat assistant](https://www.servicenow.com/docs/access?context=add-assets&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   By default, all Now Assist skills \(Now Assist Q&amp;A, Now Assist multi-turn catalog ordering, Now Assist topics, subflows and actions, custom skills, and AI agents\) are turned on. Therefore, the Now Assist skills page has been removed.
    -   Map an asset to an assistant. Assets are the building blocks of each assistant, providing them with instructions and functionality for helping users. Assets include topics, subflows and actions, custom skills, and AI agents. For Now Assist panel - Developer assistant, only topics \(asset type\) is available.
    -   In edit mode, assets are found within the Information Sources sub-tab.
    [Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Leverage Now Assist capabilities in Google chat.
    -   Use **Prominent action button override** to allow a different chat assistant other than the default assistant to be launched on a mobile app.
    -   In edit mode, display experiences are found within the Settings sub-tab.
    [Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   The **Add ServiceNow Platform** drop-down menu has replaced the **Add agent experience** drop-down menu. A Now Assist panel assistant can't be added to other display experiences.
    -   In edit mode, display experiences are found within the Settings sub-tab.
    [Brand an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Minor enhancements to the look-and-feel of the standard chat preview pane.
    -   In edit mode, branding is found within the Settings sub-tab.
    [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   A standard chat preview pane is shown for the default greeting topic \(Now Assist – Greeting\) and the default closing topic \(Now Assist – Closing\). Selecting custom topics won’t show a preview pane.
    -   Fallbacks have a standard chat preview pane and each fallback is shown if toggled on.
    -   For the Now Assist panel - Platform \(default\) assistant, web search, record producer, and custom fallback are available options. End this chat and survey are available for the standard chat experience.
    -   In edit mode, chat experience is found within the Settings sub-tab.
    [Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Web search, response streaming, document uploads, and closed chat were moved from the Manage chat experience page to its own page. By default all chat features except web search are turned on.
    -   Response streaming can be turned on at the assistant level regardless of whether Dynamic Translation is turned on or off. However, response streaming doesn't work when Dynamic Translation is being used.
    -   In addition to web search, response streaming, document uploads, and closed chat, Now Assist panel Platform assistant has voice input. Voice input allows users to use a microphone to enter the input.
    -   In edit mode, additional chat features are found within the Settings sub-tab.
    [Review chat assistant settings](https://www.servicenow.com/docs/access?context=review-assistant-settings&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   New sections that have been added include: Agentic support, Knowledge Graphs, Assets, and Chat features.
    -   Testing an assistant has been removed from the Review page.
    [Test a chat assistant](https://www.servicenow.com/docs/access?context=test-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Test a chat assistant from **Assistant Designer** &gt; **Assistants** tab or from within each page while in edit mode.
    [Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Edit a chat assistant from **Assistant Designer** &gt; **Assistants** tab. You will be directed through an edit flow with a slightly different UI from the create flow.
    [Analyzing assistants](https://www.servicenow.com/docs/access?context=ai-engagement-analytics&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Monitor, evaluate, and optimize the performance of your AI-powered assistants within the **Analytics** tab of [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
-   **[Copy received messages](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Use the copy message icon in the feedback panel to copy received Virtual Agent responses.

-   **[New system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**
    -   Set the **com.glide.cs.nass.synthesized\_response.disabled\_popover.hide** to `true` to hide the popover for disabled catalog items for Now Assist in Virtual Agent and Now Assist panel's enhanced chat.
    -   Set the **sn\_ais\_assist.enable\_pi\_in\_nba** property to `true` to allow conversational history-based suggested actions and fill multiple suggested action slot options.
    -   View the **sn\_nowassist\_va.enable\_nass\_show\_all\_options** property to decide whether to allow the **View all options** link in an enhanced chat conversation's greeting topic.
    -   The **com.glide.interactive\_view.enabled** property opens an interactive side panel view next to the chat window. The default value is `true` to activate AI Engagement Experience on your instance.
-   **[View org chart in the interactive view](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Select **View org chart** from the people citation's popover in Now Assist panel's enhanced chat or Now Assist in Virtual Agent enhanced chat/enhanced chat's full-page experience. The person's organizational chart appears to the right of the chat conversation in an area known as the interactive view. You can switch between multiple organizational charts via a drop-down in the interactive view if you open multiple people citations' org charts in the same conversation.


-   **[Select continue or move to next task button](https://www.servicenow.com/docs/access?context=nava-standard-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    The **Continue to next task** button appears in the new **Ready to move on to your next task** card whenever multiple questions are found in a single standard chat user's message. The **Move on to the next task** citation appears at the end of an enhanced chat's synthesized response whenever multiple questions or requests are found along with an action in the user's single message. Whenever either **Continue to next task** \(standard chat\) or **Move on to the next task** \(enhanced chat\) is selected, the second question or request is reviewed and a synthesized response is sent back regarding the user's second question or request.

-   **[Multiple questions in a single user message are answered consecutively](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Virtual Agent can answer multiple questions that were submitted in a single message query. Now Assist panel or Now Assist in Virtual Agent answers the multiple questions consecutively in a response.

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Use **sn\_aia.use\_agents\_in\_planner** to configure AI agent discovery behavior. The default value is `true`, preferring AI agents over assets including catalogs, topics, Q&amp;A knowledge base articles, workflows, and sub-workflows. When set to `false`, there’s no preference for AI agents. AI agents and assets are treated the same.

-   **[New defaults for Now LLM Service](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Now Assist in Virtual Agent and Now Assist panel will use an upgraded Now LLM Service as the default. For more information, see the [Now LLM Service Upgrade FAQ: Everything You Need to Know About the v2.0 Model Transition \[KB2556891\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2556891) article in the Now Support Knowledge Base.


-   **[Configure additional user interface and experience options for enhanced chat](https://www.servicenow.com/docs/access?context=ac-configure-chat-branding&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Customize and configure the Search Toggle Button Label for enhanced chat's full-page experience. Additionally, you can configure the Enable Unread Conversation Count Display and Left Panel Header Label for enhanced chat and enhanced chat's full-page experience.

-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[View agentic conversations processing steps](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    View agentic conversational processing steps and stop the flow, if needed.

-   **[View extended entities and records](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    View extended entities and records in standard and enhanced chat conversations that come from the additional custom tables associated with the Knowledge Graph Natural Language Query \(NLQ\) schema such as:

    -   Assets
    -   Incidents
    -   Recently viewed knowledge base articles
    -   Requests
    -   Tasks
-   **[View suggested queries in the portal’s search bar and chat window](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    View the most frequently asked queries in the portal’s search bar and enhanced chat’s Virtual Agent. Any search query entered into the portal’s search bar or Virtual Agent is incorporated into the greeting topic for future conversations as a suggested query. Suggested queries are only included in the Virtual Agent greeting topic whenever no promoted assets are designated.

-   **[Work with suggested queries](https://www.servicenow.com/docs/access?context=nava-sys-props&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Two system properties were added to enable the suggested queries feature: **sn\_nowassist\_va.enable\_suggested\_queries** and **sn\_nowassist\_va.max\_suggested\_queries**.

-   **[Configure AI search answers OneExtend capability for web search](https://www.servicenow.com/docs/access?context=configure-ai-search-answers-capability-for-web-search&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Configure the AI Search answers capability via `sys_one_extend_capability.list` to establish the web search AI provider and work with API keys, if needed.

-   **[Expanding AI provider support for web search](https://www.servicenow.com/docs/access?context=configure-ai-search-answers-capability-for-web-search&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    OpenAI, Perplexity, and Google Gemini support web search.

-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Enhancements to Now Assist in Virtual Agent assistants and Now Assist panel Platform and Developer assistants. Options vary for Now Assist panel assistants.

    [Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Configure assistants by domain.
    [Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent: For mobile search widgets, enable the search bar to open into a full-page experience.
    [Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Now Assist panel Platform assistant: Enable enhanced chat for a conversational experience that includes a dynamic, movable, and re-sizable chat window, plus access to multiple active conversations.
    -   Now Assist panel Developer assistant: Not applicable.
    [Assign search sources to a chat assistant](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Add internal and external search sources, such as catalog items and Microsoft SharePoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural Language Query schema to enable users to perform a data query during a conversation.
    -   Now Assist panel Platform assistant:
        -   Add internal and external search sources, such as catalog items and Microsoft SharePoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural Language Query schema to enable users to perform a data query during a conversation.
    -   Now Assist panel Developer assistant: Not applicable.
    [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Select a custom greeting topic, closing topic, error topic, and survey for your assistant.
        -   Select one or more fallback options: live agent, web search, record producer, end this chat, and custom fallback.
        -   Enable the web search fallback option and web search mode to enable users to search the web from within a chat window.
    -   Now Assist panel Platform assistant:
        -   Select a custom greeting topic or error topic for your assistant.
        -   Fallback options don't apply to Now Assist panel Platform assistant.
        -   Enable web search mode to enable users to search the web from within a chat window.
    -   Now Assist panel Developer assistant: Not applicable.
-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the enhanced Now Assist panel for a more intuitive and personalized experience. The updated Now Assist panel is re-sizable and can be moved anywhere on the ServiceNow AI platform.


## UI changes

-   **[UI Virtual Agent Designer updates](https://www.servicenow.com/docs/access?context=vad-topics-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**
    -   Use a new option in the Actions on row icon to remove an LLM assistant from a given asset.
    -   View a tooltip if you try to promote more than six topics for a given LLM assistant.
    -   View a list of available asset types and their descriptions when you select **Create asset** in the Asset library tab.
-   **[UI chat assistant updates](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**
    -   Configuring a chat or voice assistant is done in **All** &gt; **Assistant Designer** &gt; **Assistants** tab. **All** &gt; **Conversational Interfaces** &gt; **Assistants** contains a **Manage assistants** button that directs you to Assistant Designer.
    -   Chat and voice assistants are shown in both card and map views.
    -   Pages within the chat assistant setup have been removed, added, or moved to a different spot within the create or edit flow.
        -   The Overview page has been replaced by the Basic details page.
        -   Assign Now Assist skills page has been removed. Admins no longer need to turn on/off Now Assist skill types at the assistant level in Now Assist Admin console and no longer need to assign Now Assist skill types at the assistant level.
        -   When adding search sources, an **External Content Connectors** link directs you to create or configure external sources. \(This replaces the External Content Connectors card.\) The following sections have been removed from the search sources page: Now Assist topics, Custom skills, AI agents, and Conversational subflows and actions. They are now within the Assets page.
        -   Knowledge Graph was moved from the Information sources page to its own page.
        -   Assets such as topics, subflows and actions, custom skills, and AI agents are added on the Assets page. In the display experience for Now Assist panel assistants, a **ServiceNow platforms** header is shown.
        -   Minor enhancements to the standard chat preview pane when branding an assistant.
        -   Promoted assets tab within the Chat experience page has been moved to the **Information sources \(sub-tab\)** &gt; **Asset visibility** &gt; **Promoted** while in edit mode.
        -   Web search mode, response streaming, document uploads, and closed chats have been moved to its own Chat features page.
        -   Testing a chat assistant is no longer part of the Review page. Access it from the **Assistant Designer** &gt; **Assistants** tab, or on each page while in edit mode.
        -   Editing a chat assistant is done from the **Assistant Designer** &gt; **Assistants** tab.
-   **[UI enhanced chat updates](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**
    -   Dynamic processing messages for agentic conversations are now consolidated under one View AI Steps header rather than under several View AI Steps headers.
    -   The **View all options** link shows below the suggested or promoted topics cards on the greeting topic in Now Assist in Virtual Agent and Now Assist panel's enhanced chat. At least one suggested or promoted asset has to be enabled for this link to show.
    -   The auto-complete suggestion type in the Ask Now Assist header appears at the top of the portal search bar's drop-down list. The results in the Ask Now Assist header can now show more targeted search results from AI Search rather than the GlideRecord. The entered search term can appear highlighted in bold after you have configured AI Search as the source for Ask Now Assist suggestions. For more information about this configuration, see [Configure AI Search as the source for Ask Now Assist suggestions](https://www.servicenow.com/docs/access?context=configure-ai-search-source-ask-now-assist-suggestions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
    -   The static and dynamic choice nodes now appear differently in standard and enhanced chat depending on the number of choices for single-select options. For example:
        -   2-5 choices appear as pills
        -   6 or more choices appear as a choice list with a scroll bar
    -   The input bar for enhanced chat has moved all icons below any inputted text. Uploaded documents appear above any inputted text.
    -   The float, pinned, and 90% screen views of enhanced chat now have a gradient border around them.
    -   The enhanced chat full-page experience was updated so that the Now Assist and Search button tabs that were originally center-aligned buttons are now left-aligned tabs that no longer look like buttons.

-   **[Agentic conversation processing messages for Now Assist panel and Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Before receiving a response, you receive acknowledgment messages from the Virtual Agent and on-screen processing messages to let you know where the agent is at in the agentic processing flow. The on-screen processing messages appear in present tense until the processing flow is complete. After the processing flow is complete, then the on-screen messages change to past tense and a View AI Steps section header appears above the processed messages. You can expand the collapsed View AI Steps section header to view the processed messages.


-   **[UI chat updates](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**
    -   The enhanced chat navigation area was updated. The New Chat, Chats, Support, and Settings icons were reworked into a simplified subheader. Additionally, each chat title now appears in the simplified subheader.
    -   The enhanced chat's subheader reflects conversational modes in a banner whenever you enter into a specific mode, such as web search, live agent, or document upload.
    -   In the enhanced chat's **Chats** &gt; **Closed chats** section, hover over a chat to view the delete option and complete the delete confirmation prompts.
    -   Minor animations occur in the following five enhanced chat transitions:
        -   Hovering over the chat icon.
        -   Minimizing and opening the chat icon.
        -   Transitioning from a floating chat window to a pinned chat window and vice versa.
        -   Transitioning from a floating chat window to a 90% modal and vice versa.
        -   Transitioning from a pinned chat window to a 90% modal and vice versa.

            **Note:** Transition animation doesn't apply to custom icons.

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[UI admin guided setup updates](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**



    -   The **Manage search profile** button replaces the search profile text link.
    -   The Add external search sources drop-down list has been replaced with the Add search sources drop-down list to include internal and external search sources.
    -   The simple and advanced views within the Chat experience page are consolidated into a single view.
    -   The **Copy existing configuration** button is featured more prominently, and it's shown with information about its use.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Conversational Platform Now Assist skills are active by default](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The following Platform Now Assist skills are active by default and no longer visible in Now Assist Admin console:

    -   Now Assist Multi-Turn Catalog Ordering
    -   Now Assist Q&amp;A Genius Results
    -   Now Assist Topics
    -   Subflows and actions
    -   Custom skills
    -   AI agents

-   **[Additional fallback options](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    There are up to five fallback options that can be presented to end users:

    -   **Search the web**: Triggers web search mode and uses the internet to search for the results.

        **Note:** Only the last query entered into the conversation is considered when entering web search mode via the fallback option.

    -   **Request a live chat**: Triggers live agent mode and routes you to a human support representative.
    -   **Create a generic ticket**: Creates a record.
    -   **End this chat**: Ends the chat.

        **Note:** This option is only available to standard chat conversations.

    -   **Custom fallback option**: Presents a fallback Virtual Agent topic.
-   **[Web search mode enhancements](https://www.servicenow.com/docs/access?context=web-search-requestor&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Manually enter into web search mode via the input bar for standard and enhanced chat conversations. Web search mode includes in-line citations and the associated sources. A web search mode banner appears in enhanced chat conversations that end users can use to end the mode.

-   **[Profanity recognition response](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    If Now Assist Guardian is enabled and the end user's request contains profane content, the Virtual Agent responds with a message prompt to re-enter an appropriate request without profanity or offensive content.


## Deprecations

-   In Patch 4, **sn\_aia.use\_agents\_in\_planner** system property has been removed. The system property was used for configuring AI agent discovery behavior.
-   In Patch 4, Now Assist skills page in the assistant admin guided setup has been removed due to the skills being turned on by default.
-   In Patch 1, Bing support for the searching and scraping search result type is no longer supported when adding a web search tool in Now Assist Skill Kit.

## Activation information

**Note:** When you upgrade to Zurich Patch 2 or later, agentic AI is the primary orchestration in Virtual Agent. For more information about agentic AI, see [Agentic conversations in Virtual Agent](https://www.servicenow.com/docs/access?context=agentic-conversations-vad&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following products are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&version=zurich&pubname=zurich-application-development&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
-   [Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)
-   [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)
-   [Now Assist for Employee Experience](https://www.servicenow.com/docs/access?context=now-assisit-employee-exp&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)
-   [Now Assist for Operational Sustainability Management](https://www.servicenow.com/docs/access?context=now-assist-for-esg&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for Operational Technology Manager \(OTM\)](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)
-   [Now Assist for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=now-assist-for-operational-technology-service-management&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)
-   [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US)
-   [Now Assist for Public Sector Digital Services \(PSDS\)](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)
-   [Now Assist for Sales Force Automation \(SFA\)](https://www.servicenow.com/docs/access?context=now-assist-for-sales-and-order-management-som&version=zurich&pubname=zurich-order-management&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)
-   [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)
-   [Now Assist for Zero Copy Connector](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connector-for-erp&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)

For more information, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

## Additional requirements

[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.

## Browser requirements

Now Assist in Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Localization information

[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) is supported for non-streaming Now Assist Virtual Agent conversations. For details, see [Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US), [Using language detection and dynamic machine translation in Virtual Agent enhanced chat conversations](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US), and [Using language detection and dynamic machine translation in Virtual Agent NLU and LLM standard chat conversations](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation-standard-chat-nlu&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    ServiceNow® Now Assist uses agentic AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The Now Assist in AI Search ServiceNow® Store application combines the power of search with the Now LLM Service agentic AI model to answer questions in user searches with actionable AI-generated summaries of relevant Knowledge articles.

-   **[Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Unlock your enterprise productivity with ServiceNow® Virtual Agent. Increase deflections by empowering your employees and customers to serve themselves using a friendly messaging interface, featuring prebuilt conversations powered by artificial intelligence.


**Parent Topic:**[Conversational Interfaces release notes](conversational-interfaces-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

