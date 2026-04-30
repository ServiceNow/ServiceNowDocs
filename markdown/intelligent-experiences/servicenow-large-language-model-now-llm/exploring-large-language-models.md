---
title: Large language models on the ServiceNow AI Platform
description: ServiceNow AI Platform utilises large language models \(LLM\) for generative AI and agentic AI functionality. You can choose the ServiceNow LLM or supported third-party models. LLMs bring about the Generative AI application capabilities by understanding and generating human language, and processing vast amount of data.
locale: en-US
release: yokohama
product: ServiceNow Large Language Model \(Now LLM\)
classification: servicenow-large-language-model-now-llm
topic_type: concept
last_updated: "2025-06-30"
reading_time_minutes: 3
breadcrumb: [Enable AI experiences]
---

# Large language models on the ServiceNow AI Platform

ServiceNow AI Platform® utilises large language models \(LLM\) for generative AI and agentic AI functionality. You can choose the ServiceNow® LLM or supported third-party models. LLMs bring about the Generative AI application capabilities by understanding and generating human language, and processing vast amount of data.

## Third-party model strategy

ServiceNow® supports third-party AI model providers, which signifies that the admin persona can select a third-party large language or an AI model provider for Now Assist skills that are available out of box. The Now LLM Service is the default LLM. Find the supported model providers, the LLM services and the version.

|Model provider|Large language model|Version|Deployment policy|
|--------------|--------------------|-------|-----------------|
|ServiceNow®|Now LLM Service|Latest update for your instance|Default|
|Microsoft Azure|Azure OpenAI|OpenAI GPT-4.1 and GPT-4.1-mini|[https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/deployment-types\#global-standard](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/deployment-types#global-standard)|
|Google|Google Gemini|Gemini 2.5 Flash and 2.5 Pro|[https://cloud.google.com/vertex-ai/generative-ai/docs/learn/locations](https://cloud.google.com/vertex-ai/generative-ai/docs/learn/locations)|
|AWS|AWS Claude|Claude 3.7 Sonnet|[https://docs.aws.amazon.com/bedrock/latest/userguide/models-regions.html](https://docs.aws.amazon.com/bedrock/latest/userguide/models-regions.html)|

**Note:** Some out of box skills, Agents, and Agentic Workflows do not support Now LLM Service or third party model providers. To learn more about the exceptions to LLM service and third party model providers support, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB2222333](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2222333)

## Large language model selection

This selection is supported at various levels such as, skill, skill group and instance levels. However, the controls that define LLMs mapping to different skills, allowed at various global locations, are configured and approved in AI Control Tower by the AI steward. The model provider options for custom skills created in Now Assist skill kit and AI Agent Studio are also configured in AI Control Tower.

The **Manage large language models** feature enables the admin persona to perform additional actions like:

-   Edit the model provider at the instance, skill group and skill levels
-   Deactivate active skills which are non-compliant with fallback as **No**. See [Explore AI model providers](../../ai-governance-workspace/concept/ai-model-providers.md) to learn more.
-   View audit history on policy updates by AI steward in AI Control Tower
-   Select allowed model providers across domain separated instances.

See [Manage large language models](../../now-assist-admin/task/manage-large-language-models.md) to learn about managing.

For more information on selecting and updating model providers, see [Edit model providers](../../now-assist-admin/task/edit-model-providers.md).

-   **[Now LLM Service updates](../../now-assist-platform/reference/now-llm-model-updates.md)**  
The Now LLM Service provides access to specialized large language models \(LLMs\) that are developed by ServiceNow. It also provides access to open-source LLMs that are selected, configured, or enhanced by ServiceNow, from the ServiceNow community and partners. Review these reference materials and model cards for additional information about the Now LLM Service and about the models used.
-   **[General guidelines for writing instructions for generative AI large language models \(LLMs\)](../../now-assist-platform/concept/llm-instruction-guidelines.md)**  
When using Now Assist products and skills, you may have the option to give specific instructions or other guidance to the LLM. Writing generative AI instructions is different from conducting a keyword search. Use the following general guidelines when crafting your instructions.
-   **[Discrepancies when using different AI search tools](aisearch-differences.md)**  
Different AI search tools may return different answers for the same or similar searches. This difference in results is expected. It occurs because each large language model \(LLM\) uses a different approach to find results and generate answers that match your search.
-   **[Long term stable models](long-term-stable-models.md)**  
Long term stable \(LTS\) models support regulated industries, such as financial institutions, with stronger AI lifecycle management, governance, transparency, and compliance tools.

**Parent Topic:**[Enable AI experiences](../reference/ai-products.md)

