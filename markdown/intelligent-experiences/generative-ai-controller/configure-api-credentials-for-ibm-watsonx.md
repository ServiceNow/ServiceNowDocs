---
title: Configure API credentials for IBM watsonx
description: Configure your API credentials to use IBM watsonx Granite models in custom workflows and Virtual Agent Designer topics.
locale: en-US
release: yokohama
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring API credentials for generative AI capabilities, Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure API credentials for IBM watsonx

Configure your API credentials to use IBM watsonx Granite models in custom workflows and Virtual Agent Designer topics.

## Before you begin

To use IBM watsonx large language models \(LLMs\), you must configure your credentials to use the Generative AI Controller capabilities.

Role required: admin

## About this task

In order to use models with IBM watsonx as your LLM provider for Generative AI Controller capabilities, you must have an active connection configured.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

2.  Open the record named IBM watsonx.

3.  Select the **Create New Connection &amp; Credential** related link.

    ![Create New Connection & Credential related link highlighted on the screen.](../image/gai-create-new-connection-ibm.png)

4.  In the API key field, enter your API key.

    For more information about generating an API key, see IBM's [documentation for generating API keys for authentication](https://www.ibm.com/docs/en/watsonx/watsonxdata/1.1.x?topic=started-generating-api-keys).

5.  Create a connection by selecting **Create**.


## Result

You can now use capabilities labeled with IBM watson in Flow Designer, Virtual Agent Designer, and scripts like background scripts and business rules to create custom experiences with generative AI.

![Complete connection for IBM watsonx.](../image/gai-created-connection-ibm.png)

## What to do next

If you want to use generative AI capabilities through your MID Server, open the new Connection record, select the **Use MID server** check box, and save the record.

