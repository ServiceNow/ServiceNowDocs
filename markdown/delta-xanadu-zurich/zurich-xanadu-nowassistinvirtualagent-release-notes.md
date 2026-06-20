---
title: Combined Now Assist in Virtual Agent release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Now Assist in Virtual Agent from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-nowassistinvirtualagent-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 52
breadcrumb: [Products combined by family]
---

# Combined Now Assist in Virtual Agent release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Now Assist in Virtual Agent from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist in Virtual Agent release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist in Virtual Agent to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Now Assist in Virtual Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Use enhanced chat](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=xanadu&ft:locale=en-US)**

Enhanced chat is a conversational support experience within a resizable and moveable window that also includes the ability to have multiple active conversations and superior search capabilities. Using enhanced chat's full-page experience further intertwines chat and search capabilities by redirecting users into a full-page chat after entering a query into a portal's search bar.

-   **[View inline citations](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=xanadu&ft:locale=en-US)**

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

-   **[Use suggested actions](https://servicenow-staging.fluidtopics.net/access?context=suggested-actions&family=xanadu&ft:locale=en-US)**

View suggested actions that were related to your prior conversation and that you consider doing next. After completing a conversational catalog request, conversational subflow, or Virtual Agent topic, two suggested actions appear after a `Here's what you can do next` header.

-   **[Stream enhanced chat responses](https://servicenow-staging.fluidtopics.net/access?context=streaming-responses-requestor&family=xanadu&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Use language detection to automatically switch the conversational language for enhanced chat conversations](https://servicenow-staging.fluidtopics.net/access?context=dynamic-lang-detection-translation-enhanced-chat&family=xanadu&ft:locale=en-US)**

Automatically switch the conversational language to the user's detected language during LLM enhanced chat conversations when language detection is turned on. This automatic switch can occur when a user enters an utterance at the start of a new conversation or within the portal home page’s search field.

-   **[Recognize the Boolean user input control during dynamic translation](https://servicenow-staging.fluidtopics.net/access?context=multi-language-options-va&family=xanadu&ft:locale=en-US)**

Recognize the Boolean user input control in chat conversations during dynamic translation.

-   **[Adjust Shorten responses toggle to impact Show more option in chat](https://servicenow-staging.fluidtopics.net/access?context=va-text-response&family=xanadu&ft:locale=en-US)**

For bot text responses, adjust the **Shorten responses** toggle in Virtual Agent Designer to turn off the **Show more** option on the user side. When **Shorten responses** is turned off, the **Show more** option does not appear in the chat to the user and the full answer is displayed rather than a truncated response.

-   **[Configuring Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

In addition to configuring Now Assist in Virtual Agent assistants, admins can configure the default Now Assist panel assistants. Options may vary for Now Assist panel assistants.

[Create an assistant](https://servicenow-staging.fluidtopics.net/access?context=create-assistant&family=xanadu&ft:locale=en-US)

    -   If multiple assistants are created, users can chat simultaneously with multiple assistants. Conversations are independent from each other.
    -   Turn on or off Now Assist panel \(agent or creator\) assistant. Contact support to configure Now Assist panel assistants.
[Assign Now Assist skills to an assistant](https://servicenow-staging.fluidtopics.net/access?context=assign-na-skills-assistant&family=xanadu&ft:locale=en-US)

    -   Now Assist Topic skill must be turned on at the assistant level for document uploads to be activated when managing the chat experience. For more information, see [Manage an assistant chat experience](https://servicenow-staging.fluidtopics.net/access?context=manage-assistant-chat-experience&family=xanadu&ft:locale=en-US).
    -   Create and manage agentic workflows in Now Assist AI Agents Studio and assign the workflows to the assistant.
[Display your assistant on a portal or channel](https://servicenow-staging.fluidtopics.net/access?context=display-assistant-portal-channel&family=xanadu&ft:locale=en-US)

    -   Display Now Assist in Virtual Agent enhanced chat, with or without the full-page experience, on your portal or mobile app. This dynamic window includes the ability to have multiple active conversations and search capabilities. To use enhanced chat, portals and mobile apps require AI Search to be enabled. For more information on the prerequisites, see [Portal prerequisites for enhanced chat](https://servicenow-staging.fluidtopics.net/access?context=prerequisites-enhanced-chat&family=xanadu&ft:locale=en-US) and [Mobile app prerequisites for enhanced chat](https://servicenow-staging.fluidtopics.net/access?context=mobile-prereqs-enhanced-chat&family=xanadu&ft:locale=en-US).
[Manage an assistant chat experience](https://servicenow-staging.fluidtopics.net/access?context=manage-assistant-chat-experience&family=xanadu&ft:locale=en-US)

    -   Upload documents to Now Assist in Virtual Agent standard chat or enhanced chat experience. The Now Assist topics skill must be enabled in Now Assist skills. For more information on file formats, see [Upload documents in Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=upload-documents-na-va&family=xanadu&ft:locale=en-US).
[Review assistant settings](https://servicenow-staging.fluidtopics.net/access?context=review-assistant-settings&family=xanadu&ft:locale=en-US)

    -   Document uploads appear as active if it's turned on when managing the chat experience.
-   **[Upload documents in Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=upload-documents-na-va&family=xanadu&ft:locale=en-US)**

Upload or drag and drop files to Now Assist in Virtual Agent \(standard chat or enhanced chat\). The assistant analyzes and understands the content of the files, and a user can ask questions about the content of the files or get a summary.

-   **[Now Assist in Virtual Agent system properties](https://servicenow-staging.fluidtopics.net/access?context=nava-sys-props&family=xanadu&ft:locale=en-US)**

Enable suggested actions in Now Assist in Virtual Agent so that users are offered options for what they can do after completing a prior action. Suggested actions is applicable to standard and enhanced chat, mobile, and Microsoft Teams.


-   **[Stream chat responses](https://servicenow-staging.fluidtopics.net/access?context=streaming-responses-requestor&family=xanadu&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.


-   **[Use Now Assist to call Microsoft Active Directory v2 actions](https://servicenow-staging.fluidtopics.net/access?context=ms-ad-v2-spoke&family=xanadu&ft:locale=en-US)**

Install Now Assist for Conversational Spokes plugin and start utilizing the conversational ability of the Look up User spoke action. You can call this action from a conversational interface like Now Assist.

-   **[Run an action from a conversation](https://servicenow-staging.fluidtopics.net/access?context=conversational-actions&family=xanadu&ft:locale=en-US)**

Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational action from Workflow Studio. View and edit conversational actions within Virtual Agent Designer.

-   **[Run a subflow from a conversation](https://servicenow-staging.fluidtopics.net/access?context=conversational-subflows&family=xanadu&ft:locale=en-US)**

Run a Workflow Studio subflow from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio. View and edit conversational subflows within Virtual Agent Designer.

-   **[AI generated topic description message within topic migration](https://servicenow-staging.fluidtopics.net/access?context=migrate-nlu-llm&family=xanadu&ft:locale=en-US)**

A `Topic description generated by Now Assist` message now appears near the **Topic Description** field during the topic migration's Review descriptions step.

-   **[Small talk for LLM conversations](https://servicenow-staging.fluidtopics.net/access?context=create-small-talk&family=xanadu&ft:locale=en-US)**

Use small talk in LLM conversations for greetings and farewells along with gratitude and complaint statements. A Semantic Filtering Framework \(SFF\) detects small talk and generates an appropriate response.

-   **[Language detection for LLM conversations](https://servicenow-staging.fluidtopics.net/access?context=multi-language-options-va&family=xanadu&ft:locale=en-US)**

Use language detection for your LLM conversations to improve your user's experience.

-   **[Virtual Agent Designer Topics home page](https://servicenow-staging.fluidtopics.net/access?context=vad-topics-page&family=xanadu&ft:locale=en-US)**

A new list-based Virtual Agent Designer home page appears for users who have activated Now Assist in Virtual Agent and the Agent assist Topics skill. The card-based UI is still available for those users who use only NLU/keyword or Virtual Agent Lite.

-   **[Virtual Agent Designer user input controls](https://servicenow-staging.fluidtopics.net/access?context=va-user-inputs&family=xanadu&ft:locale=en-US)**

Updates to LLM user inputs include:

    -   Use the Validation toggle in the Advanced section of User Inputs to confirm user input values by scripts.
    -   Use the Allow slot filling toggle on User Inputs to switch between static \(single field\) and dynamic \(define with scripts or data pill picker\) detail description modes.
    -   Get a message that a mandatory field cannot be skipped when you attempt to skip a user input with conditions not set to be skippable.
-   **[Configuring Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Updates to the admin guided setup include:

    -   Enhance functionality and efficiency of your Virtual Agent by linking primary assistants to secondary assistants, enabling a primary assistant to use search sources from secondary assistants.
    -   View the relationship between primary and secondary assistants within a map view.
    -   Select portals and mobile applications to display Virtual Agents.
    -   Create conversational subflows and actions by launching Workflow Studio to make conversational subflows and actions available to the assistant.
-   **[Synthesized response](https://servicenow-staging.fluidtopics.net/access?context=using-now-assist-in-va&family=xanadu&ft:locale=en-US)**

For Now Assist in Virtual Agent users, a synthesized response can appear. A synthesized response includes a brief summary of the requested information and search results along with Genius Results. Mid-topic switching can occur during a conversation with synthesized response. Users can continue with their original request or switch the conversation's focus.

-   **[New system properties](https://servicenow-staging.fluidtopics.net/access?context=r_AvailableSystemProperties&family=xanadu&ft:locale=en-US)**

The following system property was added to increase flexibility of the search results and response:

    -   **sn\_nowassist\_va.synthesized\_autostart\_items**: When synthesized response only returns a singular action, configure whether to directly launch into that action. By default, whenever synthesized response returns a single Virtual Agent topic, that action is auto-launched. The following actions can be configured to auto-launch:
        -   Synthesized response returns a single conversational catalog item.
        -   Synthesized response returns a single Virtual Agent topic, along with Knowledge Base information.
        -   Synthesized response returns a single conversational catalog item, along with Knowledge Base information.

-   **[Delete virtual agents](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Delete a Virtual Agent from the assistants list.

-   **[Support virtual agents on a portal](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Allow public availability of an LLM-based Virtual Agent on a portal.

-   **[Display a virtual agent in a channel](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Integrate your preferred messaging channels to display your Virtual Agent.

-   **[Install proactive triggers](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Install Proactive Triggers from within the Review page.

-   **[Support notifications in virtual agents](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US)**

Support actionable and non-actionable notifications for LLM conversations in Virtual Agent.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Assistant Designer](https://servicenow-staging.fluidtopics.net/access?context=assistant-designer&family=yokohama&ft:locale=en-US)**

Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library, and Analytics.

[Configuring assistants overview](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=yokohama&ft:locale=en-US)

    -   Access the **Assistants** tab within [Assistant Designer](https://servicenow-staging.fluidtopics.net/access?context=assistant-designer&family=yokohama&ft:locale=en-US) by navigating to **All** &gt; **Assistant Designer**. The **Assistants** tab is only available for customers who have the Now Assist license. NLU-only customers don't have access to [Assistant Designer](https://servicenow-staging.fluidtopics.net/access?context=assistant-designer&family=yokohama&ft:locale=en-US).
[View assistants](https://servicenow-staging.fluidtopics.net/access?context=view-assistants&family=yokohama&ft:locale=en-US)

    -   View chat and voice assistants within the **Assistants** tab of [Assistant Designer](https://servicenow-staging.fluidtopics.net/access?context=assistant-designer&family=yokohama&ft:locale=en-US).
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
[Create a voice assistant](https://servicenow-staging.fluidtopics.net/access?context=configure-voice-assistants&family=yokohama&ft:locale=en-US)

    -   Start creating an AI voice assistant by providing a name and description. Tag to a business unit to analyze your voice assistant.
    -   Power your voice assistant with agentic experience by adding AI agents.
    -   Personalize your voice assistant by choosing a language, adding a welcome message, and an AI voice persona.

**Note:** The supported languages are:

        -   English
        -   German
        -   Spanish
    -   Secure the voice interactions by setting up caller authentication methods and safeguards.
[Create a chat assistant](https://servicenow-staging.fluidtopics.net/access?context=create-assistant&family=yokohama&ft:locale=en-US)

    -   Add basic details such as a name and description for your chat assistant, and set your assistant as a primary assistant. The Basic details page within the UI has replaced the Overview page.
    -   Now Assist panel – Platform \(default\) assistant can be set as a primary assistant and linked to secondary assistants. Now Assist panel – Developer assistant doesn't have this option.
    -   The name and description of the Now Assist panel assistants can't be changed.
[Use agentic support](https://servicenow-staging.fluidtopics.net/access?context=use-agentic-support&family=yokohama&ft:locale=en-US)

    -   Let the assistant use AI agent skills and agentic orchestration. Admins can choose between agentic or standard \(Q&amp;A\) modes depending on business needs and user experience goals. Turn on or off the **Prioritize AI agents during skills discovery** feature.
[Assign search sources](https://servicenow-staging.fluidtopics.net/access?context=add-info-sources-assistant&family=yokohama&ft:locale=en-US)

    -   Restore search sources back to the default \(Now Assist Multi-Turn Catalog Ordering and Now Assist Q&amp;A\).
    -   Now Assist panel - Platform \(default\) assistant now has the option to copy an existing search configuration.
    -   Dynamic global search configuration has been added to the list of search application configurations.
    -   Create or configure additional search sources by selecting the **External Content Connectors** link. This replaces a card view.
    -   Manage knowledge articles by selecting the **Knowledge Center** link.
    -   In edit mode, search sources are found within the Information Sources sub-tab.
[Add a Knowledge Graph schema](https://servicenow-staging.fluidtopics.net/access?context=add-kg-schema-assistant&family=yokohama&ft:locale=en-US)

    -   Adding a Knowledge Graph schema has moved from the Information sources page to its own page.
    -   Add a Knowledge Graph schema is now available for the Now Assist panel - Platform \(default\) assistant. For the NLQ schema, if Global Graph or Global Graph Mini is selected, you have the option to select tags for specific workspaces that are active on the instance.
    -   Define the mapping relationship between individual workspaces on the instance and predefined Knowledge Graph tags when Global Schema is selected for NLQ.
    -   In edit mode, Knowledge Graph is found within the Information Sources sub-tab.
[Add assets](https://servicenow-staging.fluidtopics.net/access?context=add-assets&family=yokohama&ft:locale=en-US)

    -   By default, all Now Assist skills \(Now Assist Q&amp;A, Now Assist multi-turn catalog ordering, Now Assist topics, subflows and actions, custom skills, and AI agents\) are turned on. Therefore, the Now Assist skills page has been removed.
    -   Map an asset to an assistant. Assets are the building blocks of each assistant, providing them with instructions and functionality for helping users. Assets include topics, subflows and actions, custom skills, and AI agents. For Now Assist panel - Developer assistant, only topics \(asset type\) is available.
    -   In edit mode, assets are found within the Information Sources sub-tab.
[Select a display experience](https://servicenow-staging.fluidtopics.net/access?context=display-assistant-portal-channel&family=yokohama&ft:locale=en-US)

    -   Leverage Now Assist capabilities in Google chat.
    -   Use **Prominent action button override** to allow a different chat assistant other than the default assistant to be launched on a mobile app.
    -   In edit mode, display experiences are found within the Settings sub-tab.
[Display assistant on Platform or ServiceNow Studio](https://servicenow-staging.fluidtopics.net/access?context=display-nap-assistant&family=yokohama&ft:locale=en-US)

    -   The **Add ServiceNow Platform** drop-down menu has replaced the **Add agent experience** drop-down menu. A Now Assist panel assistant can't be added to other display experiences.
    -   In edit mode, display experiences are found within the Settings sub-tab.
[Brand an assistant](https://servicenow-staging.fluidtopics.net/access?context=brand-assistant&family=yokohama&ft:locale=en-US)

    -   Minor enhancements to the look-and-feel of the standard chat preview pane.
    -   In edit mode, branding is found within the Settings sub-tab.
[Manage chat experience](https://servicenow-staging.fluidtopics.net/access?context=manage-assistant-chat-experience&family=yokohama&ft:locale=en-US)

    -   A standard chat preview pane is shown for the default greeting topic \(Now Assist – Greeting\) and the default closing topic \(Now Assist – Closing\). Selecting custom topics won’t show a preview pane.
    -   Fallbacks have a standard chat preview pane and each fallback is shown if toggled on.
    -   For the Now Assist panel - Platform \(default\) assistant, web search, record producer, and custom fallback are available options. End this chat and survey are available for the standard chat experience.
    -   In edit mode, chat experience is found within the Settings sub-tab.
[Enable additional chat features](https://servicenow-staging.fluidtopics.net/access?context=additional-chat-features&family=yokohama&ft:locale=en-US)

    -   Web search, response streaming, document uploads, and closed chat were moved from the Manage chat experience page to its own page. By default all chat features except web search are turned on.
    -   Response streaming can be turned on at the assistant level regardless of whether Dynamic Translation is turned on or off. However, response streaming doesn't work when Dynamic Translation is being used.
    -   In addition to web search, response streaming, document uploads, and closed chat, Now Assist panel Platform assistant has voice input. Voice input allows users to use a microphone to enter the input.
    -   In edit mode, additional chat features are found within the Settings sub-tab.
[Review settings](https://servicenow-staging.fluidtopics.net/access?context=review-assistant-settings&family=yokohama&ft:locale=en-US)

    -   New sections that have been added include: Agentic support, Knowledge Graphs, Assets, and Chat features.
    -   Testing an assistant has been removed from the Review page.
[Test a chat assistant](https://servicenow-staging.fluidtopics.net/access?context=test-assistant&family=yokohama&ft:locale=en-US)

    -   Test a chat assistant from **Assistant Designer** &gt; **Assistants** tab or from within each page while in edit mode.
[Edit a chat assistant](https://servicenow-staging.fluidtopics.net/access?context=edit-assistant&family=yokohama&ft:locale=en-US)

    -   Edit a chat assistant from **Assistant Designer** &gt; **Assistants** tab. You will be directed through an edit flow with a slightly different UI from the create flow.
[Analyzing assistants](https://servicenow-staging.fluidtopics.net/access?context=ai-engagement-analytics&family=yokohama&ft:locale=en-US)

    -   Monitor, evaluate, and optimize the performance of your AI-powered assistants within the **Analytics** tab of [Assistant Designer](https://servicenow-staging.fluidtopics.net/access?context=assistant-designer&family=yokohama&ft:locale=en-US).
-   **[Copy received messages](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=yokohama&ft:locale=en-US)**

Use the copy message icon in the feedback panel to copy received Virtual Agent responses.

-   **[New system properties](https://servicenow-staging.fluidtopics.net/access?context=nava-sys-props&family=yokohama&ft:locale=en-US)**
    -   Set the **com.glide.cs.nass.synthesized\_response.disabled\_popover.hide** to `true` to hide the popover for disabled catalog items for Now Assist in Virtual Agent and Now Assist panel's enhanced chat.
    -   Set the **sn\_ais\_assist.enable\_pi\_in\_nba** property to `true` to allow conversational history-based suggested actions and fill multiple suggested action slot options.
    -   View the **sn\_nowassist\_va.enable\_nass\_show\_all\_options** property to decide whether to allow the **View all options** link in an enhanced chat conversation's greeting topic.
    -   The **com.glide.interactive\_view.enabled** property opens an interactive side panel view next to the chat window. The default value is `true` to activate AI Engagement Experience on your instance.
-   **[View org chart in the interactive view](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=yokohama&ft:locale=en-US)**

Select **View org chart** from the people citation's popover in Now Assist panel's enhanced chat or Now Assist in Virtual Agent enhanced chat/enhanced chat's full-page experience. The person's organizational chart appears to the right of the chat conversation in an area known as the interactive view. You can switch between multiple organizational charts via a drop-down in the interactive view if you open multiple people citations' org charts in the same conversation.


-   **[Select continue or move to next task button](https://servicenow-staging.fluidtopics.net/access?context=nava-standard-chat&family=yokohama&ft:locale=en-US)**

The **Continue to next task** button appears in the new **Ready to move on to your next task** card whenever multiple questions are found in a single standard chat user's message. The **Move on to the next task** citation appears at the end of an enhanced chat's synthesized response whenever multiple questions or requests are found along with an action in the user's single message. Whenever either **Continue to next task** \(standard chat\) or **Move on to the next task** \(enhanced chat\) is selected, the second question or request is reviewed and a synthesized response is sent back regarding the user's second question or request.

-   **[Multiple questions in a single user message are answered consecutively](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=yokohama&ft:locale=en-US)**

Virtual Agent can answer multiple questions that were submitted in a single message query. Now Assist panel or Now Assist in Virtual Agent answers the multiple questions consecutively in a response.

-   **[Now Assist in Virtual Agent system properties](https://servicenow-staging.fluidtopics.net/access?context=nava-sys-props&family=yokohama&ft:locale=en-US)**

Use **sn\_aia.use\_agents\_in\_planner** to configure AI agent discovery behavior. The default value is `true`, preferring AI agents over assets including catalogs, topics, Q&amp;A knowledge base articles, workflows, and sub-workflows. When set to `false`, there’s no preference for AI agents. AI agents and assets are treated the same.


-   **[Configure additional user interface and experience options for enhanced chat](https://servicenow-staging.fluidtopics.net/access?context=ac-configure-chat-branding&family=yokohama&ft:locale=en-US)**

Customize and configure the Search Toggle Button Label for enhanced chat's full-page experience. Additionally, you can configure the Enable Unread Conversation Count Display and Left Panel Header Label for enhanced chat and enhanced chat's full-page experience.

-   **[New third-party AI model provider options available for all Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[View agentic conversations processing steps](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=yokohama&ft:locale=en-US)**

View agentic conversational processing steps and stop the flow, if needed.

-   **[View extended entities and records](https://servicenow-staging.fluidtopics.net/access?context=using-now-assist-in-va&family=yokohama&ft:locale=en-US)**

View extended entities and records in standard and enhanced chat conversations that come from the additional custom tables associated with the Knowledge Graph natural language query \(NLQ\) schema such as:

    -   Assets
    -   Incidents
    -   Recently viewed knowledge base articles
    -   Requests
    -   Tasks
-   **[View suggested queries in the portal’s search bar and chat window](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=yokohama&ft:locale=en-US)**

View the most frequently asked queries in the portal’s search bar and enhanced chat’s Virtual Agent. Any search query entered into the portal’s search bar or Virtual Agent is incorporated into the greeting topic for future conversations as a suggested query. Suggested queries are only included in the Virtual Agent greeting topic whenever no promoted assets are designated.

-   **[Work with suggested queries](https://servicenow-staging.fluidtopics.net/access?context=nava-sys-props&family=yokohama&ft:locale=en-US)**

Two system properties were added to enable the suggested queries feature: **sn\_nowassist\_va.enable\_suggested\_queries** and **sn\_nowassist\_va.max\_suggested\_queries**.

-   **[Configure AI search answers OneExtend capability for web search](https://servicenow-staging.fluidtopics.net/access?context=configure-ai-search-answers-capability-for-web-search&family=yokohama&ft:locale=en-US)**

Configure the AI Search answers capability via `sys_one_extend_capability.list` to establish the web search AI provider and work with API keys, if needed.

-   **[Expanding AI provider support for web search](https://servicenow-staging.fluidtopics.net/access?context=configure-ai-search-answers-capability-for-web-search&family=yokohama&ft:locale=en-US)**

OpenAI, Perplexity, and Google Gemini support web search.

-   **[Configuring assistants overview](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=yokohama&ft:locale=en-US)**

Enhancements to Now Assist in Virtual Agent assistants and Now Assist panel Platform and Developer assistants. Options vary for Now Assist panel assistants.

[Create a chat assistant](https://servicenow-staging.fluidtopics.net/access?context=create-assistant&family=yokohama&ft:locale=en-US)

    -   Configure assistants by domain.
[\[Placeholder link text to key bundle-convint.assign-na-skills-assistant\]](https://servicenow-staging.fluidtopics.net/access?context=assign-na-skills-assistant&family=yokohama&ft:locale=en-US)

    -   Now Assist in Virtual Agent assistants: By default, all global skill types are turned on in Now Assist Admin console.
    -   Now Assist panel Platform assistant: By default, all global skill types, except for Catalog skill, are turned on in Now Assist Admin console.
    -   Now Assist panel Developer assistant: By default, Now Assist Topic skill is turned on in Now Assist Admin console. No other skills are available for the Now Assist panel Developer assistant.
[Select a display experience](https://servicenow-staging.fluidtopics.net/access?context=display-assistant-portal-channel&family=yokohama&ft:locale=en-US)

    -   Now Assist in Virtual Agent: For mobile search widgets, allow the search bar to open into a full-page experience.
[Display assistant on Platform or ServiceNow Studio](https://servicenow-staging.fluidtopics.net/access?context=display-nap-assistant&family=yokohama&ft:locale=en-US)

    -   Now Assist panel Platform assistant: Enable enhanced chat for a conversational experience that includes a dynamic, movable, and resizable chat window, plus access to multiple active conversations.
    -   Now Assist panel Developer assistant: Not applicable.
[Assign search sources](https://servicenow-staging.fluidtopics.net/access?context=add-info-sources-assistant&family=yokohama&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Add internal and external search sources, such as catalog items and Microsoft Sharepoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural language query schema to allow users to perform a data query during a conversation.
    -   Now Assist panel Platform assistant:
        -   Add internal and external search sources, such as catalog items and Microsoft Sharepoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural language query schema to allow users to perform a data query during a conversation.
    -   Now Assist panel Developer assistant: Not applicable.
[Manage chat experience](https://servicenow-staging.fluidtopics.net/access?context=manage-assistant-chat-experience&family=yokohama&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Select a custom greeting topic, closing topic, error topic, and survey for your assistant.
        -   Select one or more fallback options: live agent, web search, record producer, end this chat, and custom fallback.
        -   Enable web search fallback option and web search mode to allow users to search the web from within a chat window.
    -   Now Assist panel Platform assistant:
        -   Select a custom greeting topic or error topic for your assistant.
        -   Fallback options don't apply to Now Assist panel Platform assistant.
        -   Enable web search mode to allow users to search the web from within a chat window.
    -   Now Assist panel Developer assistant: Not applicable.
-   **[Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=yokohama&ft:locale=en-US)**

Use the enhanced Now Assist panel for a more intuitive and personalized experience. The updated Now Assist panel is re-sizable and can be moved anywhere on the ServiceNow AI platform.


-   **[Now Assist in Virtual Agent system properties](https://servicenow-staging.fluidtopics.net/access?context=nava-sys-props&family=yokohama&ft:locale=en-US)**

Enable pinning a chat window on a portal by using the **sn\_nowassist\_va.enhanced\_chat\_pin\_enabled.&lt;portal-url&gt;** system property.


-   **[Use enhanced chat](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=yokohama&ft:locale=en-US)**

Enhanced chat is a conversational support experience within a resizable and moveable window that also includes the ability to have multiple active conversations and superior search capabilities. Using enhanced chat's full-page experience further intertwines chat and search capabilities by redirecting users into a full-page chat after entering a query into a portal's search bar.

-   **[View inline citations](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=yokohama&ft:locale=en-US)**

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

-   **[Use suggested actions](https://servicenow-staging.fluidtopics.net/access?context=suggested-actions&family=yokohama&ft:locale=en-US)**

View suggested actions that were related to your prior conversation and that you consider doing next. After completing a conversational catalog request, conversational subflow, or Virtual Agent topic, two suggested actions appear after a `Here's what you can do next` header.

-   **[Stream enhanced chat responses](https://servicenow-staging.fluidtopics.net/access?context=streaming-responses-requestor&family=yokohama&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Use language detection to automatically switch the conversational language for enhanced chat conversations](https://servicenow-staging.fluidtopics.net/access?context=dynamic-lang-detection-translation-enhanced-chat&family=yokohama&ft:locale=en-US)**

Automatically switch the conversational language to the user's detected language during LLM enhanced chat conversations when language detection is turned on. This automatic switch can occur when a user enters an utterance at the start of a new conversation or within the portal home page’s search field.

-   **[Recognize the Boolean user input control during dynamic translation](https://servicenow-staging.fluidtopics.net/access?context=multi-language-options-va&family=yokohama&ft:locale=en-US)**

Recognize the Boolean user input control in chat conversations during dynamic translation.

-   **[Adjust Shorten responses toggle to impact Show more option in chat](https://servicenow-staging.fluidtopics.net/access?context=va-text-response&family=yokohama&ft:locale=en-US)**

For bot text responses, adjust the **Shorten responses** toggle in Virtual Agent Designer to turn off the **Show more** option on the user side. When **Shorten responses** is turned off, the **Show more** option does not appear in the chat to the user and the full answer is displayed rather than a truncated response.

-   **[Configuring assistants overview](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=yokohama&ft:locale=en-US)**

In addition to configuring Now Assist in Virtual Agent assistants, admins can configure the default Now Assist panel assistants. Options may vary for Now Assist panel assistants.

[Create a chat assistant](https://servicenow-staging.fluidtopics.net/access?context=create-assistant&family=yokohama&ft:locale=en-US)

    -   If multiple assistants are created, users can chat simultaneously with multiple assistants. Conversations are independent from each other.
    -   Turn on or off Now Assist panel \(agent or creator\) assistant. Contact support to configure Now Assist panel assistants.
[\[Placeholder link text to key bundle-convint.assign-na-skills-assistant\]](https://servicenow-staging.fluidtopics.net/access?context=assign-na-skills-assistant&family=yokohama&ft:locale=en-US)

    -   Now Assist Topic skill must be turned on at the assistant level for document uploads to be activated when managing the chat experience. For more information, see [Manage chat experience](https://servicenow-staging.fluidtopics.net/access?context=manage-assistant-chat-experience&family=yokohama&ft:locale=en-US).
    -   Create and manage agentic workflows in Now Assist AI Agents Studio and assign the workflows to the assistant.
[Select a display experience](https://servicenow-staging.fluidtopics.net/access?context=display-assistant-portal-channel&family=yokohama&ft:locale=en-US)

    -   Display Now Assist in Virtual Agent enhanced chat, with or without the full-page experience, on your portal or mobile app. This dynamic window includes the ability to have multiple active conversations and search capabilities. To use enhanced chat, portals and mobile apps require AI Search to be enabled. For more information on the prerequisites, see [Portal prerequisites for enhanced chat](https://servicenow-staging.fluidtopics.net/access?context=prerequisites-enhanced-chat&family=yokohama&ft:locale=en-US) and [Mobile app prerequisites for enhanced chat](https://servicenow-staging.fluidtopics.net/access?context=mobile-prereqs-enhanced-chat&family=yokohama&ft:locale=en-US).
[Manage chat experience](https://servicenow-staging.fluidtopics.net/access?context=manage-assistant-chat-experience&family=yokohama&ft:locale=en-US)

    -   Upload documents to Now Assist in Virtual Agent standard chat or enhanced chat experience. The Now Assist topics skill must be enabled in Now Assist skills. For more information on file formats, see [Upload documents](https://servicenow-staging.fluidtopics.net/access?context=upload-documents-na-va&family=yokohama&ft:locale=en-US).
[Review settings](https://servicenow-staging.fluidtopics.net/access?context=review-assistant-settings&family=yokohama&ft:locale=en-US)

    -   Document uploads appear as active if it's turned on when managing the chat experience.
-   **[Upload documents](https://servicenow-staging.fluidtopics.net/access?context=upload-documents-na-va&family=yokohama&ft:locale=en-US)**

Upload or drag and drop files to Now Assist in Virtual Agent \(standard chat or enhanced chat\). The assistant analyzes and understands the content of the files, and a user can ask questions about the content of the files or get a summary.

-   **[Now Assist in Virtual Agent system properties](https://servicenow-staging.fluidtopics.net/access?context=nava-sys-props&family=yokohama&ft:locale=en-US)**

Enable suggested actions in Now Assist in Virtual Agent so that users are offered options for what they can do after completing a prior action. Suggested actions is applicable to standard and enhanced chat, mobile, and Microsoft Teams.

-   **[Web Search custom skill](https://servicenow-staging.fluidtopics.net/access?context=web-search-custom-skill&family=yokohama&ft:locale=en-US)**

Use the Web Search custom skill to query the internet for information using a third-party AI. The skill triggers when the LLM and AI Search cannot provide an answer. Both values are shown in the System Properties \[sys\_properties\] table item **sn\_nowassist\_va.websearch\_fallback\_enabled**. Set a chosen definition \(such as Perplexity\) to `true` in the AI Search answers OneExtend capability along with its matching API in the Credentials list. You can set one definition and credential to true at any one time.


-   **[Stream chat responses](https://servicenow-staging.fluidtopics.net/access?context=streaming-responses-requestor&family=yokohama&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Benefit from Knowledge Graph integration](https://servicenow-staging.fluidtopics.net/access?context=exploring-knowledge-graph&family=yokohama&ft:locale=en-US)**

Receive fewer Virtual Agent slot-fill questions during conversations whenever Knowledge Graph is activated.

-   **[Receive personalized synthesized response answers with Knowledge Graph integration](https://servicenow-staging.fluidtopics.net/access?context=access-knowledge-graph-designer&family=yokohama&ft:locale=en-US)**

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
-   **[Configuring assistants overview](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=yokohama&ft:locale=en-US)'**

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
-   **[Using Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=using-now-assist-in-va&family=yokohama&ft:locale=en-US)**

Search through external content connections such as Microsoft SharePoint or Confluence if external search sources are added to information sources when [Configuring assistants overview](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=yokohama&ft:locale=en-US).

Select an inline citation to show a popover containing a link to an article or source, or a description and action to start a request.

Citations with an action are shown after a second clarifying question from Virtual Agent.

Change the order of the fallback and revisit options in the **View more options** results list that appears in the synthesized response. Use the **sn\_nowassist\_va.synth\_response\_revisit\_position** system property with either the **BEFORE\_FALLBACK** or **AFTER\_FALLBACK** values.

Show or hide the **Need more help** button in the synthesized response by using the **show\_view\_more\_for\_synthesized** system property.

Turn on or off regular results in Virtual Agent from the following Now Assist Search Results Output Types table using the parameter **now\_assist\_va\_search\_results\_output\_type.list** parameter.

Use prechat and postchat surveys with GPT4o and LLAMA. Users can select data pills or enter strings for responses.

Use new prebuilt topics for prechat and postchat surveys in LLM conversations.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Assistant Designer](https://servicenow-staging.fluidtopics.net/access?context=assistant-designer&family=zurich&ft:locale=en-US)**

Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library, and Analytics.

[Configuring assistants overview](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=zurich&ft:locale=en-US)

    -   Access the **Assistants** tab within [Assistant Designer](https://servicenow-staging.fluidtopics.net/access?context=assistant-designer&family=zurich&ft:locale=en-US) by navigating to **All** &gt; **Assistant Designer**. The **Assistants** tab is only available for customers who have the Now Assist license. NLU-only customers don't have access to [Assistant Designer](https://servicenow-staging.fluidtopics.net/access?context=assistant-designer&family=zurich&ft:locale=en-US).
[View assistants](https://servicenow-staging.fluidtopics.net/access?context=view-assistants&family=zurich&ft:locale=en-US)

    -   View chat and voice assistants within the **Assistants** tab of [Assistant Designer](https://servicenow-staging.fluidtopics.net/access?context=assistant-designer&family=zurich&ft:locale=en-US).
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
[Create a voice assistant](https://servicenow-staging.fluidtopics.net/access?context=configure-voice-assistants&family=zurich&ft:locale=en-US)

    -   Start creating an AI voice assistant by providing a name and description. Tag to a business unit to analyze your voice assistant.
    -   Power your voice assistant with agentic experience by adding AI agents.
    -   Personalize your voice assistant by choosing a language, adding a welcome message, and an AI voice persona.

**Note:** The supported languages are:

        -   English
        -   German
        -   Spanish
    -   Secure the voice interactions by setting up caller authentication methods and safeguards.
[Create a chat assistant](https://servicenow-staging.fluidtopics.net/access?context=create-assistant&family=zurich&ft:locale=en-US)

    -   Add basic details such as a name and description for your chat assistant, and set your assistant as a primary assistant. The Basic details page within the UI has replaced the Overview page.
    -   Now Assist panel – Platform \(default\) assistant can be set as a primary assistant and linked to secondary assistants. Now Assist panel – Developer assistant doesn't have this option.
    -   The name and description of the Now Assist panel assistants can't be changed.
[Use agentic support](https://servicenow-staging.fluidtopics.net/access?context=use-agentic-support&family=zurich&ft:locale=en-US)

    -   Let the assistant use AI agent skills and agentic orchestration. Admins can choose between agentic or standard \(Q&amp;A\) modes depending on business needs and user experience goals. Turn on or off the **Prioritize AI agents during skills discovery** feature.
[Assign search sources](https://servicenow-staging.fluidtopics.net/access?context=add-info-sources-assistant&family=zurich&ft:locale=en-US)

    -   Restore search sources back to the default \(Now Assist Multi-Turn Catalog Ordering and Now Assist Q&amp;A\).
    -   Now Assist panel - Platform \(default\) assistant now has the option to copy an existing search configuration.
    -   Dynamic global search configuration has been added to the list of search application configurations.
    -   Create or configure additional search sources by selecting the **External Content Connectors** link. This replaces a card view.
    -   Manage knowledge articles by selecting the **Knowledge Center** link.
    -   In edit mode, search sources are found within the Information Sources sub-tab.
[Add a Knowledge Graph schema](https://servicenow-staging.fluidtopics.net/access?context=add-kg-schema-assistant&family=zurich&ft:locale=en-US)

    -   Adding a Knowledge Graph schema has moved from the Information sources page to its own page.
    -   Add a Knowledge Graph schema is now available for the Now Assist panel - Platform \(default\) assistant. For the NLQ schema, if Global Graph or Global Graph Mini is selected, you have the option to select tags for specific workspaces that are active on the instance.
    -   Define the mapping relationship between individual workspaces on the instance and predefined Knowledge Graph tags when Global Schema is selected for NLQ.
    -   In edit mode, Knowledge Graph is found within the Information Sources sub-tab.
[Add assets](https://servicenow-staging.fluidtopics.net/access?context=add-assets&family=zurich&ft:locale=en-US)

    -   By default, all Now Assist skills \(Now Assist Q&amp;A, Now Assist multi-turn catalog ordering, Now Assist topics, subflows and actions, custom skills, and AI agents\) are turned on. Therefore, the Now Assist skills page has been removed.
    -   Map an asset to an assistant. Assets are the building blocks of each assistant, providing them with instructions and functionality for helping users. Assets include topics, subflows and actions, custom skills, and AI agents. For Now Assist panel - Developer assistant, only topics \(asset type\) is available.
    -   In edit mode, assets are found within the Information Sources sub-tab.
[Select a display experience](https://servicenow-staging.fluidtopics.net/access?context=display-assistant-portal-channel&family=zurich&ft:locale=en-US)

    -   Leverage Now Assist capabilities in Google chat.
    -   Use **Prominent action button override** to allow a different chat assistant other than the default assistant to be launched on a mobile app.
    -   In edit mode, display experiences are found within the Settings sub-tab.
[Display assistant on Platform or ServiceNow Studio](https://servicenow-staging.fluidtopics.net/access?context=display-nap-assistant&family=zurich&ft:locale=en-US)

    -   The **Add ServiceNow Platform** drop-down menu has replaced the **Add agent experience** drop-down menu. A Now Assist panel assistant can't be added to other display experiences.
    -   In edit mode, display experiences are found within the Settings sub-tab.
[Brand an assistant](https://servicenow-staging.fluidtopics.net/access?context=brand-assistant&family=zurich&ft:locale=en-US)

    -   Minor enhancements to the look-and-feel of the standard chat preview pane.
    -   In edit mode, branding is found within the Settings sub-tab.
[Manage chat experience](https://servicenow-staging.fluidtopics.net/access?context=manage-assistant-chat-experience&family=zurich&ft:locale=en-US)

    -   A standard chat preview pane is shown for the default greeting topic \(Now Assist – Greeting\) and the default closing topic \(Now Assist – Closing\). Selecting custom topics won’t show a preview pane.
    -   Fallbacks have a standard chat preview pane and each fallback is shown if toggled on.
    -   For the Now Assist panel - Platform \(default\) assistant, web search, record producer, and custom fallback are available options. End this chat and survey are available for the standard chat experience.
    -   In edit mode, chat experience is found within the Settings sub-tab.
[Enable additional chat features](https://servicenow-staging.fluidtopics.net/access?context=additional-chat-features&family=zurich&ft:locale=en-US)

    -   Web search, response streaming, document uploads, and closed chat were moved from the Manage chat experience page to its own page. By default all chat features except web search are turned on.
    -   Response streaming can be turned on at the assistant level regardless of whether Dynamic Translation is turned on or off. However, response streaming doesn't work when Dynamic Translation is being used.
    -   In addition to web search, response streaming, document uploads, and closed chat, Now Assist panel Platform assistant has voice input. Voice input allows users to use a microphone to enter the input.
    -   In edit mode, additional chat features are found within the Settings sub-tab.
[Review settings](https://servicenow-staging.fluidtopics.net/access?context=review-assistant-settings&family=zurich&ft:locale=en-US)

    -   New sections that have been added include: Agentic support, Knowledge Graphs, Assets, and Chat features.
    -   Testing an assistant has been removed from the Review page.
[Test a chat assistant](https://servicenow-staging.fluidtopics.net/access?context=test-assistant&family=zurich&ft:locale=en-US)

    -   Test a chat assistant from **Assistant Designer** &gt; **Assistants** tab or from within each page while in edit mode.
[Edit a chat assistant](https://servicenow-staging.fluidtopics.net/access?context=edit-assistant&family=zurich&ft:locale=en-US)

    -   Edit a chat assistant from **Assistant Designer** &gt; **Assistants** tab. You will be directed through an edit flow with a slightly different UI from the create flow.
[Analyzing assistants](https://servicenow-staging.fluidtopics.net/access?context=ai-engagement-analytics&family=zurich&ft:locale=en-US)

    -   Monitor, evaluate, and optimize the performance of your AI-powered assistants within the **Analytics** tab of [Assistant Designer](https://servicenow-staging.fluidtopics.net/access?context=assistant-designer&family=zurich&ft:locale=en-US).
-   **[Copy received messages](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=zurich&ft:locale=en-US)**

Use the copy message icon in the feedback panel to copy received Virtual Agent responses.

-   **[New system properties](https://servicenow-staging.fluidtopics.net/access?context=nava-sys-props&family=zurich&ft:locale=en-US)**
    -   Set the **com.glide.cs.nass.synthesized\_response.disabled\_popover.hide** to `true` to hide the popover for disabled catalog items for Now Assist in Virtual Agent and Now Assist panel's enhanced chat.
    -   Set the **sn\_ais\_assist.enable\_pi\_in\_nba** property to `true` to allow conversational history-based suggested actions and fill multiple suggested action slot options.
    -   View the **sn\_nowassist\_va.enable\_nass\_show\_all\_options** property to decide whether to allow the **View all options** link in an enhanced chat conversation's greeting topic.
    -   The **com.glide.interactive\_view.enabled** property opens an interactive side panel view next to the chat window. The default value is `true` to activate AI Engagement Experience on your instance.
-   **[View org chart in the interactive view](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=zurich&ft:locale=en-US)**

Select **View org chart** from the people citation's popover in Now Assist panel's enhanced chat or Now Assist in Virtual Agent enhanced chat/enhanced chat's full-page experience. The person's organizational chart appears to the right of the chat conversation in an area known as the interactive view. You can switch between multiple organizational charts via a drop-down in the interactive view if you open multiple people citations' org charts in the same conversation.


-   **[Select continue or move to next task button](https://servicenow-staging.fluidtopics.net/access?context=nava-standard-chat&family=zurich&ft:locale=en-US)**

The **Continue to next task** button appears in the new **Ready to move on to your next task** card whenever multiple questions are found in a single standard chat user's message. The **Move on to the next task** citation appears at the end of an enhanced chat's synthesized response whenever multiple questions or requests are found along with an action in the user's single message. Whenever either **Continue to next task** \(standard chat\) or **Move on to the next task** \(enhanced chat\) is selected, the second question or request is reviewed and a synthesized response is sent back regarding the user's second question or request.

-   **[Multiple questions in a single user message are answered consecutively](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=zurich&ft:locale=en-US)**

Virtual Agent can answer multiple questions that were submitted in a single message query. Now Assist panel or Now Assist in Virtual Agent answers the multiple questions consecutively in a response.

-   **[Now Assist in Virtual Agent system properties](https://servicenow-staging.fluidtopics.net/access?context=nava-sys-props&family=zurich&ft:locale=en-US)**

Use **sn\_aia.use\_agents\_in\_planner** to configure AI agent discovery behavior. The default value is `true`, preferring AI agents over assets including catalogs, topics, Q&amp;A knowledge base articles, workflows, and sub-workflows. When set to `false`, there’s no preference for AI agents. AI agents and assets are treated the same.

-   **[New defaults for Now LLM Service](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Now Assist in Virtual Agent and Now Assist panel will use an upgraded Now LLM Service as the default. For more information, see the [Now LLM Service Upgrade FAQ: Everything You Need to Know About the v2.0 Model Transition \[KB2556891\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2556891) article in the Now Support Knowledge Base.


-   **[Configure additional user interface and experience options for enhanced chat](https://servicenow-staging.fluidtopics.net/access?context=ac-configure-chat-branding&family=zurich&ft:locale=en-US)**

Customize and configure the Search Toggle Button Label for enhanced chat's full-page experience. Additionally, you can configure the Enable Unread Conversation Count Display and Left Panel Header Label for enhanced chat and enhanced chat's full-page experience.

-   **[New third-party AI model provider options available for Now Assist](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[View agentic conversations processing steps](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=zurich&ft:locale=en-US)**

View agentic conversational processing steps and stop the flow, if needed.

-   **[View extended entities and records](https://servicenow-staging.fluidtopics.net/access?context=using-now-assist-in-va&family=zurich&ft:locale=en-US)**

View extended entities and records in standard and enhanced chat conversations that come from the additional custom tables associated with the Knowledge Graph Natural Language Query \(NLQ\) schema such as:

    -   Assets
    -   Incidents
    -   Recently viewed knowledge base articles
    -   Requests
    -   Tasks
-   **[View suggested queries in the portal’s search bar and chat window](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=zurich&ft:locale=en-US)**

View the most frequently asked queries in the portal’s search bar and enhanced chat’s Virtual Agent. Any search query entered into the portal’s search bar or Virtual Agent is incorporated into the greeting topic for future conversations as a suggested query. Suggested queries are only included in the Virtual Agent greeting topic whenever no promoted assets are designated.

-   **[Work with suggested queries](https://servicenow-staging.fluidtopics.net/access?context=nava-sys-props&family=zurich&ft:locale=en-US)**

Two system properties were added to enable the suggested queries feature: **sn\_nowassist\_va.enable\_suggested\_queries** and **sn\_nowassist\_va.max\_suggested\_queries**.

-   **[Configure AI search answers OneExtend capability for web search](https://servicenow-staging.fluidtopics.net/access?context=configure-ai-search-answers-capability-for-web-search&family=zurich&ft:locale=en-US)**

Configure the AI Search answers capability via `sys_one_extend_capability.list` to establish the web search AI provider and work with API keys, if needed.

-   **[Expanding AI provider support for web search](https://servicenow-staging.fluidtopics.net/access?context=configure-ai-search-answers-capability-for-web-search&family=zurich&ft:locale=en-US)**

OpenAI, Perplexity, and Google Gemini support web search.

-   **[Configuring assistants overview](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=zurich&ft:locale=en-US)**

Enhancements to Now Assist in Virtual Agent assistants and Now Assist panel Platform and Developer assistants. Options vary for Now Assist panel assistants.

[Create a chat assistant](https://servicenow-staging.fluidtopics.net/access?context=create-assistant&family=zurich&ft:locale=en-US)

    -   Configure assistants by domain.
[Select a display experience](https://servicenow-staging.fluidtopics.net/access?context=display-assistant-portal-channel&family=zurich&ft:locale=en-US)

    -   Now Assist in Virtual Agent: For mobile search widgets, enable the search bar to open into a full-page experience.
[Display assistant on Platform or ServiceNow Studio](https://servicenow-staging.fluidtopics.net/access?context=display-nap-assistant&family=zurich&ft:locale=en-US)

    -   Now Assist panel Platform assistant: Enable enhanced chat for a conversational experience that includes a dynamic, movable, and re-sizable chat window, plus access to multiple active conversations.
    -   Now Assist panel Developer assistant: Not applicable.
[Assign search sources](https://servicenow-staging.fluidtopics.net/access?context=add-info-sources-assistant&family=zurich&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Add internal and external search sources, such as catalog items and Microsoft SharePoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural Language Query schema to enable users to perform a data query during a conversation.
    -   Now Assist panel Platform assistant:
        -   Add internal and external search sources, such as catalog items and Microsoft SharePoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural Language Query schema to enable users to perform a data query during a conversation.
    -   Now Assist panel Developer assistant: Not applicable.
[Manage chat experience](https://servicenow-staging.fluidtopics.net/access?context=manage-assistant-chat-experience&family=zurich&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Select a custom greeting topic, closing topic, error topic, and survey for your assistant.
        -   Select one or more fallback options: live agent, web search, record producer, end this chat, and custom fallback.
        -   Enable the web search fallback option and web search mode to enable users to search the web from within a chat window.
    -   Now Assist panel Platform assistant:
        -   Select a custom greeting topic or error topic for your assistant.
        -   Fallback options don't apply to Now Assist panel Platform assistant.
        -   Enable web search mode to enable users to search the web from within a chat window.
    -   Now Assist panel Developer assistant: Not applicable.
-   **[Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Use the enhanced Now Assist panel for a more intuitive and personalized experience. The updated Now Assist panel is re-sizable and can be moved anywhere on the ServiceNow AI platform.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Now Assist in Virtual Agent features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Standard chat](https://servicenow-staging.fluidtopics.net/access?context=nava-standard-chat&family=xanadu&ft:locale=en-US)**

The existing Now Assist in Virtual Agent LLM conversational behavior received a terminology update and is now referred to as standard chat.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Conversational Platform Now Assist skills are active by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills&family=yokohama&ft:locale=en-US)**

The following Platform Now Assist skills are active by default and no longer visible in Now Assist Admin console:

    -   Now Assist Multi-Turn Catalog Ordering
    -   Now Assist Q&amp;A Genius Results
    -   Now Assist Topics
    -   Subflows and actions
    -   Custom skills
    -   AI agents

-   **[Additional fallback options](https://servicenow-staging.fluidtopics.net/access?context=using-now-assist-in-va&family=yokohama&ft:locale=en-US)**

There are up to five fallback options that can be presented to end users:

    -   **Search the web**: Triggers web search mode and uses the internet to search for the results.

**Note:** Only the last query entered into the conversation is considered when entering web search mode via the fallback option.

    -   **Request a live chat**: Triggers live agent mode and routes you to a human support representative.
    -   **Create a generic ticket**: Creates a record.
    -   **End this chat**: Ends the chat.

**Note:** This option is only available to standard chat conversations.

    -   **Custom fallback option**: Presents a fallback Virtual Agent topic.
-   **[Web search mode enhancements](https://servicenow-staging.fluidtopics.net/access?context=web-search-requestor&family=yokohama&ft:locale=en-US)**

Manually enter into web search mode via the input bar for standard and enhanced chat conversations. Web search mode includes in-line citations and the associated sources. A web search mode banner appears in enhanced chat conversations that end users can use to end the mode.

-   **[Profanity recognition response](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=yokohama&ft:locale=en-US)**

If Now Assist Guardian is enabled and the end user's request contains profane content, the Virtual Agent responds with a message prompt to re-enter an appropriate request without profanity or offensive content.


-   **[Standard chat](https://servicenow-staging.fluidtopics.net/access?context=nava-standard-chat&family=yokohama&ft:locale=en-US)**

The existing Now Assist in Virtual Agent LLM conversational behavior received a terminology update and is now referred to as standard chat.


-   **[Dynamic Translation calls](https://servicenow-staging.fluidtopics.net/access?context=translation-for-now-assist&family=yokohama&ft:locale=en-US)**

If native translation is enabled, a Dynamic Translation call is only made if an unsupported language for native translation is used.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**




-   **[Conversational Platform Now Assist skills are active by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills&family=zurich&ft:locale=en-US)**

The following Platform Now Assist skills are active by default and no longer visible in Now Assist Admin console:

    -   Now Assist Multi-Turn Catalog Ordering
    -   Now Assist Q&amp;A Genius Results
    -   Now Assist Topics
    -   Subflows and actions
    -   Custom skills
    -   AI agents

-   **[Additional fallback options](https://servicenow-staging.fluidtopics.net/access?context=using-now-assist-in-va&family=zurich&ft:locale=en-US)**

There are up to five fallback options that can be presented to end users:

    -   **Search the web**: Triggers web search mode and uses the internet to search for the results.

**Note:** Only the last query entered into the conversation is considered when entering web search mode via the fallback option.

    -   **Request a live chat**: Triggers live agent mode and routes you to a human support representative.
    -   **Create a generic ticket**: Creates a record.
    -   **End this chat**: Ends the chat.

**Note:** This option is only available to standard chat conversations.

    -   **Custom fallback option**: Presents a fallback Virtual Agent topic.
-   **[Web search mode enhancements](https://servicenow-staging.fluidtopics.net/access?context=web-search-requestor&family=zurich&ft:locale=en-US)**

Manually enter into web search mode via the input bar for standard and enhanced chat conversations. Web search mode includes in-line citations and the associated sources. A web search mode banner appears in enhanced chat conversations that end users can use to end the mode.

-   **[Profanity recognition response](https://servicenow-staging.fluidtopics.net/access?context=nava-enhanced-chat&family=zurich&ft:locale=en-US)**

If Now Assist Guardian is enabled and the end user's request contains profane content, the Virtual Agent responds with a message prompt to re-enter an appropriate request without profanity or offensive content.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Now Assist in Virtual Agent features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Now Assist in Virtual Agent features or functionality were deprecated.

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

-   In Patch 11, **sn\_aia.use\_agents\_in\_planner** system property has been removed. The system property was used for configuring AI agent discovery behavior.
-   In Patch 11, Now Assist skills page in the assistant admin guided setup has been removed due to the skills being turned on by default.
-   In Patch 6, Bing support for the searching and scraping search result type is no longer supported when adding a web search tool in Now Assist Skill Kit.
-   In Patch 4, support for Now Assist in Conversational IVR was removed.

</td></tr><tr><td>

Zurich

</td><td>

-   In Patch 4, **sn\_aia.use\_agents\_in\_planner** system property has been removed. The system property was used for configuring AI agent discovery behavior.
-   In Patch 4, Now Assist skills page in the assistant admin guided setup has been removed due to the skills being turned on by default.
-   In Patch 1, Bing support for the searching and scraping search result type is no longer supported when adding a web search tool in Now Assist Skill Kit.

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

-   [Now Assist for Accounts Payable Operations \(APO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-apo&family=xanadu&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-landing-cmdb&family=xanadu&ft:locale=en-US)
-   [Now Assist for Creator](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-creator-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-csm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-fsm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-financial-services-operations&family=xanadu&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://servicenow-staging.fluidtopics.net/access?context=now-assist-hs-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-hrsd&family=xanadu&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-itom&family=xanadu&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-itsm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-lsd-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for PSDS](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-psds&family=xanadu&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://servicenow-staging.fluidtopics.net/access?context=now-assist-security-incident-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-slo&family=xanadu&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spo&family=xanadu&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spmc&family=xanadu&ft:locale=en-US)

For more information, see [Configuring Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

**Note:** When you upgrade to Yokohama Patch 8 or later, agentic AI is the primary orchestration in Virtual Agent. For more information about agentic AI, see [Agentic conversations in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=agentic-conversations-vad&family=yokohama&ft:locale=en-US).

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following products are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-apo&family=yokohama&ft:locale=en-US)
-   [Now Assist for App Engine](https://servicenow-staging.fluidtopics.net/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&family=yokohama&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-landing-cmdb&family=yokohama&ft:locale=en-US)
-   [Now Assist for CWM](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-cwm-landing&family=yokohama&ft:locale=en-US)
-   [Now Assist for Creator](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-creator-landing&family=yokohama&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-csm&family=yokohama&ft:locale=en-US)
-   [Now Assist for Employee Experience](https://servicenow-staging.fluidtopics.net/access?context=now-assisit-employee-exp&family=yokohama&ft:locale=en-US)
-   [Now Assist for Enterprise Architecture \(EA\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-ea&family=yokohama&ft:locale=en-US)
-   [Now Assist](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-esg&family=yokohama&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-fsm&family=yokohama&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-financial-services-operations&family=yokohama&ft:locale=en-US)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-ham&family=yokohama&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://servicenow-staging.fluidtopics.net/access?context=now-assist-hs-landing&family=yokohama&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-hrsd&family=yokohama&ft:locale=en-US)
-   [Now Assist](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-irm&family=yokohama&ft:locale=en-US)
-   [Now Assist for ITOM](https://servicenow-staging.fluidtopics.net/access?context=now-assist-itom&family=yokohama&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-itsm&family=yokohama&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-lsd-landing&family=yokohama&ft:locale=en-US)
-   [Now Assist for Operational Technology Manager \(OTM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-otm-landing&family=yokohama&ft:locale=en-US)
-   [Now Assist for Order Management](https://servicenow-staging.fluidtopics.net/access?context=now-assist-order-management&family=yokohama&ft:locale=en-US)
-   [Now Assist for PSDS](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-psds&family=yokohama&ft:locale=en-US)
-   [Now Assist for SOM](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-sales-and-order-management-som&family=yokohama&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://servicenow-staging.fluidtopics.net/access?context=now-assist-security-incident-landing&family=yokohama&ft:locale=en-US)
-   [Now Assist for Software Asset Management \(SAM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-sam&family=yokohama&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-slo&family=yokohama&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spo&family=yokohama&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spm&family=yokohama&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spmc&family=yokohama&ft:locale=en-US)
-   [Now Assist](https://servicenow-staging.fluidtopics.net/access?context=now-assist-tprm&family=yokohama&ft:locale=en-US)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-wsd-landing&family=yokohama&ft:locale=en-US)
-   [Now Assist for Vulnerability Response](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-vulnerability-response-landing&family=yokohama&ft:locale=en-US)

 For more information, see [Configuring assistants overview](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

**Note:** When you upgrade to Zurich Patch 2 or later, agentic AI is the primary orchestration in Virtual Agent. For more information about agentic AI, see [Agentic conversations in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=agentic-conversations-vad&family=zurich&ft:locale=en-US).

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following products are available:

-   
 For more information, see [Configuring assistants overview](https://servicenow-staging.fluidtopics.net/access?context=configure-now-assist-va&family=zurich&ft:locale=en-US).

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

[Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=now-assist-in-va-landing&family=xanadu&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.

</td></tr><tr><td>

Yokohama

</td><td>

[Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=now-assist-in-va-landing&family=yokohama&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.

</td></tr><tr><td>

Zurich

</td><td>

[Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=now-assist-in-va-landing&family=zurich&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.

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

Now Assist in Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Now Assist in Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Now Assist in Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=zurich&ft:locale=en-US).

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

-   ****

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

[Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-overview&family=xanadu&ft:locale=en-US) is supported in Now Assist Virtual Agent conversations. For details, see [Enable translation for Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=enable-dynamic-translation-for-now-assist-applications&family=xanadu&ft:locale=en-US) and [Localization options for Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=multi-language-options-va&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

[Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-overview&family=yokohama&ft:locale=en-US) is supported for non-streaming Now Assist Virtual Agent conversations. For details, see [Configure multilingual service for Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=enable-dynamic-translation-for-now-assist-applications&family=yokohama&ft:locale=en-US) and [Using language detection and dynamic machine translation in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=dynamic-lang-detection-translation&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

[Dynamic Translation](https://servicenow-staging.fluidtopics.net/access?context=dynamic-translation-overview&family=zurich&ft:locale=en-US) is supported for non-streaming Now Assist Virtual Agent conversations. For details, see [Configure multilingual service for Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=enable-dynamic-translation-for-now-assist-applications&family=zurich&ft:locale=en-US), [Language detection and dynamic translation in enhanced chat](https://servicenow-staging.fluidtopics.net/access?context=dynamic-lang-detection-translation-enhanced-chat&family=zurich&ft:locale=en-US), and [Language detection and dynamic translation in standard chat](https://servicenow-staging.fluidtopics.net/access?context=dynamic-lang-detection-translation-standard-chat-nlu&family=zurich&ft:locale=en-US).

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

[Xanadu Patch 9](https://servicenow-staging.fluidtopics.net/access?context=xanadu-patch-9&family=xanadu&ft:locale=en-US)

-   Use enhanced chat to provide users with a conversational experience within a resizable and movable chat window that includes the ability to have multiple active conversations. Enhanced chat enables users to choose their way of engaging with Now Assist on their ServiceNow portals from a variety of entry points. Enhanced chat includes synthesized responses after entering a search query into a portal's search bar. If Now Assist in AI Search is turned on, enhanced chat also offers an optional full-page experience where your users can enter into a full-page chat experience after entering a search query into a portal's search bar. Enhanced chat also offers an updated, modern look and feel along with chat controls to resize and move the chat window.
-   View an expanded list of inline citations for both standard and enhanced chat. New inline citations for external content and people searches are available.
-   View and work with suggested actions after completing an action in Now Assist in Virtual Agent.
-   Stream responses for Now Assist LLM - enhanced chat conversations.
-   Upload or drag documents and images into a standard or enhanced chat.
-   Automatically switch to the user's detected language in enhanced chat conversations when language detection is turned on.
-   Enable pinning a chat window on a portal by using the **sn\_nowassist\_va.enhanced\_chat\_pin\_enabled.&lt;portal-url&gt;** system property.

 [Xanadu Patch 7](https://servicenow-staging.fluidtopics.net/access?context=xanadu-patch-7&family=xanadu&ft:locale=en-US)

-   Stream responses for Now Assist LLM chat conversations.

 [Xanadu Patch 3](https://servicenow-staging.fluidtopics.net/access?context=xanadu-patch-3&family=xanadu&ft:locale=en-US)

-   Run actions from a conversation.
-   Run subflows from a conversation.
-   Use an updated Virtual Agent Designer list-based home page that includes conversational subflows and actions.
-   Use language detection and engage in small talk within LLM conversations.
-   Link primary assistants with secondary assistants to use search sources from secondary assistants.
-   Use language detection and engage in small talk within LLM conversations.
-   Receive a synthesized response for Now Assist in Virtual Agent users.

 [Xanadu Patch 1](https://servicenow-staging.fluidtopics.net/access?context=xanadu-patch-1&family=xanadu&ft:locale=en-US)

-   Enhancements to the Now Assist in Virtual Agent admin guided setup.

See [Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=now-assist-in-va-landing&family=xanadu&ft:locale=en-US) for more information.


</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   View a people citation's org chart in the interactive view. The interactive view opens to the right of the chat conversation area.
-   Notice several UI improvements to enhanced chat and enhanced chat's full-page experience, including an updated input bar, gradient borders, copy message icon for received messages, and more.
-   Enable voice input to allow users to use a microphone to type the input. Voice input is only available for Now Assist panel Platform assistant.

 [Yokohama Patch 6](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Use agentic conversations and view agentic conversational processing flow steps.
-   View extended entities and records in standard and enhanced chat conversations if they’re associated with the Knowledge Graph natural language query \(NLQ\) schema.
-   View suggested search queries previously performed in the portal's search bar within enhanced chat conversations.
-   Work with the simplified subheader of enhanced chat.
-   Delete closed enhanced chat conversations.
-   Expand the fallback options.
-   Enter into web search mode manually via the input bar.

 [Yokohama Patch 3](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   Use enhanced chat to provide users with a conversational experience within a resizable and movable chat window that includes the ability to have multiple active conversations. Enhanced chat enables users to choose their way of engaging with Now Assist on their ServiceNow portals from a variety of entry points. Enhanced chat includes synthesized responses after entering a search query into a portal's search bar. If Now Assist in AI Search is turned on, enhanced chat also offers an optional full-page experience where your users can enter into a full-page chat experience after entering a search query into a portal's search bar. Enhanced chat also offers an updated, modern look and feel along with chat controls to resize and move the chat window.
-   View an expanded list of inline citations for both standard and enhanced chat. New inline citations for external content and people searches are available.
-   View and work with suggested actions after completing an action in Now Assist in Virtual Agent.
-   Stream responses for Now Assist LLM - enhanced chat conversations.
-   Upload or drag documents and images into a standard or enhanced chat.
-   Automatically switch to the user's detected language in enhanced chat conversations when language detection is turned on.
-   Use the Web Search custom skill to search for an answer on the internet.

 [Yokohama Patch 1](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-1&family=yokohama&ft:locale=en-US)

-   Stream responses for Now Assist LLM chat conversations.

 See [Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=now-assist-in-va-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 5](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Japanese language support for voice assistants enables Japanese-speaking users to experience natural, culturally appropriate interactions with AI voice agents.

 [Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   View a people citation's org chart in the interactive view. The interactive view opens to the right of the chat conversation area.
-   Notice several UI improvements to enhanced chat and enhanced chat's full-page experience, including an updated input bar, gradient borders, copy message icon for received messages, and more.
-   Enable voice input to allow users to use a microphone to type the input. Voice input is only available for Now Assist panel Platform assistant.

 [Zurich Patch 1](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Use agentic conversations and view agentic conversational processing flow steps.
-   View extended entities and records in standard and enhanced chat conversations if they’re associated with the Knowledge Graph Natural Language Query \(NLQ\) schema.
-   View suggested search queries previously performed in the portal's search bar within enhanced chat conversations.
-   Work with the simplified subheader of enhanced chat.
-   Delete closed enhanced chat conversations.
-   Expand the fallback options.
-   Enter into web search mode manually via the input bar.

 See [Now Assist in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=now-assist-in-va-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

