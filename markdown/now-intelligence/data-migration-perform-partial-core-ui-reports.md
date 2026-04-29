---
title: Migrate a selection of Core UI reports
description: Migrate a selection of your Core UI reports to Platform Analytics experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [How to migrate a few Core UI reports]
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Migrate a selection of Core UI reports

Migrate a selection of your Core UI reports to Platform Analytics experience.

## Before you begin

Role required: admin, report\_admin, or dashboard\_admin.

## About this task

Users can find these migrated reports in the Platform Analytics library. The original report is labeled Active=False.

**Note:** There is no automatic redirection from Core UI reports to the migrated Data Visualizations because dashboards that use the Core UI report still require access to it for editing purposes.

If you change a Core UI report and migrate it again from `sys_report.list`, these changes overwrite any changes made to the associated Platform Analytics experience Data Visualizations.

## Procedure

1.  Navigate to `sys_report.list`.

2.  On the Reports list, select the reports you want to migrate.

3.  From the **Action on selected rows** menu, choose **Migrate Report**.

    If any of the reports are not compatible, you’ll see the message `Migrating X of Y reports`.![Report list with two reports highlighted as well as the Migrate Report link on the Actions on selected rows menu](../image/data-migration-mig-selected-reports.png)

4.  When the migration is complete, select the banner link to view the migrated reports in the Platform Analytics Data Visualization library.


## What to do next

Verify that the migrated visualizations have all the features of the Core UI reports. For more information, see [Content not migrated or migrated in compatibility mode](../reference/data-mig-unmigrated-content.md).

