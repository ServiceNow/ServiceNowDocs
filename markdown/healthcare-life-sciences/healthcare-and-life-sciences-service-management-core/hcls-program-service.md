---
title: Program service table
description: The Program service \[sn\_hcls\_program\_service\] table stores the program services associated with a program.
locale: en-US
release: zurich
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Program service table

The Program service \[sn\_hcls\_program\_service\] table stores the program services associated with a program.

## Key features

-   Extends the Product Specification \[sn\_prd\_pm\_product\_specification\] table to model all program services available within a program.
-   Includes the program service name and duration of the program service.

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

Option to indicate that the program service is in use.

</td></tr><tr><td>

End Date

</td><td>

Date

</td><td>

End date of the program service duration.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name of the program service

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric identifier of the program service.

 The value is auto-generated and is incremented every time you add a new program service to an instance. The initial value for the **Number** field is PGSRV00001001.

**Note:** To customize the number, define the auto-numbering format for the Program service \[sn\_hcls\_program\_service\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Start Date

</td><td>

Date

</td><td>

Start date of the program service duration.

</td></tr><tr><td>

State

</td><td>

String

</td><td>

Status of the program service as **Draft** or **Published**.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Brief description of the program service.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

