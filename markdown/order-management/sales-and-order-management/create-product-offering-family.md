---
title: Create a product offering family
description: Create a product offering family for products with similar or common features that have multiple variations. You can apply common rules or attributes for product offerings at the product offering family level instead of applying them individually to each product offering.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-04-05"
reading_time_minutes: 1
breadcrumb: [Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales and Order Management]
---

# Create a product offering family

Create a product offering family for products with similar or common features that have multiple variations. You can apply common rules or attributes for product offerings at the product offering family level instead of applying them individually to each product offering.

## Before you begin

Role required: sn\_prd\_pm. product\_catalog\_admin or sn\_prd\_pm.product\_catalog\_manager

## About this task

A product offering family is a hierarchical classification of product offerings, like a category tree. Product families can have parent-child relationships \(multi-level tree\). You can define parent-child relationships, where each node in the family tree can have a parent, forming a multi-level hierarchy. With a product family you can:

-   Apply rules or default attributes at the family level, which are inherited by descendent products in the family.
-   Aggregate sales data by family, such as total revenue, including all sub-family products, for revenue reports.

For example, a product offering family hierarchy could be Hardware &gt; Computers &gt; Laptops. Each product offering inherits rules that define items such as required warranties or other features from the parent. Agents can view the product family for products in line items, which can provide context on why certain rules or discounts are applied to a product offering.

After you create product offering families, you assign a product offering to a product offering family when you create a product offering.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Offerings** &gt; **Product Offering Families**.

4.  Select **New**.

    Fill-in the form.

    |Field|Description|
    |-----|-----------|
    |Number|System-assigned number for the product offering family.|
    |Name|Product offering family name|
    |Description|Short description of the product offering family.|
    |Parent family|If the product offering family that you're creating is a child of an existing product offering family, select the parent product offering family.|

5.  Select **Save**.

    The product offering family is available for use and can be selected when you create a product offering.


## What to do next

[Create product offerings](som-create-product-offering.md)

