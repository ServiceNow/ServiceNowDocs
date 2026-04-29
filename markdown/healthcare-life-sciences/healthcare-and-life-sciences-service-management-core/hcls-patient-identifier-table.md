---
title: Patient identifier table
description: The Patient identifier \[sn\_hcls\_patient\_identifier\] table stores the identification details of a patient.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Patient identifier table

The Patient identifier \[sn\_hcls\_patient\_identifier\] table stores the identification details of a patient.

## Key features

Stores the various patient identifiers associated with a patient in your healthcare organization.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_rkd_g4t_mpb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

String

</td><td>

Patient ID number associated with the patient name.

 This field is read-only.

</td></tr><tr><td>

Value

</td><td>

String

</td><td>

The value of the associated identifier type. For example, if Health Insurance ID is selected in the identifier type field, the value here should reflect the patient's health insurance ID number or code.

</td></tr><tr><td>

Identifier type

</td><td>

Choice list

</td><td>

The type of patient identifier indicated. Options are:

-   Medical Record Number
-   Social Security Number
-   Health Insurance ID
-   Driver's Licence
-   Passport Number
-   Biometric Identifiers

</td></tr><tr><td>

Identifier system

</td><td>

String

</td><td>

The system associated with this patient identifier.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

The associated patient name as indicated on the patient record.

</td></tr><tr><td>

Valid from

</td><td>

Date/time

</td><td>

The date from which this identifier is considered valid.

</td></tr><tr><td>

Valid to

</td><td>

Date/time

</td><td>

The date at which this identifier expires.

</td></tr><tr><td>

Issuing authority

</td><td>

String

</td><td>

The authority or agency that issued this patient identifier.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

