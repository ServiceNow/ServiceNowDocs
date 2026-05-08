---
title: Assign user roles in Sales Customer Relationship Management applications
description: The Sales Customer Relationship Management \(Sales CRM\) applications use roles to control access to features and capabilities. Roles also determine access to information for data security, identify users, and define the work that users perform in your organization.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, Sales Customer Relationship Management]
---

# Assign user roles in Sales Customer Relationship Management applications

The Sales Customer Relationship Management \(Sales CRM\) applications use roles to control access to features and capabilities. Roles also determine access to information for data security, identify users, and define the work that users perform in your organization.

## Overview of roles

Roles define the functions available to users of the Sales CRM applications, including:

-   Product Catalog Management
-   Pricing Management
-   Lead Management
-   Opportunity Management
-   Quote Management
-   Sales Agreement Management
-   Order Management

Assign roles to users and groups by using the ServiceNow AI Platform user administration feature.

-   To assign a role to a user, see Assign a role to a user.
-   To assign a role to a group, see Assign a role to a group.

## Lead Management roles

The roles in the following table apply to Lead Management.

|Role|Description|
|----|-----------|
|Lead Agent \[sn\_customerservice.csm\_workspace\_user\]|Identifies, nurtures, and converts leads into opportunities. Creates, reads, updates, and deletes leads. Has access to CSM Workspace. I|
|Sales Agent \[sn\_sales\_common.sales\_manager\]|Role that has access to CSM and lead entities.|
|Sales Operations Specialist \[sn\_sales\_common.sales\_ops\_specialist\]|Enhances efficiency and accuracy in sales operations. Read access to lead entities. Configures sales processes in an organization.|
|Lead Viewer \[sn\_prd\_pm.product\_catalog\_viewer\] \[sn\_csm\_ctxrul\_mgt.context\_variable\_viewer\]\[sn\_csm\_ctxrul\_mgt.rule\_matrix\_viewer\]|Granular role that has access to view product catalog entities such as product offerings.|
|Lead Writer|Read access to all lead tables such as header and line items.|

## Opportunity Management roles

The roles in the following table apply to Opportunity Management. To learn more about these roles, see [Opportunity Management](opportunity-management.md).

|Role|Description|
|----|-----------|
|Sales Agent \[sn\_sales\_common.sales\_agent\]|Identifies, nurtures, and converts opportunities into successful sales. Creates, reads, and updates opportunities.|
|Sales Manager \[sn\_sales\_common.sales\_manager\]|Reviews open opportunities and assigns them to sales agents. Creates, reads, and updates opportunities.|
|Sales Operations Specialist \[sn\_sales\_common.sales\_ops\_specialist\]|Enhances efficiency and accuracy in sales operations. Configures sales processes in an organization.|
|sn\_opty\_mgmt\_core.opportunity\_setup\_viewer|Granular role that has access to sale cycle and stages.|
|sn\_opty\_mgmt\_core.opportunity\_setup\_writer|Granular role that has access to sales cycle and stages.|
|sn\_opty\_mgmt\_core.opportunity\_viewer|Read access to all opportunity tables such as header and line items.|
|sn\_opty\_mgmt\_core.opportunity\_writer|Read access to all opportunity tables such as header and line items.|

## Quote Management roles

The roles in the following table apply to Quote Management.

|Role|Description|
|----|-----------|
|Sales Agent \[sn\_sales\_common.sales\_agent\]|Identifies, nurtures, and converts quotes into successful sales.|
|Sales Manager \[sn\_sales\_common.sales\_manager\]|Assigns quotes to sales agents or sales teams.|
|Sales Operation Specialist \[sn\_sales\_common.sales\_ops\_specialist\]|Enhances efficiency and accuracy in sales operations. Configures sales processes in sales operations.|

## Sales Agreement Management roles

<table id="table_wwg_4vy_hcc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sales Agent, Sales Manager, Data Viewer

 sn\_sales\_agmt\_core.sales\_agreement\_viewer

</td><td>

Read operations on sales agreements, sales agreement lines, and related data such as characteristics, price lists, and other tables.

</td></tr><tr><td>

Sales Agent, Sales Manager

 sn\_sales\_agmt\_core.sales\_agreement\_writer

</td><td>

Create, read, and update operations on sales agreements and sales agreement lines.

</td></tr></tbody>
</table>## Product Catalog Management roles

The roles in the following table apply to Product Catalog Management.

|Role|Description|
|----|-----------|
|Product Catalog Manager \[sn\_prd\_pm.product\_catalog\_manager\]|Create, read, update, and delete product, service, and resource specifications.|
|Product Catalog Admin \[sn\_prd\_pm.product\_catalog\_admin\]|Create, read, update, and delete product, service, resource specifications, characteristics, and characteristic options. Can also export and import catalog entities and set up any catalog-related system properties.|
|Product Catalog Viewer \[sn\_prd\_pm.product\_catalog\_viewer\]|Read access to product, service, resource specifications, characteristics, and characteristic options.|

## Pricing Management roles

The roles in the following table apply to Pricing Management.

