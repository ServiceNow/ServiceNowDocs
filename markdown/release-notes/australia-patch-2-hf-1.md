---
title: Australia Patch 2 Hotfix 1
description: The Australia Patch 2 Hotfix 1 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/australia-patch-2-hf-1.html
release: australia
product: Release Notes
classification: release-notes
topic_type: reference
last_updated: "2026-06-19"
reading_time_minutes: 6
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 2 Hotfix 1

The Australia Patch 2 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 05-24-2026\_0242

    Build tag: glide-australia-02-11-2026\_\_patch2-hotfix1-05-05-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Access Analyzer

 PRB1993028

 [KB2820230](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2820230)

</td><td>

Instance scan jobs can hang and are not terminated due to checks not being optimized

</td><td>

Instance scan jobs triggered by the Access Auditor Suite, which is a part of the Access Analyzer \(sn\_access\_analyzer\) store application, may hang or fail to terminate. This may cause multiple jobs to accumulate over several days, consuming multiple workers and preventing  other jobs from running. This may cause performance issues on the instance. This issue affects Access Analyzer \(sn\_access\_analyzer\) versions 6.0.0 through 6.0.5, as well as version 6.1.0.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Authentication

 PRB1969882

 [KB2718536](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718536)

</td><td>

Login screen performance issues on iOS 26.2 RC and in Zurich instances

</td><td>

After upgrading to iOS 26.2, users are unable to log in to any instance using the Now Mobile app. The login page is extremely slow or unresponsive, and it can fail to load or accept credentials. The issue affects multiple users and device models. It's reproducible across different instances, and it also impacts the Agent app.

</td><td>

1.  On iOS, navigate to the Now Mobile App.
2.  Connect to a Zurich or later family release instance.

 Observe that the screen loads slowly and is non-responsive.

</td></tr><tr><td>

Change Management

 PRB2021436

</td><td>

Instances should not get license restriction ACLs

</td><td>

This issue was observed in Australia. Licensing controls are enforced when there are entries in subscription\_entitlement.

</td><td>

Log in to any Australia non-prod instance.

 Notice that the licensing controls are enforced when there are entries in subscription\_entitlement, even if the instance is open.

</td></tr><tr><td>

Change Management

 PRB2021441

 [KB3032668](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3032668)

</td><td>

Unable to rollback the plugin 'com.snc.itsm.foundation.license\_control'

</td><td>

 

</td><td>

1.  Log in to an Australia instance with com.snc.itsm.foundation .license\_control installed.
2.  Install any other family plugin after that.

 Notice that the plugin 'com.snc.itsm.foundation.license\_control' is no longer able to rollback.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2007256

 [KB2925734](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2925734)

</td><td>

The text search doesn't return results in non-English languages

</td><td>

After downloading language plugins and switching the system language to a non-English language, results aren't returned when the property 'glide.db\_query.replace\_distinct\_with\_groupby' is set to 'false.' When the language is set to English, results are returned.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Instance Scan

 PRB1992382

 [KB2901125](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2901125)

</td><td>

Instance scan jobs get stuck in a sleep loop for days, which causes the subsequent scans to fail

</td><td>

Instance Scan findings are written to the database asynchronously and are tracked using a global counter. If any write fails, the counter doesn't decrement properly; it goes up but never comes back down. This causes all future scans to hang indefinitely, waiting for a counter that will never reach zero. There's no timeout or logging to flag this, so scans can get stuck silently.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Live Archive

 PRB2022367

</td><td>

In AttachmentMigrationService, copy-then-delete causes silent data loss through cascade delete on sys\_attachment\_attribute, dp\_attachment\_protection\_history, and sys\_attachment\_migration\_status

</td><td>

AttachmentMigrationService migrates attachments between the storage backends 'ROWSTORE' and 'COLUMNSTORE' by creating a new sys\_attachment row with a new sys\_id, and then deleting the old one. Deleting the old sys\_attachment triggers reference\_cascade\_rule='delete' on every child table that references it, which silently destroys records that reference the old sys\_id, even though a valid replacement exists. The cascade engine has no knowledge of the new sys\_id, so the new sys\_attachment ends up with no associated child rows. The following child tables suffer silent data loss on every migrated attachment: sys\_attachment\_attribute \(per-attachment metadata\), sys\_attachment\_migration\_status \(migration tracking history\), and dp\_attachment\_protection\_history \(data-privacy / compliance audit trail\).

