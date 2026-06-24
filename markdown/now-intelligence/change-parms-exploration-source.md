---
title: Change the parameters for a data source in an exploration
description: In an AI Data Explorer exploration, change the filter conditions for a table source. Then regenerate a response with updated data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/change-parms-exploration-source.html
release: zurich
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 1
keywords: [exploration, source conditions, indicator parameters, filter conditions, edit source]
breadcrumb: [Questions and responses in an exploration, Use, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Change the parameters for a data source in an exploration

In an AI Data Explorer exploration, change the filter conditions for a table source. Then regenerate a response with updated data.

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

    The Source dialog opens.

    \[Omitted image "nowass-expl-response-source-editor.png"\] Alt text: Response source editor for table source with condition builder.

5.  Change the filter conditions to meet your needs.

6.  Select **Regenerate**.


## Result

The data visualization, summary, and suggested follow-on questions are regenerated using your modified conditions or parameters.

**Note:** Regenerating a response removes all changes that you made manually to the text in the summary.

**Parent Topic:**[Questions and responses in an exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/ask-expl-questions.md)

