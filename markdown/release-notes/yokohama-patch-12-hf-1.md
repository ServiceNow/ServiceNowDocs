---
title: Yokohama Patch 12 Hotfix 1
description: The Yokohama Patch 12 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-02-12"
reading_time_minutes: 3
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 12 Hotfix 1

The Yokohama Patch 12 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 02-09-2026\_2259

    Build tag: glide-yokohama-12-18-2024\_\_patch12-hotfix1-02-06-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

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

Database Persistence - Data Management

 PRB1939498

</td><td>

Migration to RaptorDB brings column length changes, which could impede archive table synchronization

</td><td>

The synchronization should run quickly, but this scenario can occur and slow down the process.

</td><td>

1.  Provision an instance on MariaDB.
2.  Create some archive rules.
3.  Archive some data.
4.  Migrate the instance to RaptorDB.
5.  Install a plugin that will cause many table schema updates that propagate to archive tables, such as 'Discovery and Service Mapping Patterns.'

Observe what happens during archive table synchronization.


 Expected behavior: The synchronization shouldn't be vulnerable to caches that take a long time to build.

 Actual behavior: The synchronization could become vulnerable to caches that take a long time to build.

</td></tr><tr><td>

Application Manager

 PRB1986694

</td><td>

App Manager and 'My Company Applications' incorrectly shows available updates after update checker

</td><td>

When publishing a new version of the app, it doesn't appear in 'My Company Application'.

</td><td>

1.  Log in as an admin user on an instance \(TD1\).
2.  Navigate to **My Company Application**.

Notice that as soon as the user lands on this page, it will automatically start the sync.

3.  Wait for the sync to complete.
4.  Search for the application to install, such as 'Test MyCompany App1'.

Notice that 'Test MyCompany App1' shows up with available versions.

5.  From another instance \(TD2\) publish a new version of 'Test MyCompany App1'.
6.  As an admin user on instance TD1, navigate to **My Company Application**.
7.  Wait for the sync to complete.
8.  Search for the application 'Test MyCompany App1'.

Notice that the new version of the application is not showing under 'My Company Application'.


 Expected behavior: The new version of the app is visible.

 Actual behavior: The new version of the app is not showing up.

</td></tr><tr><td>

Word Document APIs

 PRB1987850

</td><td>

Issue with document sync when paragraph properties do not exist

</td><td>

An error occurs when attempting to sync the document. This issue occurs when the document was generated using ChatGPT or other AI tools, or when content controls are positioned on blank text.

</td><td>

1.  Make changes to the content control fields with 'Track Changes' on.

Observe that the selected paragraph should not have any styling.

2.  Attempt to replace the value.

 Notice that it will throw an error.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 12](yokohama-patch-12.md)
-   [Yokohama Patch 11](yokohama-patch-11.md)
-   [Yokohama Patch 10](yokohama-patch-10.md)
-   [Yokohama Patch 9](yokohama-patch-9.md)
-   [Yokohama Patch 8](yokohama-patch-8.md)
-   [Yokohama Patch 7](yokohama-patch-7.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