</td><td>

1.  Open an instance with the columnar attachments plugin, 'com.glide.data\_management .columnar\_attachments,' enabled.
2.  Create a sys\_attachment row for any storage type, such as 'ROWSTORE', and note that the sys\_id equals 'X'.
3.  Insert child rows referencing 'X' with the following:
    -   sys\_attachment\_attribute: row with the sys\_attachment = X sys\_attachment\_migration\_status: row with the attachment = X
    -   dp\_attachment\_protection\_history: row with the attachment = X
4.  Trigger the migration via AttachmentMigrationService.migrateAttachments\(\[X\], AttachmentStorageType.ROWSTORE, AttachmentStorageType.COLUMNSTORE\).
5.  Query each of the three child tables for the original sys\_id 'X' after the call returns.

 Expected behavior: All three child tables still contain rows for the migrated attachment, either against the same sys\_id, or under copy-then-delete which is re-pointed to the new sys\_id.

 Actual behavior: All three child tables contain zero rows for the original sys\_id 'X'. The new sys\_attachment record, the new sys\_id 'Y', exists with the migrated chunk data, but contains no rows in any of these three child tables. The data is silently lost and no error is logged. This occurs in any instance running on a build that includes AttachmentMigrationService for track, datamanagement, and downstream.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2025067

</td><td>

The sys\_translated record for par\_dashboard\_tab is overwritten

</td><td>

This can cause translations to be lost.

</td><td>

1.  In English, create a sys\_translated record as follows:
    -   Label: あいう
    -   Table: par\_dashboard\_tab
    -   Element: name
    -   Language: ja
    -   Value: TabName
2.  Create a PAE Dashboard.
3.  Add a tab with the same name as the sys\_translated value \(TabName\).
4.  Save the dashboard.
5.  Create another dashboard.
6.  Add a tab with the same name as the sys\_translated value again.
7.  Save the dashboard.
8.  Switch the language to Japanese.
9.  Return to one of the dashboards.
10. Rename the tab あいう to さしす.
11. Check the other dashboard tab.

 Observe that the translation is lost because the sys\_translated record is overwritten.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2022823

</td><td>

Allow users to configure the re-direction of Core UI Performance Analytics widgets to the Analytics Hub instead of to 'KPI details'

</td><td>

Users that activated Next Experience after migrating or upgrading to Australia will be redirected to 'KPI details' when selecting a Performance Analytics widget, even if they keep using Core UI dashboards. This issue occurs because the unified\_analytics property forces the re-direction to 'KPI details'.

</td><td>

 

</td></tr><tr><td>

Related Lists

 PRB2025356

</td><td>

User can't add records in a related list because of the strict ACL check and missing ACLs for required roles

</td><td>

Users with missing ACLs are not able to add new records in the related list due to a strict ACL check.

</td><td>

1.  Log in as a user with the catalog\_admin, delegated\_developer, and ITIL roles.
2.  Navigate to the 'Catalog Task' record page.
3.  Navigate to the Approvers related list.
4.  Select the **Edit** button.
5.  Add a few members as approvers.
6.  Select **Save**.

 Notice that no approver is added in the related list. Required field level ACLs are missing for these roles and there's no way to bypass the strict ACL check.

</td></tr><tr><td>

Upgrade Center

 PRB2023239

 [KB3015307](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3015307)

</td><td>

There is a mismatch in the glide version between the Appnode and the Database following the upgrade

</td><td>

A new code path introduced the MariaDBI18NSQLFormatter class. When the sys\_properties record of the 'com.glide.db.session \_language\_collation\_feature' property is set to true, it takes a code path upon upgrade or restart where an instance will not come up. When 'com.glide.db.session \_language\_collation\_feature' is false, the code path exits early and doesn't cause this issue.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB2007255

</td><td>

There's memory pressure on nodes due to high memory for the cache 'com.glide.cs.qlue.module.coma.MessageBatchingSession'

</td><td>

Users with 2GB nodes may encounter memory issues that can cause the events process jobs to yield.

</td><td>

Run a heap dump.

 Observe that MacMessageBatchingSession or MessageBatchingSession uses over 50 MB of memory.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/available-versions.md)

