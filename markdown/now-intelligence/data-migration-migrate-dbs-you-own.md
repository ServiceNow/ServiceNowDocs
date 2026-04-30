---
title: Migrate dashboards that you own
description: Migrate dashboards that you own, including reports, interactive filters, and Performance Analytics widgets to Platform Analytics experience.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-05-14"
reading_time_minutes: 1
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

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards**.![Personal dashboard showing the individual migration banner.](../image/data-migration-mig-indiv-db1.png)

2.  Select the dashboard that you want to migrate.

3.  Select **Switch to Platform Analytics experience**.

    This converts the dashboard from Core UI to the new experience, marks the old version Inactive, and opens the converted dashboard.


## Result

The migrated dashboard appears in the Platform Analytics library. Links to the original Core UI dashboard redirect to the library as well.

## What to do next

Verify that the migrated dashboard has all the features of the Core UI dashboard, either as fully migrated content or as iframed content. For more information, see [Content not migrated or migrated in compatibility mode](../reference/data-mig-unmigrated-content.md).

To roll back a migrated dashboard, select the More actions menu \(![More actions menu icon](../../../administer/integrationhub/images/more-actions-menu-icon.png)\) and choose **Switch to the Core UI**.

![More actions menu with Switch to the Core UI option highlighted](../image/data-migration-roll-back-indiv-db.png)

