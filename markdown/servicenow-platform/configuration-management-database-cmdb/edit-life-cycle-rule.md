---
title: Edit and activate a life-cycle rule \(in Core UI\)
description: Create, edit, or activate a retirement definition that reflects the retirement state in your organization, for a class. Tables that are targeted in CMDB Data Manager life-cycle policies, must be associated with an active retirement definition. Target CIs in Retire policies, are set to match their associated class retirement definitions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/configuration-management-database-cmdb/edit-life-cycle-rule.html
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [CMDB Data Manager \(Core UI\), CMDB data management, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Edit and activate a life-cycle rule \(in Core UI\)

Create, edit, or activate a retirement definition that reflects the retirement state in your organization, for a class. Tables that are targeted in CMDB Data Manager life-cycle policies, must be associated with an active retirement definition. Target CIs in Retire policies, are set to match their associated class retirement definitions.

## Before you begin

Role required:

-   data\_manager\_user has read access
-   cmdb\_admin and data\_manager\_admin have full access

## About this task

Retirement definitions in the base system are inactive and you must activate any retirement definition that you want to use with a CMDB Data Manager life-cycle policy. To activate a retirement definition, set its **Active** attribute to **true**.

Each CMDB class can be associated with only a single retirement definition. Retirement definitions are stored in the CMDB Retirement Custom Definitions \[cmdb\_retirement\_custom\_definitions\] table.

You can alternatively manage retirement definitions in CMDB Data Manager in CMDB Workspace. For more information, see [Administer Data Manager in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/administer-data-manager.md) and [Manage retirement definitions for CMDB Data Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/data-manager-manage-ret-def-wrkspc.md). Regardless of where you manage retirement definitions, those same definitions are used in both the Data Manager legacy built on Core UI and Data Manager in CMDB Workspace.

Always be aware of the automatic derivation of retirement definitions throughout the class hierarchy. For example, an active retirement definition for the Configuration Item \[cmdb\_ci\] class can potentially be in effect throughout the entire CMDB hierarchy \(aside from classes with their own retirement definition\).

**Note:** The retirement definition for the cmdb\_ci class, can't be deactivated or deleted.

## Procedure

1.  Navigate to **Configuration** &gt; **CMDB Retirement Definitions**.

2.  In the list view, select the retirement definition/table that you want to edit and then edit or fill out the CMDB Retirement Custom Definition form.

<table id="table_dpn_g2t_pvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Activates the retirement definition.

</td></tr><tr><td>

Table

</td><td>

The CMDB class that the retirement definition applies to. The retirement definition will be derived by all child classes of the specified parent class.

</td></tr><tr><td>

Retirement definition

</td><td>

One or more attribute conditions that together define the retirement state for the class.

 Target CIs in Retire policies that belong to the specified table, are set as specified in the retirement definition. Therefore, you can only use **AND** clauses in this definition while **OR** clauses aren't applicable.

</td></tr></tbody>
</table>3.  Select **Update**.


## Result

After the deletion, a retirement definition for the class is derived from a parent class.

## What to do next

To delete a retirement definition \(in Core UI\), the retirement definition must be in an inactive mode \(**Active** = **false**\):

1.  Navigate to **Configuration** &gt; **CMDB Retirement Definitions**, and then select the retirement definition that you want to delete.
2.  On the CMDB Retirement Custom Definition form, select **Delete**.
3.  In the Delete retirement definition form, select **Delete**.

