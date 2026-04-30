---
title: Configure product data
description: Configure product data including product models, sold products, install base items and installed products.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configure product data

Configure product data including product models, sold products, install base items and installed products.

## Before you begin

Role required: admin

## About this task

-   **Product models:** A product is a type of good or service that your company sells and supports. Product models identify different types of products, such as service, hardware, software, or consumables.

    **Note:** Product models require the Model Management plugin \(com.snc.model\).

-   **Sold products:** The products and components that have been sold to an account or a consumer.
-   **Install base items:** Items that represent the instances that have been installed or provisioned for a customer.
-   **Installed products:** Provide information on the sold products and how they are deployed or installed. Use installed products to create an association between sold products and install base items.

## Procedure

-   You can import the following product data using guided setup.

    -   [Import product models with guided setup](import-csm-product-models.md)
    -   [Import sold products with guided setup](import-csm-sold-products.md)
    -   [Import install base items with guided setup](import-csm-install-base-items.md)
    -   [Import installed products with guided setup](import-csm-installed-products.md)
-   You can create new product data using the Customer Service Management application.

    -   [Create a product model](c_CreateAProductModel.md)
    -   [Create sold products](create-sold-item.md)
    -   [Create install base items](create-install-base-item.md)
    -   [Create installed products](create-deployed-sold-item.md)
-   You can configure the following relationships and associations after importing or creating product data:

    -   Product models
        -   [Associate service offerings to product models](associate-service-offering-product.md)
        -   [Configure product model and catalog item relationships](create-csm-product-model-items.md)
    -   Sold products
        -   [Associate service offerings with sold products](asssociate-service-offering-sold-prod.md)
        -   [Associate sold products with contracts](add-sold-product-contract.md)

