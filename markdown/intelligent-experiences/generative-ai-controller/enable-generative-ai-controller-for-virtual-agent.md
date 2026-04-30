---
title: Enable a generative AI capability in Virtual Agent Designer
description: Add generative AI functionality to Virtual Agent topics to generate text, summarize information, analyze user sentiment, and interact with large language models \(LLMs\).
locale: en-US
release: xanadu
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Enable a generative AI capability in Virtual Agent Designer

Add generative AI functionality to Virtual Agent topics to generate text, summarize information, analyze user sentiment, and interact with large language models \(LLMs\).

## Before you begin

You must be on Vancouver patch 2 or a later release.

Role required: admin

## Procedure

1.  Go to the OneExtend Builder Configs table by entering `sys_one_extend_builder_config.list` in the navigation filter.

2.  Open the Virtual Agent Designer record.

3.  In the OneExtend Builder Capabilities related list, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Capability|Capability that is available in the Virtual Agent Designer with your preferred provider. You must have at least one provider for the capabilities, but you don't need to use the same provider for all the capabilities.|
    |Execution Mode|Mode that determines when a capability is executed in relation to other processes. For Virtual Agent Designer, select `Async`. The `Sync` and `Fire and Forget` options aren’t supported.|

    ![Form completed with generic prompt as the definition and async as the execution mode](../image/gaic-builder-config.png "Generic Prompt builder definition form")

5.  Select **Submit**.

6.  Repeat steps 3 through 5 for each capability that you want to enable.


## Result

Generative AI capabilities are available for Virtual Agent Designer.

## What to do next

Create topics and topic blocks and enhance your Virtual Agent with generative AI capabilities.

You can also access the Workflow Studio actions directly with the Action topic block in Virtual Agent Designer.

