---
title: Configure retriever chunking and reranking
description: Configure chunking and reranking for a retriever that uses hybrid or semantic search to control how retrieved content is split, ranked, and passed to the LLM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-skill-kit/retriever-chunking.html
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Add a retriever, Add a tool, Create a prompt, Using AI Skill Kit, AI Skill Kit, Enable AI experiences]
---

# Configure retriever chunking and reranking

Configure chunking and reranking for a retriever that uses hybrid or semantic search to control how retrieved content is split, ranked, and passed to the LLM.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

To set up the chunking and reranking options for a retriever, you must have a retriever tool added to your skill with the **Hybrid** or **Semantic** search criteria. The following steps come after the semantic configuration in [Add a retriever](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/add-retriever.md).

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select the skill that you’re adding a retriever to.

3.  [Add a retriever](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/add-retriever.md).

4.  On the form, fill in the fields.

<table id="table_zcj_zmc_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Max number of chunks per document

</td><td>

Maximum number of chunks to return per document. The default value is 10.

</td></tr><tr><td>

Chunking strategy

</td><td>

-   Fixed size

Fixed size breaks down the full text into smaller passages. You can choose the passage size limit in number of words or number of sentences.

-   Small to big

Small to big enables you to choose the top K best-matched indexed chunks and expand them to include surrounding chunks. Then the expanded chunks are linked together into a large text and broken into smaller passages.

Don’t use the small to big chunking strategy if you’re using full text or truncate index chunking configuration.

</td></tr><tr><td>

Chunking unit

</td><td>

-   Words
-   Sentences


</td></tr><tr><td>

Chunk size

</td><td>

Size of the returned chunks. The default value for word size is 750. The default value for sentence size is 40.

</td></tr><tr><td>

Expanded snippet size

</td><td>

Size of the expanded chunks included when you select the small to big chunking strategy.

</td></tr><tr><td>

Top K results

</td><td>

Number of chunks that the reranker returns. If this field is empty, the reranker returns the number of results set in the retriever Limit field.

</td></tr></tbody>
</table>5.  Select **Next**.

6.  Select the type of condition to evaluate when the tool runs.

7.  Select **Next**.

8.  Review the selections that you made for the tool and select **Add tool**.


**Parent Topic:**[Add a retriever](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-skill-kit/add-retriever.md)

