---
title: Work notes analysis
description: Work notes analysis helps you understand the operational reasons behind activity transitions, as recorded in work notes and comments. Typical examples include transitions from resolved to work in progress or changes in assignment groups, such as from service desk to specialist group.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Analyzing and getting process insights, Use, Process Mining, Platform Analytics]
---

# Work notes analysis

Work notes analysis helps you understand the operational reasons behind activity transitions, as recorded in work notes and comments. Typical examples include transitions from resolved to work in progress or changes in assignment groups, such as from service desk to specialist group.

To better understand the reasons behind a transition, work notes from both agents and requesters are analyzed. This involves extracting notes recorded immediately before and after the transition event. These notes are then grouped using clustering techniques to identify patterns and categorize similar records.

There are two types of work notes analysis. You can do a clustering with or without the Now Assist capability. For information on using work notes analysis with Now Assist capability, see [Using Now Assist for Process Mining](use-na-process-mining.md).

**Note:** Work notes analysis is available for a record count between 100 and 300,000.

You can use the Now Assist feature for work notes analysis even with 5-50 eligible work notes. If there are less than 25 eligible work notes, the system will not run clustering, but will put all the work notes into one LLM call, otherwise clustering will be performed before calling the LLM.

-   **[Configure work notes analysis](../task/configure-worknotes-analysis.md)**  
Configure work notes analysis for a process table to view the work notes analysis for a project based on that process table.
-   **[Perform work notes analysis](../task/perform-worknotes-analysis.md)**  
Generate a work notes analysis on a transition.
-   **[Resubmit work notes analysis](../task/resubmit-worknotes-analysis.md)**  
If a work notes analysis fails for some reason, you can resubmit it.

**Parent Topic:**[Analyzing and getting process insights](analyze-get-process-insights.md)

