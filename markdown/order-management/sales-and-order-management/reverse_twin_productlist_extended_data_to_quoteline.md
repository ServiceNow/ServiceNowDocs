---
title: Using ProductList.extended to populate the Quote Line record
description: You can use the Extended product data object to populate custom fields on the Quote Line record.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [ProductList.Type options: Accessory and Component, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Using ProductList.extended to populate the Quote Line record

You can use the Extended product data object to populate custom fields on the Quote Line record.

Populate custom fields in the Quote Line record by utilizing the `extended` product data object in Advanced Product Actions.

```
ProductList.extended = { "key": "value" };
```

The key must match the API name of the fields on both the Product Option and Quote Line objects. This takes advantage of Salesforce CPQ twinning. For information about twinning in Salesforce CPQ, see the following Salesforce documentation topic:

[Mapping of Custom Salesforce CPQ Fields Between Objects](https://help.salesforce.com/s/articleView?id=sf.cpq_twin_fields.htm&type=5)

In the following video, a custom text field with the variable name `Color_c` is created on both the Product Option and Quote Line objects. Then the extended product data in the advanced product action is defined as `ProductList.extended = { "Color__c": color };`. `Color_c` serves as the key, and the previously defined `color` variable in the script is assigned.

[Reverse Twin ProductList.extended Data To QuoteLine](https://www.youtube.com/watch?v=6nTxqPTOgic)

Reverse twinning extended product data also enables admins to populate quote line data directly to the Quote Line Editor \(QLE\). The custom Quote Line field must be added to the Line Editor field set.

**Note:** Salesforce CPQ does not allow users to edit the following product option fields, including when passing data back from an external configurator such as ServiceNow CPQ.

-   Product Code
-   Product Configuration Type
-   Product Description
-   Product Family
-   Product Name
-   Product Quantity Scale
-   Product Subscription Pricing
-   Price Editable

**Related topics**  


[Adding custom attributes to the product list](productlist_extended_adding_custom_attributes_in_the_productlist.md)

