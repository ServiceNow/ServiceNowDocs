---
title: Configuring product offer eligibility
description: You can filter the product catalog, offering categories, and product offerings dynamically, to display only the appropriate catalog, categories, and offerings for which a customer is eligible. Your agents see this filtered product information when they're creating opportunities, quotes, and orders.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Configuring product offer eligibility

You can filter the product catalog, offering categories, and product offerings dynamically, to display only the appropriate catalog, categories, and offerings for which a customer is eligible. Your agents see this filtered product information when they're creating opportunities, quotes, and orders.

## Product offer eligibility overview

As a product catalog admin or manager, you create the business rules that filter the product catalogs, offering categories, and product offerings to display only the eligible products for customers when agents are creating quotes or orders. Filtering the products helps agents sell the correct products to customers. The filters are based on decision rules that you set in the following product eligibility matrices:

-   **Product Offering Catalog Eligibility**: Define the eligibility rules to be applied to product offering catalogs. For example, you can use this matrix to filter sales catalogs based on customer location, such as country, state, or city.
-   **Product Offering Category Eligibility**: Define the eligibility rules to be applied to product offering categories.
-   **Product Offering Eligibility**: Define the eligibility rules to be applied to product offerings.

These matrices are frameworks for setting the conditions and the context variables that control the catalogs, product categories, and product offerings displayed. You can use system-defined context variables provided with Product Catalog Management and Pricing Management, or you can work with your admin to develop your own custom context variables, such as marketing segment or sales channel, to be used in the eligibility matrices.

## Configuration tasks

Complete the following tasks to set up product eligibility matrices.

|Task|Description|Role|
|----|-----------|----|
|[Create a custom context variable](../task/som-create-context-variable.md) \(if needed\)|Review system-defined and existing custom context variables. If needed, add a new context variable, then [map the customer variable to a transaction entity](../task/som-map-variable.md).|Admin|
|[Create a rule entity filter](../task/som-create-rule-entity-filter.md)|Define the eligibility filters for a product entity.|Product catalog admin or manager|
|[Define product eligibility rules in a product eligibility matrix](../task/som-define-eligibility-rules.md)|Define the eligibility rules in the decision table of a product eligibility matrix.|Product catalog admin or manager|

