---
title: How parent/child relationships function when multiple BOMs are displayed
description: See how product relationships are displayed in a product list that includes more than one bill of materials.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# How parent/child relationships function when multiple BOMs are displayed

See how product relationships are displayed in a product list that includes more than one bill of materials.

If a parent or child product is not displayed in a BOM because it has a different BOM type than its parent or child product, an effectiveParent propertyis set to determine how to display the hierarchy.

Parent/child product relationships between products with different BOM types will appear in the product list similarly to the example below. Here, the parent of Grandchild Product2 is the child product. Child Product is a manufacturing item, while Grandchild Product2 is a sales item. Because Child Product is not shown in the sales BOM, Parent Product is shown as the parent \(becoming the effective parent\) of Grandchild Product2.

![Sales BOM](../images/cpq-parent-child-multiple-boms.png)

