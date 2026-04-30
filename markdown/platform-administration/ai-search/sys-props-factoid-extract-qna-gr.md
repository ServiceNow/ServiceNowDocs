---
title: System properties for factoid extraction in Q&amp;A Genius Results
description: A system property determines how the system extracts factoids from knowledge articles when computing Q&amp;A Genius Results.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Q&amp;A Genius Results, Genius Result configurations in the base system, Genius Results, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# System properties for factoid extraction in Q&amp;A Genius Results

A system property determines how the system extracts factoids from knowledge articles when computing Q&amp;A Genius Results.

<table id="table_fwz_xn5_b1c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ais.genius\_result.qna\_mode

</td><td>

Specifies the factoid extraction mode that you want Q&amp;A Genius Results to use. For more information on factoid extraction, see the [Factoid extraction for Q&amp;A Genius Results](../concept/factoid-extraction-qa-grs-ais.md) section.

-   Type: string
-   Default value: **none**
-   Location: System Property \[sys\_properties\] table
-   Supported values:
    -   **none**: Q&amp;A Genius Result answer cards display the full extracted snippet from the source HTML article without highlighting.
    -   **sentence**: Q&amp;A Genius Result answer cards display the sentence from the source HTML article that contains the factoid, with the factoid highlighted if possible.
    -   **snippet**: Q&amp;A Genius Result answer cards display the full extracted snippet from the source HTML article, with the factoid highlighted if possible.

</td></tr></tbody>
</table>**Parent Topic:**[Q&amp;A Genius Results](../concept/genius-result-q-a-ais.md)

