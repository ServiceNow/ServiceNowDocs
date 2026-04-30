---
title: Configure purchase requisition line-level questions in ShoppingHub
description: As a procurement administrator, you can create configurable, line-level questions for shoppers to provide the information needed to complete the purchase during the checkout process in Shopping Hub. These questions are defined in Catalog Builder and specific to certain products or product categories.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Complete your checkout, Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure purchase requisition line-level questions in ShoppingHub

As a procurement administrator, you can create configurable, line-level questions for shoppers to provide the information needed to complete the purchase during the checkout process in Shopping Hub. These questions are defined in Catalog Builder and specific to certain products or product categories.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## About this task

Plugin required: Shopping Hub \(sn\_spend\_uib\)

Use a record producer to create a custom set of questions to ask shoppers during the quick and full checkout for specific products or product categories. Build this record producer in Catalog Builder using the **ShoppingHub: Additional information on supplier products or product models or product categories** template. For information on how to create a record producer, see [Create a catalog item using a template](https://www.servicenow.com/docs/access?context=create-item-cat-builder&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

![ShoppingHub additional information for supplier product.](../image/sh-addl-catalog.png)

Shopping Hub checks for the existence of the record producer used for the additional information configuration in the specified order:

-   Supplier product
-   Product model
-   Product category
-   Parent category

## Procedure

1.  Navigate to Supplier Products, Product Models, or Model Categories.

2.  Select and open a record for a supplier product, product model, or a model category.

3.  In the Related Links section, select **Add additional information**.

    ![Add additional information option in Related Links.](../image/sh-addl-info.png)

    The Create record producer page opens in Catalog Builder.

4.  In Catalog Builder, configure a record producer using the **ShoppingHub: Additional information on supplier products or product models or product categories** template.

    This record producer is used to store additional information from a shopper specific to a purchase.

    **Note:** For information on how to create a record producer, see [Create a catalog item using a template](https://www.servicenow.com/docs/access?context=create-item-cat-builder&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

5.  Navigate to **ShoppingHub** &gt; **Administration** &gt; **ShoppingHub Configuration**.

    ![ShoppingHub Configuration page showing the Content details tab and Record producer field.](../image/sh-addl-questions-record.png)

6.  In the **Name** field, enter a name for the configuration.

7.  In the **Configuration type** field, select the **Additional Information**.

8.  In the **Content details** tab, do one or more of the following as needed.

    -   In the **Supplier product** field, search for and add a supplier product that you want to display additional information at checkout.
    -   In the **Product model** field, search for and add a product model that you want to display additional information at checkout.
    -   In the **Product category** field, search for and add a product category that you want to display additional information at checkout.
    **Note:** Shopping Hub checks for the existence of the record producer used for the additional information configuration in the specified order:

    -   Supplier product
    -   Product model
    -   Product category
    -   Parent category
9.  In the **Record producer** field, search for and select the record producer you created.

    You must first create this record producer using the **ShoppingHub: Additional information on supplier products or product models or product categories** template.

10. Select **Submit**.

    The questions added in the record producer for a specific product, product model, or product category appear during checkout in Shopping Hub.


**Parent Topic:**[Complete your checkout](complete-your-checkout.md)

