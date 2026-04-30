---
title: Components installed with Order Management
description: Several types of components are installed with activation of the Order Management plugin, including tables and user roles.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-09-04"
reading_time_minutes: 3
breadcrumb: [Order Management reference, Reference, Sales Customer Relationship Management]
---

# Components installed with Order Management

Several types of components are installed with activation of the Order Management plugin, including tables and user roles.

## Roles installed

<table id="table_s22_cjx_ngc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Order Fulfillment Agent

 \[sn\_ind\_tmt\_orm.order\_fulfilment\_agent\]

</td><td>

Views product order, product order task, service order, and resource order. Can edit some fields from the tasks.

</td><td>

-   sn\_customerservice.case\_viewer
-   sn\_tmt\_core.outbound\_request\_read
-   sn\_ind\_tmt\_orm.fulfillment\_writer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_prd\_invt.product\_inventory\_relationship\_write
-   sn\_sla\_definition\_read
-   awa\_agent
-   sn\_ind\_tmt\_orm.order\_creator
-   sn\_fallout\_mgmt.fallout\_creator
-   sn\_prd\_invt.product\_inventory\_relationship\_creat
-   sn\_prd\_invt.product\_inventory\_relationship\_rea
-   wm\_basic

</td></tr><tr><td>

Order Fulfilment Manager

 \[sn\_ind\_tmt\_orm.order\_fulfilment\_manager\]

</td><td>

Views and edits product order, product order task, service order, and resource order.

</td><td>

-   sn\_ind\_tmt\_orm.order\_fulfilment\_agent
-   sn\_ind\_tmt\_orm.order\_approver
-   sn\_prd\_invt.product\_inventory\_relationship\_delete

</td></tr><tr><td>

Service Order Agent

 \[sn\_ind\_tmt\_orm.service\_order\_agent\]

</td><td>

Views service order and resource order. Can edit some fields from the tasks.

</td><td>

-   wm\_basic
-   sn\_prd\_invt.product\_inventory\_relationship\_read
-   awa\_agent
-   sn\_sla\_definition\_read
-   sn\_ind\_tmt\_orm.order\_creator
-   sn\_tmt\_core.outbound\_request\_read
-   sn\_ind\_tmt\_orm.fulfillment\_writer
-   sn\_prd\_invt.product\_inventory\_relationship\_create
-   sn\_prd\_invt.product\_inventory\_relationship\_write
-   sn\_customerservice.case\_viewer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_fallout\_mgmt.fallout\_creator

</td></tr><tr><td>

Service Order Manager

 \[sn\_ind\_tmt\_orm.service\_order\_manager\]

</td><td>

Views and edits service order and resource order.

</td><td>

-   sn\_ind\_tmt\_orm.service\_order\_agent
-   sn\_ind\_tmt\_orm.order\_approver
-   sn\_prd\_invt.product\_inventory\_relationship\_delete

</td></tr><tr><td>

Order Approver

 \[sn\_ind\_tmt\_orm.order\_approver\]

</td><td>

Approves customer orders in Order Management for Telecommunications. This role is included in the Order Management Business Stakeholder role.

</td><td>

sn\_ind\_tmt\_orm.order\_viewer

</td></tr><tr><td>

Order Viewer

 \[sn\_ind\_tmt\_orm.order\_viewer\]

</td><td>

Views customer, product, service, and resource orders and any related order tasks in Order Management for Telecommunications. This role is included in the Order Management Business Stakeholder role.

</td><td>

