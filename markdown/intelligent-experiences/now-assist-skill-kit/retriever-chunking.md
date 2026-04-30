---
title: Retriever chunking and reranking
description: When you’re building a skill prompt that uses a retriever you can use chunking and reranking to enhance the accuracy and relevance of your responses.
locale: en-US
release: yokohama
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Add a retriever, Add a tool, Create a prompt, Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Retriever chunking and reranking

When you’re building a skill prompt that uses a retriever you can use chunking and reranking to enhance the accuracy and relevance of your responses.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

To set up the chunking and reranking options for a retriever, you must have a retriever tool added to your skill with the **Hybrid** or **Semantic** search criteria. The following steps come after the semantic configuration in [Add a retriever](add-retriever.md).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you’re adding a retriever to.

3.  [Add a retriever](add-retriever.md).

4.  On the form, fill in the fields.

<table id="table_zcj_zmc_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Max number of chunks per document

</td><td>

The maximum number of chunks that you want returned per document. The default value is 10.

</td></tr><tr><td>

Chunking strategy

</td><td>

-   Fixed size

Fixed size breaks down the full text into smaller passages. You can choose the passage size limit in number of words or number of sentences.

-   Small to big

Small to big enables you to choose the top K best matched indexed chunks and expand them to include surrounding chunks. Then the expanded chunks are linked together into a large text and broken into smaller passages.

Don’t use the small to big chunking strategy if you’re using full text or truncate index chunking configuration.

</td></tr><tr><td>

Chunking unit

</td><td>

-   Words
-   Sentences


</td></tr><tr><td>

Chunk size

</td><td>

The size of the chunks that are returned. The default value for word size is 750. The default value for sentence size is 40.

</td></tr><tr><td>

Expanded snippet size

</td><td>

The size of the expanded chunks that are included when you select the small to big chunking strategy.

</td></tr><tr><td>

Top K results

</td><td>

The number of chunks the reranker returns. If you leave this field empty, the default number of chunks that are returned will be the limit you entered.

</td></tr></tbody>
</table>5.  Select **Next**.

6.  Select the type of condition that you want to be evaluated when the tool is executed.

7.  Select **Next**.

8.  Review the selections that you made for the tool and select **Add tool**.


**Parent Topic:**[Add a retriever](add-retriever.md)

