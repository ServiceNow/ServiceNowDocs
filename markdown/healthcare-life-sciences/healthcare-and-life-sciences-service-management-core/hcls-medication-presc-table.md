---
title: Medication Prescription table
description: The Medication Prescription \[sn\_hcls\_medication\_prescription\] table stores the information about prescriptions ordered for a patient.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Medication Prescription table

The Medication Prescription \[sn\_hcls\_medication\_prescription\] table stores the information about prescriptions ordered for a patient.

## Key features

Includes the medication prescription details, prescription status, dosage, and diagnosis details.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case

</td><td>

Reference

</td><td>

Parent case associated with the medication prescription.

</td></tr><tr><td>

Days supply

</td><td>

Integer

</td><td>

Number of days for which the medication is prescribed.

</td></tr><tr><td>

Date authored

</td><td>

Date/Time

</td><td>

Date and time when the prescription was written.

</td></tr><tr><td>

Dosage instructions

</td><td>

String

</td><td>

Instructions for the dosage of the medication product.

</td></tr><tr><td>

External identifier

</td><td>

String

</td><td>

Identifier of the record in an electronic medical record \(EMR\) system.

</td></tr><tr><td>

Medication product

</td><td>

Reference

</td><td>

Medication product being prescribed for the patient.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the enrolled program.

 The value is auto-generated and is incremented every time you add a new observation to your ServiceNow instance. The initial value for the **Number** field is MEDPR00001001.

**Note:** To customize the number, define the auto-numbering format for the Medication Prescription \[sn\_hcls\_medication\_prescription\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Organization

</td><td>

Reference

</td><td>

Healthcare provider that is responsible for the prescription.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Name of the patient to whom the medication will be given.

</td></tr><tr><td>

Practitioner

</td><td>

Reference

</td><td>

Name of the practitioner who ordered the prescription for the patient.

</td></tr><tr><td>

Primary diagnosis

</td><td>

Reference

</td><td>

Main condition in a patient submitted by the practitioner as the reason for the healthcare service requested.

</td></tr><tr><td>

Prior prescription

</td><td>

Reference

</td><td>

Prescription ordered earlier for the patient.

</td></tr><tr><td>

Priority

</td><td>

Choice list

</td><td>

Urgency of the prescription that is used to make informed decision if needing to be prioritized.

</td></tr><tr><td>

Quantity

</td><td>

Decimal

</td><td>

Quantity of the specified medication in one fill.

</td></tr><tr><td>

Reference Medication event

</td><td>

Reference

</td><td>

Encounter that identifies the occurrence of contact between patient and healthcare provider.

</td></tr><tr><td>

Refills

</td><td>

Integer

</td><td>

Number of authorized refills for the medication.

</td></tr><tr><td>

Secondary diagnosis

</td><td>

Reference

</td><td>

Coexisting condition that might exist in a patient submitted by the practitioner.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Status

</td><td>

Choice list

</td><td>

Status of the ordered prescription.

 The following statuses are available by default:

-   Active
-   Draft
-   Cancelled
-   Completed
-   Entered in error
-   Expired
-   On-Hold
-   Stopped
-   Unknown

 For more information about the available statuses, see [medication prescription statuses](https://www.hl7.org/fhir/http://www.hl7.org/fhir/2015may/medication-prescription-status.html) defined in the FHIR specifications.

</td></tr><tr><td>

Status reason

</td><td>

String

</td><td>

Explanation of the selected status.

</td></tr><tr><td>

Tertiary diagnosis

</td><td>

Reference

</td><td>

Highly specialized medical care recommended for the patient by the practitioner.

</td></tr><tr><td>

Validity start date

</td><td>

Date

</td><td>

Earliest time of the validity period of the prescription.

</td></tr><tr><td>

Validity end date

</td><td>

Date

</td><td>

Latest time of the validity period of the prescription.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

