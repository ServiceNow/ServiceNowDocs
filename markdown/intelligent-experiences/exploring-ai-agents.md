---
title: Exploring Now Assist AI agents
description: Learn how the Now Assist AI agents application can help to improve live agent productivity by using AI agents to perform tasks. AI agents simulate human-like intelligence to handle various tasks that range from automated responses to complex problem solving.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 6
keywords: [AI Agents, Agentic AI]
breadcrumb: [Now Assist AI agents, Enable AI experiences]
---

# Exploring Now Assist AI agents

Learn how the Now Assist AI agents application can help to improve live agent productivity by using AI agents to perform tasks. AI agents simulate human-like intelligence to handle various tasks that range from automated responses to complex problem solving.

## Now Assist AI agents terminology

-   **Agentic system**: An [agentic system](../reference/na-aia-glossary.md#) is a type of software or AI that perceives its environment, decides that are based on that perception, and takes actions to achieve specific goals, often with minimal human intervention. An agentic system can learn, adapt, and operate independently to solve problems or perform tasks.
-   **AI agent**: On the ServiceNow AI Platform agentic system, an AI agent contains a set of large language model \(LLM\) instructions with the tools to perform these specific tasks.
-   **Agentic workflow**: In the agentic system on your instance, an agentic workflow contains a set of LLM instructions with one or more AI agents that can execute an objective.

## AI agents overview

The Now Assist AI agents application is designed to securely leverage your data, workflows, and integrations natively on the ServiceNow AI Platform. AI agents can dynamically adjust the actions that are based on the progress and changing conditions of incidents or cases to help ensure that they stay focused on achieving their objectives.

Use AI agents to do the following tasks for your organization:

-   Dynamically figure out a plan to resolve an incident or case.
-   Collaborate with other AI agents for subtasks as needed.
-   Take feedback from humans as needed.
-   Work on knowledge-intensive tasks that need information, understanding, and skills to accomplish that task.
-   Find a solution by using multiple sources of knowledge or similar incidents.
-   Plan to solve an issue with human collaboration.
-   Avoid iterations and discovery by defining a specific flow.

You can create, duplicate, or modify agentic workflows. You must activate the base system agentic workflows before they can be used. For more information about activating an agentic workflow, see [agentic workflow template](../task/activate-aia-use-case.md). For more information about cloning an agentic workflow, see [Clone an agentic workflow](../task/clone-aia-usecase.md).

The base system agentic workflows remain read only. You must duplicate them to use them. For more information about cloning an agentic workflow, see [Clone an agentic workflow](../task/clone-aia-usecase.md). You can modify the duplicated base system agentic workflow to meet your requirements. For more information, see [Modify an agentic workflow](../task/modify-aia-use-case.md). You must activate the base system agentic workflows before they can be used. For more information about activating an agentic workflow, see [agentic workflow template](../task/activate-aia-use-case.md).

## AI agents configuration and execution

![Workflow describing the configuration of Now Assist AI agents and how they work to execute an agentic workflow.](../image/now-assist-ai-agents-workflow.png)

Now Assist AI agents have two components: AI agents and agentic workflows. By using Guided Setup in AI Agent Studio, you create AI agents and workflows, add tools or define triggers, and define the availability or display location. After they're created, you can duplicate, modify, and test them in AI Agent Studio.

In run time, triggers in the primary and secondary interfaces cause agentic workflow execution, where one or more AI agents execute the plan with the help of the AI Agent Orchestrator to accomplish the task. After agentic workflow execution, the output appears in the Now Assist panel. To learn more about what an AI Agent Orchestrator is, see the [Now Assist AI Agents Orchestrator](exploring-ai-agents.md#section_hvq_fd3_k2c) section in this topic.

## How to put Now Assist AI agents to work

AI agents can use a variety of tools, such as web searches, record operations, and flows, to work on agentic workflows that you define.

Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview** &gt; **Get an overview of what to expect** and select **View steps** to see how you can successfully put your AI agents to work.

1.  Create an agentic workflow: agentic workflows define the problem and situation that you want your AI agents to work on. Without an agentic workflow, your agents don’t know when or what to work on.
2.  Create AI agents: AI agents use tools to execute tasks. Consider the tasks needed to solve the agentic workflow you created. Create one or more agents to execute those tasks.
3.  Test the agentic workflow: See how your AI agents perform. Make adjustments to either the agentic workflow or AI agents. Test until everything’s working the way you want.
4.  Deploy: Put your AI agents to work across your organization.

## Now Assist AI agents Orchestrator

You can use the AI Agent Orchestrator to verify that your AI agent teams work together and track agentic workflows across the enterprise.

The AI Agent Orchestrator in the agentic framework is a coordinator entity that handles collaboration across multiple agents by routing requests from one agent to other agents to help accomplish a complex task. The AI Agent Orchestrator can also reach out to one of the agents involved in the task accomplishment to get the missing context or information from the user for task completion.

AI agents don’t work in isolation. If they get stuck or fail completing a task, they can go back to the AI Agent Orchestrator and ask for help, using the iterative aspect of the AI agents.

## Citations in Now Assist AI agents

When you execute AI agents and agentic workflows in Now Assist AI agents, you can see citations on the Now Assist panel by default that provide summaries to get similar incidents and relevant knowledge articles.

Generating citations:

-   Citations are generated by the LLM \(Large Language Model\), which use the information available to it.
-   URLs can’t be generated by LLM if relevant information isn’t provided.
-   LLMs need provide proper URLs for better results.
-   Citation URLs return directly from the tool’s outputs.
-   The LLM is instructed not to generate or assume citations if they aren’t present.

**Note:** Invalid or malformed URLs won’t be displayed to the user.

Citations with similar incidents and relevant knowledge articles appear in the Sources section of the AI Agent Studio Chat and on the Now Assist panel and in with click-able links that direct you to the incident or knowledge article.

![Citations in the output of an executed agentic workflow with sources on AI Agent Studio.](../image/aia-citations.png)

![Citations in the output of an executed agentic workflow with sources on the Now Assist panel.](../image/aia-citations-nap.png)

You can hide citations for specific agentic workflows or AI agents where it’s necessary or confidential. For more information, see [Disable citations in AI Agent Studio](../task/aia-hide-citations.md).

## User impersonation in Now Assist AI agents

The agentic workflow executes tools as the logged-in user in the Now Assist panel. Any operations that are performed within the tool in this flow are also executed as the logged-in user. After impersonation is enabled, testing an AI agent uses the instance-level impersonation.

Administrators can see logs with individual AI agent names as a record of who approved the agentic action in an agentic workflow. The logs help when determining a point of contact if there’s an issue with the approved agentic action by the AI agent.

With impersonation, the fulfiller in the Now Assist panel and the requester in Virtual Agent can see the transactions recorded in the name of the AI agent that performed the agentic workflow execution.

