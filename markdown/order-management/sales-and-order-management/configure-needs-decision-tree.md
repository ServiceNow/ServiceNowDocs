---
title: Create a decision tree for a needs template
description: Create a decision tree that defines the questions that agents answer to determine customer needs and get product recommendations.
locale: en-US
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

-   [Decision trees in Guided decision](https://www.servicenow.com/docs/access?context=decision-trees-in-guided-decisions&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) - Become familiar with the basic elements of a decision tree and how they work, such as node types, linking inputs in nodes, and decision tree paths.
-   [Example configuration of a decision tree](https://www.servicenow.com/docs/access?context=example-decision-tree&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) - Walk through an example decision tree, including preparations for creating a decision tree, to understand the end-to-end configuration of a decision tree.
-   [Answer types for questions](https://www.servicenow.com/docs/access?context=type-of-answer&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) - Learn about the various types of answers, such as Choice, Date, or Integers.

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

[Build a needs decision tree](build-needs-decision-tree.md) using Decision Tree Builder.

