---
title: Now Assist in Virtual Agent release notes
description: The ServiceNow Now Assist in Virtual Agent application uses generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses large language models \(LLMs\) to create a natural-language conversational experience that can improve the success of your self-service workflows. Now Assist in Virtual Agent was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-08"
reading_time_minutes: 33
---

# Now Assist in Virtual Agent release notes

The ServiceNow® Now Assist in Virtual Agent application uses generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses large language models \(LLMs\) to create a natural-language conversational experience that can improve the success of your self-service workflows. Now Assist in Virtual Agent was enhanced and updated in the Yokohama release.

## Now Assist in Virtual Agent highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   View a people citation's org chart in the interactive view. The interactive view opens to the right of the chat conversation area.
-   Notice several UI improvements to enhanced chat and enhanced chat's full-page experience, including an updated input bar, gradient borders, copy message icon for received messages, and more.
-   Enable voice input to allow users to use a microphone to type the input. Voice input is only available for Now Assist panel Platform assistant.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Use agentic conversations and view agentic conversational processing flow steps.
-   View extended entities and records in standard and enhanced chat conversations if they’re associated with the Knowledge Graph natural language query \(NLQ\) schema.
-   View suggested search queries previously performed in the portal's search bar within enhanced chat conversations.
-   Work with the simplified subheader of enhanced chat.
-   Delete closed enhanced chat conversations.
-   Expand the fallback options.
-   Enter into web search mode manually via the input bar.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Use enhanced chat to provide users with a conversational experience within a resizable and movable chat window that includes the ability to have multiple active conversations. Enhanced chat enables users to choose their way of engaging with Now Assist on their ServiceNow portals from a variety of entry points. Enhanced chat includes synthesized responses after entering a search query into a portal's search bar. If Now Assist in AI Search is turned on, enhanced chat also offers an optional full-page experience where your users can enter into a full-page chat experience after entering a search query into a portal's search bar. Enhanced chat also offers an updated, modern look and feel along with chat controls to resize and move the chat window.
-   View an expanded list of inline citations for both standard and enhanced chat. New inline citations for external content and people searches are available.
-   View and work with suggested actions after completing an action in Now Assist in Virtual Agent.
-   Stream responses for Now Assist LLM - enhanced chat conversations.
-   Upload or drag documents and images into a standard or enhanced chat.
-   Automatically switch to the user's detected language in enhanced chat conversations when language detection is turned on.
-   Use the Web Search custom skill to search for an answer on the internet.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   Stream responses for Now Assist LLM chat conversations.

