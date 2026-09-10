---
title: Configure API credentials for Azure OpenAI
description: Configure your API credentials to use Azure OpenAI as your LLM provider for Generative AI Controller capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/generative-ai-controller/configure-api-credentials-for-azure-openai.html
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring API credentials for generative AI capabilities, Configuring Generative AI Controller, Generative AI Controller, AI Admin Hub, Enable AI experiences]
---

# Configure API credentials for Azure OpenAI

Configure your API credentials to use Azure OpenAI as your LLM provider for Generative AI Controller capabilities.

## Before you begin

To use generative AI capabilities with Azure OpenAI, you must have an Azure resource with an API key.

Role required: admin

## About this task

To use models with Azure OpenAI as your LLM provider for Generative AI Controller capabilities, you must have an active connection configured.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

2.  Open the Generative AI provider record for Azure OpenAI.

3.  Select the **Create New Connection &amp; Credential** related link.

    \[Omitted image "gai-create-new-connection-azure.png"\] Alt text: Create New Connection &amp; Credential related link highlighted on the screen.

4.  Edit the Connection URL to include your resource name.

    For Azure OpenAI, your Connection URL is in the form `https://{your-resource-name}.openai.azure.com`. See the [Azure OpenAI documentation](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/reference#completions) for more information.

5.  In the API key field, enter the API key for the provider.

    **Note:** The characters in the API key field are masked in the user interface.

6.  Create a connection by selecting **Create**.


## Result

You can now use capabilities labeled with Azure OpenAI as your LLM provider for Generative AI Controller capabilities.

\[Omitted image "gai-created-connection-azure.png"\] Alt text: Complete connection for Azure OpenAI.

## What to do next

If you want to use generative AI capabilities through your MID Server, open the new Connection record, select the **Use MID server** check box, and save the record.

Activate generative AI skills in the AI Admin Hub console for your workflow. For more information, see [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

