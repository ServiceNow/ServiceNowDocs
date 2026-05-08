---
title: Design and assign
description: With the design and assign function, you can build a digital representation of your network inventories and your network service in the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Modeling your workflow, Explore, Telecommunications Network Inventory]
---

# Design and assign

With the design and assign function, you can build a digital representation of your network inventories and your network service in the Telecommunications Network Inventory application.

## Design and assign overview

By using the design and assign function, you perform inventory tasks sequentially or in parallel to set a network design criteria that initiate s change workflows. With these workflows, you can assign inventory resources and instantiate your network inventory. You can also perform the design and assign function with the information that you collected from the customer orders.

When you perform the design and assign function in the Telecommunications Network Inventory application, you use the standard processes from the Change Management and Workflow Studio applications. Create a change request enables you to instantiate the network inventory resources to support your network service topologies. It helps you efficiently build new network capacity with accurate resource allocation. You can also automate workflows to create and expand your network service.

You can design and configure both simple circuits and a complex network infrastructure. You can then perform path analysis and computations for your network assignments​. You can also apply virtual local area network \(VLAN\) and link aggregation group \(LAG\) assignment rules for Passive Optical Networks \(PONs\). By using the design and assign function, you enforce technology and process restrictions as you design and allocate your network resources.

## Design and assign workflow

![Infographic showing the workflow diagram of design and assign process. To learn more, see following text.](../image/MMASSET0020469-Telecommunications-design-and-assign-landing.png)

Before you start the design and assign function, you define the models, model relationships, templates, and template relationships for your design criteria. Then the ServiceNow AI Platform generates an automated workflow that performs all the tasks that are required to instantiate a network inventory.

As an inventory template or catalog manager, you can do the following tasks to instantiate your network inventory:

1.  Create the inventory models. You create an inventory model to track the technical information from the manufacturer about a network asset. When you instantiate an inventory record, your inventory record contains this standard manufacturer information. To learn more, see [Create inventory models](creating-your-inventory-models.md).
2.  Create the model relationship. The model relationship captures the relationships between the inventory models. To learn more, see [Model relationships](inventory-modeling-process.md).
3.  Create the inventory template. You create the network inventory template that contains the business guidance rules from a telecommunications provider. To learn more, see [Create inventory template for network asset instantiation](preparing-inv-templates-network-asset-generation.md).

You can then instantiate a new network inventory record by using the change management workflow to fulfill the network designs. As an inventory agent, you perform the following tasks:

1.  Create the change request with the change model. To learn more, see [Create a change request from Network Inventory Workspace](../task/create_a_change_request_in_tni.md).
2.  Create the change tasks from the change request. The network asset instantiation takes place using an Application programming interface \(API\) or change task that you create from the change request. To learn more, see [Create and execute a change task in Telecommunications Network Inventory](../task/create-change-task-in-tni.md).

When you complete the task, the following processing takes place:

-   A network inventory record is generated. The record is based on the same structural relationships that you defined for the inventory templates and associated inventory models. The configured item consists of your inventory model and all the related inventory models.
-   If you integrate with other operational and business support systems, the process triggers an internal workflow. This workflow completes the purchase, installation, shipment, and instantiation of your network asset at the designated site. This internal workflow is based on the individual tasks or lists of tasks that are associated with the inventory model in Workflow Studio.

## Instantiation example

You can create a set of network inventory records to fulfill an order request for Gigabyte Passive Optical Networks \(GPON\) broadband by using the design and assign function. To learn more, see [Design and assign GPON broadband service](gpon-broadband-service.md).

**Parent Topic:**[Modeling your workflow](telecommunications-network-inventory-workflow.md)

**Related topics**  


[bundle-cadev.flow-designer]

[bundle-itsm.c_ITILChangeManagement]

[Network inventory models](using-inventory-models-tni.md)

[Network inventory templates](using-templates-tni.md)

[Model relationships](inventory-modeling-process.md)

