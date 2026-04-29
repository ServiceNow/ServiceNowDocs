---
title: Transaction Manager use case: Apply parent line discounts to child lines
description: Transaction Manager can help manage transactions whose configurable products have many child and grandchild transaction line items.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transaction Manager: Use cases, Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager use case: Apply parent line discounts to child lines

Transaction Manager can help manage transactions whose configurable products have many child and grandchild transaction line items.

A single transaction may include multiple configurable products, and each configurable product may have more than 100 child, grandchild, or other descendant transaction line items.

Discounting at the transaction header level could apply a uniform discount across all products and transaction line items. Conversely, applying discounts at the transaction line-level lets you discount individual products and lines at different rates. However, for a product with many descendant line items, this may become burdensome.

Using the `.parent` system field enables the look up of a parent line-item field, which can then be applied to only the child lines of that product. For example, a picklist can be used at the header level to designate the discounting method to apply.

![Discounting at the transaction header](../images/cpq-txn-mgr-use-case-apply-line-discounts-1.png)

When **Parent Line Discounting** is selected, a rule sets the descendant line’s discount field equal to that of its parent line.

![Discounting at the transaction header](../images/cpq-txn-mgr-use-case-apply-line-discounts-2.png)

**Parent Topic:**[Transaction Manager: Use cases](transaction-manager-use-cases.md)

