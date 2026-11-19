---
title: Zurich Patch 9 Hotfix 1
description: The Zurich Patch 9 Hotfix 1 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-9-hf-1.html
release: zurich
topic_type: reference
last_updated: "2026-05-29"
reading_time_minutes: 6
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 9 Hotfix 1

The Zurich Patch 9 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 05-21-2026\_2126

    Build tag: glide-zurich-07-01-2025\_\_patch9-hotfix1-05-05-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/upgrade.md).

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

Authentication

 PRB1969882

</td><td>

Login screen performance issues on iOS 26.2 RC and in Zurich instances

</td><td>

After upgrading to iOS 26.2, users are unable to log in to any instance using the Now Mobile app. The login page is extremely slow or unresponsive, and it can fail to load or accept credentials. The issue affects multiple users and device models. It's reproducible across different instances, and it also impacts the Agent app.

</td><td>

1.  On iOS, navigate to the Now Mobile App.
2.  Connect to a Zurich or later family release instance.

 Observe that the screen loads slowly and is non-responsive.

</td></tr><tr><td>

Code Signing

 PRB2014768

</td><td>

Increase the code signing validity window maximum from 60 minutes to 4 hours

</td><td>

In the 'Scan Signatures' module, the **Data source** field is incorrectly set to false for records that have valid, successfully created signatures. These signatures return true when validated via a background script. The issue occurs because the effective maximum of com.snc.kmf. signature .validity\_window is 60 minutes, which prevents customers from configuring longer validity windows, especially when the consecutive signature generation takes time.

</td><td>

1.  Open an instance.
2.  Navigate to 'Update Set: Test Code Signing Updates'.
3.  Validate that the signature is created for the **Data source** field.
4.  Select **Scan Signature**.

 Observe that the signature state for the **Data source** field still reflects as false.

</td></tr><tr><td>

Code Signing

 PRB2014831

</td><td>

Scheduled scripts incorrectly appear in 'Update Set Signature States'

</td><td>

Currently, users are required to hold the security\_admin role to perform code signing operations on update sets. This creates several operational and security challenges. Instead, there should be a separate role that grants the ability to perform code signing operations on update sets and related artifacts within the Code Signing framework. It shouldn't grant access to security policies, ACLs, encryption contexts, or other security administration functions.

</td><td>

1.  Open an instance.
2.  Navigate to 'Update Set: Code Signing Scheduled Jobs'.
3.  Navigate to the tab 'Update Set Signature States'.

 Observe that there's no option to run signing jobs unless elevated to the 'security\_admin' role.

</td></tr><tr><td>

Code Signing

 PRB2014833

</td><td>

Enable digest creation for users with the code signing role

</td><td>

For users with the code\_signing\_user role, the 'Create Digest' functionality should be enabled for Flow Designer flows and actions. The current dependency on the security\_admin role should be removed.

</td><td>

1.  Open an instance.
2.  Navigate to 'Update Set: Code Signing Scheduled Jobs'.
3.  Navigate to the tab 'Update Set Signature States'.

 Observe that the user can't generate digest for flows unless they have the 'security\_admin' role.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2007256

 [KB2925734](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2925734)

</td><td>

The text search doesn't return results in non-English languages

</td><td>

After downloading language plugins and switching the system language to a non-English language, results aren't returned when the property 'glide.db\_query.replace \_distinct\_with\_groupby' is set to 'false.' When the language is set to English, results are returned.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Instance Scan

 PRB1992382

 [KB2901125](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2901125)

</td><td>

Instance scan jobs get stuck in sleep loop for days, which causes the subsequent scans to fail

</td><td>

Instance Scan findings are written to the database asynchronously and tracked using a global counter. If any write fails, the counter doesn't decrement properly; it goes up but never comes back down. This causes all future scans to hang indefinitely, waiting for a counter that will never reach zero. There's no timeout or logging to flag this, so scans can get stuck silently.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2025067

</td><td>

Sys\_translated record for par\_dashboard\_tab is overwritten

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

Related Lists

 PRB2025356

</td><td>

User can't add records in a related list because of strict ACL check and missing ACLs for required roles

</td><td>

Users with missing ACLs are not able to add new records in the related list due to a strict ACL check.

</td><td>

1.  Log in as a user with the catalog\_admin, delegated\_developer, and itil roles.
2.  Navigate to the 'Catalog Task' record page.
3.  Navigate to the Approvers related list.
4.  Select the **Edit** button.
5.  Add a few members as approvers.
6.  Select **Save**.

 Notice that no approvers are added in the related list. Required field level ACLs are missing for these roles and there's no way to bypass the strict ACL check.

</td></tr><tr><td>

System Events

 PRB1939688

</td><td>

Inputs aren't getting processed for subflows with inputs

</td><td>

Implement thread pool with the configurations/design. The scope excludes any changes related autoscaling or processing framework \(which means it co-exists with the jobs that are already there for flow\_engine\).

</td><td>

1.  Create a subflow with inputs.
2.  Trigger it.

 Expected behavior: All flows are completed without any errors.

 Actual behavior: A couple flows move to the completed state with an error log for not processing inputs.

</td></tr><tr><td>

Upgrade Center

 PRB2023239

 [KB3015307](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3015307)

</td><td>

Mismatch in Glide version between the Appnode and the Database following the upgrade

</td><td>

A new code path introduced the MariaDBI18NSQLFormatter class. When the sys\_properties record of the 'com.glide.db.session \_language\_collation\_feature' property is set to true, it takes a code path upon upgrade or restart where an instance will not come up. When 'com.glide.db.session \_language\_collation\_feature' is false, the code path exits early and doesn't cause this issue.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB2007255

</td><td>

There's memory pressure on nodes due to high memory for cache 'com.glide.cs.qlue. module.coma. MessageBatchingSession'

</td><td>

Users with 2GB nodes may encounter memory issues that can cause the events process jobs to yield.

</td><td>

Run a heap dump.

 Observe that MacMessageBatchingSession or MessageBatchingSession uses over 50 MB of memory.

</td></tr><tr><td>

Word Document APIs

 PRB1973625

</td><td>

Support unzipped font size up to 20 MB in Word Doc API

</td><td>

The property com.snc.word\_doc\_api .unzip\_word\_size\_limit\_mb supports only up to 10 MB file size. This is an enhancement request to support up to 20 MB.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)
-   [Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)
-   [Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)
-   [Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)
-   [Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)
-   [Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)
-   [Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)
-   [Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)
-   [Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)
-   [Zurich security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-security-notables.md)
-   [All other Zurich fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)

