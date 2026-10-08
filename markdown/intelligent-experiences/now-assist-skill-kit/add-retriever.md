---
title: Add a retriever
description: Add a retriever to your skill to augment your prompts with relevant context from AI Search results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/add-retriever.html
release: brazil
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 2
breadcrumb: [Add a tool, Create a prompt, Using AI Skill Kit, AI Skill Kit, Generative AI skills, Enable AI Experiences]
---

# Add a retriever

Add a retriever to your skill to augment your prompts with relevant context from AI Search results.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

Using a retriever in a skill enhances the relevance and coherence of a response by pulling relevant information from a source and then feeding it to a large language model \(LLM\) to create the final output. This process doesn't require model fine-tuning.

A retriever enables the chatbot to access external knowledge by fetching relevant background information, resulting in more factual, in-depth, and informed responses.

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Create a skill or select the skill that you want to add a retriever to.

3.  Select the **Tool editor** tab.

4.  Select the \(+\) icon to add a node.

5.  Select **Tool node**.

6.  Select **Retriever** from the drop-down menu.

7.  Select **Configure retriever**.

8.  On the form, fill in the fields.

<table id="table_bzy_5jv_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the retriever.

</td></tr><tr><td>

Search query

</td><td>

Information to search for. The value can be static text or a skill input.

</td></tr><tr><td>

Search space type

</td><td>

-   Table-based
-   Search-profile-based


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

Fields to return from the search sources and send to the LLM.

</td></tr><tr><td>

Limit

</td><td>

Maximum number of results to return.

</td></tr><tr><td>

Search criteria

</td><td>

-   Hybrid
-   Semantic
-   Keyword
 **Note:** If you choose Hybrid or Semantic, you can make selections for chunking and reranking. To learn more about chunking and reranking, see [Configure retriever chunking and reranking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/retriever-chunking.md).

</td></tr></tbody>
</table>9.  Select **Next**.

10. Select an embedding model.

    To learn about embedding models, see [Configuring your embedding model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/setting-up-3p-embedding-models.md).

11. If you selected **Hybrid** or **Semantic** search criteria, select a semantic index.

    A semantic index enables you to search for data based on contextual meaning.

12. If you selected **Hybrid** or **Semantic** search criteria, select **Advanced** to change the document matching threshold.

    The document matching threshold is the threshold for semantic matching. The default value is 0. You can input any value from 0 to 1. You can get more precise results with a higher value.

13. Select **Next**.

    **Note:** If you selected **Hybrid** or **Semantic** search criteria, see [Configure retriever chunking and reranking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/retriever-chunking.md) to complete setting up your retriever.

14. Review the retriever tool information.

15. Select **Add tool**.


-   **[Configure retriever chunking and reranking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/retriever-chunking.md)**  
Configure chunking and reranking for a retriever that uses hybrid or semantic search to control how retrieved content is split, ranked, and passed to the LLM.

**Parent Topic:**[Add a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/add-a-tool.md)

