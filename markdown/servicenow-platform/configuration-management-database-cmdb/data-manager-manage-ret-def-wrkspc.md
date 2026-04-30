---
title: Manage retirement definitions for CMDB Data Manager
description: Use CMDB Workspace or Service Graph Workspace to create, delete, edit, or activate retirement definitions in your organization, for a class. Tables that are targeted in CMDB Data Manager life-cycle policies, must be associated with an active retirement definition. Target CIs in Retire policies, are set to match their associated class retirement definitions.Delete a retirement definition that is no longer needed by CMDB Data Manager, in CMDB Workspace or in Service Graph Workspace.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Administer CMDB Data Manager, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage retirement definitions for CMDB Data Manager

Use CMDB Workspaceor Service Graph Workspace to create,delete, edit, or activate retirement definitions in your organization, for a class. Tables that are targeted in CMDB Data Manager life-cycle policies, must be associated with an active retirement definition. Target CIs in Retire policies, are set to match their associated class retirement definitions.

## Before you begin

Role required: sn\_cmdb\_admin

## About this task

Some retirement definitions in the base system are inactive and you must activate any retirement definition that you want to use with a CMDB Data Manager life-cycle policy by setting its **Active** attribute to **true**. Retirement definitions are stored in the CMDB Retirement Custom Definitions \[cmdb\_retirement\_custom\_definitions\] table.

When a CMDB Data manager retires a CI, ensure that any of its dependent CIs are also retired and don't remain as orphan CIs, by enabling management of dependent CIs. Orphan CIs can impact the consistency, accuracy, and integrity of the CMDB.

-   For information about enabling and managing dependent CIs, especially in the context of cascade-retire, cascade-archive, and cascade-delete, see [Dependent CIs management](../concept/manage-dependent-ci.md).
-   For details and definitions of independent and dependent CIs, see [CMDB classifications and class dependency](../concept/c_CMDBClassifications.md).

**Note:**

-   Always be aware of the automatic derivation of retirement definitions throughout the class hierarchy. For example, an active retirement definition for the Configuration Item \[cmdb\_ci\] class can potentially be in effect throughout the entire CMDB hierarchy \(aside from classes with their own retirement definition\).
-   You can't deactivate \(or delete\) the retirement definition of the Configuration Item \[cmdb\_ci\] class.
-   Each CMDB class can be associated with only a single retirement definition.

## Procedure

1.  Open either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace**, and then select the **Data Manager** quick link on the Home view.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, in the navigation panel, select the Governance icon. Then, in the Governance pane, select **Data Manager overview**.
2.  In the Get started area on the Data Manager overview page, select **Manage retirement definitions**.

3.  On the Data Manager settings page, review the Retirement definitions list view.

    1.  Drill down to a definition and then, on the Retirement definition form, toggle the **Active** switch to activate or deactivate a definition.

    2.  Edit the conditions on the definition.

    3.  Select **Save definition**.

4.  On the Data Manager settings page, select **Add definition**.

5.  Fill out the Retirement definition form and then select **Save definition**.

<table id="table_o4v_222_fzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Toggles the retirement definition between active and inactive.

</td></tr><tr><td>

Table

</td><td>

Table that the retirement definition applies to. The retirement definition will be derived by all child classes of the specified parent class.

</td></tr><tr><td>

Condition builder

</td><td>

Condition that reflects on what retirement means in the organization.Target CIs in Retire policies that belong to the specified table are set as specified in the retirement definition. You can, therefore, only use **AND** clauses in the definition. **OR** clauses aren't applicable.

</td></tr></tbody>
</table>
## Delete a CMDB Data Manager retirement definition

Delete a retirement definition that is no longer needed by CMDB Data Manager, in CMDB Workspaceor in Service Graph Workspace.

### Before you begin

The following restrictions are in effect:

-   The retirement definition that you want to delete must be in an inactive mode \(**Active** = **false**\).
-   The retirement definition for the Configuration Item \[cmdb\_ci\] class can't be deleted.

Role required: sn\_cmdb\_admin, data\_manager\_admin

### About this task

### Procedure

1.  Open either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace**, and then select the **Data Manager** quick link on the Home view.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**. Then, in the navigation panel, select the Governance icon. Then, in the Governance pane, select **Data Manager overview**.
2.  In the Get started area on the Data Manager overview page, select **Manage retirement definitions**.

3.  On the Data Manager settings page, in the Retirement definitions tile select the retirement definition that you want to delete.

4.  On the Retirement definition page, select **Delete definition**.

5.  In the Deleted retirement definition dialog box, select **Delete**.


### Result

After the deletion, a retirement definition for the class is derived from a parent class.