-   sn\_prd\_invt.product\_inventory\_viewer
-   sn\_sales\_agmt\_core.sales\_agreement\_viewer
-   sn\_customerservice.customer\_data\_viewer
-   sn\_prd\_pm.product\_catalog\_viewer
-   sn\_bus\_loc.ibl\_viewer
-   agent\_workspace\_user
-   sn\_bus\_loc.ebl\_viewer
-   sn\_csm\_pricing.pricelist\_viewer
-   canvas\_user
-   sn\_ord\_qual\_mgmt.alternate\_proposal\_read
-   sn\_ind\_tmt\_orm.fulfillment\_viewer
-   sn\_tmt\_core.inbound\_queue\_read
-   sn\_prd\_invt.product\_inventory\_operations\_read
-   sn\_service\_org.customer\_criteria\_read
-   sn\_change\_read

</td></tr><tr><td>

Fulfillment Writer

 \[sn\_ind\_tmt\_orm.fulfillment\_writer\]

</td><td>

Granular role to grant write access to fulfillment tasks.

</td><td>

-   sn\_ind\_tmt\_orm.fulfillment\_viewer
-   sn\_tmt\_core.outbound\_request\_write

</td></tr><tr><td>

Order Agent

 \[sn\_ind\_tmt\_orm.order\_agent\]

</td><td>

Reads, creates, and updates access to orders, order line items, order characteristic values, and price adjustments. Also, reads order tasks, product order, service order, and resource orders.

</td><td>

-   sn\_ind\_tmt\_orm.order\_creator
-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.sn\_customer\_menu\_viewer

</td></tr><tr><td>

Order admin

 \[sn\_ind\_tmt\_orm.order\_admin\]

</td><td>

Reads, writes, and updates access for Order tables.

</td><td>

-   sn\_ind\_tmt\_orm.order\_agent
-   sn\_ind\_tmt\_orm.order\_approver

</td></tr><tr><td>

Order Creator

 \[sn\_ind\_tmt\_orm.order\_creator\]

</td><td>

Creates orders. Use this role to send order via REST Web Services.

</td><td>

-   sn\_ord\_qual\_mgmt.alternate\_proposal\_write
-   sn\_ind\_tmt\_orm.order\_viewer
-   sn\_ord\_qual\_mgmt.alternate\_proposal\_create

</td></tr><tr><td>

Order Integrator

 \[sn\_ind\_tmt\_orm.order\_integrator\]

</td><td>

Creates orders. Use this role to send order via REST Web Services.

</td><td>

-   sn\_prd\_invt.product\_inventory\_operations\_create
-   sn\_tmt\_core.inbound\_queue\_create
-   sn\_tmt\_core.inbound\_queue\_create
-   sn\_tmt\_core.outbound\_request\_write
-   sn\_ind\_tmt\_orm.order\_creator

</td></tr></tbody>
</table>## Tables installed

<table id="table_w22_cjx_ngc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order Line Related Items

 \[sn\_ind\_tmt\_orm\_order\_line\_related\_items\]

</td><td>

Indicates associations between an order line item and its related items or product inventory.

</td></tr><tr><td>

Inflight Order Line Item Change

 \[sn\_ind\_tmt\_orm\_inflight\_order\_line\_item\_change\]

</td><td>

Tracks changes made to order lines items whole the order is in progress.

</td></tr><tr><td>

External product inventory

 \[sn\_ind\_tmt\_orm\_external\_product\_inventory\]

</td><td>

Tracks product inventory records managed in external systems and linked to order line items.

</td></tr><tr><td>

Decomposition Rule

 \[sn\_ind\_tmt\_orm\_order\_decomposition\_rule\]

</td><td>

Defines the rules used to break down an order into smaller fulfillment tasks based on characteristics and specification.

</td></tr><tr><td>

External Sim Numbers

 \[sn\_ind\_tmt\_orm\_st\_external\_sim\_numbers\]

</td><td>

Stores Sim numbers managed in external systems for use in order processing.

</td></tr><tr><td>

Order Line Item Contact

 \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]

</td><td>

Stores contact details linked to a specific order line item.

</td></tr><tr><td>

Resource Order

 \[sn\_ind\_tmt\_orm\_resource\_order\]

</td><td>

Represents resource level orders and their associated tasks in the fulfillment process.

