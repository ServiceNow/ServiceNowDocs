---
title: Select the LLM for AI agents and agentic workflows
description: Choose the large language model \(LLM\) service provider for Now Assist AI agents in AI Agent Studio.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-04-05"
reading_time_minutes: 1
keywords: [global LLM, AI agent LLM, use case LLM, agentic workflow LLM, GPT-4, GPT-4o, GPT4, GPT4o]
breadcrumb: [Configuring Now Assist AI agents, Now Assist AI agents, Enable AI experiences]
---

# Select the LLM for AI agents and agentic workflows

Choose the large language model \(LLM\) service provider for Now Assist AI agents in AI Agent Studio.

## Before you begin

Role required: sn\_aia.admin

## About this task

LLMs are part of the foundation of agentic AI. Different LLMs can provide slightly different performance and responses. You can select which LLM to use at a global level for agentic AI from the AI Agent Studio to help adjust the response quality to best fit your agentic workflows.

**Note:** If you already have agents built and you change the global LLM, then you must test the agents after making the change.

Depending on your region, you may have to consent to using a different service provider.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings**.

2.  Navigate to the **Manage LLMs** tab.

3.  In the provider field dropdown, select your LLM provider.

    Your choices are the following:

    -   Azure OpenAI
    -   Now LLM Generic
    If you use Azure OpenAI, then Virtual Agent is able to discover AI agents in conversations. If Now LLM Generic is enabled, then AI agent discovery isn’t available.

4.  Select **Save** to save your changes.


## Result

Your chosen LLM is used globally for all AI agents and agentic workflows.

