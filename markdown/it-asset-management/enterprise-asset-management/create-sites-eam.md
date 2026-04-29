---
title: Create sites in the Enterprise Asset Management
description: Create a site for asset groups in the Enterprise Asset Management application.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Asset Management, IT Asset Management]
---

# Create sites in the Enterprise Asset Management

Create a site for asset groups in the Enterprise Asset Management application.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

For detailed information on what sites are and how are they used in asset groups, see [Asset groups in Enterprise Asset Management](../concept/asset-groups-eam.md).

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Enterprise asset estate** &gt; **Asset groups**.

2.  Select **Sites**.

3.  Select **New** to open the Create New Equipment Model Entity page.

4.  On the form, fill in the fields.

<table id="table_znn_d4d_mfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity name

</td><td>

Name of the equipment model entity.

</td></tr><tr><td>

Short code

</td><td>

Short code that is assigned to this equipment model entity.

</td></tr><tr><td>

Parent

</td><td>

Parent of the entity. Once a parent is selected, the **Template** field is automatically populated

</td></tr><tr><td>

Path

</td><td>

Auto-generated based on the short code and the hierarchy.

</td></tr><tr><td>

Template

</td><td>

The template that defines the hierarchy of the parent according to the ISA-95 hierarchical entity model.

</td></tr><tr><td>

Location

</td><td>

Location of the equipment model entity. For example, Atlanta Building 64 would be the location for each associated equipment model that is located there.

</td></tr><tr><td>

Level

</td><td>

The hierarchical levels of a site with site being at the highest level, followed by area, work center, and work unit.

</td></tr><tr><td>

Site

</td><td>

Refers to an ISA-95 hierarchical entity model. Sites are entity records in the Equipment Model Entity \[cmdb\_ci\_ot\_isa\_entity\] table, organized in a hierarchical structure.

</td></tr><tr><td>

Company

</td><td>

Name of the company that this entity belongs to.

</td></tr><tr><td>

Business Unit

</td><td>

Business unit of the company that this entity belongs to.

</td></tr><tr><td>

Short Description

</td><td>

A description of the site entity.

</td></tr><tr><td>

Assigned to

</td><td>

The person primarily responsible for the entity.

</td></tr><tr><td>

Support group

</td><td>

The group to contact if you encounter any issues with the entity.

</td></tr><tr><td>

Managed by

</td><td>

Name of the assigned person who owns and is responsible for managing this entity.

</td></tr><tr><td>

Managed by group

</td><td>

The group who maintains the entity.

</td></tr><tr><td>

Process criticality

</td><td>

Measure of how critical, or important, the equipment model entity is to the process. Select the process criticality for the entity. For example:-   1 - most critical.
-   2 - somewhat critical.


</td></tr><tr><td>

Operational status

</td><td>

Current operational status of the entity:-   **Operational**: Entity that is fully operational in the production process.
-   **Non-Operational**: Entity that is non-operational in the production process.


</td></tr></tbody>
</table>5.  Select **Save**.

    The newly created site appears in the Sites tab.


