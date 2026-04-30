---
title: Create an order guide variable
description: You can create variables within an order guide.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Order guides, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an order guide variable

You can create variables within an order guide.

To create or edit order guide variables, open an order guide, then select an entry from the **Variables** related list.

Service catalog variables within order guides define the questions and potential answers presented to the customer while ordering. This information is used by order guide rules. Variables can also be cascaded, which passes the variable values along to individual ordered items.

Pricing is not supported for an order guide variable, even when you define the pricing for the variable though a variable set, and associate the variable set to the order guide.

-   **[Create an item variable assignment](../task/t_CreateAnItemVarAssignment.md)**  
Create an item variable assignment that enables the catalog admin set up a default value mechanism in the order guide context so that the user can focus only on required values.
-   **[Cascade an order guide variable](c_CascadeTheOrderGuideVariables.md#)**  
Cascading enables values entered for variables in the initial order form to be passed to the equivalent variables in the ordered catalog items.

**Parent Topic:**[Order guides](c_ServiceCatalogOrderGuides.md)

