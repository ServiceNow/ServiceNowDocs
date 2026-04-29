---
title: Retire a de-duplication template
description: Retire a template that is no longer needed for processing its de-duplication tasks which remediate duplicate CIs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CI de-duplication experience in a workspace, Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Retire a de-duplication template

Retire a template that is no longer needed for processing its de-duplication tasks which remediate duplicate CIs.

## Before you begin

The template that you want to retire must be in an [unpublished state](workspc-dedup-unpublish-template.md).

Role required:

-   To access the [Management view in CMDB Workspace](../concept/cmdb-workspace-mangmnt-view.md) to perform de-duplication tasks, sn\_cmdb\_admin
-   To access the [Governance view in Service Graph Workspace](../concept/sg-workspace-governance-view.md) to perform de-duplication tasks: sn\_cmdb\_editor or sn\_cmdb\_admin
-   To perform this task, cmdb\_dedup\_admin or any role containing cmdb\_dedup\_admin \(such as sn\_cmdb\_admin\)

## Procedure

1.  Navigate to either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Management** in the CMDB Workspace menu bar.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and then select the Governance icon in the navigation panel.
2.  Select the **De-duplication Template Library** link in Management tools, in the Manage section.

3.  In the library pane, select the template that you want to retireand then select **Retire**.

4.  Select the template's context menu and then select **Retire template**.

5.  In the Retire template dialog box, select **Retire**.


## Result

A retired template is no longer available in the De-duplication dashboard and can't be used for remediation.

**Parent Topic:**[CI de-duplication experience in CMDB Workspace and in Service Graph Workspace](../concept/dedup-ci-exp-cmdb-workspace.md)

