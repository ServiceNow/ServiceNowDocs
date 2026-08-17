---
title: ServiceNow Otto for Virtual Agent readiness on the ServiceNow AI Platform
description: ServiceNow Otto for Virtual Agent with AI-driven capabilities that understand natural language, guide users through complex tasks, and deliver high-confidence answers without relying on rigid keyword matching or manual configurations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/sn-ai-impl-nava.html
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, agentic AI, AI readiness]
breadcrumb: [Application readiness, ServiceNow AI implementation, Enable AI experiences]
---

# ServiceNow Otto for Virtual Agent readiness on the ServiceNow AI Platform

ServiceNow® Otto for Virtual Agent with AI-driven capabilities that understand natural language, guide users through complex tasks, and deliver high-confidence answers without relying on rigid keyword matching or manual configurations.

ServiceNow® Otto for Virtual Agent provides the following features:

-   AI asset discovery

    Say goodbye to time-consuming keyword or NLU configurations. ServiceNow Otto uses LLMs to automatically discover and match user intents to Virtual Agent topics and other AI assets, including generative AI skills, AI agents and agentic workflows, and subflows and actions.

-   Simplified deployment

    Using LLM-powered Virtual Agent topics, teams can accelerate rollout and improve conversation quality. This means less effort spent on manual tuning and more time delivering value.

-   AI Search Genius Results

    Users receive curated, actionable responses via Genius cards, which contain summarized knowledge with direct actions such as `Request this item`.

-   Conversational catalog ordering

    Users can request Service Catalog items using natural conversation. Virtual Agent asks clarifying questions and confirms the user's intent before completing the request.

    **Note:** Service Catalog items must be marked as conversational to work with Virtual Agent. For details, see [Catalog item conversational details page overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/using-catalog-conversational-experience.md).

-   Multi-turn Q&amp;A

    Follow-up questions are handled seamlessly, allowing users to refine their queries and get better answers.


Setting up ServiceNow® Otto for Virtual Agent requires customizing or creating a new LLM assistant. You can assign an assistant to one or more portals. If LLM Virtual Agent topics aren't associated with an LLM assistant, they aren't discoverable.

## High-level checklist

-   **1. Install ServiceNow® Otto for Virtual Agent**

    You can install it from the Conversational Interfaces admin console once you have installed a ServiceNow Otto product such as ServiceNow Otto for IT Service Management \(ITSM\) or the appropriate product tier.

    To set up ServiceNow® Otto for Virtual Agent, you configure an assistant.

    See: [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/configure-now-assist-va.md)

-   **2. Review your Virtual Agent topic inventory**

    Review your topics and identify high-volume user intents. You can use the Conversational Analytics dashboard and Automation Discovery reports.

    Why? This helps you identify the top self-solve opportunities in Virtual Agent.

    See:

    -   [Analyzing assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/ai-engagement-analytics.md)
    -   [Create an Automation Discovery report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/create-auto-discovry-report.md)
-   **Review your knowledge base**

    Identify KB articles that can self-serve any of the top intents you identified.

    Why? This simplifies topic management and enables self-service.

    See: [Knowledge Base readiness for AI on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sn-ai-impl-kb-readiness.md)

-   **4. Migrate NLU topics to LLM**

    Use the topic migration tool in Virtual Agent to convert NLU topics to LLM.

    Why? Leverage existing Virtual Agent topics with minimal effort.

    See: [Migrating NLU/keyword Virtual Agent topics to LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/llm-topic-migration.md)

-   **5. Review Service Catalog items**

    Identify self-serve catalog items that can be replaced with existing LLM topics.

    Why? To avoid redundancy and eliminate the need to create new Virtual Agent topics.

    See: [Service Catalog readiness for AI on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sn-ai-impl-srvc-catalog.md)

-   **Review LLM Virtual Agent topics that come with Now Assist**

    Use these LLM topics as a starting point for Virtual Agent topic creation.

    Why? New LLM versions of older NLU Virtual Agent topics reduce rework.

    See: [ITSM Virtual Agent pre-built LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/itsm-va-prebuilt-topics.md)


## Tips

-   When migrating legacy NLU topics, ensure that you optimize topic descriptions so that the topic is clearly described and aligned with the intent and expected results.

    For details, see [LLM description and instruction guidelines for Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/va-llm-instruction-guidelines.md).

-   You can customize the look of your assistant and the chat experience during guided setup.

    For details, see [Brand and personalize an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/brand-assistant.md).

-   You can choose the chat experience you want for each assistant:
    -   [Standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/nava-standard-chat.md)
    -   [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/nava-enhanced-chat.md)
-   You can integrate ServiceNow® Otto for Virtual Agent with Microsoft Teams.

    For details, see [Integrating ServiceNow Otto for Virtual Agent with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/integrating-now-assist-va-msteams.md).


For more information about conversational catalogs in AI, see the following information from ServiceNow Community and YouTube:

-   [How to request catalog items in ServiceNow Otto for Virtual Agent](https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-request-catalog-items-in-now-assist-in-virtual-agent/ta-p/2747811)
-   [Microsoft Copilot integration with Now Assist FAQ - Zurich release](https://www.servicenow.com/community/virtual-agent-nlu-articles/microsoft-copilot-integration-with-now-assist-faq-zurich-release/ta-p/3048238)
-   [AI Academy: Enhanced chat experience with ServiceNow Otto for Virtual Agent](https://www.youtube.com/watch?v=UD7IneCtpxk)

