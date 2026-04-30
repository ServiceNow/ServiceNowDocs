---
title: Set the factoid extraction mode for Q&amp;A Genius Results
description: Specify how you want factoid extraction to display and highlight answers for Q&amp;A Genius Results.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2024-11-05"
reading_time_minutes: 1
breadcrumb: [Q&amp;A Genius Results, Genius Result configurations in the base system, Genius Results, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set the factoid extraction mode for Q&amp;A Genius Results

Specify how you want factoid extraction to display and highlight answers for Q&amp;A Genius Results.

## Before you begin

Role required: ais\_admin

## About this task

As a search administrator, you can specify the factoid extraction mode for Q&amp;A Genius Results by setting the value of the **glide.ais.genius\_result.qna\_mode** system property. This system property does not exist in the base system, so you may have to add it.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Search for a system property record with name **glide.ais.genius\_result.qna\_mode**.

    -   If a system property record with this name exists, open the record by selecting it.
    -   If no system property record with this name exists, select **New**, then enter `glide.ais.genius_result.qna_mode` in the System Property form's **Name** field.
3.  In the System Property form's **Value** field, enter one of the following values:

    -   **none** if you want to disable factoid extraction and highlighting for Q&amp;A Genius Results.
    -   **sentence** if you want Q&amp;A Genius Result answer cards to display only the sentence containing the factoid \(and to highlight the factoid\).
    -   **snippet** if you want Q&amp;A Genius Result answer cards to display the full extracted text snippet containing the factoid \(and to highlight the factoid\).
    For details on these system property values, see the [System properties for factoid extraction in Q&amp;A Genius Results](../reference/sys-props-factoid-extract-qna-gr.md) section.

4.  Save the modified System Property record by selecting **Submit** or **Update**.


**Parent Topic:**[Q&amp;A Genius Results](../concept/genius-result-q-a-ais.md)

