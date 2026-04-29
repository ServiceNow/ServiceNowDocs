---
title: Configure a third-party LLM provider as default for Now Assist for Spokes
description: Configure a third-party LLM provider as the default LLM provider that can create a spoke using Now Assist.Set a third-party LLM provider as the default LLM provider to create a spoke using the Now Assist for Spokes from the Now Assist Admin panel.Configure a third-party LLM provider as the default LLM provider for creating a spoke using Now Assist after installing the Now Assist Skill Kit.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Now Assist to create spokes and build actions, Building spokes using Spoke Generator, Workflow Studio, Build workflows]
---

# Configure a third-party LLM provider as default for Now Assist for Spokes

Configure a third-party LLM provider as the default LLM provider that can create a spoke using Now Assist.

## Before you begin

Role required: admin

## About this task

ServiceNow provides multiple third-party LLM providers that can generate a spoke using Now Assist for Spokes. Set one of these LLM providers as the default LLM provider to generate spokes by using either of the two ways:

-   From the Now Assist Admin panel.
-   After installing the Now Assist Skill Kit.

## Use the Now Assist Admin panel

Set a third-party LLM provider as the default LLM provider to create a spoke using the Now Assist for Spokes from the Now Assist Admin panel.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  On the left panel, select Manage model providers.

3.  Select the **Model providers** tab.

    ![Model providers tab.](../images/llm-sel-model-provider-tab.png)

4.  Select **Edit model provider**.

5.  Select the **Customize** tab.

6.  Select **Edit provider for skill**.

7.  In the Select skills field, enter `Spoke generation` and then select Spoke Generation OOB.

8.  In the Default LLM provider list, select the LLM provider that you want to set as default.

9.  Select **Save and activate**.

10. On the confirmation dialog, select **Yes, activate**.

    You have set the LLM provider you chose as the default LLM provider to create a spoke using the Now Assist for Spokes.


## Configure after installing the Now Assist Skill Kit

Configure a third-party LLM provider as the default LLM provider for creating a spoke using Now Assist after installing the Now Assist Skill Kit.

### Before you begin

-   Make sure that the Now Assist Skill Kit \(sn\_skill\_builder\) is installed.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the **ServiceNow skills** tab.

3.  Search for `Spoke Generation` skill and open it.

4.  In the **Spoke Generation skill**, select the **Skill settings** tab.

5.  Select a LLM provider of your choice and toggle the **Make default** switch.

    **Note:** Currently, Azure OpenAI, Google Gemini, and Anthropic Claude on AWS LLMs are supported.

    ![Configuring third-party LLMs for Now Assist for Creator](../images/na-creator-tpt-llms-config.png)


### Result

You can now create a spoke from Now Assist using the selected LLM provider.

