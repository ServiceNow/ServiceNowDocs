---
title: Large language models and providers
description: Large language models \(LLMs\) power every Now Assist generative AI capability. Understand how LLMs work on the ServiceNow AI Platform, choose model providers, and write effective instructions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-large-language-models-providers.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [large language models, LLM, Now LLM Service, model providers, long-term stable models, prompt writing]
breadcrumb: [Enable AI Experiences]
---

# Large language models and providers

Large language models \(LLMs\) power every Now Assist generative AI capability. Understand how LLMs work on the ServiceNow AI Platform, choose model providers, and write effective instructions.

Large language models \(LLMs\) are the engine behind generative AI capabilities. Every skill, AI agent, and agentic workflow on the ServiceNow AI Platform relies on an LLM to interpret context, reason through tasks, and generate responses from your enterprise data.

## Large language models on the ServiceNow AI Platform

An LLM is a machine learning model trained on large datasets to generate text-based responses. Because LLMs are probabilistic rather than deterministic, the same prompt may produce slightly different outputs each time. Learning this characteristic helps you set appropriate expectations and design effective interactions with AI capabilities. To understand how LLMs generate responses and why their probabilistic nature shapes the way you design AI interactions, see [Large language models on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

## Now LLM Service

The ServiceNow AI Platform manages LLM interactions through Now LLM Service, which provides access to optimized models hosted by ServiceNow. Now LLM Service handles model selection, routing, and updates so that AI capabilities on your instance stay current without manual model management. Long-term stable \(LTS\) model options are available for organizations that require predictable behavior over extended periods, such as those in regulated industries. To use hosted models that handle selection, routing, and updates for you, including long-term stable models for regulated environments, see [Model provider updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/now-llm-model-updates.md).

## Writing effective instructions

How you write instructions and prompts for an LLM directly affects the quality of its output. General guidelines for writing effective instructions help you craft clear, specific prompts that produce consistent, useful results. These guidelines apply whether you're configuring base system skills, building custom skills with AI Skill Kit, or defining instructions for AI agents. To write clear, specific instructions that produce consistent results across skills, AI Skill Kit, and AI agents, see [General guidelines for writing instructions for generative AI large language models \(LLMs\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/llm-instruction-guidelines.md).

## Providers and models

The ServiceNow AI Platform supports third-party model providers and the Now LLM Service. Configure provider connections, create model records, and understand the capabilities and constraints, such as context windows and token limits, that affect how AI features perform on your instance.

**Note:** If you notice inconsistencies in AI-generated results when using different search tools on your instance, refer to the topic on discrepancies when using different AI search tools.

To connect third-party model providers, create model records, and work within context-window and token limits, see [Providers and Models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/providers-and-models.md).

