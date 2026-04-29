---
title: Run work notes analysis
description: Generate a work notes analysis on a transition.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Now Assist for Process Mining, Use, Process Mining, Platform Analytics]
---

# Run work notes analysis

Generate a work notes analysis on a transition.

## Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

**Note:** Work notes with more than 5 words and fewer than 100 words are considered for the analysis.

You can use the Now Assist feature for work notes analysis even with 5-50 eligible work notes. If there are less than 25 eligible work notes, the system will not run clustering, but will put all the work notes into one LLM call, otherwise clustering will be performed before calling the LLM.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Process Mining Workspace**.

2.  From the list of projects, select a project.

3.  Select any transition.

    A window is displayed with all the details.

    ![Work notes analysis](../image/na-worknotes.png)

4.  From the **Investigate** section, select **Work notes analysis**.

    A scheduled task starts.

5.  After the scheduled task is complete, select **View result**.

    The result is displayed.

    ![Work notes analysis result using Now Assist](../image/na-worknotes-result.png)

    Use the thumbs up and thumbs down icons to provide feedback for the result that you have received.


**Parent Topic:**[Using Now Assist for Process Mining](../concept/use-na-process-mining.md)

