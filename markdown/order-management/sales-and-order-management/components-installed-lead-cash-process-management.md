---
title: Components installed with Lead-to-Cash Process Management
description: Several types of components are installed with activation of the Lead-to-Cash Process Management plugin, including tables and user roles.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Lead-to-Cash Process Management reference, Order operations, Reference, Sales and Order Management]
---

# Components installed with Lead-to-Cash Process Management

Several types of components are installed with activation of the Lead-to-Cash Process Management plugin, including tables and user roles.

## Roles installed

<table id="table_pg1_qvg_vfc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Sales process record viewer

 \[sn\_l2c\_cockpit.sales\_process\_record\_viewer\]

</td><td>

Views tables related to the sales process record.

</td><td>

-   sn\_customerservice.csm\_workspace\_user
-   sn\_bo\_core.business\_process\_record\_viewer

</td></tr><tr><td>

Sales process record writer

 \[sn\_l2c\_cockpit.sales\_process\_record\_writer\]

</td><td>

Views and writes tables related to the sales process record.

</td><td>

-   sn\_l2c\_cockpit.sales\_process\_record\_viewer
-   sn\_bo\_core.business\_process\_record\_writer

</td></tr><tr><td>

Sales process manager

 \[sn\_l2c\_cockpit.sales\_process\_manager\]

</td><td>

Views, creates, and edits sales process records.

</td><td>

sn\_l2c\_cockpit.sales\_process\_record\_writer

</td></tr></tbody>
</table>## Tables installed

<table id="table_tg1_qvg_vfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sales Process Record

 \[sn\_l2c\_cockpit\_sales\_process\_record\]

</td><td>

Stores records used for monitoring sales-specific entities.

</td></tr></tbody>
</table>**Parent Topic:**[Lead-to-Cash Process Management reference](lead-cash-process-management-reference.md)

