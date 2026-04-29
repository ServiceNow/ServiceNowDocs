---
title: Medication Prescription form
description: The Medication Prescription form includes the details of the prescription ordered for a patient.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Medication Prescription form

The Medication Prescription form includes the details of the prescription ordered for a patient.

<table id="table_ut3_b5r_crb"><thead><tr><th>

Field

</th><th>

Description

</th></tr><tr class="sub-head"><th colspan="2">

Medication Prescription

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated number for the prescription.

</td></tr><tr><td>

Patient

</td><td>

Name of the patient to whom the medication will be given.

</td></tr><tr><td>

Medication product

</td><td>

Medication product being prescribed for the patient.

</td></tr><tr><td>

Practitioner

</td><td>

Name of the practitioner who ordered the prescription for the patient.

</td></tr><tr><td>

Prior prescription

</td><td>

Prescription ordered earlier for the patient.

</td></tr><tr><td>

Reference Medication event

</td><td>

Encounter that identifies the occurrence of contact between patient and healthcare provider.

</td></tr><tr><td>

Organization

</td><td>

Healthcare provider that is responsible for the prescription.

</td></tr><tr><td>

Dosage specification

</td><td>

Dosage specification for the patient.

 **Note:** This field is set as mandatory only when a program is associated with the case. In this case, the medication prescription is entered according to the dosage specification published for the program.

</td></tr><tr><td>

Status

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

Explanation of the selected status.

</td></tr><tr><td>

Priority

</td><td>

Urgency of the prescription that is used to make informed decision if needing to be prioritized.

</td></tr><tr><td>

Date authored

</td><td>

Date and time when the prescription was written.

</td></tr><tr><td>

Validity start date

</td><td>

Earliest time of the validity period of the prescription.

</td></tr><tr><td>

Validity end date

</td><td>

Latest time of the validity period of the prescription.

</td></tr><tr><td>

External ID

</td><td>

Identifier of the record in an electronic medical record \(EMR\) system.

</td></tr><tr><td>

Case

</td><td>

Enrollment case associated with the prescription.

</td></tr><tr><td class="sub-head" colspan="2">

Diagnosis details

</td></tr><tr><td colspan="2">

When a program is associated with the case, each field in this section is automatically set to its corresponding value included in the program.

</td></tr><tr><td>

Primary diagnosis

</td><td>

Main condition in a patient submitted by the practitioner as the reason for the healthcare service requested.

</td></tr><tr><td>

Tertiary diagnosis

</td><td>

Highly specialized medical care recommended for the patient by the practitioner.

</td></tr><tr><td>

Secondary diagnosis

</td><td>

Coexisting condition that might exist in a patient submitted by the practitioner.

</td></tr><tr><td class="sub-head" colspan="2">

Dosage characteristics

</td></tr><tr><td colspan="2">

This section appears only when a dosage specification is associated with the medication prescription. The section displays dosage characteristics configured by your administrator for the selected dosage specification.

</td></tr><tr><td class="sub-head" colspan="2">

Dosage details

</td></tr><tr><td colspan="2">

This section is automatically populated when a dosage specification is selected for the medication prescription. The fields within this section are read-only and populated corresponding to their dosage characteristics. When no dosage specification is selected, the section displays the value as entered by a healthcare representative.

</td></tr><tr><td>

Dosage

</td><td>

Recommendation of the medication dosage.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of the specified medication in one fill.

</td></tr><tr><td>

Number of authorized refills

</td><td>

Number of authorized refills for the medication.

</td></tr><tr><td>

Instructions for patient

</td><td>

Instructions for the dosage of the medication product.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences Service Management Core reference](hcls-serv-mgmt-core-reference.md)

