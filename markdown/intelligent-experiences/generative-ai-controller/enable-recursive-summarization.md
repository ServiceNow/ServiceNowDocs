---
title: Enable recursive summarization for large inputs
description: Use recursive summarization to break down the requests to the large language models \(LLMs\) into smaller pieces so that you can maintain the context for generative AI capabilities.
locale: en-US
release: yokohama
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Enable recursive summarization for large inputs

Use recursive summarization to break down the requests to the large language models \(LLMs\) into smaller pieces so that you can maintain the context for generative AI capabilities.

## Before you begin

Role required: admin

## About this task

LLMs have a maximum number of tokens that can be processed in a single request. Certain fields, such as activity fields, can have more information than can fit in within those restrictions. Recursive summarization breaks the information given to an LLM into chunks, summarizes each chunk individually, and then processes the original request with the summarized chunks. The chunks are organized with overlaps between the pieces so that the context is retained across every piece.

**Note:** Enabling recursive summarization may cause the capabilities to process large inputs more slowly because they must make multiple calls to the LLM instead of just one call.

## Procedure

1.  In the navigator filter, go to the OneExtend Capability list by entering `sys_one_extend_capability.list`.

2.  Open the record for the OneExtend capability that you want to change.

3.  In the OneExtend Definition Config related list, set **Enable Large Input Support** to true for the OneExtend Definition that you want to enable recursive summarization for.

4.  In the OneExtend Capability Attributes related list, set **Contains Large Input** to true for the fields that you want to add recursive summarization in.

    The fields that are most likely to contain a large amount of data, such as an activities field, should have their values set to true. You can also select the **Contains Large Input** check box on the OneExtend Capability Attribute record and save the record to set the value to true.


## Result

Recursive summarization is enabled for the OneExtend Capability for the fields specified in this procedure.

