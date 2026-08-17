---
title: UI Builder Agent
description: The UI Builder Agent is a ServiceNow Otto AI agent that assists low-code developers working in UI Builder by responding to questions, information requests, and page editing instructions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/uib-builder-agent-concept.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 3
breadcrumb: [Explore, UI generation, UI Builder, Builder library, Developing your application, Building applications]
---

# UI Builder Agent

The UI Builder Agent is a ServiceNow Otto AI agent that assists low-code developers working in UI Builder by responding to questions, information requests, and page editing instructions.

The UI Builder Agent is pre-configured and available in AI Agent Studio as part of the UI Generation application. It supports developers as they build and modify pages in UI Builder by providing contextual AI assistance.

The ServiceNow Otto panel displays the UI Builder agent's responses. You can access the ServiceNow Otto panel by selecting the Otto icon in the Next Experience Unified Navigation.

Administrators install the required applications, configure the agent in AI Agent Studio, enable the ServiceNow Otto panel, and activate the default ServiceNow Otto Panel - Platform assistant before developers can interact with the agent.

## Required applications

Install the following applications from Application Manager to support the UI Builder Agent:

-   ServiceNow Otto for Creator \(`sn_now_creator`\) — Provides ServiceNow Otto AI skills for creators, including UI Builder support.
-   **UI Generation** \(`sn_ui_generation`\) — Contains the UI Builder Agent definition and its associated tools. Use the Zurich version or later.
-   **Conversational Studio** \(`sn_convo_studio`\) — Provides the assistant infrastructure used by the ServiceNow Otto panel.

## Key features of UI Builder agent

The UI Builder agent provides the following features:

-   **Learn about UI Builder**

    This feature answers your questions about the UI Builder. It provides detailed information about the features and functionalities of the UI Builder, along with links to relevant product documentation.

    You can ask about specific features or tasks, such as "What is a data resource?" or "How can I add a component to my page?" You will receive instant responses based on the latest ServiceNow documentation.

-   **Understand page configuration**

    This feature offers insights into how a page is built, including its design and structure. It describes the configuration of various elements on the page, helping developers quickly anticipate how future changes might affect functionality.

    You can ask about your page's configuration. For example, you might ask: "Is dynamic theming implemented on my page?" or "Are any client scripts being used on my page?"

-   **Accelerate page configuration**

    This feature enables you to modify and enhance your page. You can apply different layouts, such as a single row or a three-column format. You can add and configure components, such as buttons with labels and links that direct users to external websites. You can also update the styling of your page, such as changing the background color.


To configure the features, see [Configure UI Builder Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/configure-ui-builder-agent.md). To use the features, see [Using UI Builder agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/using-ui-builder-agent.md).

## Activation overview

Enabling the UI Builder Agent involves the following high-level steps:

1.  Install the required applications from Application Manager.
2.  Enable the UI Builder Agent setup wizard in AI Agent Studio.
3.  Turn on the ServiceNow Otto panel in AI Admin Hub.
4.  Add a display experience to the ServiceNow Otto Panel - Platform \(default\) assistant, request AI Search activation, and activate the assistant in Assistant Designer.

**Parent Topic:**[Exploring UI generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/exploring-ui-generation.md)

**Related topics**  


[Using UI Builder agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/using-ui-builder-agent.md)

[Use case: Using UI Builder Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/use-case-ui-builder-agent.md)

