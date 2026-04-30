---
title: Large language models on the ServiceNow AI Platform
description: ServiceNow AI Platform utilizes large language models \(LLM\) for generative AI and agentic AI functionality. You can choose the ServiceNow LLM or supported third-party models. LLMs bring about the Generative AI application capabilities by understanding and generating human language, and processing vast amount of data.
locale: en-US
release: zurich
product: ServiceNow Large Language Model \(Now LLM\)
classification: servicenow-large-language-model-now-llm
topic_type: concept
last_updated: "2025-06-30"
reading_time_minutes: 3
breadcrumb: [Enable AI experiences]
---

# Large language models on the ServiceNow AI Platform

ServiceNow AI Platform® utilizes large language models \(LLM\) for generative AI and agentic AI functionality. You can choose the ServiceNow® LLM or supported third-party models. LLMs bring about the Generative AI application capabilities by understanding and generating human language, and processing vast amount of data.

## Third-party model providers

ServiceNow® supports third-party AI model providers, which signifies that the admin persona can select a third-party large language or an AI model provider for Now Assist skills that are available out of box. The Now LLM Service is the default LLM. Find the supported model providers, the LLM services and the version.

<table id="table_l55_qlf_xfc"><thead><tr><th>

Model provider

</th><th>

Large language model

</th><th>

Version

</th><th>

Deployment policy

</th></tr></thead><tbody><tr><td>

ServiceNow®

</td><td>

Now LLM Service

</td><td>

Latest update for your instance

</td><td>

Default

</td></tr><tr><td>

Microsoft Azure

</td><td>

Azure OpenAI

</td><td>

V2:OpenAI GPT 5.4, GPT-5.2, and GPT-5.2-mini

V1: GPT 4.1 and GPT 4.1 mini

</td><td>

[https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/deployment-types\#global-standard](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/deployment-types#global-standard)

</td></tr><tr><td>

Google

</td><td>

Google Gemini

</td><td>

Gemini 2.5 Flash and 2.5 Pro

</td><td>

[https://cloud.google.com/vertex-ai/generative-ai/docs/learn/locations](https://cloud.google.com/vertex-ai/generative-ai/docs/learn/locations)

</td></tr><tr><td>

AWS

</td><td>

AWS Claude

</td><td>

V2:-   Claude 4.6 Sonnet
-   Claude Haiku 4.5

V1: Claude 4.0 Sonnet

</td><td>

[https://docs.aws.amazon.com/bedrock/latest/userguide/models-regions.html](https://docs.aws.amazon.com/bedrock/latest/userguide/models-regions.html)

</td></tr></tbody>
</table>**Note:** Some out of box skills, Agents, and Agentic Workflows do not support Now LLM Service or third party model providers. To learn more about the exceptions to LLM service and third party model providers support, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB2222333](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2222333)

## Large language model selection

This selection is supported at various levels such as, skill, skill group and instance levels. However, the controls that define LLMs mapping to different skills, allowed at various global locations, are configured and approved in AI Control Tower by the AI steward. The model provider options for custom skills created in Now Assist skill kit and AI Agent Studio are also configured in AI Control Tower.

The **Manage large language models** feature enables the admin persona to perform additional actions like:

-   Edit the model provider at the instance, skill group and skill levels
-   Deactivate active skills which are non-compliant with fallback as **No**. See [Explore AI model providers](../../ai-governance-workspace/concept/ai-model-providers.md) to learn more.
-   View audit history on policy updates by AI steward in AI Control Tower
-   Select allowed model providers across domain separated instances.

See [Manage AI models](../../now-assist-admin/task/manage-large-language-models.md) to learn about managing.

For more information on selecting and updating model providers, see [Manage model providers](../../now-assist-admin/task/edit-model-providers.md).

-   **[Now LLM Service updates](../../now-assist-platform/reference/now-llm-model-updates.md)**  
The Now LLM Service provides access to specialized large language models \(LLMs\) that are developed by ServiceNow. It also provides access to open-source LLMs that are selected, configured, or enhanced by ServiceNow, from the ServiceNow community and partners. Review these reference materials and model cards for additional information about the Now LLM Service and about the models used.
-   **[General guidelines for writing instructions for generative AI large language models \(LLMs\)](../../now-assist-platform/concept/llm-instruction-guidelines.md)**  
When using Now Assist products and skills, you may have the option to give specific instructions or other guidance to the LLM. Writing generative AI instructions is different from conducting a keyword search. Use the following general guidelines when crafting your instructions.
-   **[Long term stable models](long-term-stable-models.md)**  
Long term stable \(LTS\) models support regulated industries, such as financial institutions, with stronger AI lifecycle management, governance, transparency, and compliance tools.
-   **[Discrepancies when using different AI search tools](aisearch-differences.md)**  
Different AI search tools may return different answers for the same or similar searches. This difference in results is expected. It occurs because each large language model \(LLM\) uses a different approach to find results and generate answers that match your search.
-   **[Providers and Models](providers-and-models.md)**  
You can bring your own large language model \(LLM\) provider and API to use with Now Assist.

**Parent Topic:**[Enable AI experiences](../reference/ai-products.md)

