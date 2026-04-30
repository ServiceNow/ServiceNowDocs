---
title: Virtual Agent release notes
description: The ServiceNow Virtual Agent application provides user assistance through a conversational interface so that you can design and build automated conversations that help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-06-16"
reading_time_minutes: 7
---

# Virtual Agent release notes

The ServiceNow® Virtual Agent application provides user assistance through a conversational interface so that you can design and build automated conversations that help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Yokohama release.

## Virtual Agent highlights for the Yokohama release

[Yokohama Patch 7](../quality/yokohama-patch-11.md)

-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Start the create flow for all supported conversational assets directly from Virtual Agent Designer.
-   Enhance the user experience with Slack response message streaming capability.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   View people information in the synthesized response along with people citation when you search a person in Microsoft Teams chat.
-   AI agent support for Virtual Agent.
-   View AI agents and agentic workflows in Virtual Agent Designer.
-   Select AI agents to handle tasks in the AI Connector utility. See [AI Connector utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US), [Managing AI agents in Assistant Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US), and [Using AI agents in Virtual Agent topics](https://www.servicenow.com/docs/access?context=ai-agent-custom-skill&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) for more information.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   Enhance the user experience with Microsoft Teams response message streaming capability.

[Yokohama Early Availability](../quality/yokohama-security-notables.md)

-   Enhance the overall voice-based chat experience in Conversational IVR with Now Assist.
-   Generate synthesized responses in Slack conversations with Now Assist.
-   Generate synthesized responses in Microsoft Teams conversations with Now Assist.
-   View custom skills in Virtual Agent Designer.

See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library \(previously Virtual Agent Designer\), and Analytics.

-   **[Conversational settings for Assets in the Asset library](https://www.servicenow.com/docs/access?context=asset-lib-conv-settings&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)Conversational settings**

    Manage the settings for an asset directly from the Asset library page.


-   **[Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Start the create flow for all supported conversational LLM assets directly from Virtual Agent Designer.

-   **[Assistants in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    The Now Assist Panel - Platform \(default\) assistant is now available in Virtual Agent Designer.

-   **[AI Connector utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Select AI agents to handle tasks in the AI Connector utility. For more information on AI agents in Virtual Agent Designer, see [Managing AI agents in Assistant Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) and [Using AI agents in Virtual Agent topics](https://www.servicenow.com/docs/access?context=ai-agent-custom-skill&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

-   **Virtual Agent Designer [Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Slide the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.

-   **Virtual Agent server**
    -   In chatHandshake, set **dynamic\_step\_loader\_enabled** to `true` to send stacked Agentic AI messages to server. Set **dynamic\_step\_loader\_enabled** to `false` to avoid sending messages.
    -   Pre-chat and post-chat surveys are now available for Anthropic Claude on AWS and Google Gemini LLMs. For more information on surveys, see [Chat surveys](https://www.servicenow.com/docs/access?context=ci-conversational-chat-surveys&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

-   **[AI Connector Utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Link custom skills to generative AI to add their functionality to LLM conversations.

-   **[AI agents and agentic workflows in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    View AI agents and agentic workflows created in AI Agent Studio in Virtual Agent Designer.

-   **[Shorten responses option for bot text response](https://www.servicenow.com/docs/access?context=va-text-response&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    For bot text responses, use the **Shorten responses** toggle in Virtual Agent Designer to turn on the **Show more** option in the chat on the user side.


-   **[Application scope for topics](https://www.servicenow.com/docs/access?context=vad-topic-creation-form&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Select the application scope for topics in Virtual Agent Designer.


-   **[Synthesized response in Slack conversations](https://www.servicenow.com/docs/access?context=slack-synthesized-response&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Generate synthesized responses in Slack conversations with Now Assist.

-   **[Virtual Agent feature support in Microsoft Teams conversations](https://www.servicenow.com/docs/access?context=va-teams-other-features&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Generate synthesized responses in Microsoft Teams conversations with Now Assist.

-   **[Custom skills in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=managing-custom-skills&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    View skills created in Now Assist Skill Kit in Virtual Agent Designer.

-   **[Chat surveys](https://www.servicenow.com/docs/access?context=ci-conversational-chat-surveys&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Create chat surveys compatible with LLM-enabled user inputs, aside from the Carousel user input.


## UI changes

-   **Changes to Virtual Agent Designer list view**
    -   Tabs have replaced pills in the Virtual Agent Designer list view.
    -   Hover over the tooltip icon \(![image.i-tooltip]\) to see information about the assistant you have selected from the drop-down menu.
    -   Use the new **AI agents** and **Agentic workflows** tabs to select from the types of topics on the home page, along with **Topics**, **Subflows**, **Actions**, and **Custom skills**.
    -   When a promoted asset has a conditional property that determines the context in which appears for an assistant, it's marked as **Condition applied** under **Show more**.

-   **[UI chat updates](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   The `New messages below` button in Virtual Agent was replaced with a simplified down-arrow indicator.
    -   The `New messages above` button was deprecated because Virtual Agent now auto-scrolls to the top of the oldest new message.
    -   Input text bar was updated to a more modern look and feel.
    -   The start a new conversation icon was updated.

-   **[Topic Properties tab](https://www.servicenow.com/docs/access?context=vad-topic-properties-tab&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   [Create a topic form](https://www.servicenow.com/docs/access?context=vad-topic-creation-form&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US): Read improved topic description field helper text and tooltip.
    -   [Change the application scope for Virtual Agent Designer topics](https://www.servicenow.com/docs/access?context=change-application-scope-vad&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US): View the current scope setting on the Virtual Agent Designer topic properties tab.
-   **[Topic Flow tab](https://www.servicenow.com/docs/access?context=vad-topic-flow-tab&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**
    -   View an updated `Unpublished changes` message on the header bar.
    -   Hover over the `Unpublished changes` message to get info on which changes are not yet published.
    -   Recover unsaved changes using the **Recover changes** button that appears on the header bar if you close a topic without saving.
    -   Both message and button appear on the header bar if you add a node to the canvas before closing without saving.
-   **[Testing LLM topics](https://www.servicenow.com/docs/access?context=test-llm-topics&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    View a `Matching` badge next to the skill activated during testing.

-   **[Custom skills in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=managing-custom-skills&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Use an updated Virtual Agent Designer list-based home page that includes custom skills.


## Changed in this release

-   **[Test assistant options](https://www.servicenow.com/docs/access?context=test-llm-topics&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


-   **[Dynamic Translation calls](https://www.servicenow.com/docs/access?context=translation-for-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    For Now Assist, if native translation is enabled, a Dynamic Translation call is only made if an unsupported language for native translation is used.

-   **[Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Use the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.


## Deprecations

Support for Now Assist in Conversational IVR was removed.

## Activation information

Virtual Agent is a ServiceNow AI Platform feature that is available with activation of the Glide Virtual Agent plugin \(com.glide.cs.chatbot\), which requires a separate subscription. For details, see [Activate Virtual Agent](https://www.servicenow.com/docs/access?context=activate-virtual-agent&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

**Note:** The Glide Virtual Agent plugin initially installs the Topic Recommendations and Conversational Analytics applications. Subsequent updates to these apps must be installed from the ServiceNow Store.

ServiceNow® Virtual Agent Lite is a subset of the Virtual Agent platform that is available to ServiceNow® IT Service Management \(ITSM\) customers. It doesn't require activation and works with ITSM Virtual Agent Lite conversations, which are also available to ITSM customers.

## Browser requirements

Virtual Agent supports various browsers, including Google Chrome and Microsoft Edge. For more information, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Localization information

The ServiceNow® Localization Framework is integrated in Virtual Agent.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Conversational Interfaces Console](https://www.servicenow.com/docs/access?context=ci-console&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    The ServiceNow® Conversational Interfaces Console enables you to install, manage, and monitor your virtual and live agents to support your users through chat.

-   **[Prebuilt Virtual Agent topics, topic blocks, and ServiceNow NLU models](https://www.servicenow.com/docs/access?context=prebuilt-topics-ITSM&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    The following ServiceNow® business applications provide prebuilt Virtual Agent conversation topics, NLU models, and, in some cases, topic blocks as reusable components.

    -   ServiceNow® Customer Service Management
    -   ServiceNow® Field Service Management
    -   ServiceNow® HR Service Delivery
    -   ServiceNow® Instance Security Center
    -   ServiceNow® IT Service Management
    -   ServiceNow® Project Portfolio Management
    -   ServiceNow® Universal Request
-   **[Natural Language Understanding](https://www.servicenow.com/docs/access?context=nlu-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Virtual Agent integrates with the Natural Language Understanding \(NLU\) application, which provides the NLU Workbench for creating NLU models. Virtual Agent uses these models to recognize and process user utterances, intents, and entities in bot conversations.


**Parent Topic:**[Conversational Interfaces release notes](conversational-interfaces-rn-landing.md)

