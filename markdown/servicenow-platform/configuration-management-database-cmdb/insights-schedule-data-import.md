---
title: Edit a scheduled data import from CMDB performance insights
description: Edit a scheduled data import directly from CMDB performance insights for your Service Graph Connectors. Consider enabling Concurrent Import with a custom size partition to split incoming data into multiple import sets and transform the import sets concurrently to reduce processing time.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Edit a scheduled data import from CMDB performance insights

Edit a scheduled data import directly from CMDB performance insights for your Service Graph Connectors. Consider enabling **Concurrent Import** with a custom size partition to split incoming data into multiple import sets and transform the import sets concurrently to reduce processing time.

## Before you begin

Role required: sn\_cmdb\_admin \(CMDB Admin\) and one of these roles:

-   import\_scheduler
-   import\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace menu bar, select **Insights**.

3.  On the CMDB performance insights tile, select **View performance insights**.

4.  In the Service Graph connectors tab, click the Sources with concurrent import turned off card or the Sources with non-custom size partition method card.

5.  In the Scheduled Import sets list view, select a check box next to a record.

6.  Select **Edit**.

7.  Configure the scheduled data import.

    You may need to change your application scope to create or edit a scheduled data import from CMDB Workspace.

    For more information about updating a scheduled data import, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

8.  Select **Update**.


**Parent Topic:**[CMDB Workspace store app](../concept/cmdb-workspace.md)

**Related topics**  


[Insights view in CMDB Workspace](../concept/cmdb-workspace-insights-view.md)

