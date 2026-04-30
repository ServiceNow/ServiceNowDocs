---
title: Service Portfolio Management taxonomy
description: Service Portfolio Management uses a taxonomy framework to organize and manage services in a portfolio.
locale: en-US
release: yokohama
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create portfolios, Using Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Service Portfolio Management taxonomy

Service Portfolio Management uses a taxonomy framework to organize and manage services in a portfolio.

## Portfolio structures

Prior to the Utah release, Service Portfolio Management provided one portfolio structure with taxonomy layers and nodes. With the Utah release and beyond, existing customers can move from the legacy structure to the improved standard structure by opting in via a system property. The improved standard portfolio structure no longer uses layers in the taxonomy framework. Rather, it only uses nodes. For more information on the two types of portfolio structures, see [Service Portfolio Management portfolios](SPM2-service-portfolios.md).

To upgrade to the standard portfolio structure, the portfolio\_admin navigates to **Service Portfolio Management &gt; Administration &gt; Upgrade to Standard Portfolio** to access the system property \[standard\_portfolio\_construct.turn\_on\]. Only existing customers see this menu path. New customers get the standard portfolio structure by default so this menu path isn't available.

## Legacy portfolio structure taxonomy

If you’re working in a legacy portfolio structure, then your taxonomy framework may look something like this example.

![Legacy portfolio structure taxonomy example.](../image/spm2-taxo-layers.png "Legacy portfolio structure taxonomy example")

In this example, there are two service portfolios - IT Service portfolio and Smart devices portfolio.

-   Below the service portfolios are the layers. You can have 1 to N layers and they can be a taxonomy node or a taxonomy leaf node, or both.
-   Below the layers and leaf nodes are the services and service offerings.

## Standard portfolio structure taxonomy

If you’re using the improved, standard portfolio structure, then your taxonomy framework may look something like this example.

![Standard portfolio structure taxonomy example](../image/spm2-taxo-nodes.png "Standard portfolio structure taxonomy example")

In this example, there’s one service portfolio at the top — Smart devices.

-   Below the service portfolio, is the node level.
    -   You can have 1 to N node levels.
    -   A node level can contain both a taxonomy node and a leaf node.
    -   Assign multiple nodes \(rather than layers\) for more flexibility as you structure your service portfolios. For example, a single portfolio can have multiple levels of depth via node-to-node relationships.
-   Below the taxonomy node levels are the services and service offerings.

    **Note:** You can see a visual relationship map of nodes, services, and service offerings in Digital Portfolio Management \(DPM\). For more information, see [Getting started with Digital Portfolio Management](../../digital-portfolio-management/concept/dpm-using-cfx.md).


-   **[Create taxonomy layer definitions](../task/create-or-mod-SPM2-taxonomy-layers.md)**  
Create an unlimited number of taxonomy layers to organize, label, and manage your service portfolio. Taxonomy layers represent the highest containment levels of your service portfolio. Each level supports branches, or nodes, that contain child nodes or services in a hierarchical top-to-bottom structure.
-   **[Create taxonomy nodes](../task/create-or-mod-SPM2-taxonomy-nodes.md)**  
Create an unlimited number of nodes, or branches, and add them to your service portfolio taxonomy layers. By configuring taxonomy nodes, you can successfully achieve a highly detailed and organized service portfolio containing multiple elemental layers—from general to specific.

**Parent Topic:**[Create portfolios in Service Portfolio Management](../task/create-or-modify-SPM2-portfolios.md)

**Related topics**  


[Create taxonomy nodes](../task/create-or-mod-SPM2-taxonomy-nodes.md)

[Create taxonomy layer definitions](../task/create-or-mod-SPM2-taxonomy-layers.md)

[View relationship maps in Digital Portfolio Management](../../digital-portfolio-management/concept/dpm-view-relationship-map.md)

