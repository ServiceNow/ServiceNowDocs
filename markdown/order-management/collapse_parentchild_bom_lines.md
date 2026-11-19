---
title: Collapse parent or child BOM lines
description: You can configure child products to hide under their parent products unless expanded.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/collapse\_parentchild\_bom\_lines.html
release: zurich
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [ProductList.Type options: Accessory and Component, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Collapse parent or child BOM lines

You can configure child products to hide under their parent products unless expanded.

## Default behavior

When product actions are set with a defined parent/child relationship, by default, child products are indented as in the following:

\[Omitted image "cpq-bom-indent.png"\] Alt text: parent/child relationship

## Collapsible behavior

This behavior can be overridden by adding `{“hierarchyColumn”: “<productListColumnVariableName>”}` to the value column of the productList element in the layout editor or in the layout CSV file.

\[Omitted image "cpq-bom-enable-collapse.png"\] Alt text: Collapsible Behavior

## Result

\[Omitted image "cpq-bom-enable-collapse-result.png"\] Alt text: Result

Admins can change where the collapse arrow appears by defining a different product list column as the hierarchy column \(`“hierarchyColumn”`\). For example, using `quantity` in the CSV snippet above results in the following:

\[Omitted image "cpq-bom-collapse-result-alternate.png"\] Alt text: product list column

