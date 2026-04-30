---
title: Delete a connection using the map editor
description: While editing a map, you can delete a connection \(a relationship record\) from the CMDB. The CIs that are involved in the connection are not deleted from the CMDB.
locale: en-US
release: zurich
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Editing a map, Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Delete a connection using the map editor

While editing a map, you can delete a connection \(a relationship record\) from the CMDB. The CIs that are involved in the connection are not deleted from the CMDB.

## Before you begin

Role required: sn\_cmdb\_admin or sn\_cmdb\_editor

## About this task

**Warning:** Deleting a connection might result in an invalid CMDB state. Attempting to save a map that includes an orphan CI generates a warning.

The map editor does not support the following actions:

-   Editing mapped application services \(service instances\).
-   Deleting reference or endpoint connections or removing from the map a CI that has reference or endpoint connections.
-   Updating the applicative flow relationship type \(connection between endpoint CIs\).

-   When you delete a connection, the connection is removed from the map \(hidden\). The relationship is deleted from the \[cmdb\_ci\_rel\] table only when you save your changes.

-   When you delete all connections between one CI and another CI so that no connection path remains to the home node, the isolated CI and all of its downstream connections are considered an island branch. When you save, changes that you made to downstream connections are saved and the island branch CI is removed from the map \(hidden\). The CI record is not, however, removed from the CMDB.
-   When you delete all connections to and from a CI and save the change, the following actions occur:
    -   The records of all relationships — both upstream to and downstream from — the CI are deleted from the CMDB \[cmdb\_ci\_rel\] table.
    -   The CI is removed from the map \(hidden\).
    -   The record of the CI in the CMDB is not deleted.

You can learn more about relationships at [CI relationships in the CMDB](../concept/c_CIRelationships.md).

At any time, select the reset icon ![](../image/icon-um-reset-map.png) to undo all unsaved changes.

## Procedure

1.  While editing a map, take one of the following actions:

    **Note:** No deletions happen until you select **Save**.

    -   To delete a single connection, select it and then select **Delete** in the Attributes panel. Alternatively, right-click the connection and then select **Delete**.
    -   To delete only particular connections for a CI, select the CI. In the editing panel, scroll to the connections and select **Delete**.
    -   To delete all connections both upstream and downstream of a CI, select the CI and then select **Remove CI**.
2.  Deletions happen when you select **Save**.


**Related topics**  


[CI relationships in the CMDB](../concept/c_CIRelationships.md)

[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)

[Add a suggested relationship](t_AddANewSuggestedRelationship.md)

[Create or modify a connection using the map editor](unified-map-edit-connection.md)

