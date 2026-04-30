---
title: Q&amp;A Genius Results
description: Q&amp;A Genius Results display top search results extracted from HTML fields of records on the Knowledge \[kb\_knowledge\] table and tables that extend it. Each Q&amp;A Genius Result answer card shows a topic snippet and an answer snippet extracted from a single Knowledge article. You can view the full article directly from the answer card.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Genius Result configurations in the base system, Genius Results, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Q&amp;A Genius Results

Q&amp;A Genius Results display top search results extracted from HTML fields of records on the Knowledge \[kb\_knowledge\] table and tables that extend it. Each Q&amp;A Genius Result answer card shows a topic snippet and an answer snippet extracted from a single Knowledge article. You can view the full article directly from the answer card.

A snippet is a short, typically paragraph-length, section of text that contains useful and relevant information. A Genius Result answer's topic snippet indicates the subject for the answer, while the answer snippet provides details on that subject.

![Q&A answer card for knowledge article with View Article action link.](../image/genius-result-q-a.png "Sample Q&A Genius Result answer card")

Select **View Article** to view the full Knowledge article.

**Note:** Knowledge search property settings don't affect Q&amp;A Genius Results. For more information on these settings, see [Knowledge search properties](https://www.servicenow.com/docs/access?context=r_KnowledgeProperties&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Q&amp;A Genius Results only support English searches.

Because the Q&amp;A implementation is based on deep neural networks that are continually improving, Q&amp;A results for specific queries may vary from release to release. Articles boosted or promoted by result improvement rules are more likely to appear as Q&amp;A Genius Results, but aren't guaranteed to appear.

## Topic and answer snippet extraction for Q&amp;A Genius Results

By default, AI Search automatically determines which elements of a Knowledge article's HTML field values to extract as the Q&amp;A topic and answer snippets. You can't configure the criteria for this extraction behavior.

Topic and answer snippet extraction behavior varies depending on the source table for the Knowledge article:

<table id="table_fd5_31m_tnb"><thead><tr><th>

Knowledge article source

</th><th>

Q&amp;A topic and answer snippet extraction

</th></tr></thead><tbody><tr><td>

FAQ \[kb\_template\_faq\] table**Note:** This table is enabled when you activate the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\). For more information, see [Activate the Knowledge Management Advanced plugin](https://www.servicenow.com/docs/access?context=activate-knowledge-advanced-plugin&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

</td><td>

AI Search extracts the Q&amp;A topic snippet from the Knowledge article record's **Question** HTML field. It extracts the Q&amp;A answer snippet from the record's **Answer** HTML field.

</td></tr><tr><td>

Knowledge \[kb\_knowledge\] table and all other tables that extend it

</td><td>

AI Search extracts the Q&amp;A topic and answer snippets from the Knowledge article record's HTML fields.

</td></tr></tbody>
</table>Because the default extraction behavior favors search precision, it may not extract all desired Q&amp;A topic and answer snippets. You can override the extraction behavior for a Knowledge article by manually designating topic and answer snippets in that article's HTML fields. Manually designating snippets increases the likelihood that they will appear as Q&amp;A results, but doesn't guarantee that they will.

To manually designate snippets for an article, set the following HTML classes on elements in the article's HTML fields.

<table id="table_dqd_slr_snb"><thead><tr><th>

HTML Class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`class="sn_snippet_topic"`

</td><td>

Set this class on the HTML field element that contains text that you want to designate as the Q&amp;A Genius Result topic snippet for the Knowledge article.

</td></tr><tr><td>

`class="sn_snippet_answer"`

</td><td>

Set this class on the HTML element that contains text that you want to designate as the Q&amp;A Genius Result answer snippet for the Knowledge article.**Note:** Answer snippets should be from 250 to 300 characters in length. Longer answer snippets may be cut off when displayed on the Q&amp;A Genius Results card.

</td></tr></tbody>
</table>## Machine reading comprehension model

AI Search uses a machine reading comprehension \(MRC\) model to validate extracted answer snippets. The MRC model analyzes each extracted snippet to determine whether it answers your question. An answer snippet must pass this validation filter step before it can be displayed as a Q&amp;A Genius Result answer.

When you enable factoid extraction for Q&amp;A Genius Results, the MRC model also finds the exact span of text within the extracted snippet that represents the answer to your question.

You can't configure settings for MRC models or choose which model to use for Q&amp;A Genius Results. AI Search performs A/B testing with different search query parameter values to automatically select the best MRC model for you. For more details on this A/B testing process, see [Search query parameter evaluation framework](srch-qry-parm-eval-fw-ais.md#).

## Knowledge Management and Q&amp;A Genius Results

When you activate the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\), Q&amp;A Genius Results can return answers from records on the FAQ \[kb\_template\_faq\] table as well as records on the Knowledge \[kb\_knowledge\] table and its child tables.

Additionally, if a search query satisfies one of the following conditions, AI Search bypasses the usual Q&amp;A routines and returns the FAQ record's **Answer** field value as a Q&amp;A Genius Result answer:

-   The user's search query exactly matches the **Question** field value from the FAQ record.
-   A result improvement rule promotes the FAQ record to be the first result for the user's search

As an example, suppose you create an FAQ record with **Question** `How do I reset my password?`. When a user searches for `how do I reset my password`, AI Search returns a Q&amp;A Genius Result card with an answer snippet extracted from the FAQ record's **Answer** field value.

## Interaction with other search features for Q&amp;A Genius Results

The following table describes interactions between Q&amp;A Genius Results and other search features.

|Feature|Interaction with Q&amp;A Genius Results|
|-------|---------------------------------------|
|[Result improvement rules](result-improvement-rules-ais.md) with block actions|When computing Q&amp;A Genius Results for a search query, AI Search ignores blocked search results.|
|[Stop words](stop-words-ais.md)|When computing Q&amp;A Genius Results for a search query, AI Search ignores stop words in the query.|
|[Synonyms](synonyms-ais.md)|When computing Q&amp;A Genius Results for a search query, AI Search expands synonyms in the query.|
|[Typo handling](typo-handling-ais.md)|When computing Q&amp;A Genius Results for a search query, AI Search corrects terms in the query.|

-   **[Factoid extraction for Q&amp;A Genius Results](factoid-extraction-qa-grs-ais.md)**  
Factoid extraction uses the machine reading comprehension \(MRC\) model to find the exact span of text within a longer extracted snippet that represents the answer to your question.
-   **[Set the factoid extraction mode for Q&amp;A Genius Results](../task/set-factoid-extraction-mode-qna-gr.md)**  
Specify how you want factoid extraction to display and highlight answers for Q&amp;A Genius Results.
-   **[System properties for factoid extraction in Q&amp;A Genius Results](../reference/sys-props-factoid-extract-qna-gr.md)**  
A system property determines how the system extracts factoids from knowledge articles when computing Q&amp;A Genius Results.

**Parent Topic:**[Genius Result configurations in the base system](default-genius-result-configs-ais.md)

