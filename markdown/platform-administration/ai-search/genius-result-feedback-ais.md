---
title: Provide feedback on Genius Results
description: Users can submit feedback for each Genius Result answer card, specifying whether it was helpful for their search or not. For cards from default Genius Result configurations, users can also select the reason they found an answer unhelpful. AI Search records feedback responses as search signals that you can use to assess the relevancy of your Genius Result configurations.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-08-25"
reading_time_minutes: 1
breadcrumb: [Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Provide feedback on Genius Results

Users can submit feedback for each Genius Result answer card, specifying whether it was helpful for their search or not. For cards from default Genius Result configurations, users can also select the reason they found an answer unhelpful. AI Search records feedback responses as search signals that you can use to assess the relevancy of your Genius Result configurations.

## Before you begin

You must have performed a search that returned one or more Genius Result answer cards.

Role required: none

## About this task

You can provide feedback for each Genius Result answer card in your search result set, marking it as helpful or unhelpful for your search. If you mark an answer card produced by a default Genius Result configuration as unhelpful, you can also select the reason it was unhelpful.

AI Search stores user feedback for Genius Result answers as signals in the Genius Result Event Action \[sys\_search\_genius\_result\_event\_action\] table. For more information on this table, see [Search signal tables](../../search-administration/reference/search-signal-tables.md).

## Procedure

1.  On the Genius Result answer card that you want to provide feedback for, find the **Helpful?** section.

2.  Choose one of the following:

    -   If you found the Genius Result answer helpful for your search, select **Yes**.
    -   If you found the Genius Result answer unhelpful for your search, select **No**.
3.  If you selected **No** on an answer card produced by a default Genius Result configuration, choose one of the following:

    -   To indicate why you found the Genius Result answer unhelpful, select a reason from the list in the dialog box, then select **Submit feedback**.
    -   To submit your feedback without a reason, select anywhere outside the dialog box.

## Result

AI Search submits your feedback as a search signal.

**Parent Topic:**[Searching in AI Search](../concept/use-ais.md)