See [Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library, and Analytics.

    [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Access the **Assistants** tab within [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) by navigating to **All** &gt; **Assistant Designer**. The **Assistants** tab is only available for customers who have the Now Assist license. NLU-only customers don't have access to [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
    [View assistants](https://www.servicenow.com/docs/access?context=view-assistants&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   View chat and voice assistants within the **Assistants** tab of [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
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
    [Create a voice assistant](https://www.servicenow.com/docs/access?context=configure-voice-assistants&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Start creating an AI voice assistant by providing a name and description. Tag to a business unit to analyze your voice assistant.
    -   Power your voice assistant with agentic experience by adding AI agents.
    -   Personalize your voice assistant by choosing a language, adding a welcome message, and an AI voice persona.

        **Note:** The supported languages are:

        -   English
        -   German
        -   Spanish
    -   Secure the voice interactions by setting up caller authentication methods and safeguards.
    [Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Add basic details such as a name and description for your chat assistant, and set your assistant as a primary assistant. The Basic details page within the UI has replaced the Overview page.
    -   Now Assist panel – Platform \(default\) assistant can be set as a primary assistant and linked to secondary assistants. Now Assist panel – Developer assistant doesn't have this option.
    -   The name and description of the Now Assist panel assistants can't be changed.
    [Use agentic support for a chat assistant](https://www.servicenow.com/docs/access?context=use-agentic-support&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Let the assistant use AI agent skills and agentic orchestration. Admins can choose between agentic or standard \(Q&amp;A\) modes depending on business needs and user experience goals. Turn on or off the **Prioritize AI agents during skills discovery** feature.
    [Assign search sources to a chat assistant](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Restore search sources back to the default \(Now Assist Multi-Turn Catalog Ordering and Now Assist Q&amp;A\).
    -   Now Assist panel - Platform \(default\) assistant now has the option to copy an existing search configuration.
    -   Dynamic global search configuration has been added to the list of search application configurations.
    -   Create or configure additional search sources by selecting the **External Content Connectors** link. This replaces a card view.
    -   Manage knowledge articles by selecting the **Knowledge Center** link.
    -   In edit mode, search sources are found within the Information Sources sub-tab.
    [Add a Knowledge Graph schema to a chat assistant](https://www.servicenow.com/docs/access?context=add-kg-schema-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Adding a Knowledge Graph schema has moved from the Information sources page to its own page.
    -   Add a Knowledge Graph schema is now available for the Now Assist panel - Platform \(default\) assistant. For the NLQ schema, if Global Graph or Global Graph Mini is selected, you have the option to select tags for specific workspaces that are active on the instance.
    -   Define the mapping relationship between individual workspaces on the instance and predefined Knowledge Graph tags when Global Schema is selected for NLQ.
    -   In edit mode, Knowledge Graph is found within the Information Sources sub-tab.
    [Add assets to a chat assistant](https://www.servicenow.com/docs/access?context=add-assets&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   By default, all Now Assist skills \(Now Assist Q&amp;A, Now Assist multi-turn catalog ordering, Now Assist topics, subflows and actions, custom skills, and AI agents\) are turned on. Therefore, the Now Assist skills page has been removed.
    -   Map an asset to an assistant. Assets are the building blocks of each assistant, providing them with instructions and functionality for helping users. Assets include topics, subflows and actions, custom skills, and AI agents. For Now Assist panel - Developer assistant, only topics \(asset type\) is available.
    -   In edit mode, assets are found within the Information Sources sub-tab.
    [Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Leverage Now Assist capabilities in Google chat.
    -   Use **Prominent action button override** to allow a different chat assistant other than the default assistant to be launched on a mobile app.
    -   In edit mode, display experiences are found within the Settings sub-tab.
    [Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   The **Add ServiceNow Platform** drop-down menu has replaced the **Add agent experience** drop-down menu. A Now Assist panel assistant can't be added to other display experiences.
    -   In edit mode, display experiences are found within the Settings sub-tab.
    [Brand an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Minor enhancements to the look-and-feel of the standard chat preview pane.
    -   In edit mode, branding is found within the Settings sub-tab.
    [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   A standard chat preview pane is shown for the default greeting topic \(Now Assist – Greeting\) and the default closing topic \(Now Assist – Closing\). Selecting custom topics won’t show a preview pane.
    -   Fallbacks have a standard chat preview pane and each fallback is shown if toggled on.
    -   For the Now Assist panel - Platform \(default\) assistant, web search, record producer, and custom fallback are available options. End this chat and survey are available for the standard chat experience.
    -   In edit mode, chat experience is found within the Settings sub-tab.
    [Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Web search, response streaming, document uploads, and closed chat were moved from the Manage chat experience page to its own page. By default all chat features except web search are turned on.
    -   Response streaming can be turned on at the assistant level regardless of whether Dynamic Translation is turned on or off. However, response streaming doesn't work when Dynamic Translation is being used.
    -   In addition to web search, response streaming, document uploads, and closed chat, Now Assist panel Platform assistant has voice input. Voice input allows users to use a microphone to enter the input.
    -   In edit mode, additional chat features are found within the Settings sub-tab.
    [Review chat assistant settings](https://www.servicenow.com/docs/access?context=review-assistant-settings&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   New sections that have been added include: Agentic support, Knowledge Graphs, Assets, and Chat features.
    -   Testing an assistant has been removed from the Review page.
    [Test a chat assistant](https://www.servicenow.com/docs/access?context=test-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Test a chat assistant from **Assistant Designer** &gt; **Assistants** tab or from within each page while in edit mode.
    [Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Edit a chat assistant from **Assistant Designer** &gt; **Assistants** tab. You will be directed through an edit flow with a slightly different UI from the create flow.
    [Analyzing assistants](https://www.servicenow.com/docs/access?context=ai-engagement-analytics&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Monitor, evaluate, and optimize the performance of your AI-powered assistants within the **Analytics** tab of [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
-   **[Copy received messages](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Use the copy message icon in the feedback panel to copy received Virtual Agent responses.

-   **[New system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   Set the **com.glide.cs.nass.synthesized\_response.disabled\_popover.hide** to `true` to hide the popover for disabled catalog items for Now Assist in Virtual Agent and Now Assist panel's enhanced chat.
    -   Set the **sn\_ais\_assist.enable\_pi\_in\_nba** property to `true` to allow conversational history-based suggested actions and fill multiple suggested action slot options.
    -   View the **sn\_nowassist\_va.enable\_nass\_show\_all\_options** property to decide whether to allow the **View all options** link in an enhanced chat conversation's greeting topic.
    -   The **com.glide.interactive\_view.enabled** property opens an interactive side panel view next to the chat window. The default value is `true` to activate AI Engagement Experience on your instance.
-   **[View org chart in the interactive view](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Select **View org chart** from the people citation's popover in Now Assist panel's enhanced chat or Now Assist in Virtual Agent enhanced chat/enhanced chat's full-page experience. The person's organizational chart appears to the right of the chat conversation in an area known as the interactive view. You can switch between multiple organizational charts via a drop-down in the interactive view if you open multiple people citations' org charts in the same conversation.


-   **[Select continue or move to next task button](https://www.servicenow.com/docs/access?context=nava-standard-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    The **Continue to next task** button appears in the new **Ready to move on to your next task** card whenever multiple questions are found in a single standard chat user's message. The **Move on to the next task** citation appears at the end of an enhanced chat's synthesized response whenever multiple questions or requests are found along with an action in the user's single message. Whenever either **Continue to next task** \(standard chat\) or **Move on to the next task** \(enhanced chat\) is selected, the second question or request is reviewed and a synthesized response is sent back regarding the user's second question or request.

-   **[Multiple questions in a single user message are answered consecutively](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Virtual Agent can answer multiple questions that were submitted in a single message query. Now Assist panel or Now Assist in Virtual Agent answers the multiple questions consecutively in a response.

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Use **sn\_aia.use\_agents\_in\_planner** to configure AI agent discovery behavior. The default value is `true`, preferring AI agents over assets including catalogs, topics, Q&amp;A knowledge base articles, workflows, and sub-workflows. When set to `false`, there’s no preference for AI agents. AI agents and assets are treated the same.


-   **[Configure additional user interface and experience options for enhanced chat](https://www.servicenow.com/docs/access?context=ac-configure-chat-branding&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Customize and configure the Search Toggle Button Label for enhanced chat's full-page experience. Additionally, you can configure the Enable Unread Conversation Count Display and Left Panel Header Label for enhanced chat and enhanced chat's full-page experience.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[View agentic conversations processing steps](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    View agentic conversational processing steps and stop the flow, if needed.

-   **[View extended entities and records](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    View extended entities and records in standard and enhanced chat conversations that come from the additional custom tables associated with the Knowledge Graph natural language query \(NLQ\) schema such as:

    -   Assets
    -   Incidents
    -   Recently viewed knowledge base articles
    -   Requests
    -   Tasks
-   **[View suggested queries in the portal’s search bar and chat window](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    View the most frequently asked queries in the portal’s search bar and enhanced chat’s Virtual Agent. Any search query entered into the portal’s search bar or Virtual Agent is incorporated into the greeting topic for future conversations as a suggested query. Suggested queries are only included in the Virtual Agent greeting topic whenever no promoted assets are designated.

-   **[Work with suggested queries](https://www.servicenow.com/docs/access?context=nava-sys-props&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Two system properties were added to enable the suggested queries feature: **sn\_nowassist\_va.enable\_suggested\_queries** and **sn\_nowassist\_va.max\_suggested\_queries**.

-   **[Configure AI search answers OneExtend capability for web search](https://www.servicenow.com/docs/access?context=configure-ai-search-answers-capability-for-web-search&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the AI Search answers capability via `sys_one_extend_capability.list` to establish the web search AI provider and work with API keys, if needed.

-   **[Expanding AI provider support for web search](https://www.servicenow.com/docs/access?context=configure-ai-search-answers-capability-for-web-search&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    OpenAI, Perplexity, and Google Gemini support web search.

-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Enhancements to Now Assist in Virtual Agent assistants and Now Assist panel Platform and Developer assistants. Options vary for Now Assist panel assistants.

    [Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Configure assistants by domain.


    -   Now Assist in Virtual Agent assistants: By default, all global skill types are turned on in Now Assist Admin console.
    -   Now Assist panel Platform assistant: By default, all global skill types, except for Catalog skill, are turned on in Now Assist Admin console.
    -   Now Assist panel Developer assistant: By default, Now Assist Topic skill is turned on in Now Assist Admin console. No other skills are available for the Now Assist panel Developer assistant.
    [Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent: For mobile search widgets, allow the search bar to open into a full-page experience.
    [Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Now Assist panel Platform assistant: Enable enhanced chat for a conversational experience that includes a dynamic, movable, and resizable chat window, plus access to multiple active conversations.
    -   Now Assist panel Developer assistant: Not applicable.
    [Assign search sources to a chat assistant](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Add internal and external search sources, such as catalog items and Microsoft Sharepoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural language query schema to allow users to perform a data query during a conversation.
    -   Now Assist panel Platform assistant:
        -   Add internal and external search sources, such as catalog items and Microsoft Sharepoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural language query schema to allow users to perform a data query during a conversation.
    -   Now Assist panel Developer assistant: Not applicable.
    [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Select a custom greeting topic, closing topic, error topic, and survey for your assistant.
        -   Select one or more fallback options: live agent, web search, record producer, end this chat, and custom fallback.
        -   Enable web search fallback option and web search mode to allow users to search the web from within a chat window.
    -   Now Assist panel Platform assistant:
        -   Select a custom greeting topic or error topic for your assistant.
        -   Fallback options don't apply to Now Assist panel Platform assistant.
        -   Enable web search mode to allow users to search the web from within a chat window.
    -   Now Assist panel Developer assistant: Not applicable.
-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the enhanced Now Assist panel for a more intuitive and personalized experience. The updated Now Assist panel is re-sizable and can be moved anywhere on the ServiceNow AI platform.


-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Enable pinning a chat window on a portal by using the **sn\_nowassist\_va.enhanced\_chat\_pin\_enabled.&lt;portal-url&gt;** system property.


-   **[Use enhanced chat](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Enhanced chat is a conversational support experience within a resizable and moveable window that also includes the ability to have multiple active conversations and superior search capabilities. Using enhanced chat's full-page experience further intertwines chat and search capabilities by redirecting users into a full-page chat after entering a query into a portal's search bar.

-   **[View inline citations](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

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

-   **[Use suggested actions](https://www.servicenow.com/docs/access?context=suggested-actions&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    View suggested actions that were related to your prior conversation and that you consider doing next. After completing a conversational catalog request, conversational subflow, or Virtual Agent topic, two suggested actions appear after a `Here's what you can do next` header.

-   **[Stream enhanced chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Use language detection to automatically switch the conversational language for enhanced chat conversations](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Automatically switch the conversational language to the user's detected language during LLM enhanced chat conversations when language detection is turned on. This automatic switch can occur when a user enters an utterance at the start of a new conversation or within the portal home page’s search field.

-   **[Recognize the Boolean user input control during dynamic translation](https://www.servicenow.com/docs/access?context=multi-language-options-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Recognize the Boolean user input control in chat conversations during dynamic translation.

-   **[Adjust Shorten responses toggle to impact Show more option in chat](https://www.servicenow.com/docs/access?context=va-text-response&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    For bot text responses, adjust the **Shorten responses** toggle in Virtual Agent Designer to turn off the **Show more** option on the user side. When **Shorten responses** is turned off, the **Show more** option does not appear in the chat to the user and the full answer is displayed rather than a truncated response.

-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    In addition to configuring Now Assist in Virtual Agent assistants, admins can configure the default Now Assist panel assistants. Options may vary for Now Assist panel assistants.

    [Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   If multiple assistants are created, users can chat simultaneously with multiple assistants. Conversations are independent from each other.
    -   Turn on or off Now Assist panel \(agent or creator\) assistant. Contact support to configure Now Assist panel assistants.


    -   Now Assist Topic skill must be turned on at the assistant level for document uploads to be activated when managing the chat experience. For more information, see [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
    -   Create and manage agentic workflows in Now Assist AI Agents Studio and assign the workflows to the assistant.
    [Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Display Now Assist in Virtual Agent enhanced chat, with or without the full-page experience, on your portal or mobile app. This dynamic window includes the ability to have multiple active conversations and search capabilities. To use enhanced chat, portals and mobile apps require AI Search to be enabled. For more information on the prerequisites, see [Portal prerequisites for enhanced chat](https://www.servicenow.com/docs/access?context=prerequisites-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) and [Mobile app prerequisites for enhanced chat](https://www.servicenow.com/docs/access?context=mobile-prereqs-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
    [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Upload documents to Now Assist in Virtual Agent standard chat or enhanced chat experience. The Now Assist topics skill must be enabled in Now Assist skills. For more information on file formats, see [Upload documents in a chat](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
    [Review chat assistant settings](https://www.servicenow.com/docs/access?context=review-assistant-settings&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)

    -   Document uploads appear as active if it's turned on when managing the chat experience.
-   **[Upload documents in a chat](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Upload or drag and drop files to Now Assist in Virtual Agent \(standard chat or enhanced chat\). The assistant analyzes and understands the content of the files, and a user can ask questions about the content of the files or get a summary.

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Enable suggested actions in Now Assist in Virtual Agent so that users are offered options for what they can do after completing a prior action. Suggested actions is applicable to standard and enhanced chat, mobile, and Microsoft Teams.

-   **[Web Search custom skill](https://www.servicenow.com/docs/access?context=web-search-custom-skill&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Web Search custom skill to query the internet for information using a third-party AI. The skill triggers when the LLM and AI Search cannot provide an answer. Both values are shown in the System Properties \[sys\_properties\] table item **sn\_nowassist\_va.websearch\_fallback\_enabled**. Set a chosen definition \(such as Perplexity\) to `true` in the AI Search answers OneExtend capability along with its matching API in the Credentials list. You can set one definition and credential to true at any one time.


-   **[Stream chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Benefit from Knowledge Graph integration](https://www.servicenow.com/docs/access?context=exploring-knowledge-graph&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Receive fewer Virtual Agent slot-fill questions during conversations whenever Knowledge Graph is activated.

-   **[Receive personalized synthesized response answers with Knowledge Graph integration](https://www.servicenow.com/docs/access?context=access-knowledge-graph-designer&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Discover more personalized conversational catalog, topic, subflows, or action responses and receive more personalized answers for Q&amp;A Knowledge Base synthesized responses. Personalized responses may appear depending on whether the questions or requests sent to Virtual Agent trigger the Knowledge Graph user profile schema. These personalized responses are slot-filled based on the following table and column attributes:

    -   sys\_user table's columns:
        -   Name
        -   First name
        -   Last name
        -   Username
        -   Employee number
        -   Email
        -   Business phone
        -   Mobile phone
        -   Title
        -   Preferred language
        -   Time format
        -   Date format
        -   Time zone
        -   Zip code
        -   City
        -   State
    -   cmn\_location table's columns:
        -   City
        -   State
        -   Country
    -   cmn\_department table's column:
        -   Name
        -   Headcount
    -   core\_company table's column:
        -   Name
    -   manager table's columns:
        -   Name
        -   First name
        -   Last name
        -   Username
        -   Employee number
        -   Email
        -   Business phone
        -   Mobile phone
        -   Title
        -   Preferred language
        -   Time format
        -   Date format
        -   Time zone
        -   Zip code
        -   City
        -   State
    -   reportees table's columns:
        -   Name
        -   First name
        -   Last name
        -   Username
        -   Employee number
        -   Email
        -   Business phone
        -   Mobile phone
        -   Title
        -   Preferred language
        -   Time format
        -   Date format
        -   Time zone
        -   Zip code
        -   City
        -   State
    -   assets table's columns:
        -   Display name
        -   Purchase date
        -   Retired date
-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)'**

    Now Assist skills:

    -   An alert appears, at the assistant level, if a global level skill is turned off.
    -   By default, all global level skills are turned on in the Now Assist Admin console, except for subflows and actions.
    -   Custom skill is a new skill that has been added to the list of Now Assist skills.
    Display experience:

    -   Select the chat launcher function to open an assistant.
    -   Select a custom mobile app, integrated with the mobile SDK, to open an assistant.
    -   Custom apps section appears if the mobile SDK plugin is installed.
    Information sources:

    -   Add an external search source to your assistant's search profile.
    -   Create custom skills in the Now Assist Skill Kit and assign the skills to the assistant.
    -   Associate Knowledge Graph with an assistant if Knowledge Graph is enabled.
    Chat experience:

    -   Promoted topics has been renamed to promoted assets.
    -   Tags appear in promoted assets indicating whether it's a topic, subflow, or action.
    -   Streaming responses can be activated if Dynamic Translation is deactivated.
    -   Activate or deactivate pre-chat surveys as an admin with the sys\_properties.list item **com.glide.cs.nass.prechat.enabled**.
    Review:

    -   Shows whether stream responses is turned on or off.
-   **[Using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Search through external content connections such as Microsoft SharePoint or Confluence if external search sources are added to information sources when [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

    Select an inline citation to show a popover containing a link to an article or source, or a description and action to start a request.

    Citations with an action are shown after a second clarifying question from Virtual Agent.

    Change the order of the fallback and revisit options in the **View more options** results list that appears in the synthesized response. Use the **sn\_nowassist\_va.synth\_response\_revisit\_position** system property with either the **BEFORE\_FALLBACK** or **AFTER\_FALLBACK** values.

    Show or hide the **Need more help** button in the synthesized response by using the **show\_view\_more\_for\_synthesized** system property.

    Turn on or off regular results in Virtual Agent from the following Now Assist Search Results Output Types table using the parameter **now\_assist\_va\_search\_results\_output\_type.list** parameter.

    Use prechat and postchat surveys with GPT4o and LLAMA. Users can select data pills or enter strings for responses.

    Use new prebuilt topics for prechat and postchat surveys in LLM conversations.


## UI changes

-   **[UI Virtual Agent Designer updates](https://www.servicenow.com/docs/access?context=vad-topics-page&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   Use a new option in the Actions on row icon to remove an LLM assistant from a given asset.
    -   View a tooltip if you try to promote more than six topics for a given LLM assistant.
    -   View a list of available asset types and their descriptions when you select **Create asset** in the Asset library tab.
-   **[UI chat assistant updates](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
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
-   **[UI enhanced chat updates](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   Dynamic processing messages for agentic conversations are now consolidated under one View AI Steps header rather than under several View AI Steps headers.
    -   The **View all options** link shows below the suggested or promoted topics cards on the greeting topic in Now Assist in Virtual Agent and Now Assist panel's enhanced chat. At least one suggested or promoted asset has to be enabled for this link to show.
    -   The auto-complete suggestion type in the Ask Now Assist header appears at the top of the portal search bar's drop-down list. The results in the Ask Now Assist header can now show more targeted search results from AI Search rather than the GlideRecord. The entered search term can appear highlighted in bold after you have configured AI Search as the source for Ask Now Assist suggestions. For more information about this configuration, see [Configure AI Search as the source for Ask Now Assist suggestions](https://www.servicenow.com/docs/access?context=configure-ai-search-source-ask-now-assist-suggestions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
    -   The static and dynamic choice nodes now appear differently in standard and enhanced chat depending on the number of choices for single-select options. For example:
        -   2-5 choices appear as pills
        -   6 or more choices appear as a choice list with a scroll bar
    -   The input bar for enhanced chat has moved all icons below any inputted text. Uploaded documents appear above any inputted text.
    -   The float, pinned, and 90% screen views of enhanced chat now have a gradient border around them.
    -   The enhanced chat full-page experience was updated so that the Now Assist and Search button tabs that were originally center-aligned buttons are now left-aligned tabs that no longer look like buttons.

-   **[Agentic conversation processing messages for Now Assist panel and Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Before receiving a response, you receive acknowledgment messages from the Virtual Agent and on-screen processing messages to let you know where the agent is at in the agentic processing flow. The on-screen processing messages appear in present tense until the processing flow is complete. After the processing flow is complete, then the on-screen messages change to past tense and a View AI Steps section header appears above the processed messages. You can expand the collapsed View AI Steps section header to view the processed messages.


-   **[UI chat updates](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   The enhanced chat navigation area was updated. The New Chat, Chats, Support, and Settings icons were reworked into a simplified subheader. Additionally, each chat title now appears in the simplified subheader.
    -   The enhanced chat's subheader reflects conversational modes in a banner whenever you enter into a specific mode, such as web search, live agent, or document upload.
    -   In the enhanced chat's **Chats** &gt; **Closed chats** section, hover over a chat to view the delete option and complete the delete confirmation prompts.
    -   Minor animations occur in the following five enhanced chat transitions:

        -   Hovering over the chat icon.
        -   Minimizing and opening the chat icon.
        -   Transitioning from a floating chat window to a pinned chat window and vice versa.
        -   Transitioning from a floating chat window to a 90% modal and vice versa.
        -   Transitioning from a pinned chat window to a 90% modal and vice versa.
        **Note:** Transition animation doesn’t apply to custom icons.

-   **[UI admin guided setup updates](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   **Manage search profile** button replaces the search profile text link.
    -   **Add external search sources** drop-down list has been replaced with **Add search sources** drop-down list to include internal and external search sources.
    -   The simple and advanced views within the Chat experience page are consolidated into a single view.
    -   **Copy existing configuration** button is featured more prominently, and it's shown with information about its use.

-   **[UI chat updates](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   The summary card in a Now Assist in Virtual Agent conversation was updated to a more modern look and feel.
    -   The default chat widget button for enhanced chat and standard chat now differs on the portal.
    -   An Ask Now Assist header now appears with suggested searches in a drop-down on the portal's search bar.
    -   The Boolean choice, static choice, and dynamic choice controls were updated to a more modern look and feel for requesters.

-   **[UI chat updates](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   The **New messages below** button in Virtual Agent was replaced with a simplified down-arrow indicator.
    -   The **New messages above** button was deprecated because Virtual Agent now auto-scrolls to the top of the oldest new message.
    -   The Input text bar was updated to a more modern look and feel.
    -   The start a new conversation icon was updated.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Conversational Platform Now Assist skills are active by default](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The following Platform Now Assist skills are active by default and no longer visible in Now Assist Admin console:

    -   Now Assist Multi-Turn Catalog Ordering
    -   Now Assist Q&amp;A Genius Results
    -   Now Assist Topics
    -   Subflows and actions
    -   Custom skills
    -   AI agents

-   **[Additional fallback options](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    There are up to five fallback options that can be presented to end users:

    -   **Search the web**: Triggers web search mode and uses the internet to search for the results.

        **Note:** Only the last query entered into the conversation is considered when entering web search mode via the fallback option.

    -   **Request a live chat**: Triggers live agent mode and routes you to a human support representative.
    -   **Create a generic ticket**: Creates a record.
    -   **End this chat**: Ends the chat.

        **Note:** This option is only available to standard chat conversations.

    -   **Custom fallback option**: Presents a fallback Virtual Agent topic.
-   **[Web search mode enhancements](https://www.servicenow.com/docs/access?context=web-search-requestor&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Manually enter into web search mode via the input bar for standard and enhanced chat conversations. Web search mode includes in-line citations and the associated sources. A web search mode banner appears in enhanced chat conversations that end users can use to end the mode.

-   **[Profanity recognition response](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    If Now Assist Guardian is enabled and the end user's request contains profane content, the Virtual Agent responds with a message prompt to re-enter an appropriate request without profanity or offensive content.


-   **[Standard chat](https://www.servicenow.com/docs/access?context=nava-standard-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    The existing Now Assist in Virtual Agent LLM conversational behavior received a terminology update and is now referred to as standard chat.


-   **[Dynamic Translation calls](https://www.servicenow.com/docs/access?context=translation-for-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    If native translation is enabled, a Dynamic Translation call is only made if an unsupported language for native translation is used.


## Deprecations

-   In Patch 11, **sn\_aia.use\_agents\_in\_planner** system property has been removed. The system property was used for configuring AI agent discovery behavior.
-   In Patch 11, Now Assist skills page in the assistant admin guided setup has been removed due to the skills being turned on by default.
-   In Patch 6, Bing support for the searching and scraping search result type is no longer supported when adding a web search tool in Now Assist Skill Kit.
-   In Patch 4, support for Now Assist in Conversational IVR was removed.

## Activation information

**Note:** When you upgrade to Yokohama Patch 8 or later, agentic AI is the primary orchestration in Virtual Agent. For more information about agentic AI, see [Agentic conversations in Virtual Agent](https://www.servicenow.com/docs/access?context=agentic-conversations-vad&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following products are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)
-   [Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)
-   [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)
-   [Now Assist for Employee Experience](https://www.servicenow.com/docs/access?context=now-assisit-employee-exp&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)
-   [Now Assist for Operational Sustainability \(formerly ESG\)](https://www.servicenow.com/docs/access?context=now-assist-for-esg&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Operational Technology Manager \(OTM\)](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)
-   [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)
-   [Now Assist for PSDS](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=yokohama&pubname=yokohama-government-industry&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)

For more information, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

## Additional requirements

[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.

## Browser requirements

Now Assist in Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Localization information

[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) is supported for non-streaming Now Assist Virtual Agent conversations. For details, see [Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) and .

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    ServiceNow® Now Assist uses agentic AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The Now Assist in AI Search ServiceNow® Store application combines the power of search with the Now LLM Service agentic AI model to answer questions in user searches with actionable AI-generated summaries of relevant Knowledge articles.

-   **[Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Unlock your enterprise productivity with ServiceNow® Virtual Agent. Increase deflections by empowering your employees and customers to serve themselves using a friendly messaging interface, featuring prebuilt conversations powered by artificial intelligence.


**Parent Topic:**[Conversational Interfaces release notes](conversational-interfaces-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

