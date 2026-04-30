---
title: Configure sensitive data handling for generative AI
description: Set up and configure how personally identifiable information and other sensitive data is removed from generative AI prompts.
locale: en-US
release: xanadu
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure sensitive data handling for generative AI

Set up and configure how personally identifiable information and other sensitive data is removed from generative AI prompts.

## Before you begin

You can create a new Sensitive Data Regex record with a pattern or you can modify an existing record. The Generative AI category will apply the pattern to your generative AI prompts.

Role required: admin

## About this task

Personally identifiable information and other sensitive data can be masked so that it does not appear in generative AI prompts. Placeholder text is sent with the prompt instead, and that placeholder text is replaced with the original text after the response has been received. This two-way masking ensures your users see the correct values, but the LLM is not exposed to any sensitive information.

There are some considerations for using the Sensitive Data Handler with generative AI.

-   The sensitive data detection toggle in the Conversational Interfaces Settings is unrelated to the Generative AI Controller, which uses sensitive data handling capabilities separately from this utility.
-   The prompt, response, edited\_response and additional\_data fields in a conversational topic are masked during data extraction.
-   The prompt is masked before sending it to the large language model \(LLM\) by using the sensitive data handling plugin. Only regular expressions \(regexes\) in the Generative AI category are used to mask the prompt.

## Procedure

1.  Navigate to **All** &gt; **Sensitive Data Handling** &gt; **All**.

2.  Select the Sensitive Data Regex record you would like to apply for generative AI prompts.

3.  Unlock the Categories field by selecting the lock icon ![Lock icon.](../../../common/image/icon-lock.png).

4.  Enter `Generative AI` in the target field and select the record.

5.  Select the lock icon again to lock the Categories field.

6.  Set the Status field to Active if it is not already.

    ![Example sensitive data regex record with a name and pattern filled with Generative AI as the category](../image/gen-ai-sensitive-data-regex.png)

7.  Select **Update** to save the record.


