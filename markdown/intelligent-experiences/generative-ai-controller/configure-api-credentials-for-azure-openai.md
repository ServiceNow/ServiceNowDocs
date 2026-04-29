---
title: Configure API credentials for Azure OpenAI
description: Configure your API credentials to use Azure OpenAI in custom workflows and Virtual Agent Designer topics.
locale: en-US
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring API credentials for generative AI capabilities, Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure API credentials for Azure OpenAI

Configure your API credentials to use Azure OpenAI in custom workflows and Virtual Agent Designer topics.

## Before you begin

In order to use generative AI capabilities with Azure OpenAI, you must have an Azure resource with an API key.

Role required: admin

## About this task

In order to use models with Azure OpenAI as your LLM provider for Generative AI Controller capabilities, you must have an active connection configured.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

2.  Open the Generative AI provider record for Azure OpenAI.

3.  Select the **Create New Connection &amp; Credential** related link.

    ![Create New Connection & Credential related link highlighted on the screen.](../image/gai-create-new-connection-azure.png)

4.  Edit the Connection URL to include your resource name.

    For Azure OpenAI, your Connection URL is in the form `https://{your-resource-name}.openai.azure.com`. See the [Azure OpenAI documentation](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/reference#completions) for more information.

5.  In the API key field, enter the API key for the provider.

    **Note:** The characters in the API key field are masked in the user interface.

6.  Create a connection by selecting **Create**.


## Result

You can now use capabilities labeled with Azure OpenAI in Flow Designer, Virtual Agent Designer, and scripts like background scripts and business rules to create custom experiences with generative AI.

![Complete connection for Azure OpenAI.](../image/gai-created-connection-azure.png)

## What to do next

If you want to use generative AI capabilities through your MID Server, open the new Connection record, select the **Use MID server** check box, and save the record.

**Related topics**  


[Bring your own key for third-party AI provider integration](../concept/byok-for-azure-open-ai.md)

[Configure a custom resource path for BYOK models](configure-custom-resource-path-byok.md)