</td></tr><tr><td>

Order Characteristic

 \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]

</td><td>

Represents the characteristics and configurable attributes defined for an order.

</td></tr><tr><td>

Pricing Adjustments

 \[sn\_ind\_tmt\_orm\_pricing\_adjustment\]

</td><td>

Tracks adjustments such as discounts or surcharges applied to an order or order line item.

</td></tr><tr><td>

Mobile Order Task

 \[sn\_ind\_tmt\_orm\_mobile\_order\_task\]

</td><td>

Represents order tasks created for mobile services or mobile related fulfillment.

</td></tr><tr><td>

Customer Order Related Party

 \[sn\_ind\_tmt\_orm\_order\_related\_party\]

</td><td>

Represents parties linked to a customer order, such as organizations or responsible entities.

</td></tr><tr><td>

Req Def Glide

 \[sn\_ind\_tmt\_orm\_req\_def\_glide\]

</td><td>

Stores request definition data linked to variables and dictionary entries in Glide.

</td></tr><tr><td>

Domain Order Related Items

 \[sn\_ind\_tmt\_orm\_domain\_order\_related\_item\]

</td><td>

Represents items linked to a domain order, including related orders and inventory.

</td></tr><tr><td>

Product Order

 \[sn\_ind\_tmt\_orm\_product\_order\]

</td><td>

Represents customer product orders and their associated fulfillment tasks.

</td></tr><tr><td>

Covered Product

 \[sn\_ind\_tmt\_orm\_covered\_product\]

</td><td>

Represents products covered under an order line, sold product, or install base.

</td></tr><tr><td>

Service Order

 \[sn\_ind\_tmt\_orm\_service\_order\]

</td><td>

Represents customer service orders and their associated fulfillment tasks.

</td></tr><tr><td>

Decomposition Trigger

 \[sn\_ind\_tmt\_orm\_decomposition\_trigger\]

</td><td>

Defines the conditions that initiate decomposition of an order or order line.

</td></tr><tr><td>

Inflight Change Type

 \[sn\_ind\_tmt\_orm\_inflight\_change\_type\]

</td><td>

Defines the types of changes that can be applied to inflight orders or order lines.

</td></tr><tr><td>

Order Stage

 \[sn\_ind\_tmt\_orm\_order\_stage\]

</td><td>

Defines the stages an order goes through in its life cycle.

</td></tr><tr><td>

Order To Project Relationship

 \[sn\_ind\_tmt\_orm\_order\_line\_rel\_task\]

</td><td>

Indicates the relationship between an order and its associated project tasks or records.

</td></tr><tr><td>

Request Definition Characteristic

 \[sn\_ind\_tmt\_orm\_req\_def\_char\]

</td><td>

Defines the characteristics and attributes associated with a request definition.

</td></tr><tr><td>

Domain Order\[sn\_ind\_tmt\_orm\_domain\_order\]

</td><td>

Represents a domain level order that consolidates product, service, or resource orders into fulfillment tasks.

</td></tr><tr><td>

Upgrade Inventory Job

 \[sn\_ind\_tmt\_orm\_upgrade\_inventory\_job\]

</td><td>

Stores details of inventory upgrade jobs, including specifications, payload, and status.

</td></tr><tr><td>

Contract Product Offering

 \[sn\_ind\_tmt\_orm\_contract\_m2m\_product\_offering\]

</td><td>

Indicates the relationship between a contract and its associated product offerings.

</td></tr><tr><td>

Customer Order

 \[sn\_ind\_tmt\_orm\_order\]

</td><td>

Represents a customer’s order, including account, billing, shipping, pricing, and charge details.

</td></tr><tr><td>

Order Line Item

 \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td><td>

Represents the individual items in a customer order, including product, pricing, quantity, and shipping details.

</td></tr></tbody>
</table>**Parent Topic:**[Order Management reference](order-mgt-reference.md)

