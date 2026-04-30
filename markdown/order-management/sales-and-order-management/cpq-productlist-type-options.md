---
title: ProductList.Type options: Accessory and Component
description: Define quantity behavior in product hierarchies. The Accessory type keeps quantity constant; The Component type multiplies it by the parent.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-09-16"
reading_time_minutes: 1
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# ProductList.Type options: Accessory and Component

Define quantity behavior in product hierarchies. The Accessory type keeps quantity constant; The Component type multiplies it by the parent.

ProductList.Type tells ServiceNow CPQ whether to manipulate a product's quantity based on the parent-child hierarchy in which it falls. When defining product actions, the Type parameter in the ProductList object can accept two values:

-   Accessory: When the value of ProductList.Type is set to Accessory, the quantity value set in the Product Action will be replicated as is in the ServiceNow CPQ shopping cart. That is, an Accessory product's quantity stays the same, no matter the quantity of its parent \(if it has a parent\). Accessory is the default value.
-   Component: Use this value if the quantity of a child should be multiplied by the quantity of its parent. This is useful for scenarios in which the user selects a quantity for a parent and the quantity of its child item needs to be set in a specific ratio. For example, if the parent is a car and its child is a tire, the Product Action that defines the tire would have quantity = 4.

If the child's ProductList.Type is set to Component, the bill of materials will always include the correct number of tires for the number of cars requested. When car quantity = 1, tire quantity = 4; when car quantity = 3, tire quantity = 12, and so on. The calculated tire quantity will be displayed in the ServiceNow CPQ shopping cart and transferred to the Salesforce Quote Line Editor or ecommerce cart when saved.

This concept replicates Salesforce CPQ bundle pricing.

The following video details ProductList.Type options for manipulating product quantities: [ProductList.Type = Accessory v. Component](https://www.youtube.com/watch?v=3uHBOZbbiRg)

**Related topics**  


[Using ProductList.extended to populate the Quote Line record](reverse_twin_productlist_extended_data_to_quoteline.md)

