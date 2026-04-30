---
title: Publish or unpublish a de-duplication template
description: After creating a de-duplication template, you must publish the draft template to make it available to run. You might also need to unpublish a published de-duplication template so it's temporarily unavailable for de-duplication remediation, until you republish it again.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CI de-duplication experience in a workspace, Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Publish or unpublish a de-duplication template

After creating a de-duplication template, you must publish the draft template to make it available to run. You might also need to unpublish a published de-duplication template so it's temporarily unavailable for de-duplication remediation, until you republish it again.

## Before you begin

-   A template that you want to publish must not be in a published state.
-   A template that you want to unpublish must be currently published.
-   If the template that you want to unpublish is currently running or in the running queue, you must wait for the run to complete or cancel the run. In the De-duplication dashboard, select the **Running** tab, locate the template that you want to unpublish, and then select **Cancel** in the template's card.

Role required:

-   To access the [Management view in CMDB Workspace](../concept/cmdb-workspace-mangmnt-view.md) to perform de-duplication tasks, sn\_cmdb\_admin
-   To access the [Governance view in Service Graph Workspace](../concept/sg-workspace-governance-view.md) to perform de-duplication tasks: sn\_cmdb\_editor and sn\_cmdb\_admin
-   To perform this task, cmdb\_dedup\_admin or any role containing cmdb\_dedup\_admin \(such as sn\_cmdb\_admin\)

## About this task

## Procedure

1.  Navigate to either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Management** in the CMDB Workspace menu bar.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and then select the Governance icon in the navigation panel.
2.  Select the **De-duplication Template Library** link in Management tools, in the Manage section.

3.  In the libraries pane locate the template that you want to publish or unpublish and then either:

    1.  Publish: Ensure that all the sections of the template are complete and select **Publish**.

    2.  In the Publish template dialog box, select **Publish**.

    3.  Unpublish: Select **Unpublish** and in the Unpublish template dialog box, select **Unpublish**.


## Result

A published template:

-   Becomes available on the De-duplication templates page and can be used for remediation.
-   Can't be edited or retired.

An unpublished template is set back into draft mode:

-   Is no longer available on the De-duplication templates page and can't be selected for remediation.
-   Can be edited or retired.

**Parent Topic:**[CI de-duplication experience in CMDB Workspace and in Service Graph Workspace](../concept/dedup-ci-exp-cmdb-workspace.md)

