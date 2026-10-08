---
title: Migrate dashboards that you own
description: Migrate dashboards that you own, including reports, interactive filters, and Performance Analytics widgets to Platform Analytics experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/data-migration-migrate-dbs-you-own.html
release: zurich
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 2
keywords: [How to migrate your own dashboards]
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Migrate dashboards that you own

Migrate dashboards that you own, including reports, interactive filters, and Performance Analytics widgets to Platform Analytics experience.

## Before you begin

Role required: Non-admin users can migrate any dashboard they own from the dashboard itself. Users with the dashboard\_admin or higher roles can migrate any dashboard from the Dashboard Library.

## About this task

To learn about migration and its benefits, see [Platform Analytics Migration Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/data-migration.md).

**Note:** You cannot use update sets to move the migrated material from a non-production instance to a production instance. Test the migration on the non-production instance and then use Migration Center functionality to migrate the production instance. If content on a dashboard is used in only one dashboard, it will be available only on that dashboard after migration. If it is used in more than one dashboard, that content is migrated to the Platform Analytics experience library.

This task is only applicable on instances that are upgraded to releases Xanadu or later. Net new instances from Xanadu onward don't have the **Core UI** column or the **Switch to Next Experience UI** button.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards**.\[Omitted image "data-migration-mig-indiv-db1.png"\] Alt text: Personal dashboard showing the individual migration banner.

2.  Open the dashboard that you want to migrate.

    Choose from dashboards that you own that have Core UI in the **UI version** column.

    **Note:** Dashboards with custom or dynamic content blocks and any widgets that aren't base-system Performance Analytics widgets will not show the migration banner. Examples of these widgets include CMDB widgets.

    \[Omitted image "data-migration-mig-indiv-db2.png"\] Alt text: Personal dashboard showing the individual migration banner.

3.  Select **Switch to Platform Analytics experience**.

    This converts the dashboard from Core UI to the new experience, marks the old version Inactive, and opens the converted dashboard.


## Result

The migrated dashboard appears in the Platform Analytics library. Links to the original Core UI dashboard redirect to the library as well.

## What to do next

Verify that the migrated dashboard has all the features of the Core UI dashboard, either as fully migrated content or as iframed content. For more information, see [Unmigrated content and compatibility mode migrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/data-mig-unmigrated-content.md).

To roll back a migrated dashboard, select the More actions menu \(\[Omitted image "more-actions-menu-icon.png"\] Alt text: More actions menu icon\) and choose **Switch to the Core UI**.

\[Omitted image "data-migration-roll-back-indiv-db.png"\] Alt text: More actions menu with Switch to the Core UI option highlighted

