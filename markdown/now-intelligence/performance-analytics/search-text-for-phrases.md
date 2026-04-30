---
title: Search text for phrases
description: You can specify phrases that text analytics searches for, instead of searching for only the most frequent individual words.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Text analytics and text widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Search text for phrases

You can specify phrases that text analytics searches for, instead of searching for only the most frequent individual words.

## Before you begin

Role required: pa\_analyst, pa\_power\_user, or admin

## Procedure

1.  Navigate to **All** &gt; **Text analytics** &gt; **Phrases** and click **New**.

    To edit an existing text index phrases form, click the information icon for that form, then select **Open Record** from the preview window.

2.  Select the **Indicator** that you want to search for phrases.

    Text Analytics must be set up for this indicator.

3.  In the **Breakdown** and **Element** fields, you can filter the records that are searched for the phrases.

    Specify both a breakdown and an element. You can filter to a second level by filling in the level 2 **Breakdown** and **Element** fields.

4.  Enter a comma-separated series of phrases in the **Phrases** field.

    For example, enter "can't access, don't see."


## Result

When you include a text widget for this indicator in a dashboard, the specified phrases appear in the trend line.

![The phrases that were specified are visible as trend lines in the widget.](../image/text-analysis-phrases.png "Text widget with phrases "don't see" and "can't access"")

