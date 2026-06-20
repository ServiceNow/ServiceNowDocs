---
title: Retire a de-duplication template
description: Retire a template that is no longer needed for remediating de-duplication tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/configuration-management-database-cmdb/workspc-dedup-retire-template.html
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CI de-duplication experience in CMDB Workspace, Duplicate CIs remediation, CMDB data management, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Retire a de-duplication template

Retire a template that is no longer needed for remediating de-duplication tasks.

## Before you begin

The template that you want to retire must be in an [unpublished state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/workspc-dedup-unpublish-template.md).

Role required:

-   To access the [Management view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace-mangmnt-view.md) to perform de-duplication tasks, sn\_cmdb\_admin
-   To perform this task, cmdb\_dedup\_admin or any role containing cmdb\_dedup\_admin \(such as sn\_cmdb\_admin\)

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Management** in the CMDB Workspace menu bar.

2.  Select the **De-duplication Template Library** link in Management tools, in the Manage section.

3.  In the library pane, select the template that you want to retireand then select **Retire**.

4.  Select the template's context menu and then select **Retire template**.

5.  In the Retire template dialog box, select **Retire**.


## Result

A retired template is no longer available in the De-duplication dashboard and can't be used for remediation.

**Parent Topic:**[CI de-duplication experience in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/dedup-ci-exp-cmdb-workspace.md)

**Parent Topic:**[CI de-duplication experience in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/dedup-ci-exp-cmdb-workspace.md)

