---
title: Configure a third-party LLM provider for Now Assist for Creator
description: Configure a third-party LLM provider as default for creating a spoke using Now Assist.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-24"
reading_time_minutes: 1
breadcrumb: [Use Now Assist to create spokes and build actions, Building spokes using Spoke Generator, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Configure a third-party LLM provider for Now Assist for Creator

Configure a third-party LLM provider as default for creating a spoke using Now Assist.

## Before you begin

-   Make sure Now Assist Skill Kit \(sn\_skill\_builder\) is installed.
-   Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the **ServiceNow skills** tab.

3.  Search for `Spoke Generation` skill and open it.

4.  In the **Spoke Generation skill**, select the **Skill settings** tab.

5.  Select a LLM provider of your choice and toggle the **Make default** switch.

    **Note:** Currently, Azure OpenAI, Google Gemini, and Anthropic Claude on AWS LLMs are supported.

    ![Configuring third-party LLMs for Now Assist for Creator](../images/na-creator-tpt-llms-config.png)


## Result

You can now create a spoke from Now Assist using the selected LLM provider.

**Parent Topic:**[Use Now Assist to create spokes and build actions](../concept/now-assist-in-spk-gen.md)

