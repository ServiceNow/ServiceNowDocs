---
title: Program table
description: The Program \[sn\_hcls\_program\] table stores the programs offered by healthcare organizations.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Program table

The Program \[sn\_hcls\_program\] table stores the programs offered by healthcare organizations.

## Key features

-   Extends the Product Specification \[sn\_prd\_pm\_product\_specification\] table to model all programs available from healthcare organizations.
-   Includes the program name, eligibility criteria, medication product, and duration of the program.

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

Option to indicate that the program is in use.

</td></tr><tr><td>

Eligibility criteria

</td><td>

Reference

</td><td>

Checklist associated with the program.

</td></tr><tr><td>

End Date

</td><td>

Date

</td><td>

End date of the program duration.

</td></tr><tr><td>

Medication product

</td><td>

List

</td><td>

Medication product associated with the program.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name of the program

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric identifier of the program.

 The value is auto-generated and is incremented every time you add a new program to an instance. The initial value for the **Number** field is PSSPG00001001.

**Note:** To customize the number, define the auto-numbering format for the Program \[sn\_hcls\_program\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Start Date

</td><td>

Date

</td><td>

Start date of the program duration.

</td></tr><tr><td>

State

</td><td>

String

</td><td>

Status of the program as **Draft** or **Published**.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Brief description of the program as would be shown on the case name created for the program.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

