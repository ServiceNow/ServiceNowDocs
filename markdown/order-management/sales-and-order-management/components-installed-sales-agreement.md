---
title: Components installed with Sales Agreement Management
description: Several types of components are installed with activation of the Sales Agreement Management plugins, including tables and user roles.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, price, quote, Reference, Sales and Order Management]
---

# Components installed with Sales Agreement Management

Several types of components are installed with activation of the Sales Agreement Management plugins, including tables and user roles.

## Roles installed

<table id="table_xp4_np3_wbc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Role titles

</th></tr></thead><tbody><tr><td>

sn\_sales\_agmt\_core.sales\_agreement\_viewer

</td><td>

This role enables users to perform read operations on sales agreements, sales agreement lines, and related data such as characteristics, price lists, and other tables.

</td><td>

-   sn\_prd\_pm.product\_catalog\_viewer \(contains sn\_prd\_pm.characteristics\_viewer\)
-   sn\_quote\_mgmt\_core.quote\_viewer \(contains sn\_csm\_pricing.pricelist\_viewer\)

</td><td>

-   Sales agent
-   Sales manager
-   Data viewer

</td></tr><tr><td>

sn\_sales\_agmt\_core.sales\_agreement\_writer

</td><td>

This role enables users to perform, create, read, and update operations on sales agreements and sales agreement lines.

</td><td>

sn\_sales\_agmt\_core.sales\_agreement\_viewer

</td><td>

-   Sales agent
-   Sales manager

</td></tr></tbody>
</table>## Tables installed

|Table|Description|
|-----|-----------|
|sn\_sales\_agmt\_core\_sales\_agreement|Stores all the sales agreements.|
|sn\_sales\_agmt\_core\_sales\_agreement\_line|Stores the lines of a sales agreement indicating the products and services agreed for sale.|
|sn\_sales\_agmt\_core\_line\_characteristic|Stores the attributes of products and services to be sold.|
|sn\_sales\_agmt\_core\_line\_adjustment|Stores the adjustments applied during negotiation.|

**Parent Topic:**[Configure, price, quote reference](../concept/reference-cpq.md)

