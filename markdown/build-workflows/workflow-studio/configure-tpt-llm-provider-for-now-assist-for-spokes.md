---
title: Configure a third-party LLM provider as default for ServiceNow Otto for Spokes
description: Configure a third-party LLM provider as the default LLM provider that can create a spoke using ServiceNow Otto.Set a third-party LLM provider as the default LLM provider to create a spoke using the ServiceNow Otto for Spokes from the AI Admin Hub panel.Configure a third-party LLM provider as the default LLM provider for creating a spoke using ServiceNow Otto after installing the AI Skill Kit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/configure-tpt-llm-provider-for-now-assist-for-spokes.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-08-22"
reading_time_minutes: 1
breadcrumb: [Use ServiceNow Otto to create spokes and build actions, Building spokes using Spoke Generator, Use, Workflow Studio, Build workflows]
---

# Configure a third-party LLM provider as default for ServiceNow Otto for Spokes

Configure a third-party LLM provider as the default LLM provider that can create a spoke using ServiceNow Otto.

## Before you begin

Role required: admin

## About this task

ServiceNow provides multiple third-party LLM providers that can generate a spoke using ServiceNow Otto for Spokes. Set one of these LLM providers as the default LLM provider to generate spokes by using either of the two ways:

-   From the AI Admin Hub panel.
-   After installing the AI Skill Kit.

**Parent Topic:**[Use ServiceNow Otto to create spokes and build actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/now-assist-in-spk-gen.md)

## Use the AI Admin Hub panel

Set a third-party LLM provider as the default LLM provider to create a spoke using the ServiceNow Otto for Spokes from the AI Admin Hub panel.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Settings**.

2.  On the left panel, select **Manage AI models** and click **Manage model providers**.

3.  Select the **Model providers** tab.

4.  Select **Edit model provider**.

    \[Omitted image "llm-sel-model-provider-tab.png"\] Alt text: Edit model provider.

5.  Select the **Customize** tab.

6.  Select **Edit provider for skill**.

7.  In the **Select skills** field, enter `Spoke generation` and then select **Spoke Generation OOB**.

8.  From the **Choose a default LLM model provider** list, select the LLM provider that you want to set as default.

9.  Select **Save**.

10. On the confirmation dialog, select **Yes, save**.

    You have set the LLM provider you chose as the default LLM provider to create a spoke using the ServiceNow Otto for Spokes.


## Configure after installing the AI Skill Kit

Configure a third-party LLM provider as the default LLM provider for creating a spoke using ServiceNow Otto after installing the AI Skill Kit.

### Before you begin

-   Make sure that the AI Skill Kit \(sn\_skill\_builder\) is installed.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Click the **AI skills** tab.

3.  Search for `Spoke Generation` skill and open it.

4.  In the **Spoke Generation skill**, click the **Deployment and skill settings** tab.

5.  Select **General information**.

6.  Select a LLM provider of your choice and toggle the **Set as default** switch.

    **Note:** Currently, Now LLM Service, Azure OpenAI, Google Gemini, and Anthropic Claude on AWS LLMs are supported.

    \[Omitted image "na-creator-tpt-llms-config.png"\] Alt text: Configuring third-party LLMs for Now Assist for Creator

7.  Click **Save**.


### Result

You can now create a spoke from AI using the selected LLM provider.

