---
title: Create sourcing checkout record
description: Create a custom checkout to use for sourcing requests for a specific product, product model, or product category.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Sourcing checkout, Setting up primary data Shopping, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create sourcing checkout record

Create a custom checkout to use for sourcing requests for a specific product, product model, or product category.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## About this task

Utilize record producers to create a custom set of questions to ask Shoppers during checkout while initiating a sourcing request.

-   You can use a sourcing checkout for all the goods or services using the default checkout from ShoppingHub Configuration.
-   You can use a sourcing checkout for a specific supplier product, or a product model, or a product category from the **Sourcing and Purchasing Automation** tab on each record.

## Procedure

1.  Navigate to a supplier product, a product model, or a category section.

    For supplier model, **All** &gt; **Sourcing and Purchasing Automation** &gt; **Primary Data** &gt; **Supplier Product** &gt; **Create new sourcing checkout**.

    Catalog builder opens.

2.  Select **Details** to update basic information about the record producer such as the name and description.

3.  On the form, fill in the fields.

4.  Select the **Destination** tab and fill in the fields.

5.  Select the **Location** tab and select a catalog and category where requesters can find the item.

    Fill in the fields or use the available information.

6.  Select the **Questions** tab and create custom or select from the preconfigured questions.

    The following questions are available in the default sourcing checkouts.

    |Question set|Description|
    |------------|-----------|
    |**ShoppingHub: Product &amp; Other data for Checkout**|Collects data about the product that is sourced from the Shopping Hub product details page. Includes multiple variables that map to the cart line and purchase line. This is included in every Shopping Hub checkout which cannot be removed when using the catalog builder template.|
    |**ShoppingHub Checkout Delivery Date for Goods Selector**|Select a delivery date or create a blanket PR for a good. Includes multiple variables that map to the cart line and purchase line.|
    |**ShoppingHub Checkout Delivery Date for Services Selector**|Select a start date and end date or create a blanket PR for a service. Includes multiple variables that map to the cart line and purchase line.|
    |**ShoppingHub Delivery Location Selector**|Select an office location or add a new location for a product or service to be delivered to. Includes multiple variables that map to the cart line and purchase line.|
    |**ShoppingHub More Info Request**|Provide additional info while sourcing a product. Maps to the sourcing request details field in the cart line and sourcing.|
    |**ShoppingHub Other Request**|Provide details about “something else” when sourcing a product. Maps to the sourcing request details field in the cart line and sourcing request.|
    |**ShoppingHub Purchase Reason**|Provide a reason for purchase. Maps to the purchase reason field in the cart line and sourcing request.|
    |**ShoppingHub Sourcing Intent**|Select whether they want to receive a quote, a POC, more info, or something else about a good or service being sourced. Maps to the request type field in the cart line and sourcing request.|
    |**ShoppingHub: Good Delivery Date \(only\)**|Select a delivery date for a good. Maps to the estimated delivery date field in the purchase line.|
    |**ShoppingHub: Service End Date \(only\)**|Select an end date to a service. Maps to the end date field in the purchase line.|
    |**ShoppingHub: Service State Date \(only\)**|Select a start date to a service. Maps to the start date field in the purchase line.|

7.  Select the **Settings** tab and fill in the fields.

8.  Select **Review and Submit**.


**Parent Topic:**[Sourcing checkout](../concept/sourcing-checkout.md)

**Related topics**  


[Configure sourcing checkout](configure-sourcing-checkout.md)

[bundle-platcap.c_RecordProducer]

[bundle-platcap.t_DefRecProdInSCat]

