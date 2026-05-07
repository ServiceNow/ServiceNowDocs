---
title: Multiple configurations
description: As a product catalog manager, when you define a configurable product offering, you can enable agents to add multiple configurations of a child product offering. When agents add multiple configurations, they can change the quantity for each configuration of the offering, define each configuration as a separate line item, and select the appropriate options and characteristics for each configuration.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Multiple configurations

As a product catalog manager, when you define a configurable product offering, you can enable agents to add multiple configurations of a child product offering. When agents add multiple configurations, they can change the quantity for each configuration of the offering, define each configuration as a separate line item, and select the appropriate options and characteristics for each configuration.

## How multiple configurations work

When you use the Create New Product Offering form to define configurable product offerings and child product offerings, select the **Allow multiple configurations** option to enable the creation of multiple child offering configurations. For information on defining product offerings, see [Create product offerings](../task/som-create-product-offering.md).

**Note:** If the configurable product has an associated product specification, the **Allow multiple configurations** option is enabled automatically and can't be unselected.

When agents add configurable products to new opportunities, quotes, and orders, they can create multiple configurations for a child offering. They navigate to a summary page for a selected child offering. From this page, they can do the following:

-   Change the quantity of a child offering.
-   Clone a child offering.
-   Split a child offering that has a quantity greater than 1, to create child offering instances with different quantities.

Each offering instance becomes a new line item that can be configured separately.

In the following example, the Home Automation Bundle is a child offering that has a default quantity of 2 in the Quadplay Home Tech Bundle. An information icon displays next to each child offering that can have multiple configurations. The information icon, when selected, displays a message indicating that multiple configurations can be created for the child offering.

![Details tab that shows Home Automation Hub product offering with Allow multiple configurations option enabled and the Quadplay Home Tech Hub Bundle configurable product offering displayed in the product configurator](../image/om-multiple-config-instances.png "Example configurable product offering for an order")

## How multiple configurations are created

When agents review a bundle offering in the product configurator, they identify the child offerings that can have multiple configurations. They navigate to the summary page for the appropriate child offering to create multiple configurations.

In the offering summary page, a message indicates that the offering supports multiple configurations and the aggregated quantity of configurations that can be created. Agents can change the quantity of the child offering on this page.

The More options icon ![](../image/icon-three-dots.png) displays next to the **Quantity**. Selecting the icon lists the options available for creating and managing multiple configurations.

![Summary page for child offering, which shows the More options menu with the Clone and Split options for managing multiple configurations of a child product offering](../image/more-options-menu-multiconfig.png "Offering summary page with More options menu")

The following options are available to manage child offering configurations:

-   **Clone**: Create child offering configurations by copying the selected child product offering configuration. The agent is prompted to enter the number of clones to be made.

    For example, if the current child offering quantity is 2, and the agent specifies 2 copies, two identical copies of the child product offering are created. Each clone becomes a separate line item and has a quantity of 1.

-   **Split**: Create child offering configurations by splitting the current child offering quantity and distributing the quantity evenly across all the copies. The agent is prompted to enter the number of splits.

    For example, if the child offering quantity is 5, and an agent specifies 3 splits, two child offering instances are created. After the split, there are three child offering instances, where the instances have a quantity of 2, 2, and 1, respectively.

-   **Delete**: Removes the child offering instance. If deleting a child offering instance causes the number of child offers to fall below the minimum quantity defined for the product, the **Delete** option isn’t available.

When the child offering configurations are created, each offering name reflects the child product offering name followed by an incremental number. For example, Home Automation Hub configurations are named Home Automation Hub 2, Home Automation Hub 3, and so on. Agents can then select the appropriate offering instance to configure it. If the agent changes the **Quantity** value, the Current Selection pane reflects the new quantity and associated pricing.

## Validation during multiple configuration creation

As your agents create multiple configurations, the system uses the default, minimum, and maximum cardinality rules defined for the product offering to validate the configurations. If there are violations, the system displays the appropriate information and error messages in the product configurator UI.

The system also uses the cardinality rules to determine when certain configuration options \(**Split** and **Delete**\) should be enabled or turned off, based on the context. For example, if the minimum child offering quantity is 1 and a child offering has a quantity of 1, the system disables the **Delete** option in the More options menu.

## Limitations for multiple configurations

Multiple configurations aren’t supported for quotes of type sales agreements. Also, changes for quotes and orders with sold products or product inventory have the following limitations:

-   Sold products: When creating a modify order, the **Delete** option for multiple configurations is supported, but the **Clone** and **Split** options aren’t supported.
-   Product inventory: Multiple configurations are supported. The **Split** option isn’t supported.

## Setting up multiple configurations

For details on enabling and creating multiple configurations for child offerings, see the following sections:

-   [Create product offerings](../task/som-create-product-offering.md)
-   [Create multiple configurations](../task/create-multiple-child-configs.md)

