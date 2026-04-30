---
title: Select text analytics stop words
description: Select words to exclude from text analysis. You can exclude words at either the indicator source or the indicator level.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Text analytics and text widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Select text analytics stop words

Select words to exclude from text analysis. You can exclude words at either the indicator source or the indicator level.

## Before you begin

Role required: pa\_analyst or pa\_admin

## About this task

Select stop words to apply either at the indicator source or at the indicator level. If you select stop words for an indicator, you can filter the scores to which the stop words apply by breakdown and breakdown element. If you select stop words for an indicator source, you exclude them from data collection, which results in a leaner index.

By default, the Zing global stop words apply in addition to the stop words you select in this form. You can disable this behavior in the text index configuration. To find the list of the current stop words, navigate on your instance to **System Definition** &gt; **Text Index Stop Words**.

## Procedure

1.  Navigate to **Text Analytics** &gt; **Stop Words** and click **New**.

2.  In the **Type** field, select either **Indicator** or **Indicator source**.

    If you specify an indicator, you can filter the text by one or two levels of breakdown.

    When specified on the indicator source, stop words are removed from data collection to keep the index lean. However, you cannot immediately bring these stop words back into the widget by removing them from the **Stopwords** field. They do not appear until the next data collection.

    Stop words that are specified on the indicator remain in the index. These stop words can be brought back into the widget immediately by removing them from the **Stopwords** list, but index size may affect performance.

3.  Select either the **Indicator** or the **Indicator source** to which to apply the stop words.

4.  To filter the text by a breakdown, select values in the **Breakdown** and first **Element** fields.

    If you select a breakdown but not an element, the widget analyses only the text that is not associated with any element of that breakdown.

5.  If you have selected a breakdown and you want to filter the text by a second breakdown, select values in the **2nd Breakdown** and second **Element** fields.

6.  In the **Stopwords** field, enter a comma-separated list of words to exclude from the text analysis.

7.  Click **Submit**.


