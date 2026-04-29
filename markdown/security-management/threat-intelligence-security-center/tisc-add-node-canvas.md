---
title: Adding a new node to the canvas
description: Use this section to create and add new entities, including observables or objects, directly from the investigation canvas.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with Investigation Canvas, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Adding a new node to the canvas

Use this section to create and add new entities, including observables or objects, directly from the investigation canvas.

## Before you begin

This feature enables quick enrichment of the canvas without having to navigate away from the current view.

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

4.  Open any case record.

    **Note:** When creating a case, you’re required to either create a canvas or link an existing one. After linking, the canvas actions including the option to add new nodes will be automatically available in the user interface.

5.  Select **Investigation Canvas** &gt; **New Node**.

    -   You can also view the **New Node** functionality from the drop-down list of the empty**Investigation Canvas** section of the Case.
    -   Another option to view the **New Node** functionality is to view from the investigation canvas page directly.
6.  To create a node, select the appropriate **Entity Category** and **Entity Type**.

<table id="choicetable_y4f_vd5_zfc"><thead><tr><th align="left" id="d125736e155">

Field

</th><th align="left" id="d125736e158">

Description

</th></tr></thead><tbody><tr><td id="d125736e164">

**Entity Category**

</td><td>

Select the entity category such as Observable, or Object.

</td></tr><tr><td id="d125736e173">

**Entity Type**

</td><td>

Select the entity type from the available options based on the select category.**Note:**

-   When an entity type is selected, the corresponding object form is automatically displayed, showing the key fields such as Name and Description along with any required fields that are needed to identify the parent entity.
-   If you attempt to create a duplicate entity, which means if you select an entity, which is existing in the application and try to create one with the same value then an error message will appear indicating that the entity already exists in the Threat Intelligence Library with the same value and type.


</td></tr></tbody>
</table>7.  Fill the necessary object details such as name, description.

8.  Select **Add** to add the new node.

    This process automatically adds the node to the investigation canvas.

    The newly added nodes are visually differentiated with a dot ![](../image/tisc-add-new-node.png) on the node them from nodes that are imported through the library or case artifacts.

    **Important:** Newly added nodes are temporary and aren’t saved to the threat intelligence library or canvas. If you refresh the canvas before saving, these nodes will be lost. Make sure to save the canvas after adding any new nodes to retain your changes.

9.  Right click on the new node and select **Add Relationship** option to create relationships between the nodes.

    **Note:**

    -   When creating new relationships, the edges are appeared as dotted lines, indicating they are temporary nodes and aren’t saved in the Threat Intelligence Library.
    -   Newly added edges are temporary and aren’t saved to the threat intelligence library or canvas. If you refresh the canvas before saving, these edges will be lost. Make sure to save the canvas after adding any new edges to retain your changes.
    ![Investigation Canvas New node representation with dotted line](../image/tisc-add-new-node-illustration.png)

10. Right click and select **Show Details** to view the details related to the selected entity.

    **Note:** To add data, you can either click the hyperlink within the details pane or select **Open Record** option and add the required node related data.

11. Select **Add Data to Library** option to save all the nodes and edges that were temporarily added during your investigation.

    By performing this action, the temporary records are converted to permanent aggregated records within the Threat Intelligence Library.


**Parent Topic:**[Working with Investigation Canvas](../concept/tisc-investigation-canvases.md)

