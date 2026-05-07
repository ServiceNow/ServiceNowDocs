---
title: Main node configurations: A component of the Data Relationships Framework
description: Starting with Release 20.1.x, the Main node configurations, supported by the Data Relationships Framework, are available with Operational Resilience to define dependency roll-up chains. Operational Resilience administrators configure the entity types and pillars, generate the entities, and then establish relationships between different CSDM objects. After this setup is complete, data from the CMDB is fetched into Operational Resilience, displaying rolled-up dependencies in the Workspace view.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [Explore, Operational Resilience, Governance, Risk, and Compliance]
---

# Main node configurations: A component of the Data Relationships Framework

Starting with Release 20.1.x, the Main node configurations, supported by the Data Relationships Framework, are available with Operational Resilience to define dependency roll-up chains. Operational Resilience administrators configure the entity types and pillars, generate the entities, and then establish relationships between different CSDM objects. After this setup is complete, data from the CMDB is fetched into Operational Resilience, displaying rolled-up dependencies in the Workspace view.

## Data Relationships Framework

The Data Relationships Framework \(sn\_grc\_rel\_config\) application provides the underlying framework to retrieve data from the CMDB. The Main node configurations in Operational Resilience support different business views in the CSDM model. The relationships defined in the Main node configuration align with the relationships specified in the CSDM model.

## Setting up the Main node configurations

The Operational Resilience administrators set up the Main node configurations via the Main node configuration module listed in the **General administration** menu of the Core UI.

For information on configuring the Main node configurations, see [Configure the Main node configurations](../task/set-up-main-node.md).

![Source module.](../image/main-node-config-src-path.png)

Administrators can also configure the sources of the Main node configurations by accessing the Main node configuration source module. For information on configuring the Main node configuration source, see [Main node configuration source](main-node-configuration-source.md).

## Changes in the Main node configurations in Operational Resilience, version 21.1.x

Beginning with Operational Resilience, version 21.1.x, the following changes are introduced in the Main node configurations.

1.  Properties tab in the UI: A **Properties** tab has been introduced in the UI of the Main node configurations. For more information, see the "Properties tab introduced in the Main node configurations UI" section.
2.  Node relationship configurations related list: The existing Node relationship configurations related list has been enhanced. For more information, see the "Node relationship configurations related list" section.
3.  Nexus map configurations related list: Define the UI configuration for the selected main node by configuring the Nexus map configuration settings. You can configure the node and edge settings as defined in the following sections:
    -   Node configurations
    -   Node status configurations
    -   Edge configurations
    -   Edge status configurations

## Properties tab introduced in the Main node configurations UI

Two new properties have been introduced to control the display settings for node maps:

-   Maximum number of nodes: Determines the total number of nodes that are displayed in the node map.
-   Maximum number of levels: Specifies the maximum number of hierarchical levels to be shown, from top to bottom.

![Properties.](../image/main-node-config-properties-tab.png)

These properties enable you to have more customized and controlled visualization of complex node maps, enhancing the overall user experience.

## Changes in the Node relationship configurations related list

The existing Node relationship configurations related list has been updated and includes the following changes:

-   Type column: The Type column has been added, offering two distinct options for displaying node relationship information:

    -   Default type: As shown in the earlier illustration, the "Default type" column displays the hierarchy from top to bottom. It’s the default option.
    -   Group type: Aggregates data at a specific node, providing a more focused view.

        ![Group type.](../image/main-node-config-group-type.png)

    This enhancement enables for more flexible and meaningful visualization of node data.

-   Maximum number of nodes and Maximum number of levels: You can set the maximum number of nodes and levels for the map \(as shown in the **Properties** tab\). Similarly, you can also control the maximum number of children shown at the specific node relation and maximum number of levels shown at a specific node. The **Maximum number of levels** property is enabled only when the source table and target table in the Main node configuration are the same; if they’re different, this property is disabled.
-   Maximum number of children: You can control maximum number of children to be displayed at the specific node relation. The minimum value for this field is 2.
-   Direction: Another field added to the relationship configuration is "Direction," which specifies the direction of the relationship between the source and target tables. The direction can be set to either "Target to source" or "Source to target." When set to "Target to source," selecting a specific node displays all its upstream nodes, showing the relationships leading to that node. When set to "Source to target," selecting a specific node displays all its downstream nodes.

    ![Direction.](../image/main-node-config-direction.png)

    The "Direction" column helps you to visualize and understand the relationships between nodes.

