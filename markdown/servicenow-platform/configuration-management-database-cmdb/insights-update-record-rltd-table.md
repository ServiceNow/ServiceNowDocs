---
title: Edit a related table from CMDB performance insights
description: Edit a related table on the Related Entries \[cmdb\_related\_entry\] table directly from the CMDB performance insights tool in the CMDB Workspace Insights view. Update the related table to correctly reference another CI in the Referenced field when a reference is missing from the related table.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Edit a related table from CMDB performance insights

Edit a related table on the Related Entries \[cmdb\_related\_entry\] table directly from the CMDB performance insights tool in the CMDB Workspace Insights view. Update the related table to correctly reference another CI in the Referenced field when a reference is missing from the related table.

## Before you begin

Role required: sn\_cmdb\_admin \(CMDB Admin\) and any role needed to access a related table.

## About this task

A record is missing a reference when the **Referenced** field for that record is empty. CMDB performance insights enables you to easily edit related tables that are missing a reference after you drill down on a slice of the Related records missing reference chart.

You can see the full list of related tables and associated referenced fields in the Related Entries \[cmdb\_related\_entry\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**, and then in the CMDB Workspace menu bar, select **Insights**.

2.  On the CMDB performance insights tile, select **View performance insights**.

3.  Navigate to the Related records tile of the **Payloads &amp; CIs** tab and then select a slice of the chart in the Related records missing reference by table card.

4.  Select a check box next to a record and then select **Edit**.

5.  Specify applicable CMDB CI references and then select **Update**.


**Parent Topic:**[CMDB Workspace store app](../concept/cmdb-workspace.md)

**Related topics**  


[Overview of CMDB](../concept/cnfig-mgmt-and-cmdb.md)

[Insights view in CMDB Workspace](../concept/cmdb-workspace-insights-view.md)

