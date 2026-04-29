---
title: Configuring Now Assist for Creator
description: To get started using Now Assist for Creator, install Now Assist for Creator. Then turn on the skills, AI agents, or agentic workflows that you want to use.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Now Assist for Creator, create with Now Assist, Configure Now Assist for Creator, Install Now Assist for Creator, Creator Workflow, Creator Pro Plus, Build Agent, Flow generation, App generation]
breadcrumb: [Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Configuring Now Assist for Creator

To get started using Now Assist for Creator, install Now Assist for Creator. Then turn on the skills, AI agents, or agentic workflows that you want to use.

## Installing Now Assist for Creator

Check your company's entitlements to verify that you have access to Now Assist for Creator. To start using Now Assist for Creator, you must request it from the ServiceNow® Store. Once approval has been granted, you can install it on your instance. See [Install Now Assist for Creator](../../../administer/flow-designer/task/install-now-assist-for-creator.md) for more information.

## Activating AI capabilities

After installing Now Assist for Creator, you must turn on the AI capabilities that you want to use. Some AI capabilities are turned on by default, such as the Now Assist for Code skills, including code assist summarization, code assist edit, and code assist generation, and code assist autocomplete. Capabilities that aren't on by default must be turned on or activated in order to use them.

You can turn on Now Assist for Creator skills in the Now Assist Admin console. When you turn on a skill, you might have to complete additional configuration steps, such as assigning roles and restrictions for who can access the skill. See the product documentation for the skill that you want to activate for additional configuration steps.

![Now Assist for Creator skills inside the Now Assist Admin console, where you can turn skills on and off.](../image/nafc-turn-on-skill.png "Now Assist for Creator skills in the Now Assist Admin console")

AI agents and agentic workflows are activated in AI Agent Studio. When you activate an AI agent or agentic workflow, you might have to complete additional configuration steps, such as selecting a large language model \(LLM\) for the AI agent or agentic workflow and assigning roles and restrictions. See the product documentation for the AI agent or agentic workflow that you want to activate for additional configuration steps.

![Now Assist for Creator AI agents in AI Agent Studio, where you can activate and manage AI agents.](../image/nafc-ai-agents-and-workflows.png "Now Assist for Creator AI agents in AI Agent Studio")

## Required roles

To use Now Assist for Creator, you might need specific roles. Some roles are specific to the tool that the capability is embedded in, such as catalog\_builder\_editor to use the catalog item generation skill in Catalog Builder, or flow\_designer to use the flow generation skill.

Other roles might be required for Now Assist experiences, such as the now\_assist\_panel\_user role for creating applications in ServiceNow Studio with the app generation skill.

Now Assist for Creator has its own role, now.assist.creator, which might be required for using some Now Assist for Creator capabilities. See [Now Assist for Creator \[now.assist.creator\] role](../../../administer/creator/reference/creator-roles-1.md) for more information.

To learn what roles are required for the Now Assist for Creator AI capability you want to use, see the product documentation for the capability.

