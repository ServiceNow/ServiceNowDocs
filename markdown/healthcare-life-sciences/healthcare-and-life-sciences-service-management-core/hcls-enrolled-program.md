---
title: Enrolled Program table
description: The Enrolled Program \[sn\_hcls\_enrolled\_program\] table stores the programs that a patient has been enrolled into.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Enrolled Program table

The Enrolled Program \[sn\_hcls\_enrolled\_program\] table stores the programs that a patient has been enrolled into.

## Key features

-   Extends the Install base item \[sn\_install\_base\_item\] table to all supported enrolled programs.
-   Stores the enrolled programs sold to a patient.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_uvk_nh1_drb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date Enrolled

</td><td>

Date

</td><td>

Date when the patient was enrolled into the program.

</td></tr><tr><td>

Date Requested

</td><td>

Date

</td><td>

Date when the patient requested to be enrolled into the program.

</td></tr><tr><td>

State

</td><td>

Integer

</td><td>

State of the enrollment program.

 State is one of the following types:

-   Canceled
-   Enrolled
-   Fulfilled
-   Pending fulfillment
-   Rejected
-   Requested

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the enrolled program.

 The value is auto-generated and is incremented every time you add a new observation to your ServiceNow instance. The initial value for the **Number** field is ENPG00001001.

**Note:** To customize the number, define the auto-numbering format for the Enrolled Program \[sn\_hcls\_enrolled\_program\] table. For more information, see Add auto-numbering records in a table.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Consumer that is enrolled into the program as a patient.

</td></tr><tr><td>

Program Name

</td><td>

Reference

</td><td>

Name to identify the enrolled program.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

