---
title: Components installed with Customer Request for Quote
description: Several types of components are installed with activation of the Customer Request for Quote \(RFQ\) plugin, including tables, user roles, and plugins.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business Portal reference, Reference, Sales and Order Management]
---

# Components installed with Customer Request for Quote

Several types of components are installed with activation of the Customer Request for Quote \(RFQ\) plugin, including tables, user roles, and plugins.

## Roles installed

<table id="table_kzb_rkb_fhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

RFQ writer

 \[sn\_cust\_rfq\_core.rfq\_writer\]

</td><td>

Provides write and update access to all RFQ tables.

</td><td>

sn\_cust\_rfq\_core.rfq\_viewer

</td></tr><tr><td>

RFQ viewer

 \[sn\_cust\_rfq\_core.rfq\_viewer\]

</td><td>

Provides read-only access to all RFQ tables.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_ozb_rkb_fhc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Request for Quote

 \[sn\_cust\_rfq\_core\_rfq\]

</td><td>

Stores RFQ headers with customer information, shipping/billing addresses, pricing totals, and status tracking.

</td></tr><tr><td>

Customer Request for Quote Pricing Adjustment

 \[sn\_cust\_rfq\_core\_pricing\_adjustment\]

</td><td>

Stores discounts, surcharges, and other price modifications applied to the RFQ or individual RFQ line items.

</td></tr><tr><td>

Customer Request for Quote Line Item

 \[sn\_cust\_rfq\_core\_line\_item\]

</td><td>

Stores individual products requested in an RFQ, including quantities, pricing details, and hierarchical relationships between line items.

</td></tr><tr><td>

Customer Request for Quote Line Characteristic

 \[sn\_cust\_rfq\_core\_line\_characteristic\]

</td><td>

Stores product specifications and configurable attributes for each RFQ line item.

</td></tr></tbody>
</table>## Plugins installed

The following applications are installed as dependencies with the Customer Request for Quote application \(sn\_cust\_rfq\):

-   Customer Request for Quote Data Model \(com.sn\_cust\_rfq\_core\)
-   Product Catalog Management Core \(com.sn\_prd\_pm\)
-   Price Management \(com.sn\_csm\_pricing\)
-   Sales common \(com.sn\_l2c\_sales\_common\)
-   Product Catalog Management Portal \(com.prd\_pm\_portal\)
-   Agent Workspace \(com.agent\_workspace\)
-   Playbooks for CSM \(com.sn\_csm\_playbook\)

**Parent Topic:**[Business Portal reference for Sales and Order Management](som-business-portal-reference.md)

