---
title: Brazil Patch 1 Hotfix 1
description: The Brazil Patch 1 Hotfix 1 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/brazil-patch-1-hf-1.html
release: australia
topic_type: reference
last_updated: "2026-10-15"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Brazil release, Brazil release notes]
---

# Brazil Patch 1 Hotfix 1

The Brazil Patch 1 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 10-12-2026\_0745

    Build tag: glide-brazil-08-25-2026\_\_patch1-hotfix1-10-10-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This version is being evaluated for use in the ServiceNow Government Community Cloud \(GCC\) environment.

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

Playbooks \(Family Channel\)

 PRB2096921

</td><td>

The Playbook fails to load 'Error fetching playbook' for playbooks with 'After specific stages' once a Playbook Experience record generator has previewed them, and a NullPointerExeception \(NPE\) occurs in isOnIdealPath

</td><td>

The NullPointerException shows 'Cannot invoke ''Activity.isLaneStartActivity\(\)'' because 'activity' is null.' The PlaybookContextQuery catches it as 'Error fetching playbook', and the whole playbook response is empty, including the intake. This issue is found in Brazil instances, but works as expected in Australia because isOnIdealPath is not in that build.

</td><td>

1.  Open a thunder devsnc instance.
2.  Select **Opportunities**.
3.  Navigate to **Grant Program 1** &gt; **Apply now**.
4.  Complete the 'Answer eligibility question' activity with the answer 'Yes' to all the questions.
5.  Navigate to **Next** &gt; **Start Proposal**.

Notice that in portal, after selecting **Start Proposal**, the case \(GPR…\) is created but the playbook area stays blank. The message 'There are no playbooks available' occurs in the workspace.


 Expected behavior: The playbook renders with all stages and activities, as it does on Australia.

 Actual behavior: There is a blank playbook panel in portal. The message 'There are no playbooks available. Please contact your system administrator' occurs in the workspace. An NPE occurs in the syslog: 'GraphQL API - GlideGraphQL: Exception encountered processing path: /GlidePlaybookContext\_Query/getPlaybookContextsByParentRecord - Error fetching playbook \(no cause logged\).'

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Brazil Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/brazil-patch-1.md)
-   [Brazil security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/brazil-security-notables.md)
-   [All other Brazil fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/brazil-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/available-versions.md)

