---
title: Ledger assignment rules
description: When a purchase line is created for a purchase requisition on the ShoppingHub portal, the details of capex account, expense account, and pre-paid account are auto-populated based on applicable ledger assignment rules.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up primary data for ShoppingHub, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Ledger assignment rules

When a purchase line is created for a purchase requisition on the ShoppingHub portal, the details of capex account, expense account, and pre-paid account are auto-populated based on applicable ledger assignment rules.

The legal entity from a purchase requisition or a sourcing request determines its ERP source. This ERP source determines the appropriate ledger assignment rule for a product category, product model, supplier product, and a cost center.

For a purchase line, if rules are found for the supplier product, the related product model, and its product category, then the priority of in which those rules are triggered is in this order:

1.  Supplier product with cost center
2.  Product model with cost center
3.  Product category with cost center
4.  Spend category with cost center
5.  Supplier product
6.  Product model
7.  Product category
8.  Spend category

**Note:** If you have multiple ERP sources, you can create multiple rules but each rule can correspond to only one ERP source.

-   **[Create ledger assignment rules](../task/create-ledger-assignment-rules.md)**  
Automate ledger account assignment for a purchase line by relating ledger accounts to a supplier product, product model, product category, spend category, and cost center.

**Parent Topic:**[Setting up primary data for ShoppingHub](../reference/set-up-master-data-shopping-hub.md)

