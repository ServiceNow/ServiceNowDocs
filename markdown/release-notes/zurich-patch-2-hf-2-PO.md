---
title: Zurich Patch 2 Hotfix 2
description: The Zurich Patch 2 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-14"
reading_time_minutes: 4
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 2 Hotfix 2

The Zurich Patch 2 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 11-11-2025\_1307

    Build tag: glide-zurich-07-01-2025\_\_patch2-hotfix2-11-10-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

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

Mobile Platform

 PRB1959673

</td><td>

Offline query results are incorrect due to reference data columns being populated as null in the offline cache payload

</td><td>

On mobile, the offline query results are incorrect due to reference data columns being populated as null in the offline cache payload. This happens when the column is defined on the child table of the table used for reference input.

</td><td>

1.  Create a column 'test\_user' in wm\_task.
2.  Create a mobile screen based on wm\_task where the data item test\_user is empty.
3.  Create a record in wm\_task where wm\_task.test\_user is set to a value \(not empty\).
4.  Create another record in wm\_task where wm\_task.test\_user is empty.
5.  Create an action with an input form screen which has a reference input based on the task table which will result in records from wm\_task to be included where test\_user is not empty.
6.  Log in to the application.
7.  Download a cache.
8.  While online, navigate to the screen that was created.
    -   Observe that there's only one record.
9.  Navigate to settings.
10. Go offline
11. Navigate to the screen that was created.
    -   Observe that it displays an additional record \(it includes the wm\_task record which had a test user populated\).
12. Inspect the cache that was generated.

 Observe that there's a record for the wm\_task record in the data section, under the task table. It has a test user populated with a null value specified for the test\_user field.

</td></tr><tr><td>

Mobile Platform

 PRB1957087

</td><td>

UI policies applicable to the screen table aren't applied when offline on mobile

</td><td>

While offline and on mobile, UI policies applicable to the screen table aren't applied when the underlying record comes from an extended table of the screen table.

</td><td>

1.  Start with an existing table, such as 'wm\_task'.
2.  Create an extension of the table, 'wm\_task\_crc'.
    -   Observe that a mobile screen is created against the wm\_task table \(a record screen with a detail tab\).
3.  Create a button which will result in an edit of the wm\_task table while offline.
    -   The writeback action will require an offline step which edits a field in the detail screen or uses the declarative update action.
4.  Ensure that you have mobile UI policies created for the wm\_task table where it hides or shows the fields based on fields in the wm\_task table, which are exposed in the detail screen.
5.  Create records in the wm\_task\_crc table.
6.  Download the cache.
7.  Go offline.
8.  Navigate to the wm\_task detail screen for a record created in the wm\_task\_crc\_table.
9.  Select the button to update the record.

 Observe that the document rebuilds. The UI policies aren't applied and don't hide or show the fields.

</td></tr><tr><td>

Mobile Platform

 PRB1959666

</td><td>

Data is lost when updating the offline cache during online operations

</td><td>

While offline and on mobile, data is lost when updating the offline cache during online operations such as viewing screens or performing actions. This happens because the first screen updates information for the dot-walked \(referenced\) fields record, but the document doesn't contain all the information for all the fields for the referenced fields record. Null is filled in the database update for any field for which there isn't information.

</td><td>

1.  Set up two screens:
    -   Screen 1: A screen that's based on the wm\_task table and has data for the current task. It should also have data for a reference field, which is also based on wm\_task. \(The referenced record on wm\_task will only display 2 fields via dot-walk.\)
    -   Screen 2: A screen that's based on the wm\_task table and displays referenced records from the record in the above screen. This screen should have a condition on fields not included in the above screen.
2.  Log in to the application.
3.  Download a cache and don't go offline.
4.  Navigate to Screen 1's detail screen.
    -   Observe that the offline cache updates for the current screen and referenced records.
5.  Navigate to settings.
6.  Go offline.
7.  Navigate to Screen 2.

 Observe that the screen is missing the referenced record from Screen 1.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 2 Hotfix 1](zurich-patch-2-hf-1-PO.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

