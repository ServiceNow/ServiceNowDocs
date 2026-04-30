---
title: Enable Code Explain and Summarize
description: Enable the Code Explain and Code Summarize features by changing the default model of your instance from NowLLM to Azure OpenAI.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: task
last_updated: "2025-02-07"
reading_time_minutes: 1
breadcrumb: [Configuring code generation, Now Assist for code generation, Scripting, API implementation, API implementation and reference]
---

# Enable Code Explain and Summarize

Enable the Code Explain and Code Summarize features by changing the default model of your instance from NowLLM to Azure OpenAI.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the System Properties table:

    -   When you log in to a Now Assist for Code instance for the first time, you’ll see a notification to use GPT-4o with Now Assist for Code.

        To turn on the Code Explain and Summarize features, select **Go to turn on GPT-4o**.

    -   Navigate to **All** &gt; **System Properties**

        **Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

2.  Search for `sn_now_assist_code.code_assist_model_provider`.

3.  Edit a record in the sn\_now\_assist\_code.code\_assist\_model\_provider form by selecting **click here**.

4.  In the sn\_now\_assist\_code.code\_assist\_model\_provider form, in the **Value** field, enter `na4c_azure_openai`.

    ![The model is set to na4c_azure_openai in the Value field.](../image/now-assist-code-change-model.png)

5.  Select **Update**


## Result

All requests for the Now Assist for Code model are redirected to Azure OpenAI for evaluation and response. Additionally, you’ll get access to the Code Explain and Code Summarize features.

**Parent Topic:**[Configuring code generation](configuring-now-assist-code.md)

