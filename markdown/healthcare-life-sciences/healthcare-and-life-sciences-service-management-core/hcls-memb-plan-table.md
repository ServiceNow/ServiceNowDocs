---
title: Member plan table
description: The Member Plan \[sn\_hcls\_member\_plan\] table stores the details of a health insurance plan associated with a patient.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data Model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Member plan table

The Member Plan \[sn\_hcls\_member\_plan\] table stores the details of a health insurance plan associated with a patient.

## Key features

-   Extends the Install base item \[sn\_install\_base\_item\] table to store member plan details.
-   Models the health insurance data associated with a patient, including the member number, group number, the payer plan that is purchased and start and end dates of the plan.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_ikm_hwn_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Effective from

</td><td>

Date

</td><td>

Start date from when the member plan is effective.

</td></tr><tr><td>

Effective to

</td><td>

Date

</td><td>

End date until when the member plan is effective.

</td></tr><tr><td>

External identifier

</td><td>

String

</td><td>

Identifier of the record in an electronic medical record \(EMR\) system.

</td></tr><tr><td>

Group number

</td><td>

String

</td><td>

Group number or policy number of the member.

</td></tr><tr><td>

Member

</td><td>

Reference

</td><td>

The associated member's first and last name.

</td></tr><tr><td>

Member number

</td><td>

String

</td><td>

Unique ID number of the patient that enables healthcare providers to verify insurance coverage and arrange payment for services.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the member plan.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Name of the patient in whose name is the plan.

</td></tr><tr><td>

Plan priority

</td><td>

String

</td><td>

Priority of the plan.

 The priority of the plan is:

-   **Primary**: The first member plan to which the patient is the subscriber and that is used as if there's no other plans for the patient.
-   **Secondary**: The second member plan to which the patient is listed as a dependent.
-   **Tertiary**: The third member plan to be billed for the patient. The tertiary plan is used after the primary and secondary plans have been successfully processed.

</td></tr><tr><td>

Payer plan

</td><td>

Reference

</td><td>

Member plan taken by the patient.

</td></tr><tr><td>

Relation to subscriber

</td><td>

Reference

</td><td>

Relationship of the dependent member with the subscriber.

</td></tr><tr><td>

Rx Bin

</td><td>

String

</td><td>

Number to identify how a prescription drug will be reimbursed and where a pharmacy can send a reimbursement claim to.

</td></tr><tr><td>

Rx Group

</td><td>

String

</td><td>

Alphanumeric or numeric value of the member plan that is used to process prescription benefits.

</td></tr><tr><td>

Rx PCN

</td><td>

String

</td><td>

Processor control number \(PCN\) used in routing of pharmacy reimbursements.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Subscriber

</td><td>

Reference

</td><td>

Subscriber's patient record.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

