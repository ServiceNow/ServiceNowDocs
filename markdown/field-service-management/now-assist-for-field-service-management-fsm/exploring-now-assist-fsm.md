---
title: Exploring Now Assist for Field Service Management \(FSM\)
description: With the Now Assist for Field Service Management \(FSM\) application, users can generate work order task summaries and knowledge articles from work order task information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/now-assist-for-field-service-management-fsm/exploring-now-assist-fsm.html
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist for FSM]
---

# Exploring Now Assist for Field Service Management \(FSM\)

With the Now Assist for Field Service Management \(FSM\) application, users can generate work order task summaries and knowledge articles from work order task information.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/ai-native-sku-overview.md).

**Important:**

-   Not all model providers are available for customers with in-country SKUs, and some Now Assist products/features are currently unavailable for in-country customers. For more information, see the [KB1584492](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1584492) article in the Now Support Knowledge Base. Be sure to check for model provider availability updates in future releases.
-   Some Now Assist products/features are currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. For more information, see the [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854) article in the Now Support Knowledge Base. Be sure to check for availability updates in future releases.
-   Some Now Assist products/features are currently available only for customers in some regions. Be sure to check for availability updates in future releases.
-   Some AI products and skills are not available in Regulated Markets. For more information, see [KB2593939: Regulated Markets AI Products/Skills Not Available](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=e8d7cc82475aba90b7832920326d4362). Be sure to check for availability updates in future releases.

## Now Assist for Field Service Management \(FSM\) Overview

The following generative AI capabilities are available:

-   Work order task summarization can help agents close tasks faster by generating summaries from work order task information. Automated content entry with Now Assist for Field Service Management \(FSM\) optimizes summary creation, reducing agent time on the application and providing higher-quality details in the work notes.
-   Knowledge generation can help an agent to streamline content creation, An agent can automatically generate knowledge articles by using the relevant data from the work order task record. By not having to generate knowledge articles manually, this feature saves your agents valuable time and effort.

## Skills

The Now Assist for FSM application includes generative AI skills that enable users to generate summary notes on work order tasks in any state, or generate knowledge articles from closed work order tasks.

-   **Work order task summarization**

    Enables users to generate a task closure summary using pre-configured inputs from the work order task.

    The work order task summarization skill generates a summary from the following work order task fields:

    -   Description
    -   Short description
    -   Work notes
    -   Additional comments
-   **Sidebar summarization**

    Enables users to summarize Sidebar discussions and save the summary in the work notes.

-   **Knowledge generation**

    Enables an agent to generate a knowledge article from a case after closing the work order task.

    The knowledge generation skill displays a pop-up window that an agent can use to generate a knowledge article based on similar work order tasks and review it before publishing the knowledge article draft.


## AI agents

The Now Assist for FSM application includes AI agents that automate field service tasks on the platform or on the ServiceNow Agent mobile application. For more information about setting up and using AI agents, see [Using agentic AI in Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/now-assist-for-field-service-management-fsm/fsm-ai-agent-use-cases.md).

-   **Create work order**

    Creates a work order using text or an image. The AI agent can be accessed on the platform or on the ServiceNow Agent mobile application.

-   **Parts Manager**

    Tracks and validates parts usage when closing work order tasks. The AI agent analyzes activity notes to update parts statuses and automatically adjusts inventory.


