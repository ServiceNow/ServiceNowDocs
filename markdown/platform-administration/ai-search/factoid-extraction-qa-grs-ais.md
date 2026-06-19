---
title: Factoid extraction for Q&amp;A Genius Results
description: Factoid extraction uses the machine reading comprehension \(MRC\) model to find the exact span of text within a longer extracted snippet that represents the answer to your question.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/factoid-extraction-qa-grs-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Q&amp;A Genius Results, Genius Result configurations in the base system, Genius Results, Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Factoid extraction for Q&amp;A Genius Results

Factoid extraction uses the machine reading comprehension \(MRC\) model to find the exact span of text within a longer extracted snippet that represents the answer to your question.

## Enabling factoid extraction

To enable factoid extraction for Q&amp;A Genius Results, set the **glide.ais.genius\_result.qna\_mode** system property to **sentence** or **snippet**.

For details on setting this system property, see the [Set the factoid extraction mode for Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/set-factoid-extraction-mode-qna-gr.md) section. To learn about the effects of this system property's values, see the [System properties for factoid extraction in Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/sys-props-factoid-extract-qna-gr.md) section.

## Examples of factoid extraction

The following images illustrate how the **glide.ais.genius\_result.qna\_mode** system property setting affects the display of Q&amp;A Genius Result answer cards for a sample `What is the Windows key?` search in Service Portal.

-   With the system property set to **none**, the Q&amp;A Genius Result answer card displays the full extracted text snippet with no highlighting:

    \[Omitted image "qna\_mode-none.png"\] Alt text: Q&amp;A Genius Result answer card in Service Portal with glide.ais.genius\_result.qna\_mode system property set to none.

-   With the system property set to **sentence**, the Q&amp;A Genius Result answer card displays only the sentence containing the factoid, and highlights the factoid:

    \[Omitted image "qna\_mode-sentence.png"\] Alt text: Q&amp;A Genius Result answer card in Service Portal with glide.ais.genius\_result.qna\_mode system property set to sentence.

-   With the system property set to **snippet**, the Q&amp;A Genius Result answer card displays the full extracted text snippet and highlights the factoid:

    \[Omitted image "qna\_mode-snippet.png"\] Alt text: Q&amp;A Genius Result answer card in Service Portal with glide.ais.genius\_result.qna\_mode system property set to snippet.


**Parent Topic:**[Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/genius-result-q-a-ais.md)

