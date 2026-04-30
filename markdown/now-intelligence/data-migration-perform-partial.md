---
title: Perform a partial migration of dashboards
description: Migrate a selection of your existing dashboards, reports, interactive filters, and Performance Analytics widgets to Platform Analytics. Migration works the same whether you choose to migrate some or all of your content. However, you can move some of your content to evaluate the process or when you have a large number of dashboards and want to migrate in segments.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [How to migrate a few dashboards]
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Perform a partial migration of dashboards

Migrate a selection of your existing dashboards, reports, interactive filters, and Performance Analytics widgets to Platform Analytics. Migration works the same whether you choose to migrate some or all of your content. However, you can move some of your content to evaluate the process or when you have a large number of dashboards and want to migrate in segments.

## Before you begin

Role required: You can migrate any dashboard you own. Users with admin or dashboard\_admin roles can migrate any dashboard.

## About this task

Run and test the migration first on a single, non-production instance. After you’re satisfied with the results, launch the migration on the production instance.

**Note:**

If content on a dashboard is used in only one dashboard, it will be available only on that dashboard after migration. If it is used in more than one dashboard, that content is migrated to the Platform Analytics experience library.

If you change a Core UI dashboard after migration and migrate it again, the changed dashboard overwrites the originally migrated dashboard.

You cannot move the migrated artifacts from a non-production instance to a production instance.

If you delete a migrated dashboard, that dashboard isn’t migrated if full migration is performed on your instance. You can migrate it again using the steps in this topic. If you want to remigrate a Core UI dashboard, be sure to delete the existing migrated dashboard to avoid duplicating dashboard content.

The migrated dashboard appears in the Platform Analytics library. Links to the original Core UI dashboard redirect to the library as well.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Migration Center**.

    If you’re already familiar with the migration process, navigate to `pa_dashboards.list` and follow the instructions from step 4.

2.  Review the information about the migration process under Learn about Platform Analytics.

3.  Select **Try your content** to choose a subset of your data to Platform Analytics.

4.  On the Dashboards list, select the dashboards you want to migrate.

5.  From the **Action on selected rows** menu, choose **Migrate Dashboard**.

    ![Dashboard list with three dashboards highlighted as well as the Migrate Dashboard link on the Actions on selected rows menu](../image/data-migration-mig-selected.png)

6.  When the migration is complete, select the banner link to view the migrated dashboards on the dashboard overview.

    The first link takes you to the PAR Dashboards list. You can review the dashboards' forms there. The second takes you to the Dashboard Overview where you can view the migrated dashboards in the Analytics Center. ![Data migration complete banner with link to dashboard overview](../image/data-migration-db-overview-link.png)


## What to do next

Verify that the migrated dashboards have all the features of the Core UI dashboards, either as fully migrated content or as iframed content. For more information, see [Content not migrated or migrated in compatibility mode](../reference/data-mig-unmigrated-content.md).

