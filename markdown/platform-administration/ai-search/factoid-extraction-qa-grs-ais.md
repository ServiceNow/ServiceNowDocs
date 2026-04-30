---
title: Factoid extraction for Q&amp;A Genius Results
description: Factoid extraction uses the machine reading comprehension \(MRC\) model to find the exact span of text within a longer extracted snippet that represents the answer to your question.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Q&amp;A Genius Results, Genius Result configurations in the base system, Genius Results, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Factoid extraction for Q&amp;A Genius Results

Factoid extraction uses the machine reading comprehension \(MRC\) model to find the exact span of text within a longer extracted snippet that represents the answer to your question.

## Enabling factoid extraction

To enable factoid extraction for Q&amp;A Genius Results, set the **glide.ais.genius\_result.qna\_mode** system property to **sentence** or **snippet**.

For details on setting this system property, see the [Set the factoid extraction mode for Q&amp;A Genius Results](../task/set-factoid-extraction-mode-qna-gr.md) section. To learn about the effects of this system property's values, see the [System properties for factoid extraction in Q&amp;A Genius Results](../reference/sys-props-factoid-extract-qna-gr.md) section.

## Examples of factoid extraction

The following images illustrate how the **glide.ais.genius\_result.qna\_mode** system property setting affects the display of Q&amp;A Genius Result answer cards for a sample `What is the Windows key?` search in Service Portal.

-   With the system property set to **none**, the Q&amp;A Genius Result answer card displays the full extracted text snippet with no highlighting:

    ![Q&A Genius Result answer card in Service Portal with glide.ais.genius_result.qna_mode system property set to none.](../image/qna_mode-none.png)

-   With the system property set to **sentence**, the Q&amp;A Genius Result answer card displays only the sentence containing the factoid, and highlights the factoid:

    ![Q&A Genius Result answer card in Service Portal with glide.ais.genius_result.qna_mode system property set to sentence.](../image/qna_mode-sentence.png)

-   With the system property set to **snippet**, the Q&amp;A Genius Result answer card displays the full extracted text snippet and highlights the factoid:

    ![Q&A Genius Result answer card in Service Portal with glide.ais.genius_result.qna_mode system property set to snippet.](../image/qna_mode-snippet.png)


**Parent Topic:**[Q&amp;A Genius Results](genius-result-q-a-ais.md)

