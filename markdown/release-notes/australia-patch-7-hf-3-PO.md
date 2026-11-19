---
title: Australia Patch 7 Hotfix 3
description: The Australia Patch 7 Hotfix 3 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/australia-patch-7-hf-3-PO.html
release: australia
topic_type: reference
last_updated: "2026-11-13"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 7 Hotfix 3

The Australia Patch 7 Hotfix 3 release contains fixes to these problems.

-   **Build information:**

    Build date: 11-10-2026\_1059

    Build tag: glide-australia-02-11-2026\_\_patch7-hotfix3-11-06-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/upgrade.md).

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

List Controller

 PRB1975958

</td><td>

Non-admins are unable to access the 'LIST' page in the CSM/ FSM workspace when the user does not have access to the first category displayed on the list

</td><td>

When opening the CSM workspace and the list page, no lists open. The page shows the following error: 'Exception encountered processing path: /GlideListLayout\_Query/getListLayout - You do not have access to this table.' This occurs only when the user does not have read access to the first list on the page.

</td><td>

1.  Log in to an instance.
2.  Create a new table in the sys\_db\_object table. For example, snc\_list\_issue and make sure to create an access control so only users with a certain role, such as snc\_list\_issue\_user\_role, has read access to this table.
3.  As an admin user, create a sys\_ux\_list\_category record for CSM workspace with the order -999999.
4.  Create a sys\_ux\_list record for CSM workspace for the table created in Step 2 with the category from Step 3.
5.  Create a new user with the snc\_internal role and the sn\_customerservice\_agent role. Do not assign the new role snc\_list\_issue\_user\_role you created.
6.  Create a sys\_ux\_applicability record with just the snc\_internal role.
7.  Create a corresponding sys\_ux\_applicability\_m2m\_list record.
8.  Assign it to the list created in Step 4.

 Expected behavior: The page shows all lists and categories the user has access to. When opening on the specific list the user do not have access, it should display an error.

 Actual behavior: The lists or categories that user has access to does not show up at all, and the page displays error.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 7 Hotfix 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-7-hf-2-PO.md)
-   [Australia Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-6.md)
-   [Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-5.md)
-   [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-4.md)
-   [Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-3.md)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-security-notables.md)
-   [All other Australia fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/available-versions.md)

