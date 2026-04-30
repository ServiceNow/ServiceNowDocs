---
title: Add a retriever
description: Add a retriever to your prompt to augment and add context to your prompts with AI search results.
locale: en-US
release: xanadu
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2024-10-07"
reading_time_minutes: 2
breadcrumb: [Create a prompt, Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Add a retriever

Add a retriever to your prompt to augment and add context to your prompts with AI search results.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

Using a retriever in a skill enhances the relevance and coherence of a response by pulling relevant information from a source and then feeding it to a large language model \(LLM\) to create the final output. This process leads to smoother conversational flow and better scalability as data grows, without requiring model fine-tuning.

A retriever enables the chatbot to access external knowledge by fetching relevant background information, resulting in more factual, in-depth, and informed responses.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Create a new skill or select the skill that you want to add a retriever to.

3.  Select **Add Tool**.

4.  Select **Retriever** from the drop-down menu.

5.  Select **Configure retriever**.

6.  On the form, fill in the fields.

<table id="table_bzy_5jv_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name for the retriever.

</td></tr><tr><td>

Search query

</td><td>

The information that you want to search for. It can be static text or a skill input.

</td></tr><tr><td>

Search profile

</td><td>

A group of search sources.

</td></tr><tr><td>

Search sources

</td><td>

Tables in ServiceNow that have been indexed and can be used for search.

</td></tr><tr><td>

Fields returned

</td><td>

The fields that you want returned from the search sources and sent to the large language model \(LLM\).

</td></tr><tr><td>

Limit

</td><td>

The maximum number of results that are returned.

</td></tr><tr><td>

Search criteria

</td><td>

-   Hybrid
-   Semantic
-   Keyword
 **Note:** If you choose Hybrid or Semantic, you can make selections for chunking and reranking. To learn more about chunking and reranking, see [Retriever chunking and reranking](retriever-chunking.md).

</td></tr></tbody>
</table>7.  Select **Next**.

8.  If you selected **Hybrid** or **Semantic** search criteria, select a semantic index.

    A semantic index enables you to search for data based on contextual meaning.

9.  If you selected **Hybrid** or **Semantic** search criteria, select **Advanced** to change the document matching threshold.

    The document matching threshold is the threshold for semantic matching. The default value is 0. You can input any value from 0 to 1. You can get more precise results with a higher value.

10. Select **Next**.

    **Note:** If you selected **Hybrid** or **Semantic** search criteria, see [Retriever chunking and reranking](retriever-chunking.md) to complete setting up your retriever.

11. Review the retriever tool information.

12. Select **Add tool**.


-   **[Retriever chunking and reranking](retriever-chunking.md)**  
When you’re building a skill prompt that uses a retriever you can use chunking and reranking to enhance the accuracy and relevance of your responses.

**Parent Topic:**[Create a prompt](create-prompt-template.md)

