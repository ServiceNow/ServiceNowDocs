---
title: Now Assist in Virtual Agent readiness on the ServiceNow AI Platform
description: Now Assist enhances Virtual Agent with AI-driven capabilities that understand natural language, guide users through complex tasks, and deliver high-confidence answers without relying on rigid keyword matching or manual configurations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, agentic AI, AI readiness]
breadcrumb: [Application readiness, ServiceNow AI implementation, Enable AI experiences]
---

# Now Assist in Virtual Agent readiness on the ServiceNow AI Platform

Now Assist enhances Virtual Agent with AI-driven capabilities that understand natural language, guide users through complex tasks, and deliver high-confidence answers without relying on rigid keyword matching or manual configurations.

Now Assist in Virtual Agent provides the following features:

-   AI asset discovery

    Say goodbye to time-consuming keyword or NLU configurations. Now Assist uses LLMs to automatically discover and match user intents to Virtual Agent topics and other AI assets, including generative AI skills, AI agents and agentic workflows, and subflows and actions.

-   Simplified deployment

    Using LLM-powered Virtual Agent topics, teams can accelerate rollout and improve conversation quality. This means less effort spent on manual tuning and more time delivering value.

-   AI Search Genius Results

    Users receive curated, actionable responses via Genius cards, which contain summarized knowledge with direct actions such as `Request this item`.

-   Conversational catalog ordering

    Users can request Service Catalog items using natural conversation. Virtual Agent asks clarifying questions and confirms the user's intent before completing the request.

    **Note:** Service Catalog items must be marked as conversational to work with Virtual Agent. For details, see Catalog item conversational details page overview.

-   Multi-turn Q&amp;A

    Follow-up questions are handled seamlessly, allowing users to refine their queries and get better answers.


Setting up Now Assist in Virtual Agent requires customizing or creating a new LLM assistant. You can assign an assistant to one or more portals. If LLM Virtual Agent topics aren't associated with an LLM assistant, they aren't discoverable.

## High-level checklist

-   **1. Install Now Assist in Virtual Agent**

    You can install it from the Conversational Interfaces admin console once you have installed a Now Assist product such as Now Assist for IT Service Management \(ITSM\).

    To set up Now Assist in Virtual Agent, you configure an assistant.

    See: Configuring assistants overview

-   **2. Review your Virtual Agent topic inventory**

    Review your topics and identify high-volume user intents. You can use the Conversational Analytics dashboard and Automation Discovery reports.

    Why? This helps you identify the top self-solve opportunities in Virtual Agent.

    See:

    -   Conversational Analytics dashboard in Platform Analytics experience
    -   Create an Automation Discovery report
-   **Review your knowledge base**

    Identify KB articles that can self-serve any of the top intents you identified.

    Why? This simplifies topic management and enables self-service.

    See: [Knowledge Base readiness for Now Assist on the ServiceNow AI Platform](sn-ai-impl-kb-readiness.md)

-   **4. Migrate NLU topics to LLM**

    Use the topic migration tool in Virtual Agent to convert NLU topics to LLM.

    Why? Leverage existing Virtual Agent topics with minimal effort.

    See: Migrating NLU/keyword Virtual Agent topics to LLM topics

-   **5. Review Service Catalog items**

    Identify self-serve catalog items that can be replaced with existing LLM topics.

    Why? To avoid redundancy and eliminate the need to create new Virtual Agent topics.

    See: [Service Catalog readiness for Now Assist on the ServiceNow AI Platform](sn-ai-impl-srvc-catalog.md)

-   **Review LLM Virtual Agent topics that come with Now Assist**

    Use these LLM topics as a starting point for Virtual Agent topic creation.

    Why? New LLM versions of older NLU Virtual Agent topics reduce rework.

    See: ITSM Virtual Agent pre-built LLM topics


## Tips

-   When migrating legacy NLU topics, ensure that you optimize topic descriptions so that the topic is clearly described and aligned with the intent and expected results.

    For details, see LLM description and instruction guidelines for Virtual Agent topics.

-   You can customize the look of your assistant and the chat experience during guided setup.

    For details, see Brand an assistant.

-   You can choose the chat experience you want for each assistant:
    -   Standard chat
    -   Enhanced chat
-   You can integrate Now Assist in Virtual Agent with Microsoft Teams.

    For details, see Integrating Now Assist in Virtual Agent with Microsoft Teams.


For more information about conversational catalogs in AI, see the following information from ServiceNow Community and YouTube:

-   [How to request catalog items in Now Assist in Virtual Agent](https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-request-catalog-items-in-now-assist-in-virtual-agent/ta-p/2747811)
-   [Microsoft Copilot integration with Now Assist FAQ - Zurich release](https://www.servicenow.com/community/virtual-agent-nlu-articles/microsoft-copilot-integration-with-now-assist-faq-zurich-release/ta-p/3048238)
-   [AI Academy: Enhanced chat experience with Now Assist in Virtual Agent](https://www.youtube.com/watch?v=UD7IneCtpxk)

