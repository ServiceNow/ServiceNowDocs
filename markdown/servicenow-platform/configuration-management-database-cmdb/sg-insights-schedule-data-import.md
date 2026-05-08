---
title: Edit a scheduled data import from CMDB performance insights in Service Graph Workspace
description: Edit a scheduled data import directly from CMDB performance insights for your Service Graph Connectors. Consider enabling Concurrent Import with a custom size partition to split incoming data into multiple import sets and transform the import sets concurrently to reduce processing time.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Edit a scheduled data import from CMDB performance insights in Service Graph Workspace

Edit a scheduled data import directly from CMDB performance insights for your Service Graph Connectors. Consider enabling **Concurrent Import** with a custom size partition to split incoming data into multiple import sets and transform the import sets concurrently to reduce processing time.

## Before you begin

Role required: sn\_cmdb\_admin \(CMDB Admin\) and one of these roles:

-   import\_scheduler
-   import\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Graph Workspace**, and then on the navigation panel, select the Insights icon.

2.  On the Insights page navigation pane, select **Performance insights**.

3.  On the CMDB performance insights page, on the Service Graph connectors tab, select the Sources with concurrent import turned off card or the Sources with non-custom size partition method card.

4.  In the Scheduled Import sets list view, select a check box next to a record.

5.  Select **Edit**.

6.  Configure the scheduled data import.

    You may need to change your application scope to create or edit a scheduled data import from Service Graph Workspace.

    For more information about updating a scheduled data import, see Schedule a data import.

7.  Select **Update**.


