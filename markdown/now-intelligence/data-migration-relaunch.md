---
title: Relaunch data migration
description: Relaunch migration when Core UI content is changed after full data migration and when earlier unsupported functionality becomes supported in the Platform Analytics experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 1
breadcrumb: [Perform full data migration, Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Relaunch data migration

Relaunch migration when Core UI content is changed after full data migration and when earlier unsupported functionality becomes supported in the Platform Analytics experience.

## About this task

When there are modified artifacts, new content, or newly supported content to migrate, a banner is shown in the Migration Center with a button labeled **Migrate again**.

**Note:** When you upgrade releases, the Migration Center automatically migrates any previously incompatible content that is now compatible.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **Migration Center**.

2.  Select **Migrate again**.

    The length of the migration process depends on the number of new artifacts that you have on your instance.

    ![Window that indicates how many dashboards and reports will be migrated and estimate of how long the process takes.](../image/data-migration-confirmation.png)

3.  Select **Prevent users from creating Core UI analytics during migration**.


## Result

The changed and new content is migrated to Platform Analytics experience.

## What to do next

Evaluate the newly migrated content. For more information, see [Evaluate full data migration](data-migration-evaluate.md).

