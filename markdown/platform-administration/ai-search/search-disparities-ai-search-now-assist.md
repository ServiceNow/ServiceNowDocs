---
title: Search result disparities between AI Search and ServiceNow Otto search features
description: The ServiceNow AI Platform offers a variety of search tools, which may return different answers for the same or similar searches. This disparity in results is expected. It occurs because each tool uses a different approach and architecture to find results and generate answers that match your search.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/search-disparities-ai-search-now-assist.html
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search result disparities between AI Search and ServiceNow Otto search features

The ServiceNow AI Platform® offers a variety of search tools, which may return different answers for the same or similar searches. This disparity in results is expected. It occurs because each tool uses a different approach and architecture to find results and generate answers that match your search.

As an example of the same search returning different answers in different search tools, consider these results that might be displayed to a user searching for `what is my travel policy`:

\[Omitted image "travel-policy-search-ai-search-results.png"\] Alt text: Employee Center portal search results for travel policy search.

\[Omitted image "travel-policy-search-now-assist-genius-result-answer.png"\] Alt text: Summary Genius Result answer generated for travel policy search.

\[Omitted image "travel-policy-search-now-assist-virtual-agent-answer.png"\] Alt text: ServiceNow Otto for Virtual Agent answer returned for travel policy question.

In this example, each search tool returns a different answer even though the user's search \(or question\) is the same in all three tools. This is expected behavior, since the search tools all handle searches differently.

## AI Search

The AI Search engine uses keyword search, meaning that it looks for the best matches for your search terms in its indexed source data. Search features such as lemma and Unicode normalization, synonyms, stop words, and typo handling may modify the set of terms that AI Search considers matches for your search, but the matching is always done on a per-term basis.

Keyword search should return consistent results for the same search until your source data is updated. Machine learning relevancy can affect the exact order in which your results appear over time, though, so even if your data doesn’t change, your search may not return exactly the same result set today as it did the previous month.

## ServiceNow Otto Genius Results

The ServiceNow Otto Genius Result configurations offered in ServiceNow Otto for AI Search use a hybrid search mode. This mode blends keyword search with semantic vector search to find results in the AI Search index based on the intention and meaning of your search as well as on the best term matches.

The most relevant matching results are merged into a prompt that's sent to a large language model \(LLM\) for answer generation. Because LLMs aren't deterministic, they don't always produce the same output even when given the same input. As a result of the non-deterministic behavior of the LLM, ServiceNow Otto Genius Results are likely to return varying results for the same search, even when submitted at the same time.

**Note:** For more information on how LLMs introduce variations into their results, see [Discrepancies when using different AI search tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aisearch-differences.md).

Between the non-deterministic LLM behavior and the difference in search matching modes, ServiceNow Otto Genius Result answers can be expected to vary significantly from results returned by AI Search for the same search terms, even when using the same search configuration in both tools. This variance is expected because the two search tools take such different approaches when finding and generating answers for your search.

## ServiceNow Otto for Virtual Agent

ServiceNow Otto for Virtual Agent uses hybrid search to find matching results in the AI Search index, like the ServiceNow Otto Genius Result configurations do.

Unlike those Genius Result configurations, however, ServiceNow Otto for Virtual Agent has its own agentic AI back-end architecture for generating responses. This architecture doesn't rely on sending a single prompt to the LLM for answer creation the way the ServiceNow Otto Genius Result architecture does.

Because of this architectural difference, results from ServiceNow Otto for Virtual Agent searches can vary from those returned by ServiceNow Otto Genius Results, even when processing the same search and using the same search configuration. Similarly, ServiceNow Otto for Virtual Agent results may vary from the results returned by AI Search keyword searches.

**Note:** If you're seeing different results for the same search in ServiceNow Otto for Virtual Agent than you are in AI Search and ServiceNow Otto Genius Results, it's worth checking that your ServiceNow Otto for Virtual Agent chat assistant uses the same search configuration as your portal's search field does. For details on copying an existing search configuration to a chat assistant, see [Assign search sources to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/add-info-sources-assistant.md).

As previously described, using the same search configuration in the portal and your chat assistant doesn't guarantee that you will see exactly the same search results in ServiceNow Otto for Virtual Agent as you see in the portal using AI Search, but it does remove one possible source of difference.

## Summary of differences between search tools

The following table summarizes some of the key differences between AI Search, ServiceNow Otto Genius Results, and ServiceNow Otto for Virtual Agent.

|Search tool|Search mode|Interaction|LLM usage|
|-----------|-----------|-----------|---------|
|AI Search|Keyword search|Query-based \(search field\)|None|
|ServiceNow Otto Genius Results|Hybrid \(blend of keyword and semantic vector\) search|Query-based \(search field\)|Most relevant search results sent to LLM in a single prompt for answer generation|
|ServiceNow Otto for Virtual Agent|Hybrid \(blend of keyword and semantic vector\) search|Conversation-based \(chat\)|Agentic AI which maintains conversational context when submitting prompts to LLM|

**Parent Topic:**[Exploring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/explore-ais.md)

**Related topics**  


[Lemma and Unicode normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/lemma-unicode-normalization-ais.md)

[Synonyms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/synonyms-ais.md)

[Stop words](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/stop-words-ais.md)

[Typo handling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/typo-handling-ais.md)

[Machine learning relevancy in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/machine-learning-relevancy-ais.md)

[Semantic vector search in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/semantic-search-ais.md)

[Hybrid search in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/hybrid-search-ais.md)

[Summary Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-multi-content-qna-genius-results.md)

[Knowledge base articles Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-qna-genius-results.md)

[Actions Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-catalog-ordering-gr.md)

[ServiceNow Otto for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-va-landing.md)

