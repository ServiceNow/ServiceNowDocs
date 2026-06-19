---
title: Configuring product offerings and catalogs
description: Create product offerings and the associated product catalogs that can be used by Sales Customer Relationship Management agents for pre-sales activities, order capture, and post-sales engagement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-media-technology/telecommunications-media-and-technology-core/configuring-product-offerings-catalog.html
release: zurich
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 2
breadcrumb: [Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Configuring product offerings and catalogs

Create product offerings and the associated product catalogs that can be used by Sales Customer Relationship Management agents for pre-sales activities, order capture, and post-sales engagement.

As a product catalog administrator or catalog manager, you complete various configuration tasks to create the product catalogs and offerings for products and services sold by your organization. You also work with your pricing administrator, who sets the pricing for your product offerings. For more information on pricing, see .

## Overview of product offering and catalog configuration

You can use the CSM Configurable Workspace to configure product offering catalogs, product offerings, and product offering relationships.

The following table identifies the configuration tasks for setting up the various features available in Product Catalog Management.

|Configuration task|Description|
|------------------|-----------|
||Create a catalog, which is the top-level entity in the catalog hierarchy. Catalogs can have categories, and categories can have subcategories or product offers.|
||Define a product offering category used to organize similar product offerings in a catalog. Catalog categories make it easier for agents to browse and navigate product offerings when creating opportunities, quotes, and orders.|
||Define the specific attributes, properties, and options that distinguish a product offering, influencing its configuration and pricing.|
||Configure and add product offerings to catalogs and categories. Once published, product offerings are available to Sales Customer Relationship Management agents as they create opportunities, quotes, and orders.|
||Add images and thumbnails to your product offerings to help agents as they build opportunities, quotes, and orders.|
||Create product relationships to bundle products and services together to streamline the order process. Product offering relationships drive the order capture experience by letting you group multiple product offerings into bundles. Bundles also let you offer special bundle pricing.|
||Control how the quantities for child line items in a product offering for a quote or order are calculated by using the **sn\_prd\_pm.enable\_cascade\_quantity** system property.|
||Add related contracts to your product offerings in the Sales Customer Relationship Management application.|
||Add a unit of measure \(UOM\) to a product offering in Sales Customer Relationship Management.|
||Create a product version to add updates to a published product offering.|
||Combine bundles of product offerings into related groups in Sales Customer Relationship Management.|
|Configure needs analysis|Create needs templates, which are questionnaires from product selection guides that your agents use to determine what product offers can be added to opportunities.|
|Configure product offering recommendations for quotes|Create offer recommendations that sales agents can use to complement or supplement items in their quotes.|
|Export and import product catalog entities|Export and import product catalog entities between ServiceNow instances. For example, you can promote catalog entities from a non-production instance to a production instance.|
|View product offering hierarchy and associated specification hierarchy|View the complete hierarchy of a product offering and any associated specifications \(product, service, and resource\). Use these views to verify that all entities have been defined and associated correctly.|
|Configure product offer eligibility|Filter the product catalog, product categories, and product offerings dynamically, to display only eligible product offerings for a customer in the product catalog.|

