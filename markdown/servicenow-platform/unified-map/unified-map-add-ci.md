---
title: Add a CI to a map using the map editor
description: You can view an existing CI on the map to enable you to create, modify, or delete its connections.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Editing a map, Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Add a CI to a map using the map editor

You can view an existing CI on the map to enable you to create, modify, or delete its connections.

## Before you begin

Role required: sn\_cmdb\_admin or sn\_cmdb\_editor

## About this task

-   You can add only CIs that have existing records in the CMDB.
-   You can add only one CI at a time.
-   You can remove an added CI from the map if you have not yet saved the CI to the map.
-   If you try add a CI that already has a connection to another CI on the map, the map re-centers and the CI is highlighted. In some cases, due to filter settings, the CI isn't displayed.
-   An added CI appears on the map but its CMDB record isn't changed unless you change the CI connections and save the changes.
-   The map editor doesn't support adding endpoint CIs.
-   After you add a CI, it can be saved to the map only if it has a path \(direct or indirect\) to the home node.

## Procedure

1.  While working in a map, select the edit map icon ![](../image/icon-um-edit-map.png) and then take one of the following actions:

    -   Select and hold \(or right-click\) in an empty spot on the map and select **Add CI**.
    -   Select the Add CI icon ![](../image/icon-um-add-ci.png).
2.  On the Add a CI panel, specify the class of CI to add.

3.  Define a filter that will generate a list of CIs of the class that you specified.

    1.  Select one CI in the filtered results list and then select **Apply filters**.

    2.  Save the condition set as a custom filter for future use.

        Select the save custom icon ![](../image/icon-um-save-custom.png) and specify a name for the filter. You can select the filter whenever you add a CI.

4.  To add a CI that is already connected to another CI on the map, select **Add to map** or skip this step for a CI that is not yet connected to another CI on the map.

    The map re-centers on the added CI. Skip the remaining steps.

5.  To add a CI that is not yet connected to another CI on the map, select **Add to map and connect**.

    The map re-centers on the added CI and the Manage connection panel ![](../image/icon-um-edit-connection.png) opens.

6.  On the Manage connection panel \(![](../image/icon-um-edit-connection.png)\), specify the settings.

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
</table>7.  When you have specified all connection settings, select **Create connection**.


