---
title: AI assets
description: Learn about the AI assets that you can create on the ServiceNow AI Platform.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-31"
reading_time_minutes: 2
breadcrumb: [Adding AI to your apps, Getting Started guide for developers, Building applications]
---

# AI assets

Learn about the AI assets that you can create on the ServiceNow AI Platform.

There are three types of AI assets that you can create on the ServiceNow AI Platform: skills, AI agents, and agentic workflows. Each AI asset type serves a different purpose and suits different use cases. Learning about what each asset is can help you decide how to approach adding AI to your custom applications. For detailed guidance about choosing the right asset type for your use case, see [Choosing the right AI capability](../../now-assist-app-engine/concept/choosing-the-right-ai-capability.md).

-   **Skills**

    A skill is a generative AI capability that completes a specific task for a defined use case. You provide the skill with an input, typically a record from a table in your application, and the skill uses an underlying large language model \(LLM\) to generate an output, such as a summary or a block of text. Skills are the most contained AI asset type and are a good starting point if you want to add a single, focused AI capability to your custom app. You can invoke skills conversationally through the Now Assist panel, through UI actions such as buttons on a record, or through Virtual Agent.

-   **AI agents**

    An AI agent is a generative AI capability that follows a set of LLM instructions and uses tools to carry out a role. Unlike skills, which complete a single task, AI agents can make decisions and take a series of actions based on their instructions and the data available to them. AI agents are well suited to use cases where there might be more varied situations with different operations and solutions.

-   **Agentic workflows**

    An agentic workflow combines one or more AI agents to accomplish a broader objective. An AI Agent Orchestrator coordinates the work between agents, directing each one to perform its part of the overall task. Agentic workflows are appropriate when the outcome requires multiple agents working in sequence or in parallel. For example, classifying a request, retrieving relevant records, and generating a recommended response in a single end-to-end workflow.


For each asset type, you can use preconfigured Now Assist Platform assets as a starting point and modify their underlying structure to fit your app's use case. Or you can build custom AI assets tailored to your app from scratch. Preconfigured assets are designed for existing platform use cases and typically require significant reconfiguration to work within custom applications. Custom AI assets can be designed for your specific tables, fields, and workflows from the beginning. For more information, see [AI capabilities for enhancing custom applications](../../now-assist-app-engine/concept/ai-capabilities-with-now-assist-for-app-engine.md).

**Parent Topic:**[Adding AI to your apps](dev-get-start-adding-ai-to-your-apps.md)

