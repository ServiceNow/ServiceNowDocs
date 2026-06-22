---
title: Create a decision tree for a needs template
description: Create a decision tree that defines the questions that agents answer to determine customer needs and get product recommendations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/sales-and-order-management/configure-needs-decision-tree.html
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure needs analysis, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Create a decision tree for a needs template

Create a decision tree that defines the questions that agents answer to determine customer needs and get product recommendations.

## Before you begin

Before creating decision trees, review the following information:

-   [Decision trees in Guided decision](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/decision-trees-in-guided-decisions.md) - Become familiar with the basic elements of a decision tree and how they work, such as node types, linking inputs in nodes, and decision tree paths.
-   [Example configuration of a decision tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/example-decision-tree.md) - Walk through an example decision tree, including preparations for creating a decision tree, to understand the end-to-end configuration of a decision tree.
-   [Answer types for questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/type-of-answer.md) - Learn about the various types of answers, such as Choice, Date, or Integers.

Role required: sn\_prd\_pm.product\_catalog\_manager, sn\_prd\_pm.product\_catalog\_admin

## Procedure

1.  In the CSM Configurable Workspace, select the **List** \[Omitted image "list-outline-24.svg"\] Alt text: view.

2.  Navigate to **Needs** &gt; **Decision Tree** and select **New**.

3.  Select **New**.

    On the form, fill in the fields.

    |FIeld|Description|
    |-----|-----------|
    |Name|Name of the decision tree.|
    |Action Label|Label of the decision tree displayed on the needs template card in the product selection guide.|
    |Description|Brief description of the decision tree. The description is displayed on the needs template card in the product selection guide.|
    |Title|Name of the decision tree on the needs template card in the product selection guide.|
    |Show a dismiss button|Option that shows or hides the **Dismiss** button that cancels the flow of a decision tree during opportunity or lead creation. This field is enabled by default.|

4.  Select **Save**

    A decision tree is created with the name specified in the **Name** field.


## What to do next

[Build a needs decision tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/build-needs-decision-tree.md) using Decision Tree Builder.

