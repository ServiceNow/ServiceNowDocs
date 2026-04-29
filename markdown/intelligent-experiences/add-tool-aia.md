---
title: Add tools and information to an AI agent
description: Add a tool to an AI agent to enable different functionalities and help your AI agents achieve their objectives.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-11-23"
reading_time_minutes: 2
breadcrumb: [Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Add tools and information to an AI agent

Add a tool to an AI agent to enable different functionalities and help your AI agents achieve their objectives.

## Tool overview

Tools provide your AI agents with the capabilities necessary to complete their tasks. When adding tools, consider how the AI agent uses them to achieve its objectives as well as how those tools interact with each other. Providing your AI agents with the appropriate tools help promote the robustness and quality of their performance.

Some additional guidelines for adding and creating tools are the following:

-   Design tools to work together. Your AI agent should solve a specific, discrete task, and the tools should give the AI agent the capabilities necessary to achieve its goal.
-   Write detailed tool descriptions. Tool descriptions are used by the AI agent to determine a tool's function. Thorough descriptions about what the tools are and how they work give the AI agent the best chance to succeed.
-   Consider the outputs of tools when creating them. Use the tool description or output transformation strategy fields to describe how to process the tool outputs. For example, if you have a tool that gathers records from a large number of tables, provide the tool with plans for how to handle the large number of records.

**Note:** If you select Google as your web search tool provider, the web search tool leverages [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment. Because grounding isn’t [data resident](https://cloud.google.com/vertex-ai/generative-ai/docs/security-controls), Google's global infrastructure routes traffic to a global datacenter for each web search request. This processing may be different than your data processing location chosen for your ServiceNow instance. Consider your organization's data policies before enabling AI agents that use Google web search tools.

Once you have added the tools to your AI agent, you can select **Save and continue** to move to the next step in the guided setup.

## Knowledge graphs

In this step, you can also add Knowledge graphs. Knowledge graphs give the AI agent information to understand the relationships between real-world entities to improve its outputs. For example, you could add a Knowledge Graph to an approval AI agent that maps users to their location, company, and department to help the AI agent understand the specific approval process to apply.

![Knowledge Graph options](../image/add-tools-2.png)

## Supervised execution mode for AI agents

You can minimize the potential negative impact of an AI agent not executing as expected by configuring AI agents' tools to run in supervised mode. Running in supervised mode means that the tools use human oversight when executing actions. You can use the Supervised mode to enhance security for agents with the capability to perform sensitive or critical actions.

You can set the supervised execution mode when creating a tool in the AI agent guided setup. For example, choose Supervised as the Execution mode when adding a catalog item tool. For reference, see [Add a catalog item to an AI agent](../task/add-catalog-ai-agent.md).

