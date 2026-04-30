---
title: Configure API Credentials for Amazon Bedrock
description: Configure your API credentials to use AWS Bedrock in custom workflows and Virtual Agent Designer topics.
locale: en-US
release: xanadu
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring API credentials for generative AI capabilities, Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure API Credentials for Amazon Bedrock

Configure your API credentials to use AWS Bedrock in custom workflows and Virtual Agent Designer topics.

## Before you begin

You must have an AWS account and the IAM user needs permission to access the bedrock:InvokeModel action.

Role required: admin

## About this task

To use Amazon Bedrock as your LLM provider for Generative AI Controller capabilities, you must have an active connection configured.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

2.  Open the record for Amazon Bedrock.

    ![Create New Connection & Credential related link highlighted on the screen.](../image/gai-create-new-connection-amazon.png)

3.  Select the **Create New Connection &amp; Credential** related link.

4.  Enter your **Region**, such as `us-east-1`.

5.  Enter your API key.

    For more information, see [AWS documentation on generating API keys](https://repost.aws/knowledge-center/create-access-key).

6.  Select **Create**.


## Result

You can use Amazon Bedrock as your provider for Generative AI Controller capabilities in Flow Designer, Virtual Agent Designer, and scripts to create custom experiences with generative AI.

![Complete connection for Amazon Bedrock.](../image/gai-created-connection-amazon.png)

