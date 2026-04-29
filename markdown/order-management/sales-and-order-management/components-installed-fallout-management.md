---
title: Components installed Fallout Management
description: Several types of components are installed with activation of the Fallout Management plugin, including tables and user roles.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order Management reference, Reference, Sales and Order Management]
---

# Components installed Fallout Management

Several types of components are installed with activation of the Fallout Management plugin, including tables and user roles.

## Roles installed

<table id="table_bxk_4wy_pgc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Fallout Manager

 \[sn\_fallout\_mgmt.fallout\_manager\]

</td><td>

Creates, views, assigns, and edits fallout records. A user with this role can also view order tasks and domain orders.

</td><td>

sn\_fallout\_mgmt.fallout\_agent

</td></tr><tr><td>

Fallout Agent

 \[sn\_fallout\_mgmt.fallout\_agent\]

</td><td>

Views order fallout records. A user with this role can also update the state of fallout records and create work notes on them. The user can also view task and domain orders.

</td><td>

-   sn\_fallout\_mgmt.fallout\_creator
-   sn\_customerservice.case\_viewer

</td></tr><tr><td>

Fallout viewer

</td><td>

Views order fallout records. A user with this role can also update the state of fallout records and view order tasks and domain orders.

</td><td>

-   sn\_ind\_tmt\_orm.order\_viewer
-   agent\_workspace\_user

</td></tr><tr><td>

Fallout Creator

</td><td>

Creates fallout records.

</td><td>

None.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fxk_4wy_pgc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fallout

 \[sn\_fallout\_mgmt\_fallout\]

</td><td>

Tracks order processing or fulfillment exceptions that require monitoring and resolution. 

</td></tr><tr><td>

Fallout type

 \[sn\_fallout\_mgmt\_fallout\_type\]

</td><td>

Defines categories of fallout to classify order processing or fulfillment exceptions.

</td></tr></tbody>
</table>**Parent Topic:**[Order Management reference](order-mgt-reference.md)

