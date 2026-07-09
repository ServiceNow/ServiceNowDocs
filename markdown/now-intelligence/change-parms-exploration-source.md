---
title: Regenerate a response in an AI Data Explorer exploration
description: Change the filter conditions for a table source or data visualization parameters for an indicator source. Then regenerate a response with updated visualizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/change-parms-exploration-source.html
release: australia
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 2
keywords: [exploration, source conditions, indicator parameters, filter conditions, edit source]
breadcrumb: [Questions and responses in an exploration, Use, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Regenerate a response in an AI Data Explorer exploration

Change the filter conditions for a table sourceor data visualization parameters for an indicator source. Then regenerate a response with updated visualizations.

## Before you begin

Role required: now\_assist\_explorer\_user and ownership or editing rights to the exploration.

## Procedure

1.  Launch AI Data Explorer.

2.  Open an exploration that has a question and response whose source you want to change.

    For example, you may have imported a data visualization, and you want a different set of filter conditions than the original.

3.  Locate the question and response of interest.

4.  Open the source editor, depending on how wide the exploration is on your screen:

    -   If the exploration is wide, you see an **Edit source** button next to the **AI** button on the response. Select it.

        \[Omitted image "nowass-expl-edit-source.png"\] Alt text: The Edit source button in a response

    -   If the exploration is narrow, you see a **View source** button instead of an **Edit source** button. Select that to open the source information, then select the \[Omitted image "edit-icon.png"\] Alt text: Edit source icon in the source information.

        \[Omitted image "nowass-expl-view-source.png"\] Alt text: The information pane that opens when you select View source for a generated response.

5.  Edit the options in the source editor.

    This editor shows some configuration options from the data visualization in the response. The options vary depending on whether the source is a table or an indicator.

    -   For a table source, you can edit the filter conditions like in a visualization's Data Source editor. You can also view the metric or open a list of table records. You cannot select from predefined conditions.

        \[Omitted image "nowass-expl-response-source-editor.png"\] Alt text: Response source editor for table source with condition builder.

    -   For each indicator in a source, you can change the following settings:

        -   The applied breakdown, like in the visualization data source editor
        -   The date range
        -   The data aggregation \(Score, Sum, Average\), like in the Date range options \(not available for time series\)
        **Note:** The period options include Weekly, which is not available in data visualizations.

        Other options include:

        -   View other properties such as the time series aggregation on the visualization.
        -   Open the indicator record through the View indicator details link.
        -   Explore the indicator in KPI Details.
        For more information about these settings, see [Automated indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/automated-indicators.md).

        \[Omitted image "aide-indicator-source-editor.png"\] Alt text: Response source editor for indicator source with condition builder.

6.  Complete your changes and select **Regenerate**.


## Result

The data visualization, summary, and suggested follow-on questions are regenerated using your modified settings.

**Note:** Regenerating a response removes all changes that you made manually to the text in the summary.

**Parent Topic:**[Questions and responses in an exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/ask-expl-questions.md)

