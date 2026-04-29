---
title: Set up blueprints
description: Blueprints define the structure of a configuration experience in CPQ. They act as containers that bring together fields, rules, layouts, and configurable products, enabling administrators to design, deploy, and manage complete configuration workflows across environments.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Set up blueprints

Blueprints define the structure of a configuration experience in CPQ. They act as containers that bring together fields, rules, layouts, and configurable products, enabling administrators to design, deploy, and manage complete configuration workflows across environments.

The blueprint defines the configuration experience. It acts as a container for all the parts necessary to be plugged in for the end- user interface. Because CPQ rules and fields are global, they can be used to facilitate any number of configuration experiences. The blueprint record allows the administrator to associate the subset of the fields and rules that are relevant to the configuration experience it represents. Further, the blueprint defines layouts and configurable products.

Unlike fields and rules, layouts can only be associated with one blueprint. A layout is defined and built in the context of, and to explicitly support, one blueprint — one configuration experience. However, a blueprint may have multiple layouts.

For Salesforce-integrated organizations, the configurable product element determines the SFDC Product2 record that, when quoted in Salesforce, launches the configuration experience defined by a blueprint. Multiple configurable products can launch the same blueprint. However, each configurable product can only be associated with one blueprint.

For a step-by-step guide to creating a blueprint, see [Create a new blueprint](cpq-create-a-new-blueprint.md).

## The blueprint definition page

The blueprint definition page holds all of the different elements that are associated with the blueprint. Each tab indicates the number of elements associated if relevant. Clicking each shows specific metadata and lets you search by name or variable name, or edit each element in the blueprint.

## The Associated Fields tab

This tab shows all of the fields that have been associated with the blueprint. The name, type, variable name, description, and last modified date of the fields are shown to the admin on this page, as well as the username of the user that last modified the field. You can also drill down to specific field types associated to the blueprint, such as sets, product pickers, and system fields.

![Associated fields](../images/cpq-blueprints-associate-fields.png)

-   Standard: Shows global fields associated with the blueprint.
-   Sets: Shows the sets and set subfields associated with the blueprint. Once a set is associated, each subfield added is automatically associated with the blueprint.
-   Product Pickers: Shows the product pickers and product picker subfields associated with the blueprint.
-   System: Automatically associated with each blueprint. If integrated with Salesforce, these fields pull data automatically upon initialization without the need to specify it in an external connection.

To learn more about fields and how to associate them with blueprints, see [Configure fields](fields_101.md).

## The Related Rules tab

This tab shows all of the rules that are related to the blueprint. Unlike fields, rules connect to a blueprint automatically as long as every field referenced by the rule is associated with the blueprint. The name, variable name, description, action types, and last modified date of the rules are shown to the admin on this page, as well as the username of the user that last modified the rule.

![Related rules](../images/cpq-blueprints-related-rules.png)

Active: Shows what rules are currently set to active in their definition. When a rule is active, it is included as a valid rule during deployment and enacts its Actions when its Conditions are fulfilled during runtime.

Inactive: Shows what rules are currently set to inactive in their definition. They are still related to the blueprint and is included if the blueprint is exported, but they are not valid when deployed and do not enact their actions during runtime.

## Layout

This tab hows all of the layouts that have been created for the blueprint. The most recently modified layout is the layout generated unless otherwise specified. The name, variable name, last modified date, and the username of the user that last modified the layout are located on this page.

![Layout screen](../images/cpq-blueprints-layout.png)

## The Configurable Product tab

This tab shows the configurable products that are linked to the blueprint. Calling a runtime API with any of the associated configurable products with the blueprint, or configuring from the product through a third-party such as Salesforce, immediately launches the blueprint. The name and product ID are present, and an admin can delete a product by clicking the Trash icon on the left.

![Configurable product](../images/cpq-blueprints-configurable-product.png)

## The Deployments tab

This tab shows the fifty most recent deployments for the blueprint. The blueprint name, variable name, and last deployment date and time are visible here, along with the username of the user that last deployed the blueprint.

![Deployments](../images/cpq-blueprints-deployments.png)

You can also see a list of the environment’s most recent deployments in the Utilities menu on the Deployment page. See [Viewing blueprint deployments](deployments_page.md).

## The Enrichments tab

This tab shows the enrichment scripts that have been created for the blueprint. These scripts run outside of the rules engine and enact their functions on their own areas, such as on initialization, BOM response, validation, or picklist extension pricing. An admin can edit these scripts or delete them using the Trash icon on the far left. For more information about enrichment scripts, see [Using external connections with OAuth support](using-external-connections-with-oauth-support.md).

![Enrichments screen](../images/cpq-blueprints-enrichments.png)

## Deploying a blueprint

CPQ configuration experiences are deployed \(made available to application end users\) at the blueprint level. Administrator edits to fields, rules, layouts, and configurable products are not visible to the end user until deployed.

To deploy a blueprint, in the Blueprints list administration page, check the box to the left of the blueprint to deploy, and then click **Deploy**. \(You can also click **Deploy** in the blueprint itself.\)

![Deployment screen](../images/cpq-blueprints-deploy.png)

The blueprint administration list page shows the deployment status of each blueprint. Icon key:

![Deployed icon](../images/cpq-blueprints-icon-deployed.png) Deployed

![Not deployed icon](../images/cpq-blueprints-icon-expiring-soon.png) Not deployed

![Expiring Soon icon](../images/cpq-blueprints-icon-not-deployed.png) Expiring Soon

In production sector environments provided to CPQ customers, once a blueprint is deployed, it remains deployed, no matter its end-user activity.

In test sector environments provided to CPQ partners, blueprints are automatically un-deployed after a period of thirty days with no end-user engagement. Redeploying the blueprint or launching a configuration of the blueprint resets the thirty-day period after ServiceNow's database syncs each evening.

In demo sector environments, blueprints are automatically un-deployed every weekend.

After a blueprint is deployed, a notification alerts you to the status of the deployment process \(either In Progress or Completed\).

![Deployments](../images/cpq-blueprints-notifications.png)

**Related topics**  


[Create a new blueprint](cpq-create-a-new-blueprint.md)

[Testing in non-production environments before migration](cpq-env-to-env-bp-migration-intro.md)

[CPQ fields, system fields, and partner fields](system_fields_vs_partner_fields.md)

[Configure fields](fields_101.md)

[Boundaries and limits](boundaries-and-limits.md)

