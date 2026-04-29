---
title: Perform a partial dashboard migration from the library
description: Migrate a selection of your existing dashboards, reports, interactive filters, and Performance Analytics widgets to Platform Analytics experience. Migration works the same whether you choose to migrate some or all of your content. However, you can move some of your content to evaluate the process or when you have a large number of dashboards and want to migrate in segments.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [How to migrate a few dashboards]
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Perform a partial dashboard migration from the library

Migrate a selection of your existing dashboards, reports, interactive filters, and Performance Analytics widgets to Platform Analytics experience. Migration works the same whether you choose to migrate some or all of your content. However, you can move some of your content to evaluate the process or when you have a large number of dashboards and want to migrate in segments.

## Before you begin

Role required: You can migrate any dashboard you own. Users with admin or dashboard\_admin roles can migrate any dashboard from the library.

## About this task

Run and test the migration first on a single, non-production instance. After you’re satisfied with the results, launch the migration on the production instance.

This task is only applicable on instances that are upgraded to releases Xanadu or later. Net new instances from Xanadu onward do not have the **Ready to migrate** column or the **Switch to Next UI** button.

**Note:**

If content on a dashboard is used in only one dashboard, it will be available only on that dashboard after migration. If it is used in more than one dashboard, that content is migrated to the Platform Analytics experience library.

The migrated dashboard appears in the Platform Analytics library. The original Core UI dashboard is listed as Inactive in the library.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Library**.

2.  On the Dashboards list, select the dashboards you want to migrate.

    Choose from dashboards that have Yes in the **Ready to migrate** column.

3.  Select **Switch to Next UI**.

    ![Dashboard library with two Core UI dashboards that are ready to migrate selected and the Switch to Next UI button highlighted](../image/data-mig-selected-from-library.png)

    A message confirming the number of dashboards you want to migrate appears. Select **Switch to Next UI** again to open the Migration Center.

4.  In the Migration Center, you can compare the two versions of the selected dashboards, view the logs, and choose which to migrate to Next Experience.

    For more information, see [Evaluate full data migration](data-migration-evaluate.md).

5.  Select **See All Content** to replace the list of selected dashboards with the list of all dashboards on the instance.

6.  Select the dashboard's name in the Migration Center to edit it before you activate.

7.  When you are satisfied, choose which dashboards to migrate and select **Activate selected**.![Migration center with two dashboards selected and the Activate selected button enabled.](../image/data-mig-activate-selected.png)


## Result

In the library, migrated dashboards are listed next to their Core UI counterparts. The Core UI versions are labeled **Active**=False. The Next Experience versions have **Ready to migrate**=Not Applicable.

## What to do next

Verify that the migrated dashboards have all the features of the Core UI dashboards, either as fully migrated content or as iframed content. For more information, see [Content not migrated or migrated in compatibility mode](../reference/data-mig-unmigrated-content.md).

