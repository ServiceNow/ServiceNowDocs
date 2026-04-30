---
title: Sales and Order Management workflows
description: Create the Sales and Order management workflows for a product and service through entity configurations and mappings. By creating this workflow, your organization can analyze lucrative business opportunities, customer leads, and the billing, support, and maintenance requirements after a sale is complete.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-02-01"
reading_time_minutes: 2
breadcrumb: [Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Sales and Order Management workflows

Create the Sales and Order management workflows for a product and service through entity configurations and mappings. By creating this workflow, your organization can analyze lucrative business opportunities, customer leads, and the billing, support, and maintenance requirements after a sale is complete.

## Workflows overview

A product goes through multiple phases and workflows from the time that a product is identified to the time that it’s purchased by the customer. The workflow includes the creation of a quote for a product or services, the creation of orders, the sold products, the install base items, and the contracts and entitlements.

If you're an administrator, you create the workflows for your organization and configure the metadata for your various lead-to-cash entities by activating the foundational Lead to Cash Core \(com.snc.l2c\_core\) application. With the Lead to Cash Core \(com.snc.l2c\_core\) plugin, you can compose and build the workflows that your organization maintains for the life cycle of a sold product. You can select multiple source objects for a single target entity to compose various workflows. For example, on the Lead to Cash Entities Mapping form on the ServiceNow AI Platform®, you select the sold product entity as a source entity and the order as a target entity. You then map these entities and configurations to create a source to the target flow that is a sold product to order flow. This mapping provides your users with a unified workflow experience across the different entities. With multi-selection, you can also select multiple opportunity lines to create a quote.

**Note:** An entity is defined as a collection of tables that have information about an order. The information can come from multiple tables.

## Entity configurations

You can configure the definition of a lead-to-cash entity by defining a name and configuration ID on the Lead to Cash Entity form. The definition creates a back and forth flow of the information between the various entities.

To learn how to create entity configurations, see [Create an entity configuration](../task/create-entity-configuration.md). To learn how to create entity mappings, see [Create an entity mapping](../task/create-entity-mapping.md).

## Reconfiguration

You can reconfigure an order or a quote that is in the **Draft** state to make customizations in the Configurator UI. After the configuration is complete, all the order line items associated with the order are also updated. To learn more about reconfiguration, see [LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

