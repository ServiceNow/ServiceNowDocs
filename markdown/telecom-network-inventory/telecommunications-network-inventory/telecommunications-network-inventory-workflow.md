---
title: Model your workflow
description: Learn how to create a network inventory record in the Telecommunications Network Inventory application to store the details about your network assets. As you create the records, you can also define the relationship between each inventory record so that you can design a digital model of your network.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Telecommunications Network Inventory]
---

# Model your workflow

Learn how to create a network inventory record in the Telecommunications Network Inventory application to store the details about your network assets. As you create the records, you can also define the relationship between each inventory record so that you can design a digital model of your network.

## Network inventory workflow overview

By building an accurate digital representation of your network, you can view your physical and logical resources, improve how those resources are used, and reduce the operational costs of your network.

You use a series of forms such as telco equipment and network interface, to create and maintain your network inventory records. You can access these forms in the Inventory node in the Network Inventory Workspace List view.

## Methods for creating a network inventory record

You can create a network record by either of these two methods in the Telecommunications Network Inventory application:

1.  Create network inventory records manually by using inventory forms. With these forms, you can create and review the network inventory records and then define the relationships between them. You can access the inventory form in the Inventory node in the Network Inventory Workspace List view. To learn more, see [Manually creating and reviewing your network asset instances](creating-telecommunications-network-inventory.md).
2.  Create network inventory records by using the design and assign function. Before you start the design and assign function, you set up the inventory model, template, and model relationships for your design criteria. By using the design and assign function, you perform inventory tasks to set a network design criteria that initiate change workflows. With these workflows, you can assign inventory resources and instantiate your network inventory record. To learn more about design and assign function, see [Design and assign](telecommunications-circuit-design-resource-assignment.md).
3.  Create network inventory records by using the Resource Inventory Open API. The Resource Inventory Open API provides endpoints to create, retrieve, and delete resources in your network. If you’re integrated with an external system, you can get the inventory records by using the Resource Inventory Open API. To learn more about the functions that enable you to query and manipulate [Network inventory templates](using-templates-tni.md) inventory records, see [Resource Inventory Open API](https://www.servicenow.com/docs/access?context=resource-inventory-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

## Inventory model and template

Inventory models and templates provide a framework for creating network inventory records in the Telecommunications Network Inventory application. A network inventory model contains the assets, services, and the relationships that define the infrastructure of your telecommunications networks. A template contains the business guidance rules on how the network asset must be configured in a network.

You can create the models, templates, and the relationships between them. You can have multiple configurations of the network inventory templates.​

-   To learn more about the inventory model, see [Network inventory models](using-inventory-models-tni.md).
-   To learn more about the inventory template, see [Network inventory templates](using-templates-tni.md).
-   To learn more about the inventory model relationship, see [Model relationships](inventory-modeling-process.md).

**Related topics**  


[Data model](uses-for-network-inventory-data.md)

