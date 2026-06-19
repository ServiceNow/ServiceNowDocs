---
title: Migrate dashboards that you own
description: Migrate dashboards that you own, including reports, interactive filters, and Performance Analytics widgets to Platform Analytics experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/data-migration-migrate-dbs-you-own.html
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

To learn about migration and its benefits, see [Platform Analytics Migration Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/data-migration.md).

**Note:** You cannot use update sets to move the migrated material from a non-production instance to a production instance. Test the migration on the non-production instance and then use Migration Center functionality to migrate the production instance.

If content on a dashboard is used in only one dashboard, it will be available only on that dashboard after migration. If it is used in more than one dashboard, that content is migrated to the Platform Analytics experience library.

This task is only applicable on instances that are upgraded to releases Australia or later. Net new instances from Australia onward do not have the **Ready to migrate** column or the **Switch to Next UI** button.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards**.

    \[Omitted image "data-migration-mig-indiv-db1.png"\] Alt text: Personal dashboard showing the individual migration banner.

2.  Select the dashboards that you want to migrate.

    Choose from dashboards that have Yes in the **Ready to migrate** column.

    **Note:** Dashboards with custom or dynamic content blocks and any widgets that are not base-system Performance Analytics widgets will not show the migration banner. Examples of these other widgets include CMDB widgets.

3.  Select **Switch to Next UI**.

    \[Omitted image "data-mig-selected-from-library.png"\] Alt text: Dashboard library with two Core UI dashboards that are ready to migrate selected and the Switch to Next UI button highlighted

    A message confirming the number of dashboards you want to migrate appears. Select **Switch to Next UI** again to open the Migration Center.


## Result

The migrated dashboard appears in the Platform Analytics library. Links to the original Core UI dashboard redirect to the library as well.

## What to do next

Verify that the migrated dashboard has all the features of the Core UI dashboard, either as fully migrated content or as iframed content. For more information, see [Content not migrated or migrated in compatibility mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/data-mig-unmigrated-content.md).

To roll back a migrated dashboard, select the More actions menu \[Omitted image "more-actions-menu-icon.png"\] Alt text: More actions menu icon and choose **Switch to the Core UI**. This option is available to analytics managers and admins for all migrated dashboards. Other dashboard owners can only roll back migrations on dashboards they have migrated themselves.

\[Omitted image "data-migration-roll-back-indiv-db.png"\] Alt text: More actions menu with Switch to the Core UI option highlighted

