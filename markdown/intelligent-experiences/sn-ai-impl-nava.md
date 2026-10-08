---
title: ServiceNow Otto for Virtual Agent readiness on the ServiceNow AI Platform
description: ServiceNow Otto for Virtual Agent has AI-driven capabilities that interpret natural language, guide users through complex tasks, and deliver high-confidence answers without relying on rigid keyword matching or manual configurations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/sn-ai-impl-nava.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Now Assist, agentic AI, AI readiness]
breadcrumb: [Application readiness, ServiceNow AI implementation, Enable AI experiences]
---

# ServiceNow Otto for Virtual Agent readiness on the ServiceNow AI Platform

ServiceNow Otto for Virtual Agent has AI-driven capabilities that interpret natural language, guide users through complex tasks, and deliver high-confidence answers without relying on rigid keyword matching or manual configurations.

ServiceNow Otto for Virtual Agent provides the following features:

-   AI asset discovery

    ServiceNow Otto for Virtual Agent uses LLMs to automatically discover and match user intents to Virtual Agent topics and other AI assets, including generative AI skills, AI agents and agentic workflows, and subflows and actions.

-   Simplified deployment

    Using LLM-powered Virtual Agent topics, teams can accelerate rollout and improve conversation quality.

-   AI Search Genius Results

    Users receive curated, actionable responses via Genius cards, which contain summarized knowledge with direct actions such as **Request this item**.

-   Conversational catalog ordering

    Users can request Service Catalog items using natural conversation. Virtual Agent asks clarifying questions and confirms the user's intent before completing the request.

    **Note:** Service Catalog items must be marked as conversational to work with Virtual Agent. For details, see [Catalog item conversational details page overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/using-catalog-conversational-experience.md).

-   Multi-turn Q&amp;A

    Follow-up questions are handled automatically, allowing users to refine their queries and get better answers.


Setting up Now Assist in Virtual Agent requires customizing or creating a new LLM assistant. You can assign an assistant to one or more portals. If LLM Virtual Agent topics aren't associated with an LLM assistant, they aren't discoverable.

## High-level checklist

-   **1. Install ServiceNow Otto for Virtual Agent**

    You can install it from the Conversational Interfaces admin console after you install an AI product such as ServiceNow Otto for IT Service Management \(ITSM\).

    To set up ServiceNow Otto for Virtual Agent, you configure an assistant.

    See: [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md)

-   **2. Review your Virtual Agent topic inventory**

    Review your topics and identify high-volume user queries. You can use Assistant Analytics to monitor, evaluate, and optimize the performance of your AI-powered assistants.

    Why? This helps you identify the top self-solve opportunities in Virtual Agent.

    See:

    -   [Conversational Analytics dashboard in Platform Analytics experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/VA-dashboard-landing-page-pae.md)
    -   [Create an Automation Discovery report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-auto-discovry-report.md)
-   **3. Review your knowledge base**

    Identify KB articles that can self-serve any of the top intents you identified.

    Why? This simplifies topic management and enables self-service.

    See: [Knowledge Base readiness for AI on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/sn-ai-impl-kb-readiness.md)

-   **4. Migrate NLU topics to LLM**

    Use the topic migration tool in Virtual Agent to convert NLU topics to LLM.

    Why? Use existing Virtual Agent topics with minimal effort.

    See: [Migrating NLU/keyword Virtual Agent topics to LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/llm-topic-migration.md)

-   **5. Review Service Catalog items**

    Identify self-serve catalog items that can be replaced with existing LLM topics.

    Why? To avoid redundancy and eliminate the need to create new Virtual Agent topics.

    See: [Service Catalog readiness for AI on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/sn-ai-impl-srvc-catalog.md)

-   **6. Review LLM Virtual Agent topics**

    Use these LLM topics as a starting point for Virtual Agent topic creation.

    Why? New LLM versions of older NLU Virtual Agent topics reduce rework.

    See: [ITSM Virtual Agent pre-built LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-va-prebuilt-topics.md)


## Tips

-   When migrating legacy NLU topics, optimize topic descriptions so that the topic is clearly described and aligned with the intent and expected results.

    For details, see [LLM description and instruction guidelines for Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/va-llm-instruction-guidelines.md).

-   You can customize the look of your assistant and the chat experience during guided setup.

    For details, see [Brand and personalize an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/brand-assistant.md).

-   You can choose the chat experience you want for each assistant:
    -   [Standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-standard-chat.md)
    -   [Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-enhanced-chat.md)
    -   [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-integrated-chat.md)
-   You can integrate ServiceNow Otto for Virtual Agent with Microsoft Teams.

    For details, see [Integrating ServiceNow Otto for Virtual Agent with Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/integrating-now-assist-va-msteams.md).


For more information about conversational catalogs in AI, see the following information from ServiceNow Community and YouTube:

-   [How to request catalog items in ServiceNow Otto for Virtual Agent](https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-request-catalog-items-in-now-assist-in-virtual-agent/ta-p/2747811)
-   [AI Academy: Enhanced chat experience with ServiceNow Otto for Virtual Agent](https://www.youtube.com/watch?v=UD7IneCtpxk)

