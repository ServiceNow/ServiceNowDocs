---
title: Change the question or filter conditions
description: Regenerate the response to a question after you change the question or the filter conditions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Questions and responses in an exploration, Use, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Change the question or filter conditions

Regenerate the response to a question after you change the question or the filter conditions.

## Before you begin

Role required: now\_assist\_explorer\_user and ownership or editing rights to the exploration.

## Procedure

1.  Launch AI Data Explorer.

2.  Open an exploration that has a question and response that you may want to change.

    For example, you may have imported a data visualization, and you want a different set of filter conditions than the original.

3.  Locate the question and response of interest.

4.  If you want to change the question, select the **Edit question** button ![Edit source icon](../../../administer/process-mining/image/edit-icon.png).

    ![The Edit Question button next to the question quoted by a response.](../image/nowass-explr-edit-question.png)

    1.  Edit the question.

    2.  Select the **Send the prompt** arrow.

        ![Question editing field showing Send the prompt arrow.](../image/nowass-expl-edit-question-send-prompt.png)

    A new response is generated, replacing the old one.

5.  To change the filter conditions, follow one of these steps, depending on how wide the exploration is on your screen:

    -   If the exploration is wide, you see an **Edit source** button next to the **AI** button on the response. Press it.

        ![The Edit source button in a response](../image/nowass-expl-edit-source.png)

    -   If the exploration is narrow, you see a **View source** button instead of an **Edit source** button. Press that to open the source information, then press the ![Edit source icon](../../../administer/process-mining/image/edit-icon.png) in the source information.

        ![The information pane that opens when you select View source for a generated response.](../image/nowass-expl-view-source.png)

    The Source dialog opens.

    ![Response source editor with condition builder.](../image/nowass-expl-response-source-editor.png)

6.  Change the filter conditions to meet your needs.

7.  Select **Regenerate**.


## Result

The data visualization, summary, and suggested follow-on questions are regenerated using your modified filter conditions.

**Note:** Regenerating a response removes all changes that you made manually to the text in the summary.

**Parent Topic:**[Questions and responses in an exploration](../concept/ask-expl-questions.md)

