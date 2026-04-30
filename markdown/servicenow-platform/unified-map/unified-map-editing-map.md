---
title: Editing maps in Unified Map
description: While you work in the map editor, you can add a CI to the map and remove \(hide\) a CI from the map. Removing a CI node from a map deletes the records of the CI relationships, but does not delete the CI record from the CMDB. You can also add, modify, and delete CI relationships in the CMDB.
locale: en-US
release: zurich
product: Unified Map
classification: unified-map
topic_type: concept
last_updated: "2025-10-02"
reading_time_minutes: 6
breadcrumb: [Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Editing maps in Unified Map

While you work in the map editor, you can add a CI to the map and remove \(hide\) a CI from the map. Removing a CI node from a map deletes the records of the CI relationships, but does not delete the CI record from the CMDB. You can also add, modify, and delete CI relationships in the CMDB.

## Actions you can take in the map editor

You can perform the following actions in the map editor:

-   Select and hold \(or right-click\) a CI, relationship, or anywhere in the map to open a context menu.
-   Select the Attributes icon ![](../image/icon-um-attributes-panel.png) to manage CIs and relationships.
-   Select the Add CI icon ![](../image/icon-um-add-ci.png) to add an existing CI and its existing relationships to the map.
-   Select a relationship or CI and then select the Manage relationship icon ![](../image/icon-um-edit-connection.png) to add, update, or delete relationships.
-   You can remove \(hide\) a CI from the map only if you added it during the current editing session and have not yet saved the map. You cannot remove a CI that was on the map when you started the editing session. Select **Remove** for a CI to delete the CMDB records for all relationships to and from the CI. The CI is removed from the map, but the CI record isn’t deleted from the CMDB. For more information, see [Delete a connection using the map editor](../task/unified-map-delete-connection.md)

## Working in the map editor

-   You must have either the sn\_cmdb\_admin or sn\_cmdb\_editor role to use the map editor.
-   Before editing a map, prepare it to optimize your experience. Use filters and levels to display the minimum set of CIs to work on. Minimizing the map makes it easier to understand and control the effects of changes that you make.
-   To edit a map, select the edit map icon ![](../image/icon-um-edit-map.png). A thick blue outline on the map indicates that the map editor is active.
-   While you work in the map editor, no changes are made to the CMDB until you select **Save**.
-   During an editing session, related items and associate badges are not shown on the map.
-   At any time, select the reset icon ![](../image/icon-um-reset-map.png) to undo all unsaved changes.
-   End an editing session by selecting **Exit**. You must exit the editor to access the timeline and controls \(search, filter, zoom, and so on\).

## Adding a CI to or removing a CI from the map

-   You can view an existing CI on the map to enable you to create, modify, or delete its connections.
-   You can add only CIs that have existing records in the CMDB.
-   If you try add a CI that already has a connection to another CI on the map, the map re-centers and the CI is highlighted. In some cases, due to filter settings, the CI isn't displayed.
-   An added CI appears on the map but its CMDB record isn't changed unless you change its connections and save the changes. After you add a CI, it can be saved to the map only if it has a path \(direct or indirect\) to the home node.
-   You can remove \(hide\) a CI from the map only if you added it during the current editing session and have not yet saved the map. You cannot remove a CI that was on the map when you started the editing session. When you remove \(hide\) a CI from the map, the record of the CI in the CMDB is not deleted. In contrast, connection records for a removed CI are affected as described in [Deleting a connection](unified-map-editing-map.md#section-connections-deleting).
-   When you delete all connections between one CI and another CI so that no connection path remains to the home node, the isolated CI and all of its downstream connections are considered an island branch. When you save, changes that you made to downstream connections are saved and the island branch CI is removed from the map \(hidden\). The CI record is not, however, removed from the CMDB.

## Creating or modifying a connection \(relationship or reference\) between CIs

Use the map editor to add a connection between two CIs or to modify an existing connection.

To learn more, see [CI relationships in the CMDB](c_CIRelationships.md).

## Deleting a connection

**Warning:** Deleting a connection might result in an invalid CMDB state. Attempting to save a map that includes an orphan CI generates a warning.

Connections that are not editable are dimmed and view-only.

-   When you delete a connection, the connection is removed from the map \(hidden\). The relationship is deleted from the \[cmdb\_ci\_rel\] table only when you save your changes.

-   When you delete all connections between one CI and another CI so that no connection path remains to the home node, the isolated CI and all of its downstream connections are considered an island branch. When you save, changes that you made to downstream connections are saved and the island branch CI is removed from the map \(hidden\). The CI record is not, however, removed from the CMDB.
-   When you delete all connections to and from a CI and save the change, the following actions occur:
    -   The records of all relationships — both upstream to and downstream from — the CI are deleted from the CMDB \[cmdb\_ci\_rel\] table.
    -   The CI is removed from the map \(hidden\).
    -   The record of the CI in the CMDB is not deleted.

## Limitations

The map editor does not support the following actions:

-   Editing mapped application services \(service instances\).
-   Deleting a CI record from or adding a CI record to the CMDB.
-   Attempting to save a map that includes an orphan CI generates a warning.
-   Adding endpoint CIs to or removing endpoint CIs from the map.
-   Deleting reference or endpoint connections or removing from the map a CI that has reference or endpoint connections.
-   Updating the applicative flow relationship type \(connection between endpoint CIs\).

**Related topics**  


[CI relationships in the CMDB](c_CIRelationships.md)

[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)

[Add a suggested relationship](../task/t_AddANewSuggestedRelationship.md)

[Add a CI to a map using the map editor](../task/unified-map-add-ci.md)

[Create or modify a connection using the map editor](../task/unified-map-edit-connection.md)

[Delete a connection using the map editor](../task/unified-map-delete-connection.md)

