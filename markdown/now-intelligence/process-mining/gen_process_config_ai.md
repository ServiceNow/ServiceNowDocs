---
title: Generate process configuration using AI
description: Use AI to generate a suggestion for the process configuration fields for a table, instead of selecting each field manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/gen\_process\_config\_ai.html
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 1
keywords: [process mining, process configuration, ai, now assist]
breadcrumb: [Creating process configuration, Use, Process Mining, Platform Analytics]
---

# Generate process configuration using AI

Use AI to generate a suggestion for the process configuration fields for a table, instead of selecting each field manually.

## Before you begin

ServiceNow Otto for Process Mining must be installed and the following skills must be enabled:

-   Generate process configuration skill: This skill is activated by default.
-   Generate state responsibility mapping skill: This skill is activated by default.

Role required: sn\_process\_mining\_power\_user or sn\_process\_mining\_admin

## About this task

AI analyzes your table's fields and how frequently they change, then suggests which fields to use for your control flow \(state\), team, and agent definitions, along with suggested breakdown, work notes, and root-cause-analysis fields.

**Note:** AI recommendation for clustering and intent and activity analysis is not supported.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the left of the page, select the Process configurations icon \(\[Omitted image "icon-process-config.png"\] Alt text: Process configuration builder\).

3.  Select **Create New**.

    The New process configuration dialog box is displayed.

    \[Omitted image "new-pr-config.png"\] Alt text: New process configuration dialog box

4.  Select a table.

5.  Select **Generate configuration** from the header.

    \[Omitted image "gen-process-config-ai-1.png"\] Alt text: Generate configuration button

    A loading indicator appears while suggestions are generated.

6.  Review the suggested fields in the dialog box that appears.

    \[Omitted image "gen-process-config-ai-2.png"\] Alt text: Review configuration

    If a field already has an existing value, it's shown alongside the suggestion in an **Existing value** column so you can compare before deciding.

    **Note:** Selecting an alternative Control flow value clears any existing Kanban mapping.

7.  Select or deselect the fields you want to apply, then select **Confirm**.

    The process configuration is displayed with all the selected values.

8.  On the Process details tab, select **Map state responsibilities** under State definition.

    The mapping is created by AI, make updates as required.


## Result

The fields you confirmed are applied to your process configuration.

**Parent Topic:**[Creating process configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/creating-process-config.md)

