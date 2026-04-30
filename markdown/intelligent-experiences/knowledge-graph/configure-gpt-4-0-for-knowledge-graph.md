---
title: Configure LLM for Knowledge Graph
description: Choose which large language model \(LLM\) service provider for Knowledge Graph.
locale: en-US
release: zurich
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [generative AI, Now Assist]
breadcrumb: [Configuring Knowledge Graph, Knowledge Graph, Enable AI experiences]
---

# Configure LLM for Knowledge Graph

Choose which large language model \(LLM\) service provider for Knowledge Graph.

## Before you begin

LLMs are part of the foundation for Knowledge Graph. Different LLMs can provide slightly different performance and responses. You can select which LLM to use for your Knowledge Graph schema.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_one\_extend\_capability.list** &gt; **TextToResult**.

2.  Open the TextToResult record and select **OneExtend Definition Configs** \(related list\).

3.  For one of the following options, change the value of the default field to **True**.

    -   **TextToResult \(NowLLM\)**
    -   **TextToResult \(Claude Large\)**
    -   **TextToResult \(GPTLarge\)**
    -   **TextToResult \(Gemini\)**
    Once you select the default LLM, ensure that the Default field value for another LLM is set to **False**.

4.  Select the LLM to open the record and update the default field to **True**.


