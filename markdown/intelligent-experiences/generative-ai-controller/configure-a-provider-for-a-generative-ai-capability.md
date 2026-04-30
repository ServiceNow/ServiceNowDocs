---
title: Set a provider for a generative AI capability
description: Determine which AI provider to use for each of the generative AI capabilities of Generative AI Controller.
locale: en-US
release: zurich
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Set a provider for a generative AI capability

Determine which AI provider to use for each of the generative AI capabilities of Generative AI Controller.

## Before you begin

Configure your credentials for your preferred provider. See [Configuring API credentials for generative AI capabilities](../concept/configuring-api-credentials-for-generative-ai-capabilities.md) for more details.

Role required: admin

## About this task

Generative AI Controller comes with four capabilities by default. You can only configure a provider for the capabilities listed in the table in step 2. If you have installed other Now Assist applications, you may see other capabilities on the OneExtend Capability table. Those other capabilities use the Now LLM Service as their provider and can't be reconfigured.

## Procedure

1.  In the navigation filter, search for the OneExtend Capability table by entering `sys_one_extend_capability.list`.

2.  Open the record for the capability that you would like to configure, such as Sentiment Analysis.

<table><thead><tr><th>

Capability

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Generate Content

</td><td>

Generate texts about a given topic with Workflow Studio and Virtual Agent Designer.

</td></tr><tr><td>

Generic Prompt

</td><td>

Create your own use case and prompt.

</td></tr><tr><td>

Sentiment Analysis

</td><td>

Analyze user sentiment with Workflow Studio and Virtual Agent Designer.

</td></tr><tr><td>

Summarize

</td><td>

Create summaries of topics with Workflow Studio and Virtual Agent Designer.

</td></tr></tbody>
</table>3.  In the OneExtend Definition Configs related list, set **Default** to `true` for your preferred capability provider.

    **Note:** By default, you can choose only one provider for a capability. For example, if **Default** is `true` for Sentiment \(OpenAI Completion\), you must set **Default** to `false` before changing **Default** to `true` for Sentiment \(Azure OpenAI\).

    ![Default builder config open with builder capability related list. The capability records and default column are highlighted.](../image/gai-configure-providers.png)

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

Aleph Alpha Completion

</td><td>

Luminous

</td></tr><tr><td>

IBM watsonx

</td><td>

Granite

</td></tr></tbody>
</table>
## Result

Flows, topics, and scripts that use the generative AI capability use the provider you've specified.

**Related topics**  


[Bring your own key for third-party AI provider integration](../concept/byok-for-azure-open-ai.md)

[Configure a custom resource path for BYOK models](configure-custom-resource-path-byok.md)

