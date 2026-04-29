---
title: Solution configuration setup
description: Solution configuration lets CPQ admins manage multiple blueprints in a single configuration. Configurable product actions include a blueprint definition and can pass data between configurations via defined fields.It's not clear to me how solution configuration and configurable product actions are related. This topic seems to concern the latter, despite the title.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Solution configuration setup

Solution configuration lets CPQ admins manage multiple blueprints in a single configuration. Configurable product actions include a blueprint definition and can pass data between configurations via defined fields.

Solution configuration is an environment level feature that is off by default. To have it enabled in an environment, log a case with CPQ Support.

Configurable product actions are a new type of product action that can be added to rules. They are similar to standard product actions, but have a blueprint defined and can include field mapping to pass data between configurations. Advanced configurable product actions require that the product ID and the blueprint fields are defined outside of the script.

## Benefits

-   For administrators:
    -   Independent deployment: Each blueprint can be deployed independently, which allows for finer granularity when making changes or updates to a blueprint.
    -   Separation of concerns: Administrators can segment out logical components from a configuration and allow different groups to work on blueprints without conflicting.
    -   Blueprint reusability: Blueprints can be reused both as part of a solution, multiple solutions, or as an independently configurable product. This leads to less duplication when a blueprint is needed for multiple contexts and less overhead for maintenance.
-   For end users:
    -   End users can seamlessly work through multiple configurations without needing to re-launch CPQ each time.
    -   You can clone the child configuration if it is a set-based configuration. The original node in a set must be in the valid state. Cloned nodes are independent of the original edits to a cloned node do not affect the source node.
    -   You can also add a blank node or remove node from the navigation sidebar.

## The end user experience

-   Launching a solution: Users launch the configurable product that they want to start from, just as they do normally. Whichever configurable product is launched becomes the root product for the solution.
-   Adding configurable products: When any of the defined rules that have a configurable product action are triggered, a new child configuration is created if a valid configurable product with a deployed blueprint is found.
-   When additional configurable products are added to the configuration, solution navigation becomes available and shows a list of the current configurable products, including the root configurable product.
-   Changing the condition of a configurable product action rule to false removes the configuration and configurable product, just as in a normal product action. This also removes changes to fields, products, nested children, or other items.
-   Viewing the bill of materials: When a configuration becomes a solution, the default product list component is hidden and replaced by the **View Full Solution** button in all configurations. In a solution, **View Full Solution** displays the entire solution BOM. Additional product lists added as tiers reflect only the currently selected configurable product and any of the child configurations below it.

## Potential errors with configurable product actions

Errors related to configurable product actions may include the following:

-   The configurable product is not found
-   The configurable product does not have a blueprint associated with it
-   The configurable product does not have a deployed blueprint
-   The blueprint does not exist
-   The blueprint is not deployed
-   The blueprint has changed

## Field mapping

Field mapping defines which fields have data passed to or from them. Field mapping happens on creation of a child configuration or when a mapped source field is changed. Fields are only mapped a single level, to continue the mapping define the mapped fields on each blueprint. Fields can only be mapped to the same type of field: text to text, number to number, and so on.

Entire sets and product pickers cannot be mapped.

## Node cloning for solution configurations

Node cloning lets you duplicate an existing, valid solution configuration node to use as the starting point for a new node. When you clone a node, both the fields and their values are copied — so you don't have to re-enter configuration data for each new node from scratch.

Cloned nodes are fully independent of the original. Changes you make to a cloned node don't affect the source node, and changes to the source node don't affect the clone.

Cloning is available from the solution configuration in a set using the navigation sidebar. A node must be in a valid state before you can clone it — this prevents incomplete configurations from being duplicated. When you clone a node that has a dependent set, a corresponding child node is created as part of the cloning operation.

## Layout

Each solution component displays its own layout from the layouts associated with the current blueprint.

When in a solution, the header, background style, buttons and product list display comes from the solution root layout that is defined in the root blueprint.

The solution navigation sidebar automatically appears when additional configurable products are added during a configuration.

## Bill of materials \(BOM\)

The bill of materials shows the items from the currently viewed configuration and any child configurations below. The entire solution BOM can be viewed at the solution root.

The BOM hierarchy is still defined via the parent product and the unique identifier fields in product actions. It is independent of the solution hierarchy, and one does not necessarily reflect the other. A child configuration may add top level items to the bill of materials.

## Other options

-   Sets make it easy to handle large numbers of rows with potentially different configurations. They support cloning rows, while set repeater layout options provide visual similarity.
-   Product pickers work well with lightly configurable products and can be customized with additional fields and bulk actions.
-   Depending on the downstream system, making multiple independent configurations may provide more flexibility than a single solution configuration.

**Related topics**  


[Node cloning for solution configuration](node-cloning-for-solution-configuration.md)

