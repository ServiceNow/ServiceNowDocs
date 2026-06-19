---
title: Review and mine your project
description: After you’ve created the project by setting the objectives, scoping the analysis, and adding improvement opportunities, it’s time to mine the project.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/review-mine.html
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a project or template using Project Builder, Use, Process Mining, Platform Analytics]
---

# Review and mine your project

After you’ve created the project by setting the objectives, scoping the analysis, and adding improvement opportunities, it’s time to mine the project.

## Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

## About this task

**Record limits for Process Mining projects**

Process Mining enforces a maximum of 500,000 records from the primary table. This limit scales down proportionally as child tables are added to the project.

|Table configuration|Record limit|
|-------------------|------------|
|1 table|500,000|
|1 table + 1 child|~250,000|
|1 table + 2 children|~125,000|
|1 table + 3 children|~100,000|

Nested child tables reduce the record limit significantly more than flat structures, because deeper relationships multiply the processing cost per record.

|Table configuration|Record limit|
|-------------------|------------|
|1 table → child → grandchild → great-grandchild|~71,000|

**What happens when the limit is exceeded**

If your record count exceeds the adjusted limit, mining is blocked. To resolve this:

-   Narrow your project filter to reduce the number of records.
-   Simplify your table structure by removing unnecessary child or nested tables.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

    If you continue from the **Improvement opportunities** page, you are on the **Review and mine** page.

2.  Select **Edit** for the project that you want to review and mine.

    You're taken to the **Review and mine** tab.

3.  On the **Review and mine** tab, review the project.

    You can do some additional steps on this page.

    \[Omitted image "mine-extra-steps.png"\] Alt text: Additional tasks

    -   Select **Manage watchlist** to add users who receive notifications regarding the status of the mined project.
    -   Select **Copy project definition** to copy the project.

        When you copy a project, the associated improvement opportunities also get copied.

    -   Select **Extract data logs** to view any logs available.
    -   Select **Delete** to delete the project.
4.  Select **Mine Project** to mine the project.

5.  On the **Mine** window, select **Sample Mine** or **Full Mine**, and select **Confirm &amp; Mine**.


## Result

The **Mining Progress** page is displayed. After the mining is completed, a **Mining Summary** page is displayed. This page provides additional details about the mining. It also lists any finding definition that wasn’t included in the mining and provides a link to understand the actual cause. You can also view the logs or go to the Process Mining Workspace and view the graph.

**Note:** If you select **Full Mine** and your project includes consumption-based tables, a warning message appears when the number of records exceeds the threshold defined in the `promin.metered_usage.warning_limit` property. To turn off this warning, set the `promin.metered_usage.warning_limit` property to **-1**. The default value for this property is -1, which means it is turned off.

\[Omitted image "mining-summary.png"\] Alt text: Mining summary

**Parent Topic:**[Create a project or template using Project Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/define-workflow-model.md)

