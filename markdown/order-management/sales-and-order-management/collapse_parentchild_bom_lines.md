---
title: Collapse parent or child BOM lines
description: You can configure child products to hide under their parent products unless expanded.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ProductList.Type options: Accessory and Component, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Collapse parent or child BOM lines

You can configure child products to hide under their parent products unless expanded.

## Default behavior

When product actions are set with a defined parent/child relationship, by default, child products are indented as in the following:

![parent/child relationship](../images/cpq-bom-indent.png)

## Collapsible behavior

This behavior can be overridden by adding `{“hierarchyColumn”: “<productListColumnVariableName>”}` to the value column of the productList element in the layout editor or in the layout CSV file.

![Collapsible Behavior](../images/cpq-bom-enable-collapse.png)

## Result

![Result](../images/cpq-bom-enable-collapse-result.png)

Admins can change where the collapse arrow appears by defining a different product list column as the hierarchy column \(`“hierarchyColumn”`\). For example, using `quantity` in the CSV snippet above results in the following:

![product list column](../images/cpq-bom-collapse-result-alternate.png)

