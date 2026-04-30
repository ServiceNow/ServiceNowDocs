---
title: Select the LLM for AI agents and agentic workflows
description: Choose the large language model \(LLM\) service provider for Now Assist AI agents in AI Agent Studio.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [global LLM, AI agent LLM, use case LLM, agentic workflow LLM, GPT-4, GPT-4o, GPT4, GPT4o]
breadcrumb: [Configure, Now Assist AI agents, Enable AI experiences]
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

2.  Navigate to the **Model provider** tab.

3.  Select **Configure** to be redirected to Now Assist Admin.

4.  In the **Choose a default model provider** field, select

    Your choices are the following:

    -   Now LLM Service
    -   AWS Claude
    -   Azure OpenAI
    -   Google Gemini
5.  Review the impacted AI agents.

    Certain AI agents may require specific model providers. Select the AI agents tab in the **Impact overview** section to see which AI agents are affected by any changes to the model provider.

6.  Select **Save**.


## Result

Your chosen LLM is used globally for all AI agents and agentic workflows.

