---
title: Solution configuration terms and considerations
description: Understand terminology, design considerations, and limits associated with solution configuration, which lets CPQ admins manage multiple blueprints in a single configuration.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Solution configuration setup, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Solution configuration terms and considerations

Understand terminology, design considerations, and limits associated with solution configuration, which lets CPQ admins manage multiple blueprints in a single configuration.

Solution configuration gives CPQ admins the ability to create and manage multiple blueprints that can work together in the end user side to provide a seamless configuration experience. For users familiar with other vendors, this is conceptually similar to “system configuration” and “nested bundles".

## Terminology

-   **Solution**

    The overall collection of blueprints \(configurations\) that are linked together. On the buyside, a configuration becomes a solution when at least one child configuration is added from a configurable product action.

-   **Solution root**

    The topmost configurable product in a solution has one or more child configurations. This is the configurable product and blueprint that is started from \(launched from eCommerce, CPQ, or other sources\) on the buyside.

-   **Parent \(Source\) blueprint**

    A blueprint that includes a rule with a configurable product action for another blueprint, hierarchically has at least one child blueprint, and may have parent blueprints itself.

-   **Child \(Target\) blueprint**

    A blueprint that is used to create a child configuration, hierarchically has at least one parent, and may have children itself, if defined in rules. It must have a valid configurable product associated with it to be used.

-   **Configurable product action**

    An extension of the product action that defines the child blueprint, configurable product, and \(optionally\) field mappings.

-   **Field Mapping**

    A field that has the data be mapped between blueprints. Part of the configurable product action.

-   **Source field**

    The field on the parent blueprint that is used for the value in a field mapping.

-   **Target field**

    The field on the child blueprint that has its value set from the field mapping.

-   **Solution hierarchy**

    The relationship between configurable products \(solution components\) in a solution configuration. This does not determine how products appear in the BOM.

-   **Solution BOM**

    The bill of materials as a rollup across all the configurations. This contains all the products that have been added across the solution, including children, grandchildren, and so on. The solution bill of materials is what is returned upon saving a solution.


## Design considerations and limits

Solution configuration is still under active development.

-   Field mapping:
    -   Data can flow only from parent to child configurations.
    -   Field values are only mapped down a single level at a time, such as parent to child, or child to grandchild.
    -   Fields can only be mapped to the same type of field, such as picklist to picklist. You cannot map picklist to text, or perform other type conversions in the mapping.
    -   Only number, text, Boolean, and picklist fields can be mapped.
        -   Mapping of an entire Set or entire product picker is not supported.
        -   Product picker subfields cannot be mapped to a field on the child.
        -   Fields that are in a set can be mapped to a field on the child.
    -   Any target fields are read only during configuration. The value is set to the same value of the source field.
    -   A system field can be used as a source field, but cannot be set as a target field.
    -   System fields always reflect the values of the source configuration that started the configuration.
-   Layout and solution navigation:
    -   Navigation in a solution is done using the Solution Navigation sidebar. No additional component or work needs to be done on a layout.
    -   Solution navigation: Users can also navigate to configurations by clicking the configurable product in the solution BOM.
    -   The header and header actions in the layout of the solution root are used across all configurations in a solution. This includes things like currency display settings and any custom branding.
        -   Save \(Quote\) and Cancel actions in the header are not scoped to the currently viewed blueprint. They apply to the whole solution.
        -   Reset, Validate \(if a validation enrichment exists on the blueprint\), and Change Layout apply to the currently viewed blueprint.
-   Configurable product actions:
    -   Configurable product actions are limited to adding only a single configurable product per product action. If multiple configurable products are needed, use multiple product actions in a rule.
    -   Once a product action has been marked as configurable, it cannot be changed back to a simple product action.
    -   Configurable product actions are supported in simple and advanced product actions.

        Advanced functions still have the product ID and the blueprint set outside of the advanced script.

    -   Configurable product actions triggering conditions are placed in a set and create multiple configurations.
-   Limits
    -   The solution hierarchy supports a maximum depth of 4 \(including the root product\). The bill of materials can have an arbitrary depth to the hierarchy.
    -   The total number of configurations in a single solution configuration session is 20: the solution root, plus up to 19 active children across all depths.
    -   No circular references are allowed in the solution hierarchy. For example, when BP1&gt;BP2, BP2 cannot create another configuration of BP1.
-   Product list and bill of materials:
    -   Bill of material: BOM hierarchy is still controlled via the **parentProduct** and **uniqueIdentifier** properties in the product action. Therefore, different configurations in a solution can add products at other levels in the BOM hierarchy.
    -   When using the **parentProduct** and **uniqueIdentifier** attributes for product hierarchy, if two child products have the same parent product and product ID but should both be displayed as separate in the BOM, each requires a unique identifier. This ensures that the UI treats them as unique products when listing them.
    -   Product list: When a configuration becomes a solution, the default product list in the layout goes away and is replaced by a **View Full Solution** button at the bottom of the Solution Navigation sidebar.
        -   This behavior can be customized in the default product list component of the solution root, in the Solution Settings section.
        -   Columns displayed in the solution BOM follow the settings in the default product list of the solution root.
        -   To display an additional product list, add it in a tier in the layout of the blueprint. This product list is scoped to that configuration and any child configurations.

