---
title: Encounter table
description: The Encounter \[sn\_hcls\_encounter\] table stores the information about an interaction between a patient and healthcare providers for providing healthcare services or assessing the health status of a patient.
locale: en-US
release: zurich
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Encounter table

The Encounter \[sn\_hcls\_encounter\] table stores the information about an interaction between a patient and healthcare providers for providing healthcare services or assessing the health status of a patient.

## Key features

-   Stores any encounters that a patient has undergone with any practitioner.
-   Includes the encounter type, service type, practitioner, location of the encounter, and start and end times of the encounter.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Appointment

</td><td>

Reference

</td><td>

Appointment marked as fulfilled and linked to the encounter.

</td></tr><tr><td>

Duration

</td><td>

Duration

</td><td>

Time during the encounter that the participant participated.

 This field is automatically set to the duration between **Start time** and **End time** of an encounter.

</td></tr><tr><td>

Encounter type

</td><td>

Reference

</td><td>

Type of encounter.

</td></tr><tr><td>

End time

</td><td>

Date/Time

</td><td>

Date and time when the participation of a patient in the encounter ended.

</td></tr><tr><td>

External id

</td><td>

String

</td><td>

Identifier of the record in an electronic medical record \(EMR\) system.

</td></tr><tr><td>

Location

</td><td>

Reference

</td><td>

Healthcare location where the encounter takes place.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the encounter.

 The value is auto-generated and is incremented every time you add a new encounter to your ServiceNow instance. The initial value for the **Number** field is ENC00001001.

**Note:** To customize the number, define the auto-numbering format for the Encounter \[sn\_hcls\_encounter\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Parent encounter

</td><td>

Reference

</td><td>

Parent healthcare event associated with the encounter.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Patient involved in the encounter.

</td></tr><tr><td>

Practitioner

</td><td>

Reference

</td><td>

Practitioner involved in the encounter.

</td></tr><tr><td>

Priority type

</td><td>

Reference

</td><td>

Urgency of the encounter that is used to make informed decisions if needing to reprioritize.

</td></tr><tr><td>

Service provider

</td><td>

Reference

</td><td>

Healthcare organization responsible for the services included in the encounter.

</td></tr><tr><td>

Service type

</td><td>

Reference

</td><td>

Broad category of the service that is to be provided.

 For more information about the available types, see [service types](https://www.hl7.org/fhir/valueset-service-type.html) defined in the FHIR specifications.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Start time

</td><td>

Date/Time

</td><td>

Date and time when the participation of a patient in the encounter began.

</td></tr><tr><td>

Status

</td><td>

Choice list

</td><td>

Status of the encounter.

 The following statuses are available by default:

-   Arrived
-   Cancelled
-   Entered in error
-   Finished
-   In progress
-   On leave
-   Planned
-   Triaged
-   Unknown

 For more information about the available statuses, see [encounter statuses](https://www.hl7.org/fhir/valueset-encounter-status.html) defined in the FHIR specifications.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

