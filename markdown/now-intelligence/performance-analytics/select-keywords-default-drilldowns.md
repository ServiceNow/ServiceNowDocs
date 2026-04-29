---
title: Save keywords for text analytics
description: You can save keywords that will always filter a text analytics widget. You can save them directly on the widget in a dashboard, choosing from the words in the word cloud. Alternatively, you can create or edit a record of saved keywords.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Text analytics and text widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Save keywords for text analytics

You can save keywords that will always filter a text analytics widget. You can save them directly on the widget in a dashboard, choosing from the words in the word cloud. Alternatively, you can create or edit a record of saved keywords.

## Before you begin

Role required: pa\_analyst or admin

## About this task

To filter a word cloud by keywords, select the words in the cloud. You can save a list of the keywords, which will be used whenever someone views the widget. Each list of keywords applies to one breakdown and element combination for the indicator in one widget. In the following example, the word "battery" has been specified as a keyword. If you select **Save**, all viewers will see this widget filtered by "battery." Anyone with the required roles can delete the saved keywords later.

![Word cloud of text from open incidents, bottom half](../image/word-cloud-bottom.png "Word cloud filtered by keyword 'battery'")

Alternatively, you can create or edit the record where the keywords are saved. This approach does not restrict your selection to keywords that have already appeared in the word cloud.

## Procedure

1.  Navigate to **All** &gt; **Text Analytics** &gt; **Keywords** and select **New**.

2.  In the **Widget** field, specify the widget to which the keywords apply.

3.  In the **Indicator** field, specify the indicator to which the keywords apply.

4.  In the **Field** field, select the indicator field that the keywords apply to.

5.  In the **Breakdown** and **Element** fields, you can filter the records to which the keywords apply by a breakdown element.

    Specify both a breakdown and an element. You can filter to a second level by filling in the level 2 **Breakdown** and **Element** fields.

    If you specify a breakdown and element combination, the keywords only apply when that combination is selected in the widget. If you do not specify a breakdown and element combination, the keywords apply for all breakdown and element combinations that do not have keywords selected specifically for them.

6.  In the **Keywords** field, enter a comma-separated list of keywords.

7.  Select **Submit**.


