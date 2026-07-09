---
title: Set up Solution Configuration
description: Solution configuration lets ServiceNow CPQ admins link multiple blueprints into a single, connected configuration session so that end users can work across related products without relaunching the configurator. Configurable product actions trigger child configurations automatically and can pass data between blueprints via field mappings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/solution-configuration-setup.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [ServiceNow CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up Solution Configuration

Solution configuration lets ServiceNow CPQ admins link multiple blueprints into a single, connected configuration session so that end users can work across related products without relaunching the configurator. Configurable product actions trigger child configurations automatically and can pass data between blueprints via field mappings.

## Solution configuration overview

Solution configuration is an environment-level feature that links multiple blueprints into a parent-child hierarchy. When a configurable product action rule is triggered during a buyer's configuration session, a child configuration is created automatically. The buyer navigates between configurations using the solution navigation sidebar, and the full bill of materials rolls up across all configurations at the solution root.

Solution configuration is off by default. To enable solution configuration in your environment, contact ServiceNow CPQ Support by using the [ServiceNow Support portal](https://support.servicenow.com). For step-by-step instructions, see [Create a case on Now Support for CPQ Customers](https://support.servicenow.com/kb?sys_kb_id=d67d3e71475d7a90f64de825126d4326&id=kb_article_view).

## Key features of solution configuration

Solution configuration includes several key features that support multi-blueprint management:

-   **Field mapping**

    Field mapping defines which fields have data passed between blueprints. Field mapping happens on creation of a child configuration or when a mapped source field is changed. Fields are only mapped a single level — to continue the mapping, define the mapped fields on each blueprint. Fields can only be mapped to the same type of field \(text to text, number to number, and so on\). Entire sets and product pickers cannot be mapped.

-   **Node cloning**

    Node cloning lets you duplicate an existing, valid solution configuration node to use as the starting point for a new node. When you clone a node, both the fields and their values are copied, so end users don't have to re-enter configuration data for each new node from scratch. Cloned nodes are fully independent of the original — changes to a cloned node do not affect the source node, and vice versa. Cloning is available from the solution configuration in a set using the navigation sidebar. A node must be in a valid state before it can be cloned, which prevents incomplete configurations from being duplicated. When you clone a node that has a dependent set, a corresponding child node is created as part of the cloning operation.

-   **Layout**

    Each solution component displays its own layout from the layouts associated with the current blueprint. When in a solution, the header, background style, buttons, and product list display come from the solution root layout that is defined in the root blueprint. The solution navigation sidebar automatically appears when additional configurable products are added during a configuration.

-   **Bill of materials \(BOM\)**

    The bill of materials shows the items from the currently viewed configuration and any child configurations below. The entire solution BOM can be viewed at the solution root. The BOM hierarchy is still defined via the parent product and the unique identifier fields in product actions. It is independent of the solution hierarchy, and one does not necessarily reflect the other. A child configuration may add top-level items to the bill of materials.


## Get started

Use the following topics to understand, set up, and work with solution configuration.

-   **[Set up solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)**

    Learn what solution configuration is, how it benefits administrators and end users, and how the bill of materials, layouts, and field mapping work.

-   **[Solution configuration terms and considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/solution_configuration_overview.md)**

    Review key terminology, design limits, and field mapping rules before you start configuring.

-   **[Enable solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/enable-solution-configuration.md)**

    Request environment enablement from Support and verify that configurable product actions are available in the admin.

-   **[Create a configurable product action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-configurable-product-action.md)**

    Link a child blueprint to a parent blueprint so that a child configuration is created when the action's condition is met.

-   **[Define field mappings for a solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/define-field-mappings-sol-config.md)**

    Pass field values from the parent blueprint to the child blueprint when a child configuration is created.

-   **[Node cloning for solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/node-cloning-for-solution-configuration.md)**

    Duplicate an existing, valid configuration node in a set to use as the starting point for a new node, preserving its field values and child hierarchy.


## Potential errors with configurable product actions

Errors related to configurable product actions may include the following:

-   The configurable product is not found
-   The configurable product does not have a blueprint associated with it
-   The configurable product does not have a deployed blueprint
-   The blueprint does not exist
-   The blueprint is not deployed
-   The blueprint has changed

If you encounter any of these errors during configuration or testing, verify that your configurable products are properly associated with deployed blueprints before proceeding.

## Alternative approaches

Solution configuration is the recommended approach for linking multiple configurable products, but consider these alternatives based on your requirements:

-   Sets: Sets make it easy to handle large numbers of rows with potentially different configurations. They support cloning rows, while set repeater layout options provide visual similarity.
-   Product pickers: Product pickers work well with lightly configurable products and can be customized with additional fields and bulk actions.
-   Multiple independent configurations: Depending on the downstream system, making multiple independent configurations may provide more flexibility than a single solution configuration.

## End user experience

When end users interact with a solution configuration, they experience a seamless workflow:

-   Launching a solution: Users launch the configurable product they want to start from, just as they do normally. Whichever configurable product is launched becomes the root product for the solution.
-   Adding configurable products: When any of the defined rules that have a configurable product action are triggered, a new child configuration is created if a valid configurable product with a deployed blueprint is found.
-   Solution navigation: When additional configurable products are added to the configuration, solution navigation becomes available and shows a list of the current configurable products, including the root configurable product.
-   Managing the solution: Changing the condition of a configurable product action rule to false removes the configuration and configurable product, just as in a normal product action. This also removes changes to fields, products, nested children, or other items.
-   Viewing the bill of materials: When a configuration becomes a solution, the default product list component is hidden and replaced by the **View Full Solution** button in all configurations. In a solution, **View Full Solution** displays the entire solution BOM. Additional product lists added as tiers reflect only the currently selected configurable product and any child configurations below it.

**Related topics**  


[Node cloning for solution configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/node-cloning-for-solution-configuration.md)

