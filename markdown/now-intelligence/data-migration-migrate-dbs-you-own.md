---
title: Migrate dashboards that you own
description: Migrate dashboards that you own, including reports, interactive filters, and Performance Analytics widgets to Platform Analytics experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [How to migrate your own dashboards]
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Migrate dashboards that you own

Migrate dashboards that you own, including reports, interactive filters, and Performance Analytics widgets to Platform Analytics experience.

## Before you begin

Role required: You can migrate any dashboard you own. Users with admin or dashboard\_admin roles can migrate any dashboard.

## About this task

To learn about migration and its benefits, see [Platform Analytics Migration Center](../concept/data-migration.md).

**Note:** If content on a dashboard is used in only one dashboard, it will be available only on that dashboard after migration. If it is used in more than one dashboard, that content is migrated to the Platform Analytics experience library.

This task is only applicable on instances that are upgraded to releases Australia or later. Net new instances from Australia onward do not have the **Ready to migrate** column or the **Switch to Next UI** button.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards**.

    ![Personal dashboard showing the individual migration banner.](../image/data-migration-mig-indiv-db1.png)

2.  Select the dashboards that you want to migrate.

    Choose from dashboards that have Yes in the **Ready to migrate** column.

    **Note:** Dashboards with custom or dynamic content blocks and any widgets that are not base-system Performance Analytics widgets will not show the migration banner. Examples of these other widgets include CMDB widgets.

3.  Select **Switch to Next UI**.

    ![Dashboard library with two Core UI dashboards that are ready to migrate selected and the Switch to Next UI button highlighted](../image/data-mig-selected-from-library.png)

    A message confirming the number of dashboards you want to migrate appears. Select **Switch to Next UI** again to open the Migration Center.


## Result

The migrated dashboard appears in the Platform Analytics library. Links to the original Core UI dashboard redirect to the library as well.

## What to do next

Verify that the migrated dashboard has all the features of the Core UI dashboard, either as fully migrated content or as iframed content. For more information, see [Content not migrated or migrated in compatibility mode](../reference/data-mig-unmigrated-content.md).

To roll back a migrated dashboard, select the More actions menu ![More actions menu icon](../../../administer/integrationhub/images/more-actions-menu-icon.png) and choose **Switch to the Core UI**. This option is available to analytics managers and admins for all migrated dashboards. Other dashboard owners can only roll back migrations on dashboards they have migrated themselves.

![More actions menu with Switch to the Core UI option highlighted](../image/data-migration-roll-back-indiv-db.png)

