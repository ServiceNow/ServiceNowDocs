---
title: System properties for NLQ Genius Results
description: A system property determines whether the system displays search result preview lists for NLQ Genius Result answers in Service Portal search applications.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [NLQ Genius Results, Genius Result configurations in the base system, Genius Results, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# System properties for NLQ Genius Results

A system property determines whether the system displays search result preview lists for NLQ Genius Result answers in Service Portal search applications.

<table id="table_fdq_xjx_fzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.service\_portal.ais\_nlq\_enabled

</td><td>

Specifies whether the system displays search result preview lists for NLQ Genius Result answers in Service Portal search applications. If you activate the NLQ Genius Result configuration in any Service Portal search application, set this system property's value to **true**.

-   Type: true \| false
-   Default value: false
-   Location: System Property \[sys\_properties\] table
-   Supported values:
    -   **true**: The system displays search result preview lists for NLQ Genius Result answers in Service Portal search applications.
    -   **false**: The system doesn’t display search result preview lists for NLQ Genius Result answers in Service Portal search applications.

**Warning:** This value prevents NLQ Genius Result answers from displaying in Service Portal search applications.


</td></tr></tbody>
</table>**Parent Topic:**[NLQ Genius Results](../concept/genius-result-nlq-ais.md)

