---
title: Add a tool to an AI agent
description: Add a tool to an AI agent to enable different functionalities and help your AI agents achieve their objectives.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add a tool to an AI agent

Add a tool to an AI agent to enable different functionalities and help your AI agents achieve their objectives.

## Tool overview

Tools provide your AI agents with the capabilities necessary to complete their tasks. When adding tools, consider how the AI agent will use them to achieve its objectives as well as how those tools interact with each other. Providing your AI agents with the appropriate tools help ensure the robustness and quality of their performance.

Some additional guidelines for adding and creating tools are the following:

-   Design tools to work together. Your AI agent should solve a specific, discrete task, and the tools should give the AI agent all of the capabilities necessary to achieve its goal.
-   Write detailed tool descriptions. Tool descriptions are used by the AI agent to determine a tool's function. Thorough descriptions about what the tools are and how they work will give the AI agent the best chance to succeed.
-   Consider the outputs of tools when creating them. Use the tool description or output transformation strategy fields to describe how to process the tool outputs. For example, if you have a tool that gathers records from a large number of tables, provide the tool with plans for how to handle the amount of records that the query could return.

**Note:** If you select Google as your web search tool provider, the web search tool leverages [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment. Because grounding is not [data resident](https://cloud.google.com/vertex-ai/generative-ai/docs/security-controls), Google's global infrastructure routes traffic to a global data center for each web search request. This processing may be different than your data processing location chosen for your ServiceNow instance. Please consider your organization's data policies before enabling AI agents that use Google web search tools.

Once you have added all of the tools to your AI agent, you can select **Save and continue** to move to the next step in the guided setup.

## Supervised execution mode for AI agents

You can minimize potential negative impact of an AI agent not executing as expected by configuring AI agents' tools to run in supervised mode. This will ensure human oversight for the tool's actions. You can use the Supervised mode to enhance security for agents with the capability to perform sensitive or critical actions.

You can set the supervised execution mode when creating a tool in the AI agent guided setup. For example, choose Supervised as the Execution mode when adding a catalog item tool. For reference, see [Add a catalog item to an AI agent](../task/add-catalog-ai-agent.md).

-   **[Add a catalog item to an AI agent](../task/add-catalog-ai-agent.md)**  
Add a Service Catalog to an AI agent in AI Agent Studio so that your users can access conversational catalog items.
-   **[Add a conversational topic to an AI agent](../task/add-va-topic-ai-agent.md)**  
Add a Virtual Agent topic to an AI agent in AI Agent Studio so that you can use conversations to get additional information from the user. For example, a conversational topic could be used to let a user select a date range for surveys.
-   **[Add a file upload to an AI agent](../task/add-file-retrieval.md)**  
Upload files for analysis by an AI agent in AI Agent Studio to grant your AI agent access to specialized knowledge.
-   **[Add a flow action to an AI agent](../task/add-flow-action-ai-agent.md)**  
Add a flow action to an AI agent in AI Agent Studio. Define the flow action to use it as a reusable operation in automating the ServiceNow AI Platform features without having to write code.
-   **[Add a Knowledge Graph to an AI agent](../task/add-knowledge-graph.md)**  
Add a Knowledge Graph to an AI agent in AI Agent Studio that uses the structured and unstructured data from different ServiceNow records to enhance the performance of AI agents.
-   **[Add a Now Assist skill to an AI agent](../task/add-skill-ai-agent.md)**  
Add a generative AI skill to an AI agent in AI Agent Studio. You can customize the skills to meet the needs of your users in different workflows.
-   **[Add a record operation to an AI agent](../task/add-database-op-ai-agent.md)**  
Add a record operation to an AI agent in AI Agent Studio to create, update, look up, or delete records.
-   **[Add a script to an AI agent](../task/add-script-ai-agent.md)**  
Create a script to add it to an AI agent in AI Agent Studio. With scripts, you can use the scriptable APIs and back-end integration to support the AI agent.
-   **[Add a search retrieval to an AI agent](../task/add-retriever-ai-agent.md)**  
Add a search retrieval to an AI agent in AI Agent Studio. Leveraging the Retrieval-Augmented Generation \(RAG\) enables an AI agent to retrieve and incorporate relevant information from an external source.
-   **[Add a subflow to an AI agent](../task/add-sub-flow-ai-agent.md)**  
Add a subflow to an AI agent in AI Agent Studio. Subflows are reusable sequences of processing steps that can be called from within a flow.
-   **[Add a web search to an AI agent](../task/add-web-search-ai-agent.md)**  
Add a web search to an AI agent in AI Agent Studio using a third-party search API such as Microsoft Bing or Google.

**Parent Topic:**[Create an AI agent](../task/configure-next-best-action-agent.md)

