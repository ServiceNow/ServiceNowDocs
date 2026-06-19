---
title: Migrate a selection of Core UI reports
description: Migrate a selection of your Core UI reports to Platform Analytics experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/data-migration-perform-partial-core-ui-reports.html
release: zurich
topic_type: task
last_updated: "2026-02-20"
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

**Note:** You cannot use update sets to move the migrated material from a non-production instance to a production instance. Test the migration on the non-production instance and then use Migration Center functionality to migrate the production instance.There is no automatic redirection from Core UI reports to the migrated data visualization because dashboards that use the Core UI report still require access to it for editing purposes.

If you change a Core UI report and migrate it again from `sys_report.list`, these changes overwrite any changes made to the associated Platform Analytics experience data visualization.

## Procedure

1.  Navigate to `sys_report.list`.

2.  On the Reports list, select the reports you want to migrate.

3.  From the **Action on selected rows** menu, choose **Migrate Report**.

    If any of the reports are not compatible, you’ll see the message `Migrating X of Y reports`.\[Omitted image "data-migration-mig-selected-reports.png"\] Alt text: Report list with two reports highlighted as well as the Migrate Report link on the Actions on selected rows menu

4.  When the migration is complete, select the banner link to view the migrated reports in the Platform Analytics Data Visualization library.


## What to do next

Verify that the migrated visualizations have all the features of the Core UI reports. For more information, see [Content not migrated or migrated in compatibility mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/data-mig-unmigrated-content.md).

