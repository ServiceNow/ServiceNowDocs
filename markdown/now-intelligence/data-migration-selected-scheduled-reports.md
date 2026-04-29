---
title: Migrate a selection of scheduled Core UI reports
description: Migrate a selection of scheduled reports to the Platform Analytics experience Scheduled export.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [How to migrate a few Core UI reports]
breadcrumb: [Migrate a selection of Core UI reports, Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Migrate a selection of scheduled Core UI reports

Migrate a selection of scheduled reports to the Platform Analytics experience Scheduled export.

## Before you begin

Role required: report\_admin or report\_scheduler

## About this task

The underlying reports in the scheduled export are migrated to the Platform Analytics library. The original scheduled report is labeled Active=False.

## Procedure

1.  Navigate to `sysauto_report.list`.

2.  On the Scheduled Email of Reports list, select the scheduled reports you want to migrate.

3.  From the **Action on selected rows** menu, choose **Migrate Scheduled Report**.

    If any of the reports are not compatible, you’ll see the message `Migrating X of Y scheduled reports`.![Scheduled report list with two reports highlighted as well as the Migrate Scheduled Report link on the Actions on selected rows menu](../image/data-migration-mig-sched-reports.png)

4.  When the migration is complete, select the banner link to view the migrated reports in the Platform Analytics Scheduled exports library.


## What to do next

Edit the migrated scheduled export as needed. For more information, see [Export a data visualization from the Visualization Designer](export-visualization-vd.md).

