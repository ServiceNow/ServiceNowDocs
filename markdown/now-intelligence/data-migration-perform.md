---
title: Perform full data migration
description: Migrate your existing dashboards, reports, interactive filters, and Performance Analytics widgets to the Platform Analytics experience.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-09-23"
reading_time_minutes: 1
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Perform full data migration

Migrate your existing dashboards, reports, interactive filters, and Performance Analytics widgets to the Platform Analytics experience.

## Before you begin

Role required: To perform the full migration and activate Platform Analytics experience: admin. Users with other admin roles \(pa\_admin, report\_admin, and dashboard\_admin\) have access to the Migration Center to evaluate the migration.

The Migration Center is only available when Next Experience is enabled. To enable Next Experience, set the value of the **glide.ui.polaris.experience** property to true.

## About this task

This topic assumes that your instance is not a net new Xanadu instance. The Migration Center is only available on upgrading instances.

Run and test the migration on a single, non-production instance. After you’re satisfied with the results of a full test migration, launch the migration on the production instance. Select **Try your content** to test the output on a limited number of dashboards.

**Note:**

If you change a Core UI dashboard after migration and migrate it again, the changed dashboard overwrites the originally migrated dashboard.

You cannot move the migrated material from a non-production instance to a production instance.

Dashboards with visualizations or other widgets migrated in compatibility mode may experience performance issues.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Migration Center**.

2.  Review the information about the migration process under Learn about Platform Analytics Experience.

    The tabs provide more information about the migration process and what you can expect from Platform Analytics.

3.  Select **Start moving** to migrate all of your content.

    The length of the migration process depends on the number of dashboards, reports, filters, and Performance Analytics widgets you have on your instance.

4.  [Evaluate the results](data-migration-evaluate.md).

5.  Select **Activate** to complete the migration process.

    The newly migrated content is not available in the Platform Analytics experience until you select **Activate**. Any menu item previously connected to Core UI dashboards and reports automatically redirects to the new migrated version.


## Result

Your dashboards and other migrated content are now found under the library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library**.

![Platform Analytics menu path](../image/data-mig-plat-admin-lib-menu-path.png)

## What to do next

[Evaluate full data migration](data-migration-evaluate.md)