-   Copy functionality at the Main node: The main node configuration now includes a **Copy** UI action. When this functionality is used, the selected main node configuration is copied and then you’re required to set up the Nexus configuration for the copied main node.

    ![Copy functionality.](../image/copy-main-node.png)


## Nexus map configurations related list

The Nexus map configurations related list has been introduced in the UI. Configuring the Nexus map configuration for the selected main node helps you to define its UI configuration, determining how the selected node would be displayed in the Nexus map. This setting includes settings for colors, icons, edge configuration, and other visual elements. A single main node configuration can have multiple Nexus configurations, enabling for different data views for the same structure. This flexibility is achieved through configuration at the Nexus map level.

![Nexus map configuration.](../image/main-node-config-nexus-map.png)

You can select the Nexus map configuration from the related list and view or update its configuration details. The Nexus map configuration for "OpRes resilience map UI" is shown in the example.

![Main node.](../image/main-node-config-nexus-map-main-node-tab.png)

For every selected main node configuration, you must choose the workspace type where you want to apply this configuration. The available workspace type includes the Operation Resilience Workspace.

**Note:** To display the Nexus map, choose the desired workspace from the available options. If the required workspace isn’t listed, you can create a workspace record by accessing the **Nexus map configuration workspace type** from the **All** menu.

The **Main node** tab displays the name of the Main node table along with its associated conditions. The **Node UI details** tab shows the Node UI type, which is set to "Node map default node" by default.

To synchronize changes made at the Main node level, such as adding or modifying relationships, into the Nexus map configuration, use the **Sync from main node configuration** UI action. This action helps you to maintain synchronization between the Main node and Nexus map configuration.

The Nexus map configuration is also referred to as the Main Node UI configuration.

Within the Nexus map configuration, you can customize two key aspects:

-   Node configuration: This setting involves configuring the UI settings for nodes, including their appearance.
-   Edge configuration: This configuration involves customizing the edges between nodes, including their type \(dashed or solid\), color, and other conditional settings.

These configurations enable you to tailor the visualization of your Nexus map according to your requirements.

## Node configurations

The Node configurations related list helps you to configure the UI settings for the selected node. Then the selected node is displayed in the Nexus map according to the UI settings. The following example shows the node configuration settings for the "Opres resilience map UI \(Top to bottom\)" Nexus map configuration.

![Main node.](../image/main-node-config-nexus-map-main-node-tab.png)

Node configuration settings: Selecting the Node configuration related list shows the node configuration settings defined for the selected node. The example shows the node configuration settings defined for the "Entity \[sn\_grc\_profile\]" table.

![Node configuration.](../image/main-node-nexus-map-node-configuration.png)

You can update the following UI parameters for the node:

-   Primary label: Update the primary label to be displayed for the node, for example, Name.
-   Icon: Update the icon to be used for the node in the main node UI, for example, briefcase-outline.
-   Secondary label: Update the secondary label to be displayed for the node, for example, class.
-   Tooltip: Update the tooltip to be displayed when hovering over the node, for example, Name.
-   **Configuration for set as main node** field \(Setting a node as the Main Node\): To enable the **Make this primary** functionality for a node \(To make a node as a primary node\), you must configure the **Configuration for set as main node** setting. This configuration reflects the hierarchy flow for the node that is designated as primary. To set a specific node as the Main node \(primary node\) at any point, select the Nexus map configuration in the **Configuration for set as main node** field. For example, when viewing node relationships from primary node A to node B and node C, the node chain such as "A -&gt;B -&gt;C" is displayed. You can select node B as the Main node \(primary node\) and then the display shows node A as the upstream node and node C as the downstream node.

    **Configuration for 360° view** field: You can configure this setting to determine the configuration to be used when viewing a 360° view, for example, **Entity**.

    **Context record**: You can define the context record for the selected entity, for example, **Applies to record**.


Node map grouping and expansion: The node map displays grouped nodes, such as first node, second node, and third group as expandable. Right-selecting on the grouped node provides the options to either expand the node or view the open list, which lists the number of nodes grouped at that point.

![Grouped node.](../image/expand-fun-node.png)![Open list.](../image/open-list.png)

