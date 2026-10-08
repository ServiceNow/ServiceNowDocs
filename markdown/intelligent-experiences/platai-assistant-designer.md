---
title: Assistants and conversations in Assistant Designer
description: Assistant Designer is the central workspace for creating, configuring, testing, and managing assistants and their conversational experiences. Administrators use it as a single place to define an assistant's knowledge sources, capabilities, behavior, and deployment channels.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-assistant-designer.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [change management, AI adoption, organizational change management, rollout strategies, adoption metrics]
breadcrumb: [Creating AI user experiences, Enable AI Experiences]
---

# Assistants and conversations in Assistant Designer

Assistant Designer is the central workspace for creating, configuring, testing, and managing assistants and their conversational experiences. Administrators use it as a single place to define an assistant's knowledge sources, capabilities, behavior, and deployment channels.

## Assistants

An assistant can answer questions, provide guidance, retrieve information, and help users complete tasks through natural language conversations. It brings together the capabilities needed for a conversational experience. These include knowledge sources, AI agents, topics, skills, actions, branding, and channel-specific settings.

Organizations can create multiple assistants for different audiences, use cases, or business functions. For example, a company might create separate assistants for employee support, customer self-service, IT help, or HR guidance. Each assistant can be deployed across channels such as portals, mobile apps, Microsoft Teams, and Slack while maintaining a consistent conversational experience. An assistant's effectiveness comes from the assets and information sources connected to it. These can include Virtual Agent topics, AI agents, skills, workflows, actions, search sources, and knowledge content. Together, these capabilities determine what the assistant can answer, what tasks it can perform, and how it engages with users.

Use Assistant Designer to create, configure, manage, and test LLM-based chat and voice assistants. How the assistant is configured impacts the quality of the experience that the user has when interacting with the assistant.

Assistant Designer has three primary tabs:

-   **Assistants**
-   **Asset library**
-   **Analytics**

## Assistants tab

The **Assistants** tab is where you create and configure individual assistants and define the overall experience. Administrators can create multiple assistants and tailor each one to a specific audience or purpose. Common configuration areas include the following:

-   The channels where the assistant is available
-   Branding and visual identity
-   Greeting, closing, and fallback messages
-   Search and knowledge configuration
-   AI agent enablement and orchestration settings
-   Overall conversational experience settings

\[Omitted image "asst-designer-assistant-tab.png"\] Alt text: Assistants tab displaying configured assistants as cards, with options to test, edit, or create assistants.

For more information, see [Assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

## Asset library tab

The **Asset library** tab is where you define the capabilities available to assistants. Assets represent the problems an assistant can help solve and the actions it can take during a conversation. Administrators create, organize, and manage these reusable conversational components, then make them available to one or more assistants.

Asset types include the following:

-   Conversational topics \(Virtual Agent topics\)
-   Subflows and actions
-   AI agents
-   Custom generative AI skills

By separating assets from assistants, organizations can reuse capabilities across multiple conversational experiences while maintaining centralized management.

\[Omitted image "asst-designer-asset-library-tab.png"\] Alt text: Asset library listing all elements available to assistants, including conversational topics, subflows and actions, custom skills, AI agents, and agentic workflows.

The Asset library includes the functionality of Virtual Agent Designer, a graphical design program that you can use to create Virtual Agent conversations. For more information, see [Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/conversation-designer-virtual-agent.md).

## Analytics tab

The **Analytics** tab helps assistant administrators monitor the performance of their AI-powered assistants across channels and workflows. It provides actionable insights into how assistants are being used, how effectively they are resolving user issues, and where improvements can be made to enhance the self-service experience. Assistant analytics looks at usage trends, adoption and engagement, user sentiment, and assist consumption.

The **Analytics** tab has several page views, each answering a different question, including the following:

-   Overview: overall assist usage and CSAT scores across everything
-   Usage: conversation volumes, which channels users use, such as Microsoft Teams, Slack, web, and mobile, and resolution vs. escalation rates
-   Adoption &amp; Engagement: user growth over time, engagement patterns, and the assist-to-execution ratio, which measures how often a suggested assist becomes a completed action
-   Sentiment: satisfaction scores, empathy indicators, and frustration signals, and indicators of the emotional quality of the conversation
-   Self-solve performance: deflection rates \(how many issues get solved without a human agent\) and effort scores \(how much work the user had to do\)
-   Assists: AI resource consumption, useful for understanding compute cost and which AI features are used
-   Voice: AI resource consumption for telephony and voice channels

\[Omitted image "NAinVA-assistant-designer-analytics-overview.png"\] Alt text: Overview dashboard page in Assistant analytics.

For more information, see [Analyzing assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ai-engagement-analytics.md).

**Parent Topic:**[Creating AI user experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-creating-ai-user-experiences.md)

