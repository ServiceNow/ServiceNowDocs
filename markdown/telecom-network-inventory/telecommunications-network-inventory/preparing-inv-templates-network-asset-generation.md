---
title: Create inventory template for network asset instantiation
description: As an inventory template manager, you create templates using functions you access from the Lists view in the Network Inventory Workspace. These templates contain the detailed business guidance rules so that you can properly configure your equipment. During this process, you also specify the relationships between each inventory template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/preparing-inv-templates-network-asset-generation.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Telecommunications Network Inventory]
---

# Create inventory template for network asset instantiation

As an inventory template manager, you create templates using functions you access from the Lists view in the Network Inventory Workspace. These templates contain the detailed business guidance rules so that you can properly configure your equipment. During this process, you also specify the relationships between each inventory template.

An inventory template includes the rules on the proper way to configure the equipment. These rules are based on the operating requirements from the manufacturer. A template also includes such information as the number of available slots and whether the hardware in a piece of equipment is compatible with the equipment that is related to it.

Your network inventory templates represent a unique configuration of a network entity that a network service provider would instantiate based on their business guidance. If you properly define your templates and their relationships, the instantiation process uses the configuration rules from the vendor and you do not generate unsupported network asset instances.

**Note:** To learn more about creating templates and generating network assets from your model and template records, see [Modeling your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md).

-   **[Create an inventory template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-inventory-templates.md)**  
Create an inventory template in the Telecommunications Network Inventory application to represent a configuration of the created inventory model.
-   **[Create a default template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-default-templates.md)**  
Create a default template in the Telecommunications Network Inventory application to capture the default attribute definition for a specific configuration item \(CI\) class.
-   **[Define or update a naming pattern for a related template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/define-update-naming-pattern.md)**  
Define a JavaScript expression that names the configuration item \(CI\) you create from a related template within an inventory template. The naming pattern can include literal text, variables from the token library, conditionals, and string transformations.

**Parent Topic:**[Using Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/using-telecom-network-inventory.md)

**Related topics**  


[Network inventory templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/using-templates-tni.md)

