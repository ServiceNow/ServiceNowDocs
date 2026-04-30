---
title: Now Assist in Virtual Agent release notes
description: The ServiceNow Now Assist in Virtual Agent application uses generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses large language models \(LLMs\) to create a natural-language conversational experience that can improve the success of your self-service workflows. Now Assist in Virtual Agent was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 12
---

# Now Assist in Virtual Agent release notes

The ServiceNow® Now Assist in Virtual Agent application uses generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses large language models \(LLMs\) to create a natural-language conversational experience that can improve the success of your self-service workflows. Now Assist in Virtual Agent was enhanced and updated in the Xanadu release.

## Now Assist in Virtual Agent highlights for the Xanadu release

[Xanadu Patch 9](../quality/xanadu-patch-9.md)

-   Use enhanced chat to provide users with a conversational experience within a resizable and movable chat window that includes the ability to have multiple active conversations. Enhanced chat enables users to choose their way of engaging with Now Assist on their ServiceNow portals from a variety of entry points. Enhanced chat includes synthesized responses after entering a search query into a portal's search bar. If Now Assist in AI Search is turned on, enhanced chat also offers an optional full-page experience where your users can enter into a full-page chat experience after entering a search query into a portal's search bar. Enhanced chat also offers an updated, modern look and feel along with chat controls to resize and move the chat window.
-   View an expanded list of inline citations for both standard and enhanced chat. New inline citations for external content and people searches are available.
-   View and work with suggested actions after completing an action in Now Assist in Virtual Agent.
-   Stream responses for Now Assist LLM - enhanced chat conversations.
-   Upload or drag documents and images into a standard or enhanced chat.
-   Automatically switch to the user's detected language in enhanced chat conversations when language detection is turned on.
-   Enable pinning a chat window on a portal by using the **sn\_nowassist\_va.enhanced\_chat\_pin\_enabled.&lt;portal-url&gt;** system property.

[Xanadu Patch 7](../quality/xanadu-patch-7.md)

-   Stream responses for Now Assist LLM chat conversations.

[Xanadu Patch 3](../quality/xanadu-patch-3.md)

-   Run actions from a conversation.
-   Run subflows from a conversation.
-   Use an updated Virtual Agent Designer list-based home page that includes conversational subflows and actions.
-   Use language detection and engage in small talk within LLM conversations.
-   Link primary assistants with secondary assistants to use search sources from secondary assistants.
-   Use language detection and engage in small talk within LLM conversations.
-   Receive a synthesized response for Now Assist in Virtual Agent users.

[Xanadu Patch 1](../quality/xanadu-patch-1.md)

-   Enhancements to the Now Assist in Virtual Agent admin guided setup.

    See [Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) for more information.


## New in the Xanadu release