|Role|Description|
|----|-----------|
|Price List Admin \[sn\_csm\_pricing.pricelist\_administrator\]|Create, update, and read pricing entities. Can also export and import pricing entities, set up or edit pricing-related system properties, and view transaction logs.|
|Price List Manager \[sn\_csm\_pricing.pricelist\_manager\]|Create, update, and read pricing entities.|
|Price List Writer \[sn\_csm\_pricing.pricelist\_writer\]|Granular role that has read, write, and delete access to pricing entities. To delete a pricing entity such as a price list or cost book, the pricing entity must be in Draft state.|
|Sales Agreement Price List Writer \[sn\_csm\_pricing.sales\_agreement\_pricelist\_writer\]|Granular role that has read and create access to pricing entities. Create access is granted only through back-end workflows. Write access only for Sales Agreement price lists. Inherited within the Sales Agreement Writer role.|
|Price List Viewer \[sn\_csm\_pricing.pricelist\_viewer\]|Granular role that has read access to pricing entities such as price lists, price list lines, cost books, cost book lines, attribute adjustments, and rule matrices.|
|Pricing integrator \[sn\_csm\_pricing.pricing\_integrator\]|Role required to access pricing features through the REST API.|

## Order Management roles

Order Management uses the roles in the following tables to control and manage access to the application features for Order Management, Service Order Management, and Fallout Management.

<table id="table_mph_dbq_11c"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order Fulfillment Manager \[sn\_ind\_tmt\_orm.order\_fulfillment\_manager\]

</td><td>

View and edit access to product orders, product order tasks, service orders, and resource orders. Fulfillment managers with this role can view, but not edit, order fallout records.The Order Fulfillment Manager receives orders, reviews order line items, checks that orders are ready for fulfillment, and then approves them.

</td></tr><tr><td>

Order Fulfillment Agent \[sn\_ind\_tmt\_orm.order-fulfillment\_agent\]

</td><td>

View access to product orders, product order tasks, service orders, and resource orders. Agents with this role can also view, but not edit, order fallout records, but they can edit some fields on the product order tasks. After the Order Fulfillment Manager approves an order, the agent performs these fulfillment tasks. This role also includes the Order Viewer \[order\_view\] role.

</td></tr><tr><td>

Order Approver \[order\_approver\]

</td><td>

View access to customer orders and product catalog data. Users with this role can approve customer orders but can't create, update, or delete an order like an Order Fulfillment Manager or Order Fulfillment Agent would do. This role also includes the Order Viewer \[order\_view\] role.

</td></tr><tr><td>

Order Viewer \[order\_viewer\]

</td><td>

View access to customer orders, product orders, product order tasks, service orders, and resource orders. You should also grant an order viewer with the sn\_prd\_pm.product\_catalog\_viewer role to access the product catalog data.

 **Note:** The order approver and order viewer roles are included in the Order Management Business Stakeholder role, which has a fee associated with it. Don’t assign these roles to users without confirming that your organization has the appropriate entitlement. To learn more, see Activate Business Stakeholder.

</td></tr><tr><td>

Fulfillment Viewer \[sn\_ind\_tmt\_orm.fulfillment\_viewer\]

</td><td>

Granular role that has read access to fulfillment tables: order tasks, domain orders, product orders, resource orders, and service orders.

</td></tr><tr><td>

Fulfillment Writer \[sn\_ind\_tmt\_orm.fulfillment\_ writer\]

</td><td>

Granular role that has read and write access to fulfillment tables: order tasks, domain orders, product orders, resource orders, and service orders. This role includes the Fulfillment Viewer \[sn\_ind\_tmt\_orm.fulfillment\_viewer\] role.

</td></tr><tr><td>

Order Agent \[sn\_ind\_tmt\_orm.order\_agent\]

</td><td>

A persona role with permissions to create, edit, view, and delete orders, order lines, and order line characteristics, as well as permissions to view tasks.

</td></tr><tr><td>

Order Admin \[sn\_ind\_tmt\_orm.order\_admin\]

</td><td>

A persona role with the same permissions as the Order Agent role \(create, edit, view, delete orders, order lines, and order line characteristics, and permissions to view tasks\). In addition, this role can configure and approve orders.

</td></tr></tbody>
</table><table id="table_oph_dbq_11c"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Order Manager \[sn\_ind\_tmt\_orm.service\_order\_manager\]

</td><td>

View and edit service order requests, service orders, resource orders, and related fulfillment tasks. A manager with this role can also view, but not edit, order fallout records.The Service Order Manager can review external service order requests, review service order line items, checks that service orders are ready for fulfillment, and then approve them.

</td></tr><tr><td>

Service Order Agent \[sn\_ind\_tmt\_orm.service\_order\_agent\]

</td><td>

View access to service order requests, service orders, resource orders, and related fulfillment tasks. Service Order Agents can edit some fields on the service order tasks. After the Service Order Fulfillment Manager approves a service order, the agent performs these tasks. This role also includes the Order Viewer \[order\_view\] role.

</td></tr></tbody>
</table><table id="table_lny_cnh_sbc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fallout Manager \[sn\_fallout\_mgmt.fallout\_manager\]

</td><td>

Create, view, assign, and edit fallout records. Managers with this role can also view order tasks and domain orders.

</td></tr><tr><td>

Fallout Agent \[sn\_fallout\_mgmt.fallout\_agent\]

</td><td>

View fallout records. Agents with this role can also update the state of fallout records and create work notes on them.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Sales Customer Relationship Management applications](som-configuring.md)

