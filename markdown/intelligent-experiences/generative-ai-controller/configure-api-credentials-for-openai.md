---
title: Configure API credentials for OpenAI
description: Configure your API credentials to use OpenAI in custom workflows and Virtual Agent Designer topics.
locale: en-US
release: zurich
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring API credentials for generative AI capabilities, Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure API credentials for OpenAI

Configure your API credentials to use OpenAI in custom workflows and Virtual Agent Designer topics.

## Before you begin

To use the OpenAI and Azure OpenAI large language models \(LLMs\), you must configure your credentials to use the Generative AI Controller capabilities.

Role required: admin

## About this task

To use models with Azure OpenAI as your LLM provider for Generative AI Controller capabilities, you must have an active connection configured.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

2.  Open the Generative AI provider record for OpenAI.

3.  Select the **Create New Connection &amp; Credential** related link.

    ![Create New Connection & Credential related link highlighted on the screen.](../image/gai-create-new-connection.png)

4.  In the API key field, enter the API key.

    For OpenAI, see your [OpenAI API keys](https://platform.openai.com/account/api-keys) for the credentials information.

5.  Create a connection by selecting **Create**.


## Result

You can now use capabilities labeled with OpenAI in Flow Designer, Virtual Agent Designer, and scripts like background scripts and business rules to create custom experiences with generative AI.

![Complete connection for OpenAI.](../image/gai-created-connection.png)

## What to do next

If you want to use generative AI capabilities through your MID Server, open the new Connection record, select the **Use MID server** check box, and save the record.

