---
title: Zurich Patch 5 Hotfix 1
description: The Zurich Patch 5 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-02-10"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 5 Hotfix 1

The Zurich Patch 5 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 02-05-2026\_1831

    Build tag: glide-zurich-07-01-2025\_\_patch5-hotfix1-02-03-2026


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

Analytics Data API

 PRB1931476

</td><td>

Issue with Incident SLA donut translation in Service Operations Workspace \(SOW\)

</td><td>

After changing the language in SOW, the Incident SLA widget appears as 'Breached'. After clearing the cache, it then appears as 'undefined'.

</td><td>

1.  Impersonate a user.
2.  Open SOW.

Notice that the Incident SLA widget label appears as 'Breached'.

3.  Change the language to any language.

Notice that the label still appears as 'Breached'.

4.  Clear the cache by cache.do.

 Notice that the label now appears as 'undefined' while the translation is already added in the sys\_ui\_message table.

</td></tr><tr><td>

Analytics Export API

 PRB1977069

</td><td>

Users are unable to schedule data visualizations

</td><td>

This issue occurs when the user is attempting to schedule and sent data visualizations as a PPT or PDF file. The mail is not generated after entering the reoccurrence, recipients and subject and selecting **Save and Send Now**. An error is observed in the syslog.

</td><td>

1.  Open any visualization.
2.  Select **Schedule**.
3.  Select the file type as PPT or PDF.
4.  Fill the Reoccurrence, Recipients and Subject.
5.  Select **Save and Send Now**.

 Observe that the mail is not generated, and that there is an error displayed in the syslog.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1984668

</td><td>

Column filter issue in the Data Visualization library page, in which the 'Does Not contain' is not working on the 'Owner' column

</td><td>

Applying the 'Does not contain' filter on the 'Owned by' column does not filter the records properly.

</td><td>

1.  Navigate to the Data visualization library page.
2.  Apply the 'Does not contain' filter on the 'Owned by' column.

 Expected behavior: All the records should be filtered by the applied filter value.

 Actual behavior: It is not filtered properly when there are multiple values.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 4](zurich-patch-4.md)
-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

