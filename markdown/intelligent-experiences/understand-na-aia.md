---
title: Understand the Now Assist AI agents
description: The Now Assist AI agents application is designed to securely leverage your data, workflows, and integrations directly within the ServiceNow AI Platform. AI agents can dynamically adjust their actions based on the progress and changing conditions of incidents or cases to help ensure that they stay focused on achieving their objectives.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-10-24"
reading_time_minutes: 2
breadcrumb: [Explore, Now Assist AI agents, Enable AI experiences]
---

# Understand the Now Assist AI agents

The Now Assist AI agents application is designed to securely leverage your data, workflows, and integrations directly within the ServiceNow AI Platform. AI agents can dynamically adjust their actions based on the progress and changing conditions of incidents or cases to help ensure that they stay focused on achieving their objectives.

## Now Assist AI agents Orchestrator

The AI Agent Studio guides users in leveraging AI agents effectively, while AI Orchestrator ensures seamless collaboration among them. The AI agent Orchestrator is a central management system that coordinates AI agents to ensure that they collaborate effectively to complete complex workflows. It can also retrieve missing context from users when needed. AI agents operate iteratively, seeking assistance from the Orchestrator if they encounter difficulties. The Orchestrator enhances inter-agent communication and centralizes coordination. The Orchestrator allows AI agents to share information effectively and transition tasks seamlessly, regardless of where the process originates. As a result, the Orchestrator is essential for managing intricate workflows, facilitating real-time adaptability, and efficient task delegation among agents.

The role of Orchestrator in AI Agent Studio:

1.  Task Coordination &amp; Execution: manages the interaction between multiple **AI agents**, ensuring that tasks are executed in the correct sequence.
2.  Dynamic Decision-Making: Can invoke AI models dynamically based on the scenario.
3.  Seamless Integration with Enterprise Systems: Works with ServiceNow workflows, CMDB, and third-party APIs to enable end-to-end automation.
4.  Handling Multi-Step Workflows: Enables chained execution of AI-driven tasks among multiple AI Agents.
5.  Policy &amp; Governance Enforcement: Enforces governance rules to ensure that AI agents adhere to compliance and security standards.

The Orchestrator works with ReAct prompt, where the previous reflection prompt has been merged with the planning prompt for a streamlined execution experience improving the efficiency and visibility of planner actions. With the ReAct prompt, a scheduling mode called Route has been introduced that enables asynchronous, parallel tool execution within agents to reduce latency and improve performance when an agent needs assistance from another agent during the execution process.

## Dynamic Orchestrator for agentic workflows

The dynamic orchestrator helps map the right agents to the user's agentic workflow to provide better performance and accuracy. When there are more than the ideal 8 to 10 AI agents available for an agentic workflow, then the dynamic orchestrator helps identify the agents that need to be considered for executing that agentic workflow in the planning phase.

## User impersonation in Now Assist AI agents

The agentic workflow executes tools as the logged-in user in the Now Assist panel. Any operations that are performed within the tool in this flow are also executed as the logged-in user. After impersonation is enabled, testing an AI agent uses the instance-level impersonation.

Administrators can see logs with individual AI agent names as a record of who approved the agentic action in an agentic workflow. The logs help when determining a point of contact if there’s an issue with the approved agentic action by the AI agent.

With impersonation, the fulfiller in the Now Assist panel and the requester in Virtual Agent can see the transactions recorded in the name of the AI agent that performed the agentic workflow execution.

**Note:** Virtual Agent can be turned on only for AI agents at the Define availability section in the AI agent guided setup. For more information, see [Create an AI agent](../task/configure-next-best-action-agent.md).

