---
title: View a table hierarchy and the extension model
description: Determine the extension model used by a table.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Table flattening, Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# View a table hierarchy and the extension model

Determine the extension model used by a table.

## Before you begin

Role required: admin

## About this task

The extension model used by a table is not immediately apparent. While a hierarchy can use a single physical table, the platform displays tables as if each logical table has a unique physical table. For example, when specifying a table for a workflow, you can select Change \[change\_request\] or Incident \[incident\] even though the parent table, Task \[task\], uses a single physical table.

Administrators can view the status of flattened table hierarchies, but cannot flatten additional hierarchies. You can [configure the form](../../form-administration/concept/configure-form-layout.md#) to add the **Extension model** field if necessary.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select a table record.

3.  Review the **Extension model** field value, which indicates whether the table hierarchy uses multiple unique tables or a single flat table.

    -   **None**: Indicates that the table uses the table per class model. Defines a unique physical table per logical table in a hierarchy. For example, there are separate physical tables for the Asset \[alm\_asset\] table, and its child tables: Hardware \[alm\_hardware\], Consumable \[alm\_consumable\], Facility \[alm\_facility\], and Software License \[alm\_license\].

        **Note:** If a table has an empty Extension Model field, it is not necessarily a Table Per Class table. If the table extends another table, it actually inherits the model from any parent tables it is extending, and only when none of the parents have a defined extension model is the table’s extension model Table Per Class. This can be seen on many tables that extend the Task table. Incident is a logical table that extends Task and is physically located on Task, but by default has a blank Extension Model value.

        When a table doesn’t extend anything at all, and has a blank Extension Model field, it is a Table Per Class table.

    -   **Table per hierarchy**: Defines a single physical table per logical table hierarchy. For example, there is a single Task \[task\] table on the MySQL database that contains all the Task, Incident, Problem and Change records. This single physical table is represented as separate logical tables.

**Parent Topic:**[Table flattening](../concept/c_TaskTableFlattening.md)

