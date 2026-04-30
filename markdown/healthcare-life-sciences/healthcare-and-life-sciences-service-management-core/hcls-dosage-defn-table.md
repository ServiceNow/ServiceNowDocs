---
title: Dosage definition table
description: The Dosage definition \[sn\_hcls\_dosage\_definition\] table models the Dosage specification \[sn\_hcls\_dosage\_specification\] table for use as a request definition parameter.
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Healthcare and Life Sciences data model tables, Healthcare and Life Sciences Service Management Core reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Dosage definition table

The Dosage definition \[sn\_hcls\_dosage\_definition\] table models the Dosage specification \[sn\_hcls\_dosage\_specification\] table for use as a request definition parameter.

## Key features

-   Extends the Request Definition \[sn\_ind\_request\_definition\] table.
-   References the Dosage specification \[sn\_hcls\_dosage\_specification\] table.
-   Includes the medication prescription details, dosage specification publishing status, program associated with the dosage specification, and diagnosis details as stored in the Dosage specification \[sn\_hcls\_dosage\_specification\] table.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_jfm_xnv_gtb"><thead><tr><th>

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

Option for enabling the dosage specification.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Additional information about the dosage specification.

</td></tr><tr><td>

Dosage definition

</td><td>

Reference

</td><td>

Models the Dosage specification \[sn\_hcls\_dosage\_specification\] table.

</td></tr><tr><td>

Medication product

</td><td>

Reference

</td><td>

Medication product being prescribed for the patient.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name to identify the dosage specification.

</td></tr><tr><td>

Primary diagnosis

</td><td>

Reference

</td><td>

Main condition in a patient submitted by the practitioner as the reason for the healthcare service requested.

</td></tr><tr><td>

Program

</td><td>

Reference

</td><td>

Program associated with the medication product,

</td></tr><tr><td>

Secondary diagnosis

</td><td>

Reference

</td><td>

Coexisting condition that might exist in a patient submitted by the practitioner.

</td></tr><tr><td>

State

</td><td>

String

</td><td>

Status of the dosage specification.

 If you have not published the dosage specification, this field is automatically set to **Draft**. If you have already published the dosage specification, this field is automatically set to **Published**.

</td></tr><tr><td>

Tertiary diagnosis

</td><td>

Reference

</td><td>

Highly specialized medical care recommended for the patient by the practitioner.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

