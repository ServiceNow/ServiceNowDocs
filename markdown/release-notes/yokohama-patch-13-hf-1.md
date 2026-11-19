---
title: Yokohama Patch 13 Hotfix 1
description: The Yokohama Patch 13 Hotfix 1 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/release-notes/yokohama-patch-13-hf-1.html
release: yokohama
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 13 Hotfix 1

The Yokohama Patch 13 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 05-20-2026\_0905

    Build tag: glide-yokohama-12-18-2024\_\_patch13-hotfix1-05-18-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/upgrade.md).

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

 Notice that no approvers are added in the related list. Required field level ACLs are missing for these roles and there's no way to bypass the strict ACL check.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 13](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-13.md)
-   [Yokohama Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-12.md)
-   [Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)
-   [Yokohama Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-10.md)
-   [Yokohama Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-9.md)
-   [Yokohama Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-8.md)
-   [Yokohama Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-7.md)
-   [Yokohama Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-6.md)
-   [Yokohama Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-5.md)
-   [Yokohama Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-4.md)
-   [Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)
-   [Yokohama Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-2.md)
-   [Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)
-   [Yokohama security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-security-notables.md)
-   [All other Yokohama fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/available-versions.md)

