---
title: Healthcare organization table
description: The Healthcare organization \[sn\_hcls\_organization\] table stores the details of a healthcare organization in your ServiceNow instance.
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Healthcare and Life Sciences data model tables, Healthcare and Life Sciences Service Management Core reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Healthcare organization table

The Healthcare organization \[sn\_hcls\_organization\] table stores the details of a healthcare organization in your ServiceNow instance.

## Key features

-   Models healthcare organizations of different types including providers and payers.
-   Other healthcare organizations can be nested within while also being associated with multiple healthcare locations.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_egs_nss_mpb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business location

</td><td>

Reference

</td><td>

The associated business location.

</td></tr><tr><td>

Identifier

</td><td>

String

</td><td>

The associated identifier of the patient.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name to identify the healthcare organization.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Patient ID number associated with the patient’s name.

 This field is read-only.

</td></tr><tr><td>

Organization type

</td><td>

Choice list

</td><td>

Type of healthcare organization you represent.

 The following types are available by default:

-   Clinical research sponsor
-   Community group
-   Educational institute
-   Government
-   Healthcare provider
-   Hospital department
-   Non-healthcare business
-   Organizational team
-   Other
-   Payer
-   Pharmaceutical company
-   Religious institution

 For more information about the available organization types, see [organization types](https://www.hl7.org/fhir/valueset-organization-type.html) defined in the FHIR specifications.

</td></tr><tr><td>

Parent

</td><td>

Reference

</td><td>

Parent organization associated with the organization.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

