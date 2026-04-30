---
title: Create a text widget
description: To help analysts visualize any patterns in user-entered text in an indicator, create a word cloud visualization in a text widget.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Text analytics and text widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Create a text widget

To help analysts visualize any patterns in user-entered text in an indicator, create a word cloud visualization in a text widget.

## Before you begin

Text indexing must be configured for the relevant indicator source, and this configuration must include the relevant indicator.

Text analytics is available only with the licensed version of Performance Analytics.

Role required: pa\_power\_user or admin

## About this task

The Text widget provides a word cloud for visualizing the frequency of words and phrases.

![Word cloud of text from open incidents, top half](../image/word-cloud-top.png "Word cloud visualization - text widget")

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Widgets** and click **New**.

2.  In the **Name** field, give the widget a name that reflects the information being displayed.

3.  In the **Type** field, select **Text**.

    If you change the value of **Type** after you fill in other fields, those fields are cleared.

    **Word Cloud** is automatically selected as the **Visualization**.

4.  In the **Indicator** field, select the main indicator for which you want to analyze text.

5.  Fill in any of the following fields:

<table id="table_b3s_1cr_w2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Breakdown and Element

</td><td>

Only text that is associated with the specified element of the specified breakdown is analyzed. Select values for both **Breakdown** and **Element**. Otherwise, only text that is not associated with any element of the breakdown is shown.

</td></tr><tr><td>

2nd Breakdown and Element

</td><td>

Drill down to a second level of breakdown and element, if a first-level breakdown and element have been specified. **Note:**

-   Second-level breakdowns must be enabled on the indicator record, in the **Collect breakdown matrix** tab.
-   **Follow element** must be disabled. Dashboard breakdowns count as one breakdown level of the two that are possible.


</td></tr></tbody>
</table>6.  To have the widget follow the breakdown elements that are selected on a breakdown dashboard, follow these steps:

    1.  Select **Follow element**.

        Selecting this option removes the ability to set a second breakdown and element on the widget.

    2.  Set which of the available breakdowns to follow in **Followed breakdown**.

        Breakdown dashboards let you select a breakdown source and elements. However, an indicator can use more than one breakdown that is based on the same breakdown source. Use this setting to determine which of these breakdowns to apply in a breakdown dashboard.

        For example, the indicator Number of open incidents uses two breakdowns: Assigned to, and Opened by. Both breakdowns are based on the Users.Active breakdown source. Consider the case where you create a widget for this indicator and you have the widget follow elements on breakdown dashboards. You want the widget to display separate values for the elements of the Assigned to breakdown. Therefore, you select **Assigned to** in the field **Followed breakdown**.

    **Note:** This widget type does not support multiple element selection. If you select multiple elements on a breakdown dashboard with this widget, the widget ignores all selected elements.

    For more information, see [Configure widgets for breakdown dashboards](set-up-widgets-for-breakdown-dashboards.md).

7.  Set the cutoff value, which filters which words and phrases are shown in the widget based on the frequency of a word or phrase in the field:

    1.  In the **Cutoff** field, select whether the cutoff value is a numerical count or a relative percentage.

        -   **Count** is the number of occurrences of a word or phrase in the field. For example, if the cutoff settings are \[\[Count\]\[Greater than or equal to\]\[10\]\], the widget shows only words and phrases that occur ten or more times.
        -   **Percentage** refers to the percent of occurrences of all words in the field that are occurrences of the word or phrase. For example, if there are 30 total occurrences of all words in the field and the cutoff settings are \[\[Percentage\]\[Greater than or equal to\]\[10\]\], the widget shows only words or phrases that occur three or more times.
    2.  In the **Cutoff conditions** field, select whether the cutoff value is a minimum or a maximum.

        -   **Greater than or equal to** has the widget show a word or phrase if it is at least as common as the cutoff value.
        -   **Less than or equal to** has the widget show a word or phrase if it is no more common than the cutoff value.
    3.  In the **Cutoff value** field, specify an integer value.

8.  Set any of the remaining display settings.

    |Field|Description|
    |-----|-----------|
    |Default field|If multiple fields are selected in the text index configuration, this field appears by default.|
    |Maximum number of words|The maximum number of words to be displayed in the word cloud|
    |Maximum number of trendlines|The maximum number of trend lines to be displayed beneath the word cloud|


## What to do next

-   Add the widget to a dashboard.
-   The admin or the dashboard owner shares the dashboard containing the widget with these users.
-   Text analysis uses special steps in the [data collection job](../concept/performance-analytics-glossary.md#). If no data is available for the widget, verify that the relevant data collection job has run and that the job collects text indexes. See [Collect initial text analytics data](collect-initial-text-analytics-data.md).
-   Filter the word cloud by keywords.

