---
title: Configure a custom resource path for BYOK models
description: Enter a custom resource path in your bring your own key \(BYOK\) model configuration so that Generative AI Controller can connect to your Azure OpenAI deployment using the correct endpoint.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/generative-ai-controller/configure-custom-resource-path-byok.html
release: zurich
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2026-04-03"
reading_time_minutes: 2
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure a custom resource path for BYOK models

Enter a custom resource path in your bring your own key \(BYOK\) model configuration so that Generative AI Controller can connect to your Azure OpenAI deployment using the correct endpoint.

## Before you begin

-   Bring your own key \(BYOK\) must be configured for your instance. For more information, see [Bring your own key for third-party AI provider integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/generative-ai-controller/byok-for-azure-open-ai.md).
-   You must have an active connection and credential alias for your Azure OpenAI service. For more information, see [Configure API credentials for Azure OpenAI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/generative-ai-controller/configure-api-credentials-for-azure-openai.md).

Role required: admin

## About this task

When you configure a bring your own key \(BYOK\) model in Generative AI Controller, it uses the connection and credential alias to send requests to your third-party AI service provider. The alias contains the base URL and API key for your provider. Some AI providers, such as Azure OpenAI, use a resource path prefix that is different from the default one that Generative AI Controller provides. This increases flexibility when you're configuring a BYOK provider, as you can tailor the resource path to your specific needs.

You configure that resource path prefix in the **Chat Completions Resource Path** connection attribute of the Azure OpenAI connection alias record.

**Note:** The custom resource path configuration is supported for Azure OpenAI only.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

2.  Open the connection alias record for Azure OpenAI.

3.  In the Connections Attributes related list, select the **Chat Completions Resource Path** attribute.

4.  In the **Default value** field, update the existing value to match your resource path prefix.

    The resource path prefix is the segment of your endpoint URL between the hostname and your deployment name.

    For example, given the Azure OpenAI endpoint URL:

    ```
    https://<your-resource-name>.openai.azure.com/openai/deployments/<your-deployment-name>
    ```

    The resource path prefix is:

    ```
    /openai/deployments
    ```

    Enter the following resource path prefix in the **Default value** field:

    ```
    /openai/deployments/
    ```

    **Note:** You can find your resource name in the Azure portal. The base URL \(https://&lt;your-resource-name&gt;.openai.azure.com\) is already configured in your Connection URL field. Do not include the deployment name in this field.

5.  Select **Update**.


## Result

Generative AI Controller uses the resource path prefix you entered to send requests to your Azure OpenAI deployment. Your agentic AI skills are ready to use this provider.