Expansion functionality: The node expansion feature enables you to view additional nodes, such as the "passenger information" level shown in the example. The expansion of the nodes is updated dynamically based on the number of levels available, enabling a more detailed and controlled exploration of the node map. By using the expand and open list options, you can efficiently navigate the map and better understand the relationships between nodes.

![Expand group.](../image/expand-group.png)

Node map aggregation feature: The node map includes an aggregation feature that enables you to group nodes at a specific level. To use this feature, you can change the main node configuration type from **Default** to **Group** as shown in the example. This action aggregates the nodes at the selected level, providing a more consolidated view.

![Group type.](../image/main-node-config-group-type.png)

When loading a map with a grouped configuration, nodes are initially displayed in a grouped state. Right-selecting on an aggregated node provides the **Open list** option, which displays the entities aggregated at that point.

![Open list option.](../image/open-list-option.png)

This feature simplifies complex node maps, allowing you to focus on specific areas of interest and enhancing overall usability. By using the Group feature, you can more easily analyze and understand the relationships between nodes.

## Node status configurations

The Node status configurations related list helps you to define conditions for a table and its related lists for the selected node. The example shows entity conditions since the Entity \[sn\_grc\_profile\] table is being used. These conditions can be set using fields from the node table or related lists. For example, when the conditions defined in the "Related list conditions" panel are met, that specific node is marked with the "Critical" color and the "Exclamation-outline" icon.

![Node status.](../image/main-node-nexus-map-node-status-configuration.png)

In this way, when the defined conditions are met, the node status configuration is updated accordingly.

You can define multiple filter conditions as shown in the Conditions column.

![Conditions.](../image/main-node-node-status-condition.png)

Default node status configuration: When a condition isn’t defined for the node status configuration, it’s the default node status configuration.

![Default node status configuration.](../image/main-node-node-status-default-condition.png)

By configuring these settings, you can customize the display and behavior of nodes in the Nexus map to suit your needs.

## Edge configurations

Edge configurations can be set up similarly to node configurations. For a given relationship between entities \(for example, upstream or downstream\), you can define two edge configurations.

![Edge configuration.](../image/main-node-nexus-map-edge-configuration.png)

Edge settings: You can customize the following edge settings:

-   Label: The label to be displayed on the edge.
-   Tooltip: The tooltip to be shown when hovering over the edge.
-   Edge type: The type of edge to be displayed \(for example, solid or dashed\).

The Edge configurations related list and Edge configuration record are displayed in the following examples.

![Edge configurations related list.](../image/edge-config-record.png)![Edge configurations record.](../image/edge-config-record.png)

The following example shows the maximum number of children from Source to target direction as 3.

![Maximum number of children.](../image/node-rel-config-3.png)

As a result, for every node, the maximum number of children shown is 3.

## Edge status configurations

Edge status configurations can be defined based on specific conditions. You can set the edge color, type, and other properties based on these conditions. For example, you can set an edge to display in magenta by default, or change its type to dashed or solid based on a specific condition. By configuring these edge settings, you can create a more informative and visually appealing Nexus map. The edge configuration settings complement the node configuration settings, enabling for a comprehensive visualization of the relationships between entities.

![Edge status configuration.](../image/edge-status-config.png)![Edge status configuration example.](../image/edge-status-config-example.png)

## Main node configurations included with the base version

The Main node configurations are included with the Operational Resilience base version. The following Main node configurations, with the source being the "OpRes CMDB", are shipped with the base version:

-   Opres with CSDM header
-   Business process to dependencies
-   Business service to dependencies
-   Service offering to dependencies
-   Service \(CMDB\)

![Menu.](../image/main-node-menu.png)

**Note:** You can fully customize the Main node configurations and for each configuration, you can configure the node relationships and Nexus map configurations from the Node relationship and Nexus map configuration related lists. For more information on how to configure the node relationships and Nexus map configurations, see [Configure the Node relationship configurations](../task/update-node-rel-config.md).

1.  Opres with CSDM header configuration for business services: The Opres with CSDM header configuration defines the relationships for a business service and is primarily used by new customers.

    This configuration sets up the direct and indirect relationships between the following objects:

    1.  Application services
    2.  Business processes
    3.  Business services
    4.  Service offerings
    The following diagram illustrates the structure of the Opres with CSDM header configuration, available as a base version in Operational Resilience. A business service can have relationships configured with one or more application services, service offerings, and business processes. When entities are generated and scheduled jobs are executed, dependencies are fetched and rolled up to the parent business service. The configuration supports multiple levels of dependencies, as shown in the example.

    ![Header.](../image/main-node-structure-opres-csdm-header.png)

    For more information on the Opres with CSDM header configuration, see [Opres with CSDM header Main node configuration](opres-with-csdm-header.md).

