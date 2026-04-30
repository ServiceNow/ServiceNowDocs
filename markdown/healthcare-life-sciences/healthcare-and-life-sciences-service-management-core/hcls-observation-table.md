---
title: Observation table
description: The Observation \[sn\_hcls\_observation\] table stores the information about measurements and simple assertions made about a patient.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data Model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Observation table

The Observation \[sn\_hcls\_observation\] table stores the information about measurements and simple assertions made about a patient.

## Key features

-   Stores any observations about a patient.
-   Includes the status, category, observed date, anatomical location, and practitioner who recorded the observation.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Anatomical location

</td><td>

Reference

</td><td>

Body sites of the observation.

</td></tr><tr><td>

Category

</td><td>

Choice list

</td><td>

High-level observation category.

 The following categories are available by default:

-   Activity
-   Exam
-   Imaging
-   Laboratory
-   Procedure
-   Social history
-   Survey
-   Therapy
-   Vital signs

 For more information about the available categories, see [observation categories](https://www.hl7.org/fhir/valueset-observation-category.html) defined in the FHIR specifications.

</td></tr><tr><td>

Date observed

</td><td>

Date/Time

</td><td>

Date and time when the observation was first recorded into the application.

</td></tr><tr><td>

Encounter

</td><td>

Reference

</td><td>

Healthcare event related to the observation.

</td></tr><tr><td>

External id

</td><td>

String

</td><td>

Identifier of the record in an electronic medical record \(EMR\) system.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the observation.

 The value is auto-generated and is incremented every time you add a new observation to your ServiceNow instance. The initial value for the **Number** field is OBSV00001001.

**Note:** To customize the number, define the auto-numbering format for the Observation \[sn\_hcls\_observation\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Observation

</td><td>

Reference

</td><td>

Code for an observation type.

 For more information about the available codes, see [observation codes](https://www.hl7.org/fhir/valueset-observation-codes.html) defined in the FHIR specifications.

</td></tr><tr><td>

Organization

</td><td>

Reference

</td><td>

Organization that is responsible for the observation.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Patient who is being observed.

</td></tr><tr><td>

Practitioner

</td><td>

Reference

</td><td>

Practitioner who is responsible for the observation.

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

Status of an observation.

 The following statuses are available by default:

-   Amended
-   Final
-   Preliminary
-   Registered

 For more information about the available statuses, see [observation statuses](https://www.hl7.org/fhir/valueset-observation-status.html) defined in the FHIR specifications.

</td></tr><tr><td>

Verification status

</td><td>

Choice list

</td><td>

Verification status to support or decline the clinical status of the condition or diagnosis.

 The following statuses are available by default:

-   Confirmed
-   Differential
-   Entered in error
-   Provisional
-   Refuted
-   Unconfirmed

 For more information about the available statuses, see [condition verification statuses](http://terminology.hl7.org/CodeSystem/condition-ver-status) defined in the FHIR specifications.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

