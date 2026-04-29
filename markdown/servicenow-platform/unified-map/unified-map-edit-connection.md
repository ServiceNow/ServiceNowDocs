---
title: Create or modify a connection using the map editor
description: Use the map editor to add a relationship between two CIs or to modify an existing relationship.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Editing a map, Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or modify a connection using the map editor

Use the map editor to add a relationship between two CIs or to modify an existing relationship.

## Before you begin

Role required: sn\_cmdb\_admin or sn\_cmdb\_editor

## About this task

-   A solid line indicates a relationship. The arrowhead indicates the dependent node.
-   A dashed line indicates a reference.
-   A badge on a line indicates the number of relationships between the CIs.

Two CIs might be connected by one or more relationships \(stored in the CI Relationship \[cmdb\_rel\_ci\] table\). For example, two CIs might be connected by the **Runs On::Runs**, **Depends On::Discovered From**, and by the **Owned By::Owns** relationships.

You can learn more about relationships at [CI relationships in the CMDB](../concept/c_CIRelationships.md).

The map editor does not support the following actions:

-   Editing mapped application services \(service instances\).
-   Deleting reference or endpoint connections or removing from the map a CI that has reference or endpoint connections.
-   Updating the applicative flow relationship type \(connection between endpoint CIs\).

**Note:** At any time, select the reset icon ![](../image/icon-um-reset-map.png) to undo all unsaved changes.

## Procedure

1.  While editing a map, specify whether to create or modify a connection.

<table id="choicetable_cb2_gjb_l2c"><thead><tr><th align="left" id="d452144e134">

Action

</th><th align="left" id="d452144e137">

Procedure

</th></tr></thead><tbody><tr><td id="d452144e143">

**Create a connection**

</td><td>

Take one of the following actions:

-   Select and hold \(or right-click\) a CI and select **Connect to**.
-   Select a CI for the connection \(either the parent or the child\) and then select the Manage connection icon ![](../image/icon-um-edit-connection.png).


</td></tr><tr><td id="d452144e168">

**Modify an existing connection**

</td><td>

Take one of the following actions:

-   Select the connection and then select the Manage connection icon ![](../image/icon-um-edit-connection.png).
-   Select a CI for the connection \(either the parent or the child\) and then select the Attributes icon ![](../image/icon-um-attributes-panel.png). All connections for the CI are listed in boxes. ![](../image/um-editor-attrib-card-cxn.png) Select **Change**.


</td></tr><tr><td id="d452144e197">

**Delete a connection**

</td><td>

For instructions, see [Delete a connection using the map editor](unified-map-delete-connection.md).

</td></tr></tbody>
</table>2.  On the Manage connection panel \(![](../image/icon-um-edit-connection.png)\), specify the settings.

<table id="table_qwp_hq5_k2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source CI

</td><td>

You can select the swap icon ![](../image/icon-um-edit-swap.png) to swap source and target.

 **Note:** In the context of a CI relationship, this is the parent CI.

</td></tr><tr><td>

Target CI

</td><td>

You can select the swap icon ![](../image/icon-um-edit-swap.png) to swap source and target.

 **Note:** In the context of a CI relationship, this is the child CI.

</td></tr><tr><td>

Show suggested relationships

</td><td>

Option to control the contents of the **Relationship type** selection box: The relationship types that are most appropriate for the two CIs appear at the top of the list.

</td></tr><tr><td>

Relationship type

</td><td>

The relationship between the CIs. For example, the relationship between the parent ‘Tomcat’ and the child ‘WAR File’ is **Contains::Contained By**.

</td></tr></tbody>
</table>3.  When you have specified all connection settings, select **Change** to change an existing connection or **Create connection** to add a connection.


**Related topics**  


[CI relationships in the CMDB](../concept/c_CIRelationships.md)

[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)

[Add a suggested relationship](t_AddANewSuggestedRelationship.md)

[Editing maps in Unified Map](../concept/unified-map-editing-map.md)

[Delete a connection using the map editor](unified-map-delete-connection.md)

