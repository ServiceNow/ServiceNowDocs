---
title: Using the conversational experience in AI Admin Center
description: Use the ServiceNow Otto panel to perform AI administration and setup tasks through a conversational interface directly in AI Admin Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/using-now-assist-panel-now-assist-center.html
release: brazil
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 4
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Using the conversational experience in AI Admin Center

Use the ServiceNow Otto panel to perform AI administration and setup tasks through a conversational interface directly in AI Admin Center.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

The ServiceNow Otto panel is enabled by default, and is accessible from every page in AI Admin Center. You can interact with your AI companion by typing questions and instructions in plain language.

For more information on the general capabilities of ServiceNow Otto panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md).

\[Omitted image "ai-admin-center-lux-otto-panel.png"\] Alt text: ServiceNow Otto panel in the AI Admin Center \(Next Experience UI\).

## AI companion capabilities

Use the ServiceNow Otto panel to perform the following types of actions in AI Admin Center:

-   **Setup and configuration**

    Start guided setup workflows for generative AI skills, AI Guardian settings, model configurations, multilingual service, data sharing and processing, integrations, and account details. The AI companion executes setup steps on your behalf and asks for your confirmation before any change takes effect.

-   **Skill activation and deactivation**

    Activate or deactivate generative AI skills through conversation. The panel presents skill details and current state before requesting confirmation.

-   **Instance and product details**

    Query configuration details about your instance including translation status, language configurations, data sharing settings, model providers, model versions, and integrations.

-   **Create and manage intents**

    Create intent records and generate the name, description, example utterances, detection criteria, and resolution criteria for them. Use the conversation to find, update, activate, deactivate, or delete existing intents.

-   **AI-assisted help**

    Ask questions about AI features, concepts, and admin tasks. The panel sources product documentation and training resources and returns answers with references and links to the source material.


After you enter your request in the chat, your AI companion generates a plan to implement your AI solution using the available AI assets. You can review the details of the solution, test it, and activate it, all in the conversation.

## Self-service conversational troubleshooting

Depending on your chat request, the self-service conversational troubleshooting AI agents may be engaged to diagnose common AI administration issues.

Self-service conversational troubleshooting can help with issues such as:

-   AI Admin Center configuration or setup problems
-   Plugin installation or activation failures
-   Missing or turned off AI application features
-   Integration connectivity or credential problems
-   Role or permission misconfigurations affecting access
-   Feature flags or activation toggles in an unexpected state
-   Compatibility conflicts between plugins or versions

For more information, see [Self-service conversational troubleshooting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-self-healing-agent.md).

## AI Admin Center help

Based on your chat request, the help AI agent may be engaged to find answers to your AI admin questions based on ServiceNow documentation. The AI agent responses provide relevant descriptions, instructions, references, and links to source documents that support your product experience.

For more information, see [AI Admin Center help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-help-agent.md).

## AI analytics Q and A

Based on your chat request, the AI Analytics Q and A AI agent may be engaged to provide answers about AI analytics in AI Admin Center including metrics, dashboard widgets, and calculations.

The AI Analytics Q and A AI agent can address topics such as:

-   KPI definitions in AI analytics dashboards, such as CSAT, deflection rate, and so on.
-   How a dashboard widget or metric is calculated
-   Data flows and processing context for AI analytics
-   Deflection log states and common deflection scenarios
-   Changes to AI analytics dashboards between releases, such as updated or removed indicators and new dashboards

For more information, see [AI Analytics Q and A agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-ask-analytics-agent.md).

## Intent management

Based on your request, an AI agent may be engaged to helps create and update Natural Language Understanding \(NLU\) intents. Intent management can help you to:

-   Create an intent.
-   Update an existing intent identified by a specific intent name or sys\_id.
-   Delete an existing intent.
-   Activate or deactivate an existing intent.
-   Look up intents by name or sys\_id.

