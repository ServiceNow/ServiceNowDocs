---
title: CPQ Configurator release notes
description: The ServiceNow CPQ Configurator interface streamlines the configuration and pricing of customizable products that are added to opportunities, quotes, and orders. It also supports product configuration when modifying sold products and contracts. CPQ Configurator is a new feature in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-02"
reading_time_minutes: 2
---

# CPQ Configurator release notes

The ServiceNow® CPQ Configurator interface streamlines the configuration and pricing of customizable products that are added to opportunities, quotes, and orders. It also supports product configuration when modifying sold products and contracts. CPQ Configurator is a new feature in the Zurich release.

## CPQ Configurator highlights for the Zurich release

-   Provides sales agents and customers with an intuitive interface for attribute-based configuration in addition to product-based configuration of customizable products.
-   Enables agents and customers to select valid product options during product configuration and view real-time updates that show how their selections affect associated pricing.
-   Enables product catalog admins to generate and update product offering blueprints that guide the accurate configuration of customizable products by agents and customers.

See [CPQ Configurator](https://www.servicenow.com/docs/access?context=explore-servicenowcpq&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

**Important:** CPQ Integration is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important upgrade information for CPQ Configurator

If you used the legacy product configurator previously and want to use the CPQ Configurator, after upgrading, you must set the **sn\_prd\_pm.enable\_advanced\_configuration** system property to true to be able to use the configurator in Sales Customer Relationship Management workflows.

.

## CPQ Configurator features

-   **[Configurable product offerings and associated blueprints](https://www.servicenow.com/docs/access?context=som-create-configurable-prod-offerings&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Create configurable products and generate the associated product offering blueprints that contain the product attributes, product relationships, product and pricing rules, and child products defined for configurable products. The blueprints also contain configuration rules for inclusion, exclusion, and determination. Catalog admins can review and update an offering blueprint in the CPQ Configurator and then publish the product offering to the product catalog.

-   **[CPQ Configurator interface](https://www.servicenow.com/docs/access?context=using-servicenowcpq&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Enable agents and customers to configure customizable products using the CPQ Configurator embedded in Sales Customer Relationship Management workflows. The configurator is used in both the CSM Configurable Workspace and the Business Portal.


## Activation information

Install the CPQ Configurator by requesting the CPQ Integration application from the ServiceNow Store. Visit the ServiceNow Store website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

Before implementing CPQ Configurator, you must prepare your environment to use it. For more information, see [Configuring CPQ Configurator](https://www.servicenow.com/docs/access?context=configuring-servicenow-cpq&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

