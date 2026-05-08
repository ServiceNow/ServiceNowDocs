---
title: Bring your own key for third-party AI provider integration
description: The bring your own key \(BYOK\) feature enables you to use your own API credentials from supported cloud AI providers, such as Azure OpenAI, Amazon Bedrock, and Google Gemini, to run Now Assist skills and AI agents.
locale: en-US
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: concept
last_updated: "2026-01-12"
reading_time_minutes: 2
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Bring your own key for third-party AI provider integration

The bring your own key \(BYOK\) feature enables you to use your own API credentials from supported cloud AI providers, such as Azure OpenAI, Amazon Bedrock, and Google Gemini, to run Now Assist skills and AI agents.

When BYOK is enabled, Now Assist sends model requests through your cloud AI provider account instead of ServiceNow AI Platform infrastructure. This approach lets you maintain ownership of your AI configuration, security controls, and data processing environment while continuing to use Now Assist capabilities.

BYOK supports the same AI models that the ServiceNow AI Platform supports. After you configure your API credentials, Now Assist uses your provider resources to process requests instead of using the default ServiceNow AI provider. BYOK keeps your keys under your control and AI workloads running within your cloud environment.

**Note:** Using your organization’s cloud AI provider account might result in additional charges from that provider. Review the provider’s pricing and terms of service before enabling BYOK.

## ServiceNow integrated model providers

BYOK supports the following cloud AI providers:

-   Azure OpenAI
-   Anthropic Claude on AWS, which is accessible through Amazon Bedrock
-   Google Gemini

## Configuring a BYOK connection with a cloud AI provider

To use your cloud AI provider resources within your ServiceNow instance, configure a connection between ServiceNow and your provider. Configuration steps vary by provider, but follow a similar high-level configuration workflow as the following steps:

1.  Create connection and credentials for the provider, such as endpoint, API key, and region.
2.  Enable BYOK for the provider in Now Assist Admin.
3.  Map ServiceNow model aliases to provider model versions. For example, map `gemini_large` → 2.5 Pro.
4.  Optionally, override variants in each skill in Version Management.
5.  Validate that requests are using your AI provider account by reviewing outbound HTTPS logs.

For step-by-step instructions for each supported cloud AI provider, see [Configure Bring Your Own Key \(BYOK\) for Now Assist and AI Agents \[KB2666298\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2666298) article in the Now Support Knowledge Base.

## High-level BYOK configuration for Azure OpenAI

1.  Set up Azure OpenAI connection with your own key to use Azure OpenAI within your ServiceNow instance.

    For more information, see [Configure API credentials for Azure OpenAI](../task/configure-api-credentials-for-azure-openai.md).

2.  Configure your Azure OpenAI model and deployment name in Generative AI Controller so your ServiceNow instance can recognize and use it.

    For more information, see Create a custom embedding model.

3.  Modify the prompt configuration to write your own prompts to send to the Azure OpenAI LLMs.

    For more information, see [Configure a generic large language model \(LLM\) connector](../task/configure-a-generic-llm-connector.md).

4.  Switch providers to use BYOK for AI processing.

    For more information, see [Manage Integration](../../now-assist-admin/task/manage-integration.md).


**Related topics**  


[Configure a custom resource path for BYOK models](../task/configure-custom-resource-path-byok.md)

