---
title: Set a provider for a generative AI capability
description: Configure LLM providers for Generative AI Controller at the backend level. For most use cases, configure capabilities using AI Admin Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/generative-ai-controller/configure-a-provider-for-a-generative-ai-capability.html
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, AI Admin Hub, Enable AI experiences]
---

# Set a provider for a generative AI capability

Configure LLM providers for Generative AI Controller at the backend level. For most use cases, configure capabilities using AI Admin Hub.

## Before you begin

Configure your credentials for your preferred provider. See [Configuring API credentials for generative AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/configuring-api-credentials-for-generative-ai-capabilities.md) for more details.

Role required: admin

## About this task

Use this procedure to configure LLM providers at the OneExtend Capability level. Generative AI capabilities are configured using the AI Admin Hub, which is the recommended approach. This procedure is for backend configuration when you need to manage custom OneExtend configurations.

## Procedure

1.  In the navigation filter, search for the OneExtend Capability table by entering `sys_one_extend_capability.list`.

2.  In the OneExtend Definition Configs related list, set **Default** to `true` for your preferred capability provider.

    **Note:** By default, you can choose only one provider for a capability. For example, if **Default** is `true` for Sentiment \(OpenAI Completion\), you must set **Default** to `false` before changing **Default** to `true` for Sentiment \(Azure OpenAI\).

    \[Omitted image "gai-configure-providers.png"\] Alt text: Default builder config open with builder capability related list. The capability records and default column are highlighted.

<table><thead><tr><th>

Capability Definition

</th><th>

Model

</th></tr></thead><tbody><tr><td>

-   OpenAI Completion
-   Azure OpenAI Completion


</td><td>

GPT-3

</td></tr><tr><td>

-   OpenAI Chat Completion
-   Azure OpenAI Chat Completion


</td><td>

GPT-3.5

</td></tr><tr><td>

-   GPT4 \(OpenAI Chat Compl\)
-   GPT4 \(Azure OpenAI Chat Compl\)


</td><td>

GPT-4

</td></tr><tr><td>

-   AI Studio \(Google Cloud Completion\)
-   AI Studio \(Google Cloud Chat Completion\)
-   Vertex AI \(Google Cloud Completion\)
-   Vertex AI \(Google Cloud Chat Completion\)


</td><td>

Google Gemini

</td></tr><tr><td>

IBM watsonx

</td><td>

Granite

</td></tr></tbody>
</table>
## Result

The provider configuration is applied at the OneExtend Capability level and is available for use by generative AI capabilities in your instance.

## What to do next

To configure generative AI capabilities through the standard approach, see , [AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md), and [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

