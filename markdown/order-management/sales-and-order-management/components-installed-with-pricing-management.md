---
title: Components installed with Pricing Management
description: Several types of components are installed with activation of the Pricing Management plugin, including tables and user roles.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, price, quote, Reference, Sales and Order Management]
---

# Components installed with Pricing Management

Several types of components are installed with activation of the Pricing Management plugin, including tables and user roles.

## Roles installed

<table id="table_fpw_5qb_ngc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Price list administrator\[sn\_csm\_pricing\_pricelist\_administrator\]

</td><td>

Create and update pricing entities, set up or edit pricing-related system properties, and view transaction logs.

</td><td>

-   sn\_csm\_pricing.pricelist\_manager
-   sn\_export\_entities.export\_user
-   import\_admin

</td></tr><tr><td>

Price list manager\[sn\_csm\_pricing\_pricelist\_manager\]

</td><td>

Create and update pricing entities such as price lists and price list lines, set up or edit pricing-related system properties, and view transaction logs.

</td><td>

sn\_csm\_pricing.pricelist\_writer

</td></tr><tr><td>

Price list writer\[sn\_csm\_pricing.pricelist\_writer\]

</td><td>

Granular role that has read, write, and delete access to pricing entities. To delete a pricing entity such as a price list or cost book, the pricing entity must be in Draft state.

</td><td>

-   decision\_table\_crud\_api
-   decision\_rule\_author
-   n\_csm\_ctxrul\_mgt.rule\_matrix\_writer
-   sn\_csm\_pricing.pricelist\_viewer
-   personalize\_decision\_table\_input

</td></tr><tr><td>

sn\_csm\_pricing.pricing\_integrator

</td><td>

Role required to access pricing features through the Pricing REST API when using the advanced configurator.

</td><td>

None

</td></tr><tr><td>

sn\_csm\_pricing.pricing\_integrator\_internal

</td><td>

Role required to access pricing features through the Pricing REST API when using the advanced configurator. Exempt from API rate limits.

</td><td>

None

</td></tr><tr><td>

Sales Agreement price list writer

 \[sales\_agreement\_pricelist\_writer\]

</td><td>

Granular role that has read, write, and delete access to pricing entities. Write access only for Sales Agreement price lists.

</td><td>

None

</td></tr><tr><td>

Price list viewer\[sn\_csm\_pricing.pricelist\_viewer\]

</td><td>

Granular role that has read access to pricing entities such as price lists, price list lines, cost books, and cost book lines.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_jpw_5qb_ngc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pricing Plan\[sn\_csm\_pricing\_pricing\_plan\]

</td><td>

Stores the pricing steps used by the pricing engine to retrieve and calculate product pricing.

</td></tr></tbody>
</table>**Parent Topic:**[Configure, price, quote reference](../concept/reference-cpq.md)

