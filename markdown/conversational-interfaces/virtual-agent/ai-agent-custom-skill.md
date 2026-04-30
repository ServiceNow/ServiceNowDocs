---
title: Using AI agents in Virtual Agent topics
description: Use an AI agent custom skill to have it perform a task passed to it, such as compiling info on a KB article.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Virtual, Agent, designer, AI, agent, connector, utility]
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Using AI agents in Virtual Agent topics

Use an AI agent custom skill to have it perform a task passed to it, such as compiling info on a KB article.

There may be AI agents installed with the Now Assist application that are not used in use cases. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

An AI agent performs a task that you pass to it inside the AI Connector utility in Virtual Agent Designer. For more information on the AI Connector utility, see [AI Connector utility](../../virtual-agent/reference/vad-ai-connector-utility.md).

For example, you can use the AI Agent in the AI Connector utility to get all data on a Knowledge Base article. The AI Agent provides the article if it is available or notifies you if it can't find it. The agent also provides data on the consolidation itself by way of its output mappings.

To see which AI agents are installed on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

To use the AI agent, select it from the **Skill type** drop-down list in the AI Connector utility, then select the AI agent's type from the **Select AI agent** drop-down. For example, to have the AI agent consolidate a knowledge base article, select **KB content consolidation AI agent**.

Define the task for the AI agent by placing a value in the **Task** input mapping variable. You can define a condition, or enter a script or command. For example, enter `return KB00090;` to have the AI agent retrieve that knowledge base article and consolidate its information into a reply in the Virtual Agent chat.

The AI agent's output mapping properties are automatically defined when you select the AI agent type. All output mappings are returned in the chat when the AI agent completes the task.

![Select the AI agent and its task type inside the AI Connector utility.](../../virtual-agent/images/ai-agent-in-connector-utility.png)

|Variable|Description|
|--------|-----------|
|Execution plan ID|ID number of the execution plan.|
|Execution state|Current state of the execution plan.|
|Objective|Intended task for the execution plan.|
|State reason|Reason for the execution plan's current state.|
|Messages|List of messages sent through the execution plan.|
|Execution tasks|List of tasks in the execution plan.|
|Execution tools|List of tools in the execution plan.|

When the AI agent performs its job, it generates the full plan showing the input and output mappings. Each plan shows the objective, all tasks performed for the objective, and any messages sent or tools used in the plan. All plans are listed in the Execution Plan \[sn\_aia\_execution\_plan\_list\] table.

![Execution plan for consolidating KB00090.](../../virtual-agent/images/ai-agent-execution-plan.png)

**Parent Topic:**[Getting started with Virtual Agent Designer](../../virtual-agent/reference/conversation-designer-virtual-agent.md)

