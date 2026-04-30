---
title: Node relationship configurations
description: Node relationship configurations are used to set up relationships between the records and objects defined in the table. You can configure the details of the main node such as its name, source, table name, filer conditions, and so on.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-11-04"
reading_time_minutes: 3
breadcrumb: [Main node configurations: A component of the Data Relationship Framework, Explore, Operational Resilience, Governance, Risk, and Compliance]
---

# Node relationship configurations

Node relationship configurations are used to set up relationships between the records and objects defined in the table. You can configure the details of the main node such as its name, source, table name, filer conditions, and so on.

For details on the updates in the Node relationship configurations introduced in Operational Resilience, version 21.1.x, refer to the "Node relationship configurations related list" in [Main node configurations: A component of the Data Relationships Framework](main-node-relationship-fw.md).

-   **Node relationship configurations related list**

    The existing Node relationship configurations related list has been updated and includes the following changes:

    -   Type column: The Type column has been added, offering two distinct options for displaying node relationship information:

        -   Default type: As shown in the earlier illustration, the "Default type" column displays the hierarchy from top to bottom. It’s the default option.
        -   Group type: Aggregates data at a specific node, providing a more focused view.

            ![Group type.](../image/main-node-config-group-type.png)

        This enhancement enables for more flexible and meaningful visualization of node data.

    -   Maximum number of nodes and Maximum number of levels: You can set the maximum number of nodes and levels for the map \(as shown in the **Properties** tab\). Similarly, you can also control the maximum number of children shown at the specific node relation and maximum number of levels shown at a specific node. The **Maximum number of levels** property is enabled only when the source table and target table in the Main node configuration are the same; if they’re different, this property is disabled.
    -   Direction: Another field added to the relationship configuration is "Direction," which specifies the direction of the relationship between the source and target tables. The direction can be set to either "Target to source" or "Source to target." When set to "Target to source," selecting a specific node displays all its upstream nodes, showing the relationships leading to that node. When set to "Source to target," selecting a specific node displays all its downstream nodes.

        ![Direction.](../image/main-node-config-direction.png)

        This enhancement provides more flexibility in visualizing and understanding the relationships between nodes.

    -   Copy functionality at the Main node: The main node configuration now includes a **Copy** UI action. When this functionality is used, the selected main node configuration is copied and then you’re required to set up the Nexus configuration for the copied main node.

For information on configuring the Node relationship configurations, see [Configure the Node relationship configurations](../task/update-node-rel-config.md).

For information on setting up relationships between different objects, see [Relationships between CSDM objects](build-up-relationships.md).

-   **[Relationships between CSDM objects](build-up-relationships.md)**  
You can configure relationships between various CSDM objects such as business services, service offerings, business processes, and application services by using the Main node configurations. The \[sn\_grc\_m2m\_profile\_profile table\] serves as the source table for establishing these relationships.

**Parent Topic:**[Main node configurations: A component of the Data Relationships Framework](main-node-relationship-fw.md)

