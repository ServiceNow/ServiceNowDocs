---
title: Configure API credentials for a generic large language model \(LLM\) connector
description: Use a generic LLM connector to connect the ServiceNow AI Platform with an external AI provider to use generative AI capabilities in custom Virtual Agent topics, Flows, or scripts, like background and business rule scripts.
locale: en-US
release: yokohama
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring API credentials for generative AI capabilities, Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure API credentials for a generic large language model \(LLM\) connector

Use a generic LLM connector to connect the ServiceNow AI Platform with an external AI provider to use generative AI capabilities in custom Virtual Agent topics, Flows, or scripts, like background and business rule scripts.

## Before you begin

You must have access to the API of an external LLM in order to configure the credentials.

Role required: admin

## About this task

You can connect an external LLM to the ServiceNow AI Platform by creating a connection alias to the model, create a model record that points to the alias, create a prompt record for the model, and then create a transformer record to transform the request or response from the LLM.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **API Key Credentials**

3.  In the **Name** field, give your API credential a name.

    Including the name of the model in the API Key Credential makes it easier to identify later.

4.  In the **API Key** field, enter your model's API key.

    ![API Key Credentials form filled with name and API key.](../image/gai-create-new-connection-custom-api.png)

5.  Select **Submit** to create the Credential.

    At this step, you have the API key information for the external LLM configured.

6.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

7.  Select **New**.

8.  In the **Name** field, enter a name for the credential alias.

    You do not need to change any other field values. ![Connection & Credentials Alias record with name filled in.](../image/gai-create-new-connection-custom-alias.png)

9.  Select **Submit.**

10. After you are redirected to the List view, find and open the record you just created.

11. Select **New** in the Connections related list to create a new Connection record.

12. Enter the name of the connection in the Name field.

13. In the **Credential** field, select the Credential record you created with the model's API key.

    You can search the list of Credentials by typing the name of the Credential in the field. You can also select the lookup icon \(![Lookup icon.](../../now-assist-admin/image/na-list-lookup-icon.png)\) to open a modal with the full list.

14. In the **Connection alias** field, select the alias record you created.

15. For the Connection URL, enter the endpoint URL for the model.

    For example, a model from Hugging Face might start with "https://api-inference.huggingface.co". You can leave the remaining fields as they are. ![HTTP(s) Connection record filled in with My Model credential, alias, and connection URL.](../image/gai-create-new-connection-custom.png)

16. Select **Submit**.


## Result

You have the connection and credential alias to use for connecting a generic LLM to use generative AI capabilities on the ServiceNow AI Platform. You can confirm this by navigating to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases** and confirming that the connection appears in the related list. ![Finished credentials and alias for custom LLM.](../image/gai-created-connection-custom.png)

## What to do next

For more information on configuring a generic LLM, see [configure a generic LLM connector](configure-a-generic-llm-connector.md)

