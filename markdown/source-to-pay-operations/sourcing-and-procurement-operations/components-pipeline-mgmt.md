---
title: Components installed with Sourcing Pipeline Management
description: Several types of components are installed with activation of the Sourcing Pipeline Management \(sn\_spend\_pipeline\) plugin, including user roles and tables.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-11-17"
reading_time_minutes: 1
breadcrumb: [Sourcing Pipeline Management, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Components installed with Sourcing Pipeline Management

Several types of components are installed with activation of the Sourcing Pipeline Management \(sn\_spend\_pipeline\) plugin, including user roles and tables.

## Roles installed

<table id="table_u4x_m1n_3hc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_spend\_pipeline.pipeline\_management\_admin

</td><td>

Can configure the Pipeline project creation rule decision table to automate the creation of pipeline projects.

</td><td>

decision\_table\_admin

</td></tr><tr><td>

sn\_spend\_pipeline.sourcing\_pipeline\_user

</td><td>

Can view and access the Pipeline Management workspace.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_y4x_m1n_3hc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract to Pipeline project Relationships \(sn\_spend\_pipeline\_m2m\_contract\)

</td><td>

Stores the many-to-many relationships between contracts and pipeline projects.

</td></tr><tr><td>

Purchase order to Pipeline project Relationships \(sn\_spend\_pipeline\_m2m\_order\)

</td><td>

Stores the many-to-many relationships between purchase orders and pipeline projects.

</td></tr><tr><td>

Purchase requisition to Pipeline project Relationships\(sn\_spend\_pipeline\_m2m\_requisition\)

</td><td>

Stores the many-to-many relationships between purchase requisitions and pipeline projects.

</td></tr><tr><td>

Sourcing Request to Pipeline project Relationships\(sn\_spend\_pipeline\_m2m\_sourcing\_request\)

</td><td>

Stores the many-to-many relationships between sourcing requests and pipeline projects.

</td></tr><tr><td>

Supplier to Pipeline project Relationships\(sn\_spend\_pipeline\_m2m\_supplier\)

</td><td>

Stores the many-to-many relationships between suppliers and pipeline projects.

</td></tr><tr><td>

Pipeline Project\(sn\_spend\_pipeline\_project\)

</td><td>

Stores the pipeline projects.Extends the Task \(task\) table.

</td></tr></tbody>
</table>**Parent Topic:**[Sourcing Pipeline Management](../concept/spo-sourcing-pipeline-mgmt.md)

