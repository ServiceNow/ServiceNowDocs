---
title: Network inventory templates
description: You define the network inventory templates that contain the business guidance rules from a telecommunications provider in the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Model your workflow, Explore, Telecommunications Network Inventory]
---

# Network inventory templates

You define the network inventory templates that contain the business guidance rules from a telecommunications provider in the Telecommunications Network Inventory application.

## Introduction to inventory template

A template includes the rules on how the equipment configurations should be generated and are based on the operating requirements from the manufacturer. It also includes the configuration and equipment compatibility information with the other types of hardware. To learn more about the network inventory templates and their relationships, see [Create inventory template for network asset instantiation](preparing-inv-templates-network-asset-generation.md).

## Types of network inventory templates

-   **Inventory Template**

    A network inventory template contains a set of detailed business guidance rules from a telecommunications provider. These rules state how the equipment configurations should be generated and are based on certain operating requirements. For example, based on the equipment model that you develop, you can create a template for use in densely populated metropolitan areas and then you can create another equipment model template for use in sparsely populated rural areas. To learn more about how to create an inventory template, see [Create an inventory template](../task/create-inventory-templates.md).

    Inventory templates also have an internal attribute that shows if an entry in an inventory template list is a singular template or a template relationship. A template relationship designates that there’s a relationship between this template and another template. These associated templates appear in the Related Template tab in the Inventory template form. To learn more about the template relationship, see [Create inventory template relationship](creating-inventory-templates-telco-equipment.md).


-   **Default Template**

    Default templates capture the default attribute values for a configuration item \(CI\) class. A template defines the set of attribute values for any resource \(equipment, card, and so on\). When this default template is associated with an inventory template, it adds these attribute values to the resource that is instantiated using that template.

    You can define multiple default templates for a single CI, such as equipment, when there are multiple business requirements for capturing different sets of attribute default values. When you create a default template and you select a CI, you can also select an associated attribute of that CI and set a value for it.

    To learn more about how to create a default template, see [Create a default template](../task/create-default-templates.md).


## Accessing the Network Inventory Template node

You can access the inventory template in the Network Inventory Templates node in the Network Inventory Workspace List view.

