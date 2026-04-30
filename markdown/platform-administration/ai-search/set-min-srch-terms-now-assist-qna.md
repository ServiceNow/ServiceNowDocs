---
title: Change the minimum search term count for Now Assist Q&amp;A Genius Results
description: Specify the minimum number of terms that a search must contain to be eligible for triggering Now Assist Q&amp;A Q&amp;A Genius Results. Searches with fewer terms don't return Now Assist Q&amp;A Genius Result answers.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-03"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist Q&amp;A Genius Results, Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Change the minimum search term count for Now Assist Q&amp;A Genius Results

Specify the minimum number of terms that a search must contain to be eligible for triggering Now Assist Q&amp;A Q&amp;A Genius Results. Searches with fewer terms don't return Now Assist Q&amp;A Genius Result answers.

## Before you begin

The Now Assist in AI Search ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install Now Assist in AI Search](install-now-assist-ais.md).

Role required: ais\_admin

## About this task

Now Assist Q&amp;A Genius Results send eligible knowledge article search results to the Now LLM Service for Q&amp;A Genius Result answer generation.

By default, the system only sends knowledge article results to the Now LLM Service when the search satisfies all of these conditions.

-   The search application is Service Portal, Virtual Agent, Employee Center, or global search.
-   The user's session language is English.
-   The search contains two or more terms.
-   The search matches the Java regular expression pattern defined by the **sn\_ais\_assist.u\_question\_regex** system property's value. This system property has no value set in the base system, so by default all search queries satisfy this condition.

You can customize the term count condition by altering the minimum term count required by Now Assist Q&amp;A Genius Result configurations.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Query Settings** &gt; **Genius Results**.

2.  Open the record for the Q&amp;A - Now Assist Genius Result configuration by selecting it from the list.

3.  In the **AI Search response processor** field, locate the following code block:

    ```
        var searchPhrase = context.getOriginalSearchPhrase();
        if (searchPhrase.split(" ").length < 2) {
            return answer;
        }
    ```

4.  Change the inequality statement's numeric argument from `2` to another positive integer.

    As an example, if you only want the Genius Result configuration to operate on searches with three or more search terms, change `2` to `3`. If you want the Genius Result configuration to operate on searches with any number of search terms, change `2` to `1`.

5.  Select **Update**.


## Result

The modified Genius Result configuration doesn't send knowledge article search results to the Now LLM Service for Q&amp;A answer generation unless the search query has enough search terms to satisfy your chosen limit.

**Parent Topic:**[Now Assist Q&amp;A Genius Results](../concept/now-assist-qna-genius-results.md)

