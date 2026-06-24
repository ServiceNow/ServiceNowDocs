---
title: Select the LLM for AI agents and agentic workflows
description: Choose the large language model \(LLM\) service provider for Now Assist AI agents in AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/select-aia-llm.html
release: zurich
topic_type: task
last_updated: "2026-03-12"
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

**Note:** If you already have agents built and you change the global LLM, then you must test the agents after making the change. You can test the models in the skill kit without changing the LLM provider for all Now Assist AI agent skills. Outside of the Skill kit, skills use whichever provider is set as default for the AI AGent SKills group.

Depending on your region, you may have to consent to using a different service provider.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Settings**.

2.  Navigate to the **Model provider** tab.

3.  Select **Configure** to be redirected to Now Assist Admin.

4.  In the **Choose a default model provider** field, select from the following choices.

    -   Now LLM Service
    -   AWS Claude
    -   Azure OpenAI
    -   Google Gemini
    -   Amazon Bedrock
    The new generative AI Config property records **sys\_generative\_ai\_config** and **sys\_generative\_ai\_prompt\_config** have been introduced for the following model providers:

    -   Amazon Bedrock: claude-sonnet-4-6
    -   Azure OpenAI: gpt 5.4
    Both the properties share a **definition** field that references the same **sys\_one\_extend\_capability\_definition** record, which identifies the LLM provider.

    **Note:** THe new prompt config records are set to **true** by default.

5.  To use a different model provider:

    1.  Navigate to the **sys\_generative\_ai\_prompt** table.

    2.  Filter and group by the relevant skill definition.

    3.  Locate the record for the appropriate skill and provider.

    4.  Set the preferred record as default.

6.  Review the impacted AI agents.

    Certain AI agents may require specific model providers. Select the AI agents tab in the **Impact overview** section to see which AI agents are affected by any changes to the model provider.

7.  Select **Save**.


## Result

Your chosen LLM is used globally for all AI agents and agentic workflows.

