---
title: Create configurable product offerings and associated blueprints
description: Create a configurable product offering and generate an associated blueprint using the CPQ Configurator. A blueprint contains the product structure and includes product attributes, product relationships, product and pricing rules, and any child products for the offering. Blueprints drive the agent and customer experience for configuring customizable products with the CPQ Configurator.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-10-02"
reading_time_minutes: 3
breadcrumb: [Create product offerings, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Create configurable product offerings and associated blueprints

Create a configurable product offering and generate an associated blueprint using the CPQ Configurator. A blueprint contains the product structure and includes product attributes, product relationships, product and pricing rules, and any child products for the offering. Blueprints drive the agent and customer experience for configuring customizable products with the CPQ Configurator.

## Before you begin

Role required: sn\_prd\_pm\_product\_catalog\_admin

## About this task

A configurable product offering, also called a complex product offering, has multiple characteristics and one or more product relationships. The process of creating a configurable product offering involves defining the product in Product Catalog Management, then generating the blueprint. The blueprint is used in the CPQ Configurator to manage the product configuration experience for agents and customers.

## Procedure

1.  Create the configurable product offering.

    1.  In the CSM Configurable Workspace, select the **List** ![image.Lists] view.

    2.  Create an offering or copy an existing offering to make a new offering.

        -   To create an offering, navigate to **Offerings** &gt; **Product Offerings** and select **New**.
        -   To copy an offering, navigate to **Offerings** &gt; **Product Offerings**, select the offering to be copied, and select **Copy**.
    3.  In the Details tab, fill in the fields to create a configurable product or modify the copy to create a product.

        **Note:** For details on creating a product offering, see [Create product offerings](som-create-product-offering.md). To identify the offering as a configurable product, select the **Configurable** option in the form, even if there are no characteristics or relationships defined. Selecting the **Configurable** option indicates that the product offering is to be configured using the CPQ Configurator.

    4.  Select **Save**.

        The **Create Configuration** button is displayed. The Record Information pane shows the synchronization state as **Sync Not Initiated**.

2.  Start the synchronization process by selecting **Create Configuration**.

    The synchronization process begins, as indicated by the synchronization state **Sync initiated**. The synchronization process creates the blueprint for the offering. If you previously defined attributes, product relationships and groups, and other product or pricing rules for the offering, that information is included in the blueprint.

    When the synchronization completes, the status changes to **Sync success**. The Configuration Setup tab \(related list\) displays the blueprint. The **Update configuration** and **Publish** buttons are also displayed.

    **Note:** If the synchronization fails, use the Configuration Errors tab \(related list\) to view the errors in the synchronization process.

    The product blueprint has the following features:

    |Blueprint feature|Description|
    |-----------------|-----------|
    |Associated Fields|Attributes and attribute types.|
    |Related Rules|Product and pricing rules.|
    |Layouts|Arrangement of the elements displayed in the configurator interface. A default layout is applied during synchronization, but you can change the layout.|
    |Configurable Products|Child products of the offering.|
    |Enrichments|Scripts used by the rules engine to retrieve external data such as pricing or product data.|

    For more information on blueprints and how you can use them, see the online help accessible from the interface.

    **Note:** If you defined rules and attributes in Product Catalog Management, those rules and attributes must be updated in Product Catalog Management and not in the blueprint. However, you can add new rules and fields using the blueprint.

3.  If you want to make further changes to the product offering, and the offering is still in Draft state, select **Update configuration** and change the offering details.

4.  When you're ready to publish the offering, select Publish.

    Another synchronization occurs, and the product offering is published to the product catalog.


