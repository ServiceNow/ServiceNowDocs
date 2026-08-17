---
title: Virtual Agent release notes
description: The ServiceNow Virtual Agent application provides user assistance through a conversational interface to help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-09-04"
reading_time_minutes: 5
---

# Virtual Agent release notes

The ServiceNow® Virtual Agent application provides user assistance through a conversational interface to help users to quickly obtain information and to perform common work tasks. Virtual Agent was enhanced and updated in the Zurich release.

## Virtual Agent highlights for the Zurich release

[Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Virtual Agent and ServiceNow Otto panel. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   [Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/vad-topics-page.md):
    -   View an updated UI for Virtual Agent Designer topics in the new Assistant Designer Asset library page.
    -   Navigate between Assistants, Asset library, and Analytics tabs in the Assistant Designer UI.
    -   Disconnect an LLM Assistant from a given asset with the Actions on Row icon \[Omitted image "kebab-menu.png"\] Alt text:in the Asset library.
    -   See descriptions of each LLM asset type when selecting **Create asset** in the Asset library.
    -   Read a tooltip that appears when you edit an LLM assistant under the Assistans tab and try to promote more than 6 topics associated with an LLM assistant.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Google Workspace chat now works with the ServiceNow® conversational interface features, including Virtual Agent, Natural Language Understanding \(NLU\), Notifications, and live agents.
-   Start the create flow for all supported conversational assets directly from Virtual Agent Designer.

See [Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/virtual-agent-landing-page.md) for more information.

## New in the Zurich release

-   **[Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/assistant-designer.md)**

    Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library \(previously Virtual Agent Designer\), and Analytics.

-   **[Conversational settings for assets in the Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/asset-lib-conv-settings.md)Conversational settings**

    Manage the settings for an asset directly from the Asset library page.


-   **[Integrating with Google Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/integrate-with-gsuite.md)**

    Integrate Google Workspace chat with the ServiceNow® conversational interface features, including Virtual Agent, Natural Language Understanding \(NLU\), Notifications, and live agents.

-   **[AI Connector utility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/vad-ai-connector-utility.md)**

    Select AI agents to handle tasks in the AI Connector utility. For more information on AI agents in Virtual Agent Designer, see [Managing AI agents in Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/managing-use-cases-ai-agents.md) and [Using AI agents in Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/ai-agent-custom-skill.md).

-   **[Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/virtual-agent-landing-page.md) server**
    -   In chatHandshake, set **dynamic\_step\_loader\_enabled** to `true` to send stacked agentic AI messages to the server. Set **dynamic\_step\_loader\_enabled** to `false` to avoid sending messages.
    -   Pre-chat and post-chat surveys are now available for Anthropic Claude on AWS and Google Gemini large language models \(LLMs\). For more information on surveys, see [Chat surveys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/ci-conversational-chat-surveys.md).
-   **[Create a Virtual Agent asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/create-virtual-agent-topic.md)**

    Start the create flow for all supported conversational LLM assets directly from Virtual Agent Designer.

-   **[Assistants in Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/conversation-designer-virtual-agent.md)**

    The Now Assist Panel - Platform \(default\) assistant is now available in Virtual Agent Designer.

-   **[Integrating ServiceNow Otto for Virtual Agent with Microsoft Copilot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/ms-copilot-na-va.md)**

    Custom Engine Agent \(CEA\) is replacing the legacy Microsoft bot framework, allowing Microsoft Copilot to discover Virtual Agent, Now Assist, and use multi-turn conversations.


## UI changes

-   **[Next Experience preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/set-up-preferences-next-experience.md)**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/vad-topics-page.md)**
    -   Tabs have replaced pills in the Virtual Agent Designer list view.
    -   Hover over the tooltip icon \(\[Omitted image "i-tooltip.png"\] Alt text:\) to see information about the assistant you have selected from the drop-down menu.
    -   Use the new **AI agents** and **Agentic workflows** tabs to select from the types of topics on the home page, along with **Topics**, **Subflows**, **Actions**, and **Custom skills**.
-   **Virtual Agent Designer [Table bot response control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/table-bot-response.md)**

    Slide the new Show links for each record toggle switch to activate links for each record in the output in your Virtual Agent conversation.


## Changed in this release

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/sn-ai-implementation-landing.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


-   **[Table bot response control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/table-bot-response.md)**

    Use the new **Show links for each record** toggle switch to activate links for each record in the output in your Virtual Agent conversation.

-   **[Test assistant options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/test-llm-topics.md)**

    The **Test** button in the Virtual Agent Designer canvas directly opens up the chat widget.


## Deprecations

-   Starting with the Zurich release, [Sensitive Data Handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/ac-sensitive-data-overview.md) and Sensitive Data Masking capability are being prepared for future deprecation. They will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

    Install the Data Privacy application as a replacement. For more information, see [Data Privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/data-privacy-landing.md).

-   Starting with the Zurich release, Microsoft LUIS is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.


## Activation information

Virtual Agent is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Conversational Interfaces release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/conversational-interfaces-rn-landing.md)

