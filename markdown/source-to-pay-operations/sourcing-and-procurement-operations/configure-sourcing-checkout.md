---
title: Configure sourcing checkout
description: As an administrator, you can configure the sourcing checkout to collect information that is relevant to a specific product, product model, or product category. You can also change the default sourcing checkout used universally. The additional information at the sourcing checkout helps understand the requirement better and enable quicker processing.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Sourcing checkout, Setting up primary data Shopping, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure sourcing checkout

As an administrator, you can configure the sourcing checkout to collect information that is relevant to a specific product, product model, or product category. You can also change the default sourcing checkout used universally. The additional information at the sourcing checkout helps understand the requirement better and enable quicker processing.

## Before you begin

Role required: sn\_shop.shopping\_hub\_admin

Configure sourcing checkouts in Shopping Hub to change all sourcing requests for a product or service throughout the system. Or you can configure for specific products and categories.

To configure a sourcing checkout for a product or service, you must first create the sourcing checkout from the purchasing automation tab of product, product model, or category. Simply select **Create new sourcing checkout**, for more information, see [Create sourcing checkout record](create-sourcing-checkout-record.md).

-   **Supplier Product**: Create or change the sourcing checkout for a specific product from a specific supplier. For example, MacBook Pros 15 inch sold by a specific supplier, for example, Apple.
-   **Product Model**: Create or change the sourcing checkout for a product model. For example, MacBook Pros 15 inch sold by any supplier.
-   **Product Categories**: Create or change the sourcing checkout for a product category. For example, Laptops.
-   **Default Sourcing Checkout**: Change the sourcing checkout for all sourcing requests of goods or services in ShoppingHub Configuration. From **Catalog builder**, edit the default checkout and submit.

    **Note:** Values defined at the supplier product take priority over the values defined at other levels.


## About this task

Configure the relevant questions in this manner.

## Procedure

1.  Select a sourcing checkout to use in one of the following locations:

    -   **Supplier Product**: Navigate to **Sourcing and Purchasing Automation** &gt; **Primary Data** &gt; **Supplier Product**.
    -   **Product Model**: Configure the details from **ShoppingHub** &gt; **Model Management** &gt; **All Models**.
    -   **Product Category** Configure the details from **ShoppingHub** &gt; **Category Management** &gt; **Product Categories**.
2.  From the **Purchasing automation** tab, select the **Sourcing checkout** field.

3.  Select one from the available list and select **Save**.

    The questions are now configured. When you leave the field blank, the default sourcing checkout questions appear at the time of checkout. When you have multiple sourcing checkouts defined, the following priority is applicable:

    -   Values defined at the supplier product take precedence over the values defined at the model or product level.
    -   Values defined at the product model take precedence over the product category.
    -   Values defined at the product category take precedence over default.
    **Note:** If you do not configure the sourcing checkout value, the default sourcing checkout is applicable.

    Once you select sourcing checkout, shoppers can view, select, and provide relevant information associated with the procurement of the product or service.


**Parent Topic:**[Sourcing checkout](../concept/sourcing-checkout.md)

**Related topics**  


[Record Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_RecordProducer.md)

[Create a record producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/t_DefRecProdInSCat.md)

[Create sourcing checkout record](create-sourcing-checkout-record.md)

