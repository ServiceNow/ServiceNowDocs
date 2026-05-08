---
title: Block migration of specific artifacts
description: Before you perform full migration, you can flag artifacts to be excluded from the migration process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Block migration of specific artifacts

Before you perform full migration, you can flag artifacts to be excluded from the migration process.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to one of the following tables to select artifacts.

    |Table|Content|
    |-----|-------|
    |sys\_report.list|Core UI data visualizations \(reports\)|
    |pa\_widgets.list|Performance analytics widgets|
    |sys\_ui\_hp\_publisher.list|Interactive filters|
    |pa\_dashboards.list|Responsive dashboards|

2.  Select the **Personalize List** icon ![Edit columns icon](../../dashboards/image/icon-cogwheel-ac.png) to add columns to the list.

3.  Move **Do not migrate in bulk** to the **Selected** column.

4.  In the column **Do not migrate in bulk**, change the flag from false to true for the artifacts you want to exclude.

    You can select multiple consecutive or non-consecutive fields. For more information, see Edit multiple records in a list using the list editor.

5.  If you can’t change the flag, edit the list control for the column.

    1.  Hover over the **Do not migrate in bulk** column title and expand the **Column options** \(![Column options](../image/column-options.png)\).

    2.  Select **Configure** &gt; **List Control**.

    3.  Change the List edit type field from `Disable list editing` to `Save data by rows`.

    4.  Select **Update**.

    You can now change the flag in the **Do not migrate in bulk** column.


## Result

When you perform a full data migration, the selected artifacts are excluded. You won't see the excluded content in the associated lists when you trigger the full migration.

## What to do next

Navigate to **All** &gt; **Performance Analytics** &gt; **Migration Center** to proceed with migrating the other artifacts on your instance. For more information, see [Perform full data migration](data-migration-perform.md).

