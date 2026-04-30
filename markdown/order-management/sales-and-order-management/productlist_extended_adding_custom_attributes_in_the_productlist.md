---
title: Adding custom attributes to the product list
description: Use ProductList.extended to add custom attributes such as cost, margin, and discount to a product list.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [ProductList.Type options: Accessory and Component, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Adding custom attributes to the product list

Use ProductList.extended to add custom attributes such as cost, margin, and discount to a product list.

Custom attributes can be added to a product list, bill of materials, or Shopping Cart beyond the standard attributes that are provided by default. Common use cases include attributes for cost, margin, list price, discount, and so on.

## Advanced Script

To add a custom attribute to a product list, use `.extended` and provide data in JSON format in an advanced script:

```
ProductList.extended = {"cost": 62};
```

To add multiple custom fields, add to the same JSON object, as shown below:

```
var myMargin = 38;
ProductList.id = "Test Product";
ProductList.price = 100;
ProductList.extended = {"cost": 62, "margin": myMargin, "customText":"Example 2"};
ProductList.description = "Example 1";
ProductList.bomType = "sales";
ProductList.next();
return ProductList; 
```

Some tips:

-   Numbers can be entered directly as the value.
-   Text should be surrounded by double quotes.
-   Variables can be used for values.
-   Math or other value manipulation must occur outside of the JSON. Use a variable to get the final value into the JSON object.

## Writing to Salesforce quote line fields

Admins can also set ProductList.extended information to map to a field on a Salesforce quote line by referencing the field name in the product action when setting the ProductList.extended information.

For example, to set the description field, admins would set the ProductList.extended information to:

```
ProductList.extended = {“SBQQ__Description__c”: “Text Description”}
```

## Layout

To add custom ProductList attributes to a layout, use `extended.{attributename}` in the value column:

![CSV file](../images/cpq-product-list-custom-attributes.png)

**Related topics**  


[Using ProductList.extended to populate the Quote Line record](reverse_twin_productlist_extended_data_to_quoteline.md)

