---
title: Program relationship table
description: The Program relationship \[sn\_hcls\_program\_relationship\] table stores the association details between a program and program service.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Program relationship table

The Program relationship \[sn\_hcls\_program\_relationship\] table stores the association details between a program and program service.

## Key features

-   Extends the Specification Relationship \[sn\_prd\_pm\_specification\_relationship\] table to define the relationship between a program and program service.
-   Includes the relationship name, program, program service, and relationship type.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_uvk_nh1_drb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

True/False

</td><td>

Option to indicate that the association between a program and a program service is in use.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name of the relationship between a program and a program service.

</td></tr><tr><td>

Source Specification

</td><td>

Reference

</td><td>

Program included in the relationship.

</td></tr><tr><td>

Target Specification

</td><td>

Reference

</td><td>

Program service included in the relationship.

</td></tr><tr><td>

Relationship Type

</td><td>

String

</td><td>

Relationship type between program and program services.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

