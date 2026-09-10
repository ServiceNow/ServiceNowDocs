---
title: Combined Now Assist in Virtual Agent release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Now Assist in Virtual Agent from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-nowassistinvirtualagent-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 20
breadcrumb: [Products combined by family]
---

# Combined Now Assist in Virtual Agent release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Now Assist in Virtual Agent from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist in Virtual Agent release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist in Virtual Agent to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Now Assist in Virtual Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Stream chat responses](https://www.servicenow.com/docs/access?context=streaming-responses-requestor&family=yokohama&ft:locale=en-US)**

Stream LLM response messages as they’re generated instead of the response text appearing all at once to end users. Responses stream in either one letter or one word at a time.

-   **[Benefit from Knowledge Graph integration](https://www.servicenow.com/docs/access?context=exploring-knowledge-graph&family=yokohama&ft:locale=en-US)**

Receive fewer Virtual Agent slot-fill questions during conversations whenever Knowledge Graph is activated.

-   **[Receive personalized synthesized response answers with Knowledge Graph integration](https://www.servicenow.com/docs/access?context=access-knowledge-graph-designer&family=yokohama&ft:locale=en-US)**

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
-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=yokohama&ft:locale=en-US)'**

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
-   **[Using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&family=yokohama&ft:locale=en-US)**

Search through external content connections such as Microsoft SharePoint or Confluence if external search sources are added to information sources when [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=yokohama&ft:locale=en-US).Select an inline citation to show a popover containing a link to an article or source, or a description and action to start a request.Citations with an action are shown after a second clarifying question from Virtual Agent.Change the order of the fallback and revisit options in the **View more options** results list that appears in the synthesized response. Use the **sn\_nowassist\_va.synth\_response\_revisit\_position** system property with either the **BEFORE\_FALLBACK** or **AFTER\_FALLBACK** values.Show or hide the **Need more help** button in the synthesized response by using the **show\_view\_more\_for\_synthesized** system property.Turn on or off regular results in Virtual Agent from the following Now Assist Search Results Output Types table using the parameter **now\_assist\_va\_search\_results\_output\_type.list** parameter.Use prechat and postchat surveys with GPT4o and LLAMA. Users can select data pills or enter strings for responses.Use new prebuilt topics for prechat and postchat surveys in LLM conversations.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Configure additional user interface and experience options for enhanced chat](https://www.servicenow.com/docs/access?context=ac-configure-chat-branding&family=zurich&ft:locale=en-US)**

Customize and configure the Search Toggle Button Label for enhanced chat's full-page experience. Additionally, you can configure the Enable Unread Conversation Count Display and Left Panel Header Label for enhanced chat and enhanced chat's full-page experience.

-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[View agentic conversations processing steps](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&family=zurich&ft:locale=en-US)**

View agentic conversational processing steps and stop the flow, if needed.

-   **[View extended entities and records](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&family=zurich&ft:locale=en-US)**

View extended entities and records in standard and enhanced chat conversations that come from the additional custom tables associated with the Knowledge Graph Natural Language Query \(NLQ\) schema such as:

    -   Assets
    -   Incidents
    -   Recently viewed knowledge base articles
    -   Requests
    -   Tasks
-   **[View suggested queries in the portal’s search bar and chat window](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&family=zurich&ft:locale=en-US)**

View the most frequently asked queries in the portal’s search bar and enhanced chat’s Virtual Agent. Any search query entered into the portal’s search bar or Virtual Agent is incorporated into the greeting topic for future conversations as a suggested query. Suggested queries are only included in the Virtual Agent greeting topic whenever no promoted assets are designated.

-   **[Work with suggested queries](https://www.servicenow.com/docs/access?context=nava-sys-props&family=zurich&ft:locale=en-US)**

Two system properties were added to enable the suggested queries feature: **sn\_nowassist\_va.enable\_suggested\_queries** and **sn\_nowassist\_va.max\_suggested\_queries**.

-   **[Configure AI search answers OneExtend capability for web search](https://www.servicenow.com/docs/access?context=configure-ai-search-answers-capability-for-web-search&family=zurich&ft:locale=en-US)**

Configure the AI Search answers capability via `sys_one_extend_capability.list` to establish the web search AI provider and work with API keys, if needed.

-   **[Expanding AI provider support for web search](https://www.servicenow.com/docs/access?context=configure-ai-search-answers-capability-for-web-search&family=zurich&ft:locale=en-US)**

OpenAI, Perplexity, and Google Gemini support web search.

-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=zurich&ft:locale=en-US)**

Enhancements to Now Assist in Virtual Agent assistants and Now Assist panel Platform and Developer assistants. Options vary for Now Assist panel assistants.

[Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&family=zurich&ft:locale=en-US)

    -   Configure assistants by domain.


    -   Now Assist in Virtual Agent assistants: By default, all global skill types are turned on in Now Assist Admin console.
    -   Now Assist panel Platform assistant: By default, all global skill types, except for Catalog skill, are turned on in Now Assist Admin console.
    -   Now Assist panel Developer assistant: By default, Now Assist Topic skill is turned on in Now Assist Admin console. No other skills are available for the Now Assist panel Developer assistant.
[Select a display experience](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&family=zurich&ft:locale=en-US)

    -   Now Assist in Virtual Agent: For mobile search widgets, enable the search bar to open into a full-page experience.
[Display assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&family=zurich&ft:locale=en-US)

    -   Now Assist panel Platform assistant: Enable enhanced chat for a conversational experience that includes a dynamic, movable, and resizable chat window, plus access to multiple active conversations.
    -   Now Assist panel Developer assistant: Not applicable.
[Assign search sources](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&family=zurich&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Add internal and external search sources, such as catalog items and Microsoft SharePoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural Language Query schema to enable users to perform a data query during a conversation.
    -   Now Assist panel Platform assistant:
        -   Add internal and external search sources, such as catalog items and Microsoft SharePoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural Language Query schema to enable users to perform a data query during a conversation.
    -   Now Assist panel Developer assistant: Not applicable.
[Manage chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&family=zurich&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Select a custom greeting topic, closing topic, error topic, and survey for your assistant.
        -   Select one or more fallback options: live agent, web search, record producer, end this chat, and custom fallback.
        -   Enable the web search fallback option and web search mode to enable users to search the web from within a chat window.
    -   Now Assist panel Platform assistant:
        -   Select a custom greeting topic or error topic for your assistant.
        -   Fallback options don't apply to Now Assist panel Platform assistant.
        -   Enable web search mode to enable users to search the web from within a chat window.
    -   Now Assist panel Developer assistant: Not applicable.
-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Use the enhanced Now Assist panel for a more intuitive and personalized experience. The updated Now Assist panel is resizable and can be moved anywhere on the ServiceNow AI platform.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Now Assist in Virtual Agent features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[UI chat updates](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&family=yokohama&ft:locale=en-US)**
    -   The **New messages below** button in Virtual Agent was replaced with a simplified down-arrow indicator.
    -   The **New messages above** button was deprecated because Virtual Agent now auto-scrolls to the top of the oldest new message.
    -   The Input text bar was updated to a more modern look and feel.
    -   The start a new conversation icon was updated.

</td></tr><tr><td>

Zurich

</td><td>

-   **[UI chat updates](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&family=zurich&ft:locale=en-US)**
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

-   **[UI admin guided setup updates](https://www.servicenow.com/docs/access?context=configure-now-assist-va&family=zurich&ft:locale=en-US)**
    -   The **Manage search profile** button replaces the search profile text link.
    -   The Add external search sources drop-down list has been replaced with the Add search sources drop-down list to include internal and external search sources.
    -   The simple and advanced views within the Chat experience page are consolidated into a single view.
    -   The **Copy existing configuration** button is featured more prominently, and it's shown with information about its use.

 -   **[Additional fallback options](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&family=zurich&ft:locale=en-US)**

There are up to five fallback options that can be presented to end users:

    -   **Search the web**: Triggers web search mode and uses the internet to search for the results.

**Note:** Only the last query entered into the conversation is considered when entering web search mode via the fallback option.

    -   **Request a live chat**: Triggers live agent mode and routes you to a human support representative.
    -   **Create a generic ticket**: Creates a record.
    -   **End this chat**: Ends the chat.

**Note:** This option is only available to standard chat conversations.

    -   **Custom fallback option**: Presents a fallback Virtual Agent topic.
-   **[Web search mode enhancements](https://www.servicenow.com/docs/access?context=web-search-requestor&family=zurich&ft:locale=en-US)**

Manually enter into web search mode via the input bar for standard and enhanced chat conversations. Web search mode includes in-line citations and the associated sources. A web search mode banner appears in enhanced chat conversations that end users can use to end the mode.

-   **[Profanity recognition response](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&family=zurich&ft:locale=en-US)**

If AI Guardian is enabled and the end user's request contains profane content, the Virtual Agent responds with a message prompt to re-enter an appropriate request without profanity or offensive content.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Now Assist in Virtual Agent features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Now Assist in Virtual Agent features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   In Patch 6, Bing support for the searching and scraping search result type is no longer supported when adding a web search tool in Now Assist Skill Kit.
-   In Patch 4, support for Now Assist in Conversational IVR was removed.

</td></tr><tr><td>

Zurich

</td><td>

-   In Patch 1, Bing support for the searching and scraping search result type is no longer supported when adding a web search tool in AI Skill Kit.

</td></tr><tr><td>

Australia

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

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist in Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist in Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Now Assist in Virtual Agent, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist in Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist in Virtual Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

