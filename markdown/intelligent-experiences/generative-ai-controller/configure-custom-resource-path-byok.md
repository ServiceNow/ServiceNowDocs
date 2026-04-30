---
title: Configure a custom resource path for BYOK models
description: Enter a custom resource path in your bring your own key \(BYOK\) model configuration so that Generative AI Controller can connect to AI service providers, such as Azure OpenAI, that use a different web address than the default.
locale: en-US
release: zurich
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2026-04-03"
reading_time_minutes: 1
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure a custom resource path for BYOK models

Enter a custom resource path in your bring your own key \(BYOK\) model configuration so that Generative AI Controller can connect to AI service providers, such as Azure OpenAI, that use a different web address than the default.

## Before you begin

Role required: admin

## About this task

When you configure a bring your own key \(BYOK\) model provider in Generative AI Controller, it uses the connection and credential alias to send requests to your AI provider. The alias contains the base URL and API key for your provider. Some AI providers, such as Azure OpenAI, include an extra path segment in their web address that Generative AI Controller does not add by default. Without this segment, Generative AI Controller requests do not reach your provider correctly.

The Resource Path field in the model configuration record is where you provide that extra segment.

**Note:** The custom resource path configuration is currently supported for Azure OpenAI only.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

2.  Open the Generative AI provider record for Azure OpenAI.

3.  In the Connections Attributes related list, select the **Chat Completions Resource Path** attribute.

4.  Enter the custom resource path for your provider's endpoint in the **Default value** field.

    For example, for Azure OpenAI, if your full endpoint URL is:

    ```
    https://<your-resource-name>.openai.azure.com/openai/deployments/<your-deployment-name>
    ```

    Enter the following resource path in the **Default value** field:

    ```
    /openai/deployments/<your-deployment-name>
    ```

    **Note:** You can find your resource name and deployment name in the Azure portal.

5.  Select **Update**.


## Result

Generative AI Controller now connects to your AI provider using the resource path you entered. Your agentic AI skills are ready to use this provider.

