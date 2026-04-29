---
title: Visualize circuits
description: The network diagram in the Telecommunications Network Inventory application graphically displays a hierarchical map of the logical connection and its underlying connection elements. You can use the network diagram to get a detailed overview of the logical connection.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Visualize circuits

The network diagram in the Telecommunications Network Inventory application graphically displays a hierarchical map of the logical connection and its underlying connection elements. You can use the network diagram to get a detailed overview of the logical connection.

The network diagram graphically displays a circuit of the logical connection elements, and the details of each element. It provides a detailed overview of a logical connection and how the various elements are connected to each other. You can view the following by using the network diagram:

-   Logical connection and all the underlying connection elements.
-   Revision of the logical connection and all underlying connection elements.
-   Protection paths of the logical connection.

A protection path of a logical connection refers to an alternative route in case the primary path \(logical connection\) fails or experiences significant issues.

The following example shows a network diagram in the Telecommunications Network Inventory application.

![View of a network diagram with map pane, details pane, and zoom options.](../image/netwotk-diagram.png "Example for a network diagram")

A network diagram contains two panels:

-   The map pane shows the map for a selected logical connection, revision of the logical connection, and protection path.
-   The details pane shows related information of the logical connection according to the current selections.

To learn more about how to use the network diagram, see [Network diagram](using-network-diagram.md).

## Map pane

The map shows all logical connection elements in the hierarchy starting with the home node CI, up to the specified level. You can expand the hierarchy levels up to three levels and view all the underlying connections. You can only expand connections that have connection elements underneath them.

You can perform the following actions in the map pane:

-   Expand and collapse the nodes and view all the underlying connections.
-   View the revision of the logical connection.
-   View the protection paths of the logical connection.
-   Use the zoom controls to zoom in and out of the map.

To learn more, see [View the details of a network diagram](../task/show-a-ci-related-details-network-diagram.md).

## Details pane

The details pane shows the related information about the logical connection elements in a network diagram. If a node is selected in the map pane, the details pane shows the related information for that node. For example, if you select a logical connection node on the network diagram, then the details pane shows all the details related to that logical connection.

You can perform the following actions in the details pane:

-   Select the info icon \(![Info Icon.](../image/icon-info.png)\) to open the details pane.
-   Select more options icon \(![More Options Icon.](../image/icon-more-option.png)\) in the details pane and then select **View Details** to redirect to the corresponding CI form.

## Access

You can access the network diagram in the Telecommunications Network Inventory Workspace as follows:

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.
2.  Open the desired logical connection record.
3.  Select **View connection** to open the network diagram for the respective logical connection.

