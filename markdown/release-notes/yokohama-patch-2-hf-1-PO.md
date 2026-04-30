---
title: Yokohama Patch 2 Hotfix 1
description: The Yokohama Patch 2 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-14"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 2 Hotfix 1

The Yokohama Patch 2 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 04-08-2025\_1902

    Build tag: glide-yokohama-12-18-2024\_\_patch2-hotfix1-04-05-2025


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

UI Form Administration

 PRB1859837

</td><td>

UX View Rule Configuration is not applied in the Workspace when a record is opened from a **Reference** field

</td><td>

UX View Rule Configurations are not applied when a record is opened in a Workspace from a **Reference** field on a form, but when opening the same record from a **Related list** in a Workspace, the UX View Rule Configuration is applied.

</td><td>

1.  Open a cmdb\_ci\_computer table.
2.  Create a Custom View.
3.  Create a Workspace View Rule on the sysrule\_view\_workspace table with the values:
    -   Table: cmdb\_ci\_computer
    -   View: Use the Custom View created
    -   Experience Restricted: Uncheck
    -   Workspace: Empty
    -   Execution Order: 1
4.  Create a UX View Rule Configuration on the sys\_ux\_view\_rules\_configuration table with the value 'Active: True'.
5.  Navigate to **Workspace View Rules** &gt; **Related list**.
6.  Add the Workspace View Rule created.
7.  Open the Service Operations Workspace.
8.  Create a new incident where the **Configuration Item** field references a **cmdb\_ci\_computer** record.
9.  Save the new incident.
10. Navigate to **Incident** &gt; **Details** &gt; **Open Record** in the **Configuration Item** field.
11. Select **Open Record** on the modal that appears.

 Observe that the Custom View created in is not applied.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

