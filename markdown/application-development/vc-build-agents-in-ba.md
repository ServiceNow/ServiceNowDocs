---
title: Creating custom agentic workflows, in-app agents, and skills with Build Agent
description: Use Build Agent to create and deploy custom agentic workflows, AI agents, and skills that add agentic experiences to your ServiceNow custom applications, supported by the built-in governance framework.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Build Agent overview, Develop, Vibe coding and AI-assisted development, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Creating custom agentic workflows, in-app agents, and skills with Build Agent

Use Build Agent to create and deploy custom agentic workflows, AI agents, and skills that add agentic experiences to your ServiceNow custom applications, supported by the built-in governance framework.

The vibe coding capabilities in Build Agent extend beyond building applications. You can use the same intent-driven approach to create custom AI agents, design agentic workflows that orchestrate multi-step automated processes, and build skills directly within your ServiceNow environment. You don't need to specify whether you want to build an agent, a workflow, or a skill. Instead, describe the business problem or outcome you want to achieve, and Build Agent determines the appropriate components to generate. Depending on your requirements, it may create an agentic workflow, one or more agents, a set of skills, or a combination of all three.

Before generating any new components, Build Agent scans your instance for existing agents, skills, and workflows that may already satisfy your requirements. If there are matches, Build Agent proposes using the existing components or creating new ones, so you can reuse what's already available before adding to your instance. In each case, Build Agent uses your instance's existing tables, roles, permissions, and automation patterns as context.

All you need to do is describe the business problem you want to solve, and Build Agent determines whether to build an agentic workflow, an agent, or set of skills, and identifies the tools required. Drawing on its understanding of your application context, Build Agent handles the complexity of agent creation for you, with no prior knowledge required and significantly less development time.

As part of the agent and skill creation process, Build Agent guides you through defining access controls and permissions alongside the agent itself, keeping governance integrated from the start. Once created, you can test and activate the agent in AI Agent Studio, then monitor and govern it in AI Control Tower.

**Note:** You need Now Assist for App Engine to create agents and skills. For more information, see [Now Assist for App Engine](../../app-engine-studio/concept/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md).

## Custom in-app agents

Build Agent reads your application's files to understand the context, then plans and creates agents and skills tailored to your app's specific use case. For example, Build Agent can identify manual tasks within your application that are candidates for automation, then plan and build a custom agent to handle them autonomously, no code required. Once created, the agent is available in AI Agent Studio for testing, trigger setup, and further configuration.

## Agentic workflows

Build Agent can generate agentic workflows that coordinate sequences of automated actions across your ServiceNow instance. Rather than scripting individual steps, you describe the end-to-end process you want to automate, and Build Agent produces a flow that connects agents, triggers, and actions in a coherent sequence. This context-awareness sets the ServiceNow approach apart from generic AI development tools: Build Agent understands constructs specific to ServiceNow to produce flows that are meaningfully integrated into the ServiceNow AI Platform.

## Skills

Build Agent can generate custom skills scoped to your application's data model, without manually authoring skill definitions. You describe what you want the skill to do, and Build Agent creates skills that align with your existing table structure, field configurations, and access controls.

You can create custom skills individually, that is, they don't need to be used as tools for an agent. Think of skills as custom instructions that you use when vibe coding to create a higher quality outcome. For more information, see Exploring Now Assist Skill Kit.

## Helpful resources

Some ServiceNow resources that can provide you with helpful information are:

-   **[Create agentic workflows, agents, and skills](../../build-agent/tasks/create-custom-ai-agent.md)**

    Details on how to create custom agentic workflows, in-app agents, and skills with Build Agent.

-   **[Pro Developer Academy: Vibe Coding AI Agents Using prompts for In-App Agents](http://youtube.com/watch?v=UUSDuYnM_E8&list=PLkGSnjw5y2U4Td38CczvfDKxhcOuwg4CC&index=1)**

    Pro Dev Academy session recording on vibe coding in-app agents.


**Parent Topic:**[AI-assisted ServiceNow AI Platform development with Build Agent](vc-build-agent-landing.md)

