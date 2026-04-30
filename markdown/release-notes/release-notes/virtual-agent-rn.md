---
title: Virtual Agent release notes
description: The ServiceNow Virtual Agent application provides user assistance through a conversational interface to help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-09-04"
reading_time_minutes: 4
---

# Virtual Agent release notes

The ServiceNow® Virtual Agent application provides user assistance through a conversational interface to help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Zurich release.

## Virtual Agent highlights for the Zurich release

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   [Assistant Designer Asset library](https://www.servicenow.com/docs/access?context=vad-topics-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US):
    -   View an updated UI for Virtual Agent Designer topics in the new Assistant Designer Asset library page.
    -   Navigate between Assistants, Asset library, and Analytics tabs in the Assistant Designer UI.
    -   Disconnect an LLM Assistant from a given asset with the Actions on Row icon ![](../../administer/virtual-agent/images/kebab-menu.png)in the Asset library.
    -   See descriptions of each LLM asset type when selecting **Create asset** in the Asset library.
    -   Read a tooltip that appears when you edit an LLM assistant under the Assistans tab and try to promote more than 6 topics associated with an LLM assistant.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Google Workspace chat now works with the ServiceNow® conversational interface features, including Virtual Agent, Natural Language Understanding \(NLU\), Notifications, and live agents.
-   Start the create flow for all supported conversational assets directly from Virtual Agent Designer.

See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for more information.

## New in the Zurich release

-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library \(previously Virtual Agent Designer\), and Analytics.

-   **[Conversational settings for Assets in the Asset library](https://www.servicenow.com/docs/access?context=asset-lib-conv-settings&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)Conversational settings**

    Manage the settings for an asset directly from the Asset library page.


-   **[Integrating with Google Workspace](https://www.servicenow.com/docs/access?context=integrate-with-gsuite&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Integrate Google Workspace chat with the ServiceNow® conversational interface features, including Virtual Agent, Natural Language Understanding \(NLU\), Notifications, and live agents.

-   **[AI Connector utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Select AI agents to handle tasks in the AI Connector utility. For more information on AI agents in Virtual Agent Designer, see [Managing AI agents in Assistant Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) and [Using AI agents in Virtual Agent topics](https://www.servicenow.com/docs/access?context=ai-agent-custom-skill&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

-   **[Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) server**
    -   In chatHandshake, set **dynamic\_step\_loader\_enabled** to `true` to send stacked agentic AI messages to the server. Set **dynamic\_step\_loader\_enabled** to `false` to avoid sending messages.
    -   Pre-chat and post-chat surveys are now available for Anthropic Claude on AWS and Google Gemini large language models \(LLMs\). For more information on surveys, see [Chat surveys](https://www.servicenow.com/docs/access?context=ci-conversational-chat-surveys&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
-   **[Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Start the create flow for all supported conversational LLM assets directly from Virtual Agent Designer.

-   **[Assistants in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    The Now Assist Panel - Platform \(default\) assistant is now available in Virtual Agent Designer.

-   **[Integrating Now Assist in Virtual Agent with Microsoft Copilot](https://www.servicenow.com/docs/access?context=ms-copilot-na-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Custom Engine Agent \(CEA\) is replacing the legacy Microsoft bot framework, allowing Microsoft Copilot to discover Virtual Agent, Now Assist, and use multi-turn conversations.


## UI changes

-   **[Next Experience preferences](https://www.servicenow.com/docs/access?context=set-up-preferences-next-experience&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Assistant Designer Asset library](https://www.servicenow.com/docs/access?context=vad-topics-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**
    -   Tabs have replaced pills in the Virtual Agent Designer list view.
    -   Hover over the tooltip icon \(![](../../administer/virtual-agent/images/i-tooltip.png)\) to see information about the assistant you have selected from the drop-down menu.
    -   Use the new **AI agents** and **Agentic workflows** tabs to select from the types of topics on the home page, along with **Topics**, **Subflows**, **Actions**, and **Custom skills**.
-   **Virtual Agent Designer [Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Slide the new Show links for each record toggle switch to activate links for each record in the output in your Virtual Agent conversation.


## Changed in this release

-   **[Table bot response control](https://www.servicenow.com/docs/access?context=table-bot-response&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Use the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.

-   **[Test assistant options](https://www.servicenow.com/docs/access?context=test-llm-topics&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


## Deprecations

-   Starting with the Zurich release, [Sensitive Data Handler](https://www.servicenow.com/docs/access?context=ac-sensitive-data-overview&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) and the [Sensitive Data Masking capability](https://www.servicenow.com/docs/access?context=va-sensitive-data-masking&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) are being prepared for future deprecation. They will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

    Install the Data Privacy application as a replacement. For more information, see [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

-   Starting with the Zurich release, Microsoft LUIS is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.


## Activation information

Virtual Agent is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Conversational Interfaces release notes](conversational-interfaces-rn-landing.md)

