---
title: Appointment participant table
description: The Appointment participant \[sn\_hcls\_appointment\_participant\] table stores the participant details of an appointment including practitioners.
locale: en-US
release: zurich
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Appointment participant table

The Appointment participant \[sn\_hcls\_appointment\_participant\] table stores the participant details of an appointment including practitioners.

## Key features

-   Stores the participant details associated with an appointment.
-   Includes the appointment name, practitioner category, participant type, and practitioner ID.

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

Identifier of the appointment entered in the electronic medical records \(EMR\) system.

</td></tr><tr><td>

Participant type

</td><td>

Choice list

</td><td>

Type of the participant.

 The following types are available by default:

-   Organization
-   Practitioner
-   Referring patient

</td></tr><tr><td>

Practitioner ID

</td><td>

Reference

</td><td>

Identifier of the practitioner entered in the EMR system.

</td></tr><tr><td>

Practitioner category

</td><td>

Choice list

</td><td>

Category of the practitioner

 The following categories are available by default:

-   Attending
-   Consulting
-   Referring provider
-   Surgical staff
-   Visiting

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

