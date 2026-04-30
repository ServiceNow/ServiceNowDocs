---
title: Condition table
description: The Condition \[sn\_hcls\_condition\] table stores the information about a condition, problem, diagnosis, or other event, situation, issue, or clinical concept that has risen to a level of concern.
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Healthcare and Life Sciences data model tables, Healthcare and Life Sciences Service Management Core reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Condition table

The Condition \[sn\_hcls\_condition\] table stores the information about a condition, problem, diagnosis, or other event, situation, issue, or clinical concept that has risen to a level of concern.

## Key features

-   Stores any medical conditions or diseases that a patient may have reported or diagnosed with.
-   Includes the condition code, anatomical location, category, clinical status, date recorded, and date of onset.

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

Body sites where the condition manifested.

</td></tr><tr><td>

Category

</td><td>

Choice list

</td><td>

Category of the condition.

 The following categories are available by default:

-   Diagnosis
-   Problem

 For more information about the available categories, see [condition categories](https://www.hl7.org/fhir/valueset-condition-category.html) defined in the FHIR specifications.

</td></tr><tr><td>

Clinical status

</td><td>

Choice list

</td><td>

Status of the subject under clinical trial.

 The following statuses are available by default:

-   Active
-   Inactive
-   Recurrence
-   Relapse
-   Remission
-   Resolved

 For more information about the available statuses, see [condition clinical statuses](https://www.hl7.org/fhir/valueset-condition-clinical.html) defined in the FHIR specifications.

</td></tr><tr><td>

Condition code

</td><td>

Reference

</td><td>

Identifier of the condition, problem, or diagnosis.

</td></tr><tr><td>

Date recorded

</td><td>

Date/Time

</td><td>

Date and time when the condition was first recorded into the application.

 This field is automatically set to the current date and time.

</td></tr><tr><td>

Encounter

</td><td>

Reference

</td><td>

Healthcare event during which this condition was created or to which the creation of this record is tightly associated.

</td></tr><tr><td>

External identifier

</td><td>

String

</td><td>

Identifier of the record in an electronic medical record \(EMR\) system.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the condition.

 The value is auto-generated and is incremented every time you add a new condition to your ServiceNow instance. The initial value for the **Number** field is COND00001001.

**Note:** To customize the number, define the auto-numbering format for the Condition \[sn\_hcls\_condition\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Onset age

</td><td>

String

</td><td>

Age at which an individual acquires, develops, or first experiences a condition or symptoms of a disease or disorder.

</td></tr><tr><td>

Onset date

</td><td>

Date/Time

</td><td>

Date and time when the condition began, in the opinion of the clinician.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Patient associated with the condition record.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Verification status

</td><td>

Choice list

</td><td>

Verification status to support or decline the clinical status of the condition.

 The following statuses are available by default:

-   Confirmed
-   Differential
-   Entered in error
-   Provisional
-   Refuted
-   Unconfirmed

 For more information about the available statuses, see [condition verification statuses](https://www.hl7.org/fhir/valueset-condition-ver-status.html) defined in the FHIR specifications.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

