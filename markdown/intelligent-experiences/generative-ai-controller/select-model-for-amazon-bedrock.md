---
title: Select a model for Amazon Bedrock
description: Choose which large language model \(LLM\) to use with Amazon Bedrock for custom skills.
locale: en-US
release: yokohama
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [aws bedrock]
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Select a model for Amazon Bedrock

Choose which large language model \(LLM\) to use with Amazon Bedrock for custom skills.

## Before you begin

You must have the latest version of Generative AI Controller and the Amazon Bedrock spoke installed on your instance. You must also set up your API credentials. For more information, see [Configure API credentials for Amazon Bedrock](configure-api-credentials-for-amazon-bedrock.md).

Role required: admin

## About this task

You may have multiple models configured to use with Amazon Bedrock. By default, the settings use Amazon's Titan model, but you can configure the spoke to use a different model by changing the Generative AI Model Config record.

## Procedure

1.  In the filter navigator, navigate to the Generative AI Model Config table by entering `sys_generative_ai_model_config.list`.

2.  Search in the Provider field column for `Amazon Bedrock`, then open the resulting record.

3.  In the Model field, enter the ID of the model that you want to use.

    You can find the model ID on the **Foundation models** &gt; **Base models** page on Amazon Bedrock.

4.  Select **Save** to update the record.

5.  Map the chosen model to a custom skill.

    1.  In the filter navigator, go to the Generative AI Config table by entering `sys_generative_ai_config.list`.

    2.  Search for the custom skill you've created that uses Amazon Bedrock as the service provider, and open the record.

        The Definition should be OneExtend Capability Definition: &lt;Name of Skill&gt;.

    3.  Set the Model field to the model ID you entered in step 3.


## Result

Your chosen model with the Amazon Bedrock provider will be used for custom skills.

## What to do next

You can create custom skills with the Amazon Bedrock provider in Now Assist Skill Kit and perform step 6 to set the new model.

