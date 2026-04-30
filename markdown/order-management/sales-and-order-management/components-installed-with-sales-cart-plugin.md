---
title: Components installed with Sales Cart
description: Several types of components are installed with activation of Sales Cart including tables, user roles, and scheduled jobs.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Sales Customer Relationship Management reference, Sales Customer Relationship Management]
---

# Components installed with Sales Cart

Several types of components are installed with activation of Sales Cart including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_wrq_rcw_tfc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Cart editor

 \[sn\_sales\_cart.cart\_editor\]

</td><td>

Creates, deletes, and edits sales cart and sales cart-related entities.

</td><td>

sn\_sales\_cart.cart\_viewer

</td></tr><tr><td>

Cart viewer

 \[sn\_sales\_cart.cart\_viewer\]

</td><td>

Views sales cart and sales cart-related entities.

</td><td>

 

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_yrq_rcw_tfc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Migrate proxy orders to sales cart

</td><td>

On-demand job that migrates draft proxy order carts to the new sales cart experience and sets the value of the **sn\_sales\_cart.show\_cart\_migration\_msg** system property to true.

 **Note:** If you used the Business Portal and are upgrading to the Zurich release, then you must run the Migrate proxy orders to sales cart job after installing the Sales Cart plugin \(sn\_sales\_cart\). Customers then don't lose products added to their carts on the Business Portal.

</td></tr></tbody>
</table>## Tables installed

<table id="table_asq_rcw_tfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sales Cart

 \[sn\_sales\_cart\]

</td><td>

Stores the main sales cart record, including customer, billing, shipping, pricing, and state details.

</td></tr><tr><td>

Sales Cart Line Characteristic

 \[sn\_sales\_cart\_line\_characteristic\]

</td><td>

Stores characteristics and options associated with individual sales cart line items.

</td></tr><tr><td>

Sales Cart Line Item

 \[sn\_sales\_cart\_line\_item\]

</td><td>

Represents individual line items within a sales cart, including products, pricing, quantities, and hierarchical relationships.

</td></tr><tr><td>

Sales Cart Pricing Adjustment

 \[sn\_sales\_cart\_pricing\_adjustment\]

</td><td>

Stores pricing adjustments applied to a sales cart or its line items, including adjustment type, value, and related references.

</td></tr></tbody>
</table>**Parent Topic:**[Sales Customer Relationship Management reference](../concept/som-reference.md)

