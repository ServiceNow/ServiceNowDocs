---
title: Components installed with Business Object Core
description: Several types of components are installed with activation of the Business Object Core plugin, including tables and user roles.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Lead-to-Cash Process Management reference, Sales Customer Relationship Management]
---

# Components installed with Business Object Core

Several types of components are installed with activation of the Business Object Core plugin, including tables and user roles.

## Roles installed

<table id="table_kff_jgh_vfc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Business object viewer

 \[sn\_bo\_core.business\_object\_viewer\]

</td><td>

Views tables related to a business object.

</td><td>

-   sn\_quote\_mgmt\_core.quote\_viewer
-   sn\_ind\_tmt\_orm.order\_viewer
-   sn\_opty\_mgmt\_core.opportunity\_viewer

</td></tr><tr><td>

Business process record viewer

 \[sn\_bo\_core.business\_process\_record\_viewer\]

</td><td>

Views tables related to the business process record.

</td><td>

sn\_bo\_core.business\_object\_viewer

</td></tr><tr><td>

Business process record writer

 \[sn\_bo\_core.business\_process\_record\_writer\]

</td><td>

Views and writes tables related to the business process record.

</td><td>

sn\_bo\_core.business\_process\_record\_viewer

</td></tr><tr><td>

Business object writer

 \[sn\_bo\_core.business\_object\_writer\]

</td><td>

Views and writes tables related to a business object.

</td><td>

sn\_bo\_core.business\_object\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_off_jgh_vfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business Process Resource

 \[sn\_bo\_core\_process\_resource\]

</td><td>

Tracks the objects and documents associated with a business process.

</td></tr><tr><td>

Business Object Relationship

 \[sn\_bo\_core\_obj\_rel\]

</td><td>

Indicates how entities are structurally connected within a process and outlines the relationships between different business object types. For example, a lead is linked to an opportunity through the **Lead** column in the Opportunity \[sn\_sales\_opportunity\] table.

</td></tr><tr><td>

Business Object Group Members

 \[sn\_bo\_core\_obj\_group\_members\]

</td><td>

Defines the relationship between business object groups and their corresponding object types, specifying which entities belong to each group.

</td></tr><tr><td>

Business Process Task

 \[sn\_bo\_core\_process\_task\]

</td><td>

Tracks individual tasks within a process.

</td></tr><tr><td>

Business Object Type

 \[sn\_bo\_core\_obj\_type\]

</td><td>

Contains the entities involved in a process and its table. For example, for order-to-cash group, the entities can be lead, opportunity, quote, order, and their respective tables.

</td></tr><tr><td>

Business Process Record

 \[sn\_bo\_core\_process\_record\]

</td><td>

Stores records that are used for monitoring various business entities.

</td></tr><tr><td>

Business Object Group

 \[sn\_bo\_core\_obj\_group\]

</td><td>

Represents the logical grouping of entities involved in a process and the category for different types of business entities.

</td></tr></tbody>
</table>**Parent Topic:**[Lead-to-Cash Process Management reference](lead-cash-process-management-reference.md)

