---
title: Book appointment table
description: The Book appointment \[sn\_hcls\_book\_appt\_task\] table stores the task details for booking an appointment associated with a healthcare case or its extended case types.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Book appointment table

The Book appointment \[sn\_hcls\_book\_appt\_task\] table stores the task details for booking an appointment associated with a healthcare case or its extended case types.

## Key features

-   Extends the Healthcare task \[sn\_hcls\_task\] table to store task details created for appointment bookings associated with a healthcare case or its extended case types.
-   Includes the task number, short description, assignment group, patient, procedure, practitioner, parent case, and task status.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment group

</td><td>

Reference

</td><td>

Group of members that is assigned the appointment booking task.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the appointment booking task.

 The value is auto-generated and is incremented every time you add a new appointment booking task to your ServiceNow instance. The initial value for the **Number** field is APPTS00001001.

**Note:** To customize the number, define the auto-numbering format for the Book appointment \[sn\_hcls\_book\_appt\_task\] table. For more information, see [Add auto-numbering records in a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AutoNumberingRecordsInATable.md).

</td></tr><tr id="patient"><td>

Patient

</td><td>

Reference

</td><td>

Name of the patient.

</td></tr><tr><td>

Parent case

</td><td>

Reference

</td><td>

Healthcare case or its extended case types associated with the appointment booking task.

</td></tr><tr id="practitioner"><td>

Practitioner

</td><td>

Reference

</td><td>

Person added as the practitioner.

</td></tr><tr><td>

Procedure

</td><td>

Reference

</td><td>

Activity that is performed on, with, or for a patient as part of the appointment.

</td></tr><tr><td>

Short description

</td><td>

String

</td><td>

Brief description of the appointment booking task.

</td></tr><tr><td>

State

</td><td>

Choice list

</td><td>

Status of the appointment booking task.

 The following task statuses for an appointment booking are available by default:

-   Canceled
-   Completed
-   Requested

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

