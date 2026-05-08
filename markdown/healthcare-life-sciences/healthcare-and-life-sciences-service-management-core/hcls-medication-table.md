---
title: Medication table
description: The Medication \[sn\_hcls\_medication\] table stores the information about a medication for the purposes of prescribing, dispensing, and administering a medication as well as for making statements about medication use.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Medication table

The Medication \[sn\_hcls\_medication\] table stores the information about a medication for the purposes of prescribing, dispensing, and administering a medication as well as for making statements about medication use.

## Key features

-   Extends the Install base item \[sn\_install\_base\_item\] table to store medication details associated with a patient.
-   Stores all medications received by a patient, including the medication name, start and end dates, status, the condition for which it was given, and the procedure it may be associated with.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition

</td><td>

Reference

</td><td>

Condition for which the medication is being administered.

</td></tr><tr><td>

Date administered

</td><td>

Date/Time

</td><td>

Date and time when the medication was administered.

</td></tr><tr><td>

Encounter

</td><td>

Reference

</td><td>

Associated encounter as part of which medication was administered.

</td></tr><tr><td>

End date

</td><td>

Date

</td><td>

Date when the patient completed taking the medication.

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

Alpha-numeric profile identifier of the medication.

 The value is auto-generated and is incremented every time you add a new medication to your ServiceNow instance. The initial value for the **Number** field is MED00001001.

**Note:** To customize the number, define the auto-numbering format for the Medication \[sn\_hcls\_medication\] table. For more information, see Add auto-numbering records in a table.

</td></tr><tr><td>

Observation

</td><td>

Reference

</td><td>

Observation associated with the medication.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Patient who received the medication and is being administered.

</td></tr><tr><td>

Procedure

</td><td>

Reference

</td><td>

Procedure during which the medication is being administered.

</td></tr><tr><td>

Medication product

</td><td>

Reference

</td><td>

Medication sold to the patient.

</td></tr><tr><td>

Parent medication

</td><td>

Reference

</td><td>

Parent medication product associated with the medication product.

</td></tr><tr><td>

Reason code

</td><td>

String

</td><td>

System-defined code that represents the reason why a medication was administered.

</td></tr><tr><td>

Reason description

</td><td>

String

</td><td>

Reason why a medication was administered.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Start date

</td><td>

Date

</td><td>

Date when the patient started taking the medication.

</td></tr><tr><td>

Status

</td><td>

Choice list

</td><td>

Status of the medication.

 The following statuses are available by default:

-   Completed
-   Entered in error
-   In progress
-   Not done
-   On hold
-   Stopped
-   Unknown

 For more information about the available statuses, see [medication statuses](https://www.hl7.org/fhir/valueset-medication-status.html) defined in the FHIR specifications.

</td></tr><tr><td>

Status reason

</td><td>

String

</td><td>

Explanation of the selected status.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