-   **[Use enhanced chat](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Enhanced chat is a conversational support experience within a resizable and moveable window that also includes the ability to have multiple active conversations and superior search capabilities. Using enhanced chat's full-page experience further intertwines chat and search capabilities by redirecting users into a full-page chat after entering a query into a portal's search bar.

-   **[View inline citations](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

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

-   **[Use suggested actions](https://www.servicenow.com/docs/access?context=suggested-actions&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    View suggested actions that were related to your prior conversation and that you consider doing next. After completing a conversational catalog request, conversational subflow, or Virtual Agent topic, two suggested actions appear after a `Here's what you can do next` header.

-   **[Stream enhanced chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Use language detection to automatically switch the conversational language for enhanced chat conversations](https://www.servicenow.com/docs/access?context=dynamic-lang-detection-translation-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Automatically switch the conversational language to the user's detected language during LLM enhanced chat conversations when language detection is turned on. This automatic switch can occur when a user enters an utterance at the start of a new conversation or within the portal home page’s search field.

-   **[Recognize the Boolean user input control during dynamic translation](https://www.servicenow.com/docs/access?context=multi-language-options-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Recognize the Boolean user input control in chat conversations during dynamic translation.

-   **[Adjust Shorten responses toggle to impact Show more option in chat](https://www.servicenow.com/docs/access?context=va-text-response&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    For bot text responses, adjust the **Shorten responses** toggle in Virtual Agent Designer to turn off the **Show more** option on the user side. When **Shorten responses** is turned off, the **Show more** option does not appear in the chat to the user and the full answer is displayed rather than a truncated response.

-   **[Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    In addition to configuring Now Assist in Virtual Agent assistants, admins can configure the default Now Assist panel assistants. Options may vary for Now Assist panel assistants.

    [Create an assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

    -   If multiple assistants are created, users can chat simultaneously with multiple assistants. Conversations are independent from each other.
    -   Turn on or off Now Assist panel \(agent or creator\) assistant. Contact support to configure Now Assist panel assistants.
    [Assign Now Assist skills to an assistant](https://www.servicenow.com/docs/access?context=assign-na-skills-assistant&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

    -   Now Assist Topic skill must be turned on at the assistant level for document uploads to be activated when managing the chat experience. For more information, see [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).
    -   Create and manage agentic workflows in Now Assist AI Agents Studio and assign the workflows to the assistant.
    [Display your assistant on a portal or channel](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

    -   Display Now Assist in Virtual Agent enhanced chat, with or without the full-page experience, on your portal or mobile app. This dynamic window includes the ability to have multiple active conversations and search capabilities. To use enhanced chat, portals and mobile apps require AI Search to be enabled. For more information on the prerequisites, see [Portal prerequisites for enhanced chat](https://www.servicenow.com/docs/access?context=prerequisites-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) and [Mobile app prerequisites for enhanced chat](https://www.servicenow.com/docs/access?context=mobile-prereqs-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).
    [Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

    -   Upload documents to Now Assist in Virtual Agent standard chat or enhanced chat experience. The Now Assist topics skill must be enabled in Now Assist skills. For more information on file formats, see [Upload documents in Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).
    [Review assistant settings](https://www.servicenow.com/docs/access?context=review-assistant-settings&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

    -   Document uploads appear as active if it's turned on when managing the chat experience.
-   **[Upload documents in Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Upload or drag and drop files to Now Assist in Virtual Agent \(standard chat or enhanced chat\). The assistant analyzes and understands the content of the files, and a user can ask questions about the content of the files or get a summary.

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Enable suggested actions in Now Assist in Virtual Agent so that users are offered options for what they can do after completing a prior action. Suggested actions is applicable to standard and enhanced chat, mobile, and Microsoft Teams.


-   **[Stream chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.


-   **[Use Now Assist to call Microsoft Active Directory v2 actions](https://www.servicenow.com/docs/access?context=ms-ad-v2-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Install Now Assist for Conversational Spokes plugin and start utilizing the conversational ability of the Look up User spoke action. You can call this action from a conversational interface like Now Assist.

-   **[Run an action from a conversation](https://www.servicenow.com/docs/access?context=conversational-actions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational action from Workflow Studio. View and edit conversational actions within Virtual Agent Designer.

-   **[Run a subflow from a conversation](https://www.servicenow.com/docs/access?context=conversational-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Run a Workflow Studio subflow from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio. View and edit conversational subflows within Virtual Agent Designer.

-   **[AI generated topic description message within topic migration](https://www.servicenow.com/docs/access?context=migrate-nlu-llm&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    A `Topic description generated by Now Assist` message now appears near the **Topic Description** field during the topic migration's Review descriptions step.

-   **[Small talk for LLM conversations](https://www.servicenow.com/docs/access?context=create-small-talk&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Use small talk in LLM conversations for greetings and farewells along with gratitude and complaint statements. A Semantic Filtering Framework \(SFF\) detects small talk and generates an appropriate response.

-   **[Language detection for LLM conversations](https://www.servicenow.com/docs/access?context=multi-language-options-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Use language detection for your LLM conversations to improve your user's experience.

-   **[Virtual Agent Designer home page](https://www.servicenow.com/docs/access?context=vad-topics-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    A new list-based Virtual Agent Designer home page appears for users who have activated Now Assist in Virtual Agent and the Agent assist Topics skill. The card-based UI is still available for those users who use only NLU/keyword or Virtual Agent Lite.

-   **[Virtual Agent Designer user input controls](https://www.servicenow.com/docs/access?context=va-user-inputs&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Updates to LLM user inputs include:

    -   Use the Validation toggle in the Advanced section of User Inputs to confirm user input values by scripts.
    -   Use the Allow slot filling toggle on User Inputs to switch between static \(single field\) and dynamic \(define with scripts or data pill picker\) detail description modes.
    -   Get a message that a mandatory field cannot be skipped when you attempt to skip a user input with conditions not set to be skippable.
-   **[Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Updates to the admin guided setup include:

    -   Enhance functionality and efficiency of your Virtual Agent by linking primary assistants to secondary assistants, enabling a primary assistant to use search sources from secondary assistants.
    -   View the relationship between primary and secondary assistants within a map view.
    -   Select portals and mobile applications to display Virtual Agents.
    -   Create conversational subflows and actions by launching Workflow Studio to make conversational subflows and actions available to the assistant.
-   **[Synthesized response](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    For Now Assist in Virtual Agent users, a synthesized response can appear. A synthesized response includes a brief summary of the requested information and search results along with Genius Results. Mid-topic switching can occur during a conversation with synthesized response. Users can continue with their original request or switch the conversation's focus.

-   **[New system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The following system property was added to increase flexibility of the search results and response:

    -   **sn\_nowassist\_va.synthesized\_autostart\_items**: When synthesized response only returns a singular action, configure whether to directly launch into that action. By default, whenever synthesized response returns a single Virtual Agent topic, that action is auto-launched. The following actions can be configured to auto-launch:
        -   Synthesized response returns a single conversational catalog item.
        -   Synthesized response returns a single Virtual Agent topic, along with Knowledge Base information.
        -   Synthesized response returns a single conversational catalog item, along with Knowledge Base information.

-   **[Delete virtual agents](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Delete a Virtual Agent from the assistants list.

-   **[Support virtual agents on a portal](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Allow public availability of an LLM-based Virtual Agent on a portal.

-   **[Display a virtual agent in a channel](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Integrate your preferred messaging channels to display your Virtual Agent.

-   **[Install proactive triggers](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Install Proactive Triggers from within the Review page.

-   **[Support notifications in virtual agents](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Support actionable and non-actionable notifications for LLM conversations in Virtual Agent.


## UI changes

-   **[UI chat updates](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**
    -   The summary card in a Now Assist in Virtual Agent conversation was updated to a more modern look and feel.
    -   The default chat widget button for enhanced chat and standard chat now differs on the portal.
    -   An Ask Now Assist header now appears with suggested searches in a drop-down on the portal's search bar.
    -   The Boolean choice, static choice, and dynamic choice controls were updated to a more modern look and feel for requesters.

-   **[UI chat updates](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**
    -   The `New messages below` button in Virtual Agent was replaced with a simplified down-arrow indicator.
    -   The `New messages above` button was deprecated because Virtual Agent now auto-scrolls to the top of the oldest new message.
    -   Input text bar was updated to a more modern look and feel.
    -   The start a new conversation icon was updated.

## Changed in this release

-   **[Standard chat](https://www.servicenow.com/docs/access?context=nava-standard-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    The existing Now Assist in Virtual Agent LLM conversational behavior received a terminology update and is now referred to as standard chat.


## Activation information

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)
-   [Now Assist for PSDS](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=xanadu&pubname=xanadu-government-industry&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=xanadu&pubname=xanadu-telecom-media-technology&ft:locale=en-US)

For more information, see [Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Additional requirements

[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US) requires a license for Virtual Agent and at least one Now Assist product.

## Browser requirements

Now Assist in Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Localization information

[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) is supported in Now Assist Virtual Agent conversations. For details, see [Enable translation for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) and [Localization options for Virtual Agent](https://www.servicenow.com/docs/access?context=multi-language-options-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    ServiceNow® Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The Now Assist in AI Search ServiceNow® Store application combines the power of search with the Now LLM Service generative AI model to answer questions in user searches with actionable AI-generated summaries of relevant Knowledge articles.

-   **[Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    Unlock your enterprise productivity with ServiceNow® Virtual Agent. Increase deflections by empowering your employees and customers to serve themselves using a friendly messaging interface, featuring prebuilt conversations powered by artificial intelligence.

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Consolidate workflow authoring, configuring, and monitoring into a single page experience. Create and manage playbooks, flows, actions, decision tables, and integrations from one design environment.


**Parent Topic:**[Conversational Interfaces release notes](../conversational-interfaces/conversational-interfaces-rn-landing.md)

**Parent Topic:**[Now Assist release notes](../now-assist/now-assist-rn-landing.md)

