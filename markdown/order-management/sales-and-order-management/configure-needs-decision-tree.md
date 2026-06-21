---
title: Create a decision tree for a needs template
description: Create a decision tree that defines the questions that agents answer to determine customer needs and get product recommendations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/order-management/sales-and-order-management/configure-needs-decision-tree.html
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring needs analysis, Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Create a decision tree for a needs template

Create a decision tree that defines the questions that agents answer to determine customer needs and get product recommendations.

## Before you begin

Before creating decision trees, review the following information:

-    - Become familiar with the basic elements of a decision tree and how they work, such as node types, linking inputs in nodes, and decision tree paths.
-    - Walk through an example decision tree, including preparations for creating a decision tree, to understand the end-to-end configuration of a decision tree.
-    - Learn about the various types of answers, such as Choice, Date, or Integers.

Role required: sn\_prd\_pm.product-catalog\_manager, sn\_prd\_pm.product-catalog\_admin

## Procedure

1.  Navigate to **All** &gt; **Product Catalog Management** &gt; **Needs** &gt; **Decision Trees**.

2.  Select **New**.

    On the form, fill in the fields.

    |FIeld|Description|
    |-----|-----------|
    |Name|Name of the decision tree.|
    |Action Label|Label of the decision tree displayed on the needs template card in the product selection guide.|
    |Description|Brief description of the decision tree displayed on the needs template card in the product selection guide.|
    |Title|Name of the decision tree on the needs template card in the product selection guide.|
    |Show a dismiss button|Option that shows or hides the **Dismiss** button that cancels the flow of a decision tree during opportunity creation. This field is enabled by default.|

3.  Select **Submit**

    A decision tree is created with the name specified in the **Name** field.


## What to do next

[Build a needs decision tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/order-management/sales-and-order-management/build-needs-decision-tree.md) using Decision Tree Builder.

