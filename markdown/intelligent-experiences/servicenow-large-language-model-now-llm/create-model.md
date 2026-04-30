---
title: Create a model
description: You can create a custom large language model \(LLM\) using ServiceNow models or models from different providers.
locale: en-US
release: zurich
product: ServiceNow Large Language Model \(Now LLM\)
classification: servicenow-large-language-model-now-llm
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 1
breadcrumb: [Providers and Models, Large language models on the ServiceNow AI Platform, Enable AI experiences]
---

# Create a model

You can create a custom large language model \(LLM\) using ServiceNow models or models from different providers.

## Before you begin

Role required: sn\_skill\_builder.sb\_model\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Providers and Models**.

2.  Select **Add model**.

3.  On the form, fill in the fields.

    ![Create a custom model form](../../now-assist-skill-kit/image/llm-custom-model.png)

    |Field|Description|
    |-----|-----------|
    |Model name|A name for the model|
    |Max tokens|Max response + max request tokens|
    |Supported languages|The languages that are supported|
    |Provider|The provider of the LLM|
    |API|The API you are using from the provider|

4.  Select **Continue**.

5.  Enter credential details

<table id="table_tvm_41g_hhc"><thead><tr><th>

Model

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Custom LLM provider

</td><td>

1.  Select **Create**.
    1.  Connection name
    2.  Connection URL
    3.  Credential type
    4.  API key
2.  Select **Select from database** and select from the dropdown menu.


</td></tr><tr><td>

-   IBM Watson
-   Now LLM Service
-   Open AI
-   Perplexity


</td><td>

Add the connection URL and API key.

</td></tr></tbody>
</table>6.  Select **Continue**.

7.  If you created a custom LLM provider, add transformer information.

    ![Add transformer form](../../now-assist-skill-kit/image/llm-transformer.png)

<table id="table_r3n_fbg_hhc"><thead><tr><th>

Option

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Existing

</td><td>

Select a transformer template:-   Default
-   Hugging face
-   Google Gemini
-   Claude


</td></tr><tr><td>

Create

</td><td>

Add transformer request and response information for your model.

</td></tr></tbody>
</table>    **Note:** If you didn't select a custom LLM provider, request and response transformers are set by the system.

8.  Select **Continue**.

9.  Select **Test connection**.

10. Select **Continue**.

11. Review and select **Finish**.


**Parent Topic:**[Providers and Models](../concept/providers-and-models.md)

