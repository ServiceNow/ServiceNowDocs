---
title: Enrolled Program Service table
description: The Enrolled Program Service \[sn\_hcls\_enrolled\_program\_service\] table stores the program services provided to a patient as part of a program enrollment process.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Enrolled Program Service table

The Enrolled Program Service \[sn\_hcls\_enrolled\_program\_service\] table stores the program services provided to a patient as part of a program enrollment process.

## Key features

-   Extends the Install base item \[sn\_install\_base\_item\] table to all supported enrolled program services.
-   Stores the enrolled program services sold to a patient.

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

Date when the patient was enrolled into the program service.

</td></tr><tr><td>

Date fulfilled

</td><td>

Date

</td><td>

Date when the service was fulfilled for the patient.

</td></tr><tr><td>

Date requested

</td><td>

Date

</td><td>

Date when the service was requested by the patient.

</td></tr><tr><td>

State

</td><td>

Integer

</td><td>

State of the enrollment program service.

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

Alpha-numeric profile identifier of the enrolled program service.

 The value is auto-generated and is incremented every time you add a new observation to your ServiceNow instance. The initial value for the **Number** field is ENSRV00001001.

**Note:** To customize the number, define the auto-numbering format for the Enrolled Program Service \[sn\_hcls\_enrolled\_program\_service\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Consumer or account that is enrolled into the program as a patient.

</td></tr><tr><td>

Program service

</td><td>

Reference

</td><td>

Name to identify the enrolled program service.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

