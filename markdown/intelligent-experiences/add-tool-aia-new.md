---
title: Add tools and information to an AI agent
description: Add a tool to an AI agent to enable different functionalities and help your AI agents achieve their objectives.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-tool-aia-new.html
release: australia
topic_type: concept
last_updated: "2025-11-23"
reading_time_minutes: 2
breadcrumb: [Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add tools and information to an AI agent

Add a tool to an AI agent to enable different functionalities and help your AI agents achieve their objectives.

## Tool overview

Tools give your AI agents the capabilities they need to complete their tasks. When adding tools, think about how the AI agent will use them to achieve its objectives and how those tools will work together. Equipping your AI agents with the right tools helps ensure robust, high-quality performance.

Consider the following guidelines when adding and creating tools:

-   Design tools to work together. Each AI agent should solve a specific, discrete task, and its tools should provide the capabilities needed to reach that goal.
-   Write detailed tool descriptions. The AI agent uses tool descriptions to understand what each tool does. Clear, thorough descriptions give the AI agent the best chance to succeed.
-   Plan for tool outputs when creating them. Use the tool description or output transformation strategy fields to explain how to process the tool outputs. For example, if a tool retrieves records from multiple tables, specify how to handle the large volume of results.

**Note:** If you select Google as your web search tool provider, the web search tool leverages [Grounding with Google Search](https://cloud.google.com/vertex-ai/generative-ai/docs/grounding/grounding-with-google-search), offered under a Global Standard deployment. Because grounding isn't [data resident](https://cloud.google.com/vertex-ai/generative-ai/docs/security-controls), Google's global infrastructure routes traffic to a global datacenter for each web search request. This processing may be different than your data processing location chosen for your ServiceNow instance. Consider your organization's data policies before enabling AI agents that use Google web search tools.

After you add the tools to your AI agent, scroll down to the next step in the guided setup.

## Knowledge graphs

You can also add Knowledge graphs in this step. Knowledge graphs provide the AI agent with information about relationships between real-world entities, which improves its outputs. For example, you could add a Knowledge Graph to an approval AI agent that maps users to their location, company, and department, helping the AI agent apply the correct approval process.

\[Omitted image "add-tools-2.png"\] Alt text: Knowledge Graph options

## Supervised vs. autonomous execution mode for AI agents

-   **Autonomous**

    The tool runs as soon as the agent selects it, with no prompt and no opportunity to intervene. Appropriate for read operations and low-consequence updates.

-   **Supervised**

    The agent pauses and asks a person to approve the action before the tool runs. Nothing happens until someone responds, so a supervised tool in a background or unattended execution stalls rather than proceeds. Use it for anything that writes, deletes, contacts a customer, or spends budget.


Execution mode is set per tool and can be changed at any time in the guided setup. A mode set during a build conversation can be set after the initial draft. See [Modify an AI agent.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-ai-agent-new.md)

You can reduce the risk of an AI agent executing unexpectedly by configuring its tools to run in supervised mode. Supervised mode means that tools use human oversight during execution. Use supervised mode to enhance security for agents that perform sensitive or critical actions.

You can set the supervised execution mode when creating a tool in the AI agent guided setup. For example, select **Supervised** as the **Execution mode** when adding a catalog item tool. For reference, see [Add a catalog item to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-catalog-ai-agent.md).

