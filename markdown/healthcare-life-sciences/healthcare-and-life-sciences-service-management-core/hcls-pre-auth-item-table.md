---
title: Pre-authorization item table
description: The Pre-authorization item \[sn\_hcls\_pre\_auth\_item\] table stores the details of items pertaining to a pre-authorization request for healthcare services.
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Healthcare and Life Sciences data model tables, Healthcare and Life Sciences Service Management Core reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Pre-authorization item table

The Pre-authorization item \[sn\_hcls\_pre\_auth\_item\] table stores the details of items pertaining to a pre-authorization request for healthcare services.

## Key features

-   Stores item information related to pre-authorization requests and pre-authorization diagnoses.
-   Includes the item order, associated pre-authorization request, and procedure code.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_awf_rm2_rvb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pre-authorization request

</td><td>

Reference

</td><td>

Associated pre-authorization request number.

</td></tr><tr><td>

Item order

</td><td>

String

</td><td>

The item being ordered.

</td></tr><tr><td>

Procedure code

</td><td>

Reference

</td><td>

Code to identify the specific procedure. Code is based on the Current Procedural Terminology \(CPT\) or Healthcare Common Procedure Coding System \(HCPCS\) coding system.

 For more information about the available codes, see [procedure codes](https://www.hl7.org/fhir/valueset-procedure-code.html) defined in the FHIR specifications.

</td></tr><tr><td>

Start date

</td><td>

Date

</td><td>

Expected item start date. For example, a treatment's start date.

</td></tr><tr><td>

End date

</td><td>

Date

</td><td>

Expected item end date. For example, a treatment's end date.

</td></tr><tr><td>

Remarks

</td><td>

String

</td><td>

Comments or additional information about the pre-authorization item.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

