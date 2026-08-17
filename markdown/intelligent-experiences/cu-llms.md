---
title: Large language models used by Content Understanding
description: The Content Understanding application uses large language models \(LLMs\) to support generative AI and agentic AI capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cu-llms.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, Document Intelligence]
breadcrumb: [Reference, Content Understanding, Enable AI experiences]
---

# Large language models used by Content Understanding

The Content Understanding application uses large language models \(LLMs\) to support generative AI and agentic AI capabilities.

## Available LLMs

You can select the LLM when creating a use case. The LLM can also be selected for the AI agent to use when processing documents and images.

Multimodal LLMs support image mode by processing multiple types of inputs — such as text, sound, and images — to generate a text response. Processing may take longer for image inputs.

**Note:** The Content insights AI agent requires a multimodal LLM. The text-only Now LLM Service is not supported for the AI agent.

AI-generated outputs may be inaccurate or incomplete. Review all AI-generated content before use.

The following table lists the available LLMs for Content Understanding.

|LLM|Highlights|
|---|----------|
|Now LLM Service - Large|Text-only model that supports natural language understanding, automation, and decision support.|
|Now LLM Service - Small|Text-only model that enhances text-based automation and content generation in ServiceNow workflows.|
|Google Cloud - Gemini Large|Multimodal model with advanced reasoning and problem-solving capabilities.|
|Google Cloud - Gemini Small|Multimodal model with strong performance in summarization, rewriting, and content transformation.|
|Azure OpenAI - GPT Large|Multimodal model with strong performance on tasks involving analysis, summarization, and multi-step problem solving.|
|Azure OpenAI - GPT Small \(default\)|Multimodal model optimized for routine workflows, including summarization, paraphrasing, and question and answer tasks.|
|Amazon Bedrock - Claude Large|Multimodal model with strong context management for long documents and dialogs.|
|Amazon Bedrock - Claude Small|Multimodal model with lower latency and higher efficiency for real-time applications.|

For more information, see [Large language models on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

**Parent Topic:**[Content Understanding Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/content-understanding-reference.md)