2.  Service \(CMDB\) configuration for services: The Service \(CMDB\) configuration defines the relationships for a service and is primarily used by existing customers. It supports only one level of dependency, such as a parent service having a child service, a process, or a dependency. A child service can have a process and a dependency \(such as Dep2 or Dep4 as shown in the example\) and a process can have a dependency \(such as Dep3 as shown in the sample hierarchy\).

    ![Sample hierarchy.](../image/s-sam-hier.png)

    For more information on the Service \(CMDB\) configuration, see [Service \(CMDB\) Main node configuration](main-node-config-bs-cmdb.md).

3.  Dependency configurations:

    The Dependency configurations define the relationships for dependencies that are related to business services, business processes, and service offerings.

    1.  Business process to dependencies: The Business process to dependencies configuration defines the relationships from a business process to its dependencies. The following diagram shows the dependency relationship framework for a business process, available as a base version in Operational Resilience. A business process can have relationships with application services, other business processes, technical services, contracts, third parties, and more. When entities are generated and scheduled jobs are executed, dependencies are fetched and rolled up to the parent business process.

        ![Processes.](../image/main-node-structure-bp.png)

        For more information on the Business process to dependencies configuration, see [Business process to dependencies Main node configuration](main-node-config-bp-to-dep.md).

    2.  Business service to dependencies: The Business service to dependencies configuration defines the relationships from a business service to its dependencies. The following diagram illustrates the dependency relationship framework for a business service, available as a base version in Operational Resilience. A business service can have relationships with locations, contracts, third-parties, third-party engagements and more. When the entities are generated and scheduled jobs are executed, dependencies are fetched and rolled up to the parent business service.

        ![Services.](../image/main-node-structure-dep-bs.png)

        For more information on the Business service to dependencies configuration, see [Business service to dependencies Main node configuration](main-node-config-bs-to-dep.md).

    3.  Service offering to dependencies: The Service offering to dependencies configuration defines the relationships from a service offering to its dependencies. The following diagram shows the dependency relationship framework for the service offerings, available as a base version in Operational Resilience. A service offering can have relationships with application services, other business processes, technical services, contracts, third parties, and more. When entities are generated and scheduled jobs are executed, dependencies are fetched and rolled up to the parent service offering.

        ![Offerings.](../image/main-node-structure-so.png)

        For more information on the Service offering to dependencies configuration, see [Service offering to dependencies Main node configuration](main-node-config-so-to-dep.md).

4.  BCM dependency configurations: When the Business Continuity Management application is installed in an instance, BCM related dependencies are fetched into the Operational Resilience application. The Main node configurations related to BCM, such as BCM-CMDB, Downstream related plan, Plan primary assets, Plan related assets, and Upstream related plans, are shown in the example.

    ![Main node configurations for BCM.](../image/bcm-related-main-node-configs.png)

    For more information on the BCM dependency configurations, see [BCM dependencies related Main node configurations](bcm-dep-config-to-opres.md).


For information on gathering data aligned with the latest CSDM model, see [Gathering data aligned with the CSDM setup](using-csdm-v5.md).

After setting up the Main node configurations, you must verify that the entities are generated in Operational Resilience. Only when the entities are generated in Operational Resilience and the relationships are created in the Main node configurations, CMDB data can be brought into Operational Resilience for reporting.

-   **[Node relationship configurations](node-relationship-configurations.md)**  
Node relationship configurations are used to set up relationships between the records and objects defined in the table. You can configure the details of the main node such as its name, source, table name, filer conditions, and so on.
-   **[Nexus map configurations](nexus-map-configuration.md)**  
Beginning with Operational Resilience, version 21.1.x, the Nexus map configuration has been introduced. To display a main node in the Operational Resilience Workspace, you must configure the Nexus map. The Node Map configuration UI allows you to visualize related data hierarchically, track issues, and identify areas needing attention for effective resolution or health monitoring.

**Parent Topic:**[Exploring Operational Resilience](what-is-opres.md)

