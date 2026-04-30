---
title: Appointment table
description: The Appointment \[sn\_hcls\_appointment\] table stores the appointment booking details for a patient in your healthcare organization.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data Model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Appointment table

The Appointment \[sn\_hcls\_appointment\] table stores the appointment booking details for a patient in your healthcare organization.

## Key features

-   Stores any appointments associated with the patient.
-   Includes the appointment type, status, service type, service category, start and end times, priority, location, and practitioner.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Actual end time

</td><td>

Date/Time

</td><td>

Actual end date and time of the appointment.

</td></tr><tr><td>

Actual start time

</td><td>

Date/Time

</td><td>

Actual start date and time of the appointment.

</td></tr><tr><td>

Additional comments

</td><td>

String

</td><td>

Detailed or expanded information to support the appointment provided when making the appointment.

</td></tr><tr><td>

Appointment Id

</td><td>

String

</td><td>

Identifier of the appointment entered in the electronic medical records \(EMR\) system.

</td></tr><tr><td>

Appointment status

</td><td>

Choice list

</td><td>

Status of an appointment.

 The following statuses are available by default:

-   Arrived
-   Booked
-   Cancelled
-   Checked in
-   Entered in error
-   Fulfilled
-   No show
-   Pending
-   Proposed
-   Waitlist

 For more information about the available statuses, see [appointment statuses](https://www.hl7.org/fhir/valueset-appointmentstatus.html) defined in the FHIR specifications.

</td></tr><tr><td>

Appointment type

</td><td>

Choice list

</td><td>

Style of appointment or patient that has been booked in the slot.

 The following types are available by default:

-   Checkup
-   Emergency
-   Follow up
-   Routine
-   Walkin

 For more information about the appointment types, see [appointment types](https://www.hl7.org/fhir/v2/0276/index.html) defined in the FHIR specifications.

</td></tr><tr><td>

Case

</td><td>

Reference

</td><td>

Case associated with this appointment.

</td></tr><tr><td>

Condition

</td><td>

Reference

</td><td>

Condition associated with the appointment.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Brief description of the appointment as would be shown on a subject line in a meeting request, or appointment list.

</td></tr><tr><td>

Duration of the appointment

</td><td>

Duration

</td><td>

Actual duration of the appointment.

</td></tr><tr><td>

Location

</td><td>

Reference

</td><td>

Location of the appointment.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the appointment.

 The value is auto-generated and is incremented every time you add a new appointment to your ServiceNow instance. The initial value for the **Number** field is APPT00001001.

**Note:** To customize the number, define the auto-numbering format for the Appointment \[sn\_hcls\_appointment\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Observation

</td><td>

Reference

</td><td>

Observation associated with the appointment.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Name of the patient.

</td></tr><tr><td>

Patient Instructions

</td><td>

String

</td><td>

Patient-facing information about the appointment.

 For example, request to bring a referral or fast from 8 p.m. the night before.

</td></tr><tr><td>

Practitioner

</td><td>

Reference

</td><td>

Person added as the practitioner.

 Practitioners associated with an appointment are referenced in the Appointment participant \[sn\_hcls\_appointment\_participant\] table.

</td></tr><tr><td>

Priority

</td><td>

Reference

</td><td>

Urgency of the appointment that is used to make informed decisions if needing to reprioritize.

</td></tr><tr><td>

Procedure

</td><td>

Reference

</td><td>

Activity that is performed on, with, or for a patient as part of the appointment.

</td></tr><tr><td>

Requested end time

</td><td>

Date/Time

</td><td>

Proposed end date and time of the appointment requested by the patient.

</td></tr><tr><td>

Requested start time

</td><td>

Date/Time

</td><td>

Proposed start date and time of the appointment requested by the patient.

</td></tr><tr><td>

Service category

</td><td>

Reference

</td><td>

Broad category of the service that is to be performed during this appointment.

 For more information about the service categories, see [service categories](https://www.hl7.org/fhir/valueset-service-category.html) defined in the FHIR specifications.

</td></tr><tr><td>

Service type

</td><td>

Reference

</td><td>

Specific service that is to be performed during this appointment.

 For more information about the service types, see [service types](https://www.hl7.org/fhir/valueset-service-type.html) defined in the FHIR specifications.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Specialty

</td><td>

Reference

</td><td>

Specialty of a practitioner that would be required to perform the service requested in this appointment.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

