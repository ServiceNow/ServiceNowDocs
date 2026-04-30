---
title: Procedure table
description: The Procedure \[sn\_hcls\_procedure\] table stores the information about an action that is or was performed on or for a patient. An action can be a physical intervention like an operation, or less invasive like long-term services, counseling, or hypnotherapy.
locale: en-US
release: zurich
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Procedure table

The Procedure \[sn\_hcls\_procedure\] table stores the information about an action that is or was performed on or for a patient. An action can be a physical intervention like an operation, or less invasive like long-term services, counseling, or hypnotherapy.

## Key features

-   Stores any medical procedures associated with a patient.
-   Includes the procedure code, status, category, date performed, location, and performing practitioner.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

Choice list

</td><td>

Code that classifies a procedure for searching, sorting, and display purposes.

 The following categories are available by default:

-   Psychiatry procedure or service
-   Counselling
-   Education
-   Surgical procedure
-   Diagnostic procedure
-   Chiropractic manipulation
-   Social service procedure

 For more information about the available types, see [procedure categories](https://www.hl7.org/fhir/valueset-procedure-category.html) defined in the FHIR specifications.

</td></tr><tr><td>

Date performed

</td><td>

Date/Time

</td><td>

Date and time when the procedure was performed.

</td></tr><tr><td>

Encounter

</td><td>

Reference

</td><td>

Encounter created as part of procedure.

</td></tr><tr><td>

External id

</td><td>

String

</td><td>

Identifier of the record in an electronic medical record \(EMR\) system.

</td></tr><tr><td>

Healthcare location

</td><td>

Reference

</td><td>

Healthcare location where the procedure happened.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the procedure.

 The value is auto-generated and is incremented every time you add a new procedure to your ServiceNow instance. The initial value for the **Number** field is PRCD00001001.

**Note:** To customize the number, define the auto-numbering format for the Procedure \[sn\_hcls\_procedure\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Observation

</td><td>

Reference

</td><td>

Observation recorded as part of procedure.

</td></tr><tr><td>

Parent

</td><td>

Reference

</td><td>

Parent healthcare event associated with the procedure.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Patient involved in the procedure.

</td></tr><tr><td>

Practitioner

</td><td>

Reference

</td><td>

Practitioner involved in the procedure.

</td></tr><tr><td>

Procedure code

</td><td>

Reference

</td><td>

Code to identify the specific procedure. Code is based on the Current Procedural Terminology \(CPT\) or Healthcare Common Procedure Coding System \(HCPCS\) coding system.

 For more information about the available codes, see [procedure codes](https://www.hl7.org/fhir/valueset-procedure-code.html) defined in the FHIR specifications.

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

Status of a procedure.

 The following statuses are available by default:

-   Completed
-   Entered In Error
-   In Progress
-   Not Done
-   On Hold
-   Preparation
-   Stopped
-   Unknown

 For more information about the available statuses, see [event statuses](https://www.hl7.org/fhir/valueset-event-status.html) defined in the FHIR specifications.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

