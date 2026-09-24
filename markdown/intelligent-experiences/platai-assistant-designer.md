---
title: Create assistants and conversations with Assistant Designer
description: Assistant Designer is the central workspace for creating, configuring, testing, and managing assistants and their conversational experiences. It gives administrators a single place to define what an assistant knows, what it can do, how it behaves, and where it is deployed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-assistant-designer.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [change management, AI adoption, organizational change management, rollout strategies, adoption metrics]
breadcrumb: [Creating AI user experiences, Enable AI Experiences]
---

# Create assistants and conversations with Assistant Designer

Assistant Designer is the central workspace for creating, configuring, testing, and managing assistants and their conversational experiences. It gives administrators a single place to define what an assistant knows, what it can do, how it behaves, and where it is deployed.

## Assistants

An assistant is the AI experience that users interact with. Think of it as a configurable AI co-worker that can answer questions, provide guidance, retrieve information, and help users complete tasks through natural language conversations. An assistant serves as the container that brings together all of the capabilities needed for a conversational experience, including knowledge sources, AI agents, topics, skills, actions, branding, and channel-specific settings.

Organizations can create multiple assistants for different audiences, use cases, or business functions. For example, a company might create separate assistants for employee support, customer self-service, IT help, or HR guidance. Each assistant can be deployed across channels such as portals, mobile apps, Microsoft Teams, and Slack while maintaining a consistent conversational experience. An assistant's effectiveness comes from the assets and information sources connected to it. These can include Virtual Agent topics, AI agents, skills, workflows, actions, search sources, and knowledge content. Together, these capabilities determine what the assistant can answer, what tasks it can perform, and how it engages with users.

Use Assistant Designer to create, configure, manage, and test LLM-based chat and voice assistants. How the assistant is configured impacts the quality of the experience that the user has when interacting with the assistant.

Assistant Designer has three primary tabs:

-   Assistants
-   Asset library
-   Analytics

## Assistants tab

The Assistants tab is where you create and configure individual assistants and define the overall experience. Administrators can create multiple assistants and tailor each one to a specific audience or purpose. Common configuration areas include the following:

-   The channels where the assistant is available
-   Branding and visual identity
-   Greeting, closing, and fallback messages
-   Search and knowledge configuration
-   AI agent enablement and orchestration settings
-   Overall conversational experience settings

\[Omitted image "asst-designer-assistant-tab.png"\] Alt text: The Assistants tab displays configured assistants as cards. You can test and edit existing assistants, or create a new one.

For more information, see [Assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

## Asset library tab

The Asset library tab is where you define the capabilities available to assistants. Assets represent the problems an assistant can help solve and the actions it can take during a conversation. Administrators create, organize, and manage these reusable conversational components, then make them available to one or more assistants.

Asset types include the following:

-   Conversational topics \(Virtual Agent topics\)
-   Subflows and actions
-   AI agents
-   Custom generative AI skills

By separating assets from assistants, organizations can reuse capabilities across multiple conversational experiences while maintaining centralized management.

\[Omitted image "asst-designer-asset-library-tab.png"\] Alt text: The Asset library lists all elements available to assistants, including conversational topics, subflows and actions, custom skills, AI agents, and agentic workflows to use in an assistant.

The Asset library includes the functionality of Virtual Agent Designer, a graphical design program that allows you to create Virtual Agent conversations. For more information, see [Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/conversation-designer-virtual-agent.md).

## Analytics tab

The Analytics tab is designed to help assistant administrators gain visibility into the performance of their AI-powered assistants across channels and workflows. It provides actionable insights into how assistants are being used, how effectively they are resolving user issues, and where improvements can be made to enhance the self-service experience. Assistant analytics looks at usage trends, adoption and engagement, user sentiment, and assist consumption.

The Analytics tab has several page views, each answering a different question, including the following:

-   Overview: Overall assist usage and CSAT scores across everything
-   Usage: Conversation volumes, which channels people actually use \(Teams, Slack, web, mobile\), and resolution vs. escalation rates
-   Adoption &amp; Engagement: User growth over time, engagement patterns, and how often a suggested assist turns into a real completed action \(the assist-to-execution ratio\)
-   Sentiment: Satisfaction scores, empathy indicators, and frustration signals—a read on the emotional quality of the conversation, not just whether it worked
-   Self-Solve Performance: Deflection rates \(how many issues get solved without a human agent\) and effort scores \(how much work the user had to do\)
-   Assists: Tracks AI resource consumption, which is useful for understanding the compute cost and which AI features are actually earning their keep
-   Voice: Tracks AI resource consumption for telephony and voice channels

\[Omitted image "NAinVA-assistant-designer-analytics-overview.png"\] Alt text: Overview dashboard page in Assistant analytics.

For more information, see [Analyzing assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ai-engagement-analytics.md).

**Parent Topic:**[Creating AI user experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-creating-ai-user-experiences.md)

