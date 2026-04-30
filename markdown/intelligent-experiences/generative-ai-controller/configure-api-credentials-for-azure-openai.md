---
title: Configure API credentials for Azure OpenAI
description: Configure your API credentials to use Azure OpenAI in custom workflows and Virtual Agent Designer topics.
locale: en-US
release: zurich
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring API credentials for generative AI capabilities, Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure API credentials for Azure OpenAI

Configure your API credentials to use Azure OpenAI in custom workflows and Virtual Agent Designer topics.

## Before you begin

You must have access to the supported Azure OpenAI models through Now Assist Admin, or an active Azure OpenAI account and a valid API key to securely connect ServiceNow to Azure OpenAI.

Role required: admin

## About this task

Enable Generative AI Controller capabilities by connecting ServiceNow to Azure OpenAI model with your API key. This involves configuring your API credentials for secure access to Azure OpenAI models.

For end-to-end configuration of Azure OpenAI in ServiceNow using your API key \(BYOK\), establish a secure connection that enables customized AI capabilities while maintaining flexibility, control, and conformance. For more information, see [KB2663518](https://support.servicenow.com/kb?sys_kb_id=af559cd64769b29477748d01426d4353&id=kb_article_view) article in the Now Support Knowledge Base.

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

