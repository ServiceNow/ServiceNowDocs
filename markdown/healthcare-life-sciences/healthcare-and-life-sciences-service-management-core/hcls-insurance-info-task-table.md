---
title: Update insurance information table
description: The Update insurance information \[hcls\_insurance\_info\_task\] table stores the task details for updating the insurance information of a patient in your healthcare organization.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Update insurance information table

The Update insurance information \[hcls\_insurance\_info\_task\] table stores the task details for updating the insurance information of a patient in your healthcare organization.

## Key features

-   Extends the Healthcare Task \[sn\_hcls\_task\] table to store task details created for updating the insurance information of a patient.
-   Includes the payment type, insurance company, insurance plan, member number, group number, Rx Bin, Rx Group, Rx PCN.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group number

</td><td>

String

</td><td>

Group number or policy number of the member.

</td></tr><tr><td>

Insurance company

</td><td>

Reference

</td><td>

Name of the company listed as a payer organization.

</td></tr><tr><td>

Medical insurance model

</td><td>

Reference

</td><td>

Payer plan associated with the patient.

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

Processor control number \(PCN\) is another identifier used to route pharmacy reimbursements.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

