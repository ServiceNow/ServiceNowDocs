---
title: View and edit the OT Network Map
description: View and edit the Operational Technology \(OT\) Network Map in the Industrial Workspace to visualize your OT networks per site and their OT devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/industrial-workspace/view-edit-ot-network-map.html
release: zurich
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-01-22"
reading_time_minutes: 3
breadcrumb: [Use, Industrial Workspace, Operational Technology]
---

# View and edit the OT Network Map

View and edit the Operational Technology \(OT\) Network Map in the Industrial Workspace to visualize your OT networks per site and their OT devices.

## Before you begin

Role required: cmdb\_ot\_isa\_viewer role and cmdb\_ot\_viewer

## Procedure

1.  Navigate to the Industrial Workspace.

2.  To open the Equipment Model Manager, select the **Equipment model** \[Omitted image "equip-model-manager-button.png"\] Alt text:icon.

3.  Select a site that you want to view the OT Network Map for.

4.  Select **View OT Network Map**.

    The network map opens in a new tab.

5.  To view the legend with an explanation of the visuals used in the network map, select the **Legend** \[Omitted image "legend-icon.png"\] Alt text: icon.

6.  To view additional information about a subnet node, hover your mouse over the node.

7.  To view additional information about a device node, hover your mouse over the node.

8.  To view the **Connection Summary** between subnet nodes, hover over the dashed line between the nodes as shown in the following image.

    \[Omitted image "connection-summary.png"\] Alt text: Connection Summary shown between subnet nodes

9.  To expand a subnet and view its individual device nodes, select the number on the subnet node.

    The number on the subnet node represents the total number of devices in the subnet. The following image shows an example of the device number.

    \[Omitted image "total-device-number-network-map.png"\] Alt text: Total number of devices shown on the subnet node

    **Note:** You can only expand one subnet at a time. For example, if Subnet A is expanded and you try to expand Subnet B, Subnet A automatically collapses.

10. To set a device node as the home node, complete the following steps.

    1.  To access the contextual actions, right-click the node or next to the device node name, select the dropdown.
    2.  Select **Set as Home node**.

        \[Omitted image "ot-network-map-set-as-home.png"\] Alt text: Set as home node menu option in the network map

        The selected device node is set as the home node and the node icon changes as shown in the following image.

        \[Omitted image "home-node.png"\] Alt text: Device node set as home node with updated node home image

11. To view the attributes for a device node, complete the following steps.

    1.  To access the contextual actions, right-click the node or next to the device node name, select the dropdown.
    2.  Select **Show attributes**.

        \[Omitted image "ot-network-map-show-attributes.png"\] Alt text: Show attributes menu option on the Network Map

        A side panel opens that shows the following attributes for the selected device node:

        -   Class
        -   Updated
        -   Location
        -   Owned by
        -   Most recent discovery
        -   Discovery source
12. To view the device connections for a device node, complete the following steps.

    1.  To access the contextual actions, right-click the node or next to the device node name, select the dropdown.
    2.  Select **Show device connections**.

        \[Omitted image "context-actions-device-node.png"\] Alt text: Show device connections UI action

        The network map updates to highlight the device-to-device connections and to show both connections within the same subnet, represented by a solid line, and cross-subnet connections, represented by a dashed line.

    3.  To see the **Device connection summary** details, hover over the IP address on the dashed line or hover over the solid line.

        The following image shows an example of the device connection summary on the dashed line.

        \[Omitted image "device-connection-summary.png"\] Alt text: Device connection summary shown for a device to device connection

    4.  To escape this view, select the dropdown again and click **Hide device connections**.
13. To apply filters to the map to refine the nodes shown, complete the following steps.

    1.  Select the **Filters** \[Omitted image "filter-list-icon.png"\] Alt text: icon.
    2.  Select or deselect the options available under the following filter categories.

        |Filter|Description|
        |------|-----------|
        |Class|The name of the assigned class for the OT device.|
        |Criticality|The measure of the relative risk to the site process due to failure of the device.|
        |Manufacturer|The device manufacturer.|
        |Purdue level|The assigned Purdue level. Ranges 0–5.|
        |Discovery source|The Discovery source for the OT device data.|

    3.  Select **Apply**.
    4.  To return to the default settings, select **Reset filters** and click **Apply**.
14. To search for a subnet, device node, managed network, and so on in the node map, use the **Find on map** search bar.

15. To align the map back on the home node, select the **Align to home node** \[Omitted image "align-home-node.png"\] Alt text: icon in the control panel.


**Parent Topic:**[Using the Industrial Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/industrial-workspace/using-industrial-workspace.md)

