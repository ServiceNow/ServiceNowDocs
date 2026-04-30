---
title: Zurich Patch 3 Hotfix 1
description: The Zurich Patch 3 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-06"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 3 Hotfix 1

The Zurich Patch 3 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 11-04-2025\_1344

    Build tag: glide-zurich-07-01-2025\_\_patch3-hotfix1-10-30-2025


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

Granular Delegation

 PRB1914000

</td><td>

Adhoc Granular Delegation intermittently doesn't work

</td><td>

This issue only happens when the delegation rule condition is added on the child table of the task field, which is added on the delegation rule.

</td><td>

1.  Activate the Granular Delegation plugin.
2.  Create the delegation rule table on the change\_request table.
3.  Choose the second step table.
4.  Set the filter to active = true.
5.  Select the **Assignments** and **Approvals** check boxes.
6.  Log in as an admin.
7.  Navigate to **All** &gt; **change\_request.list**.
8.  Create a new change request \(Normal\) with the Assignment group as 'Hardware'.
9.  Assign it to David Loo.
10. Change the state of the change request to 'Assess'.
11. Impersonate the user David Loo.
12. Navigate to **All** &gt; **Employee Center**.
13. Select **My Tasks**.
14. In the Open Tasks list, find the newly created change request.
15. Select **Delegate this task**.
16. Delegate it to Luke Wilson, with the start date as yesterday and the end date as tomorrow.

 Expected behavior: The UI shows the task as delegated to Luke Wilson with an option to edit.

 Actual behavior: The user sees a 'Success', but the UI still shows the 'Delegate this task' link.

</td></tr><tr><td>

Predictive Intelligence

 PRB1954123

 [KB2594708](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2594708)

</td><td>

Mutual TLS \(mTLS\) is enabled on Zurich instances, causing access issues for inbound integrations

</td><td>

Due to the updates related to the Predictive Intelligence plugin, mutual TLS \(mTLS\) is enabled on customer instances after a Zurich upgrade. This may result in instance access issues for inbound integrations.

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

