---
title: Claim header table
description: The Claim header \[sn\_hcls\_claim\_header\] table stores the details of the main claim submitted on behalf of a patient to a payer organization.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Claim header table

The Claim header \[sn\_hcls\_claim\_header\] table stores the details of the main claim submitted on behalf of a patient to a payer organization.

The table has the following features:

-   Stores the main claim submitted on behalf of a patient to a payer organization.
-   Enables including multiple claim lines.
-   Includes the payer, transaction control number, type, status, patient, member plan, medical record number, account number, and various dates and amounts.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_i41_xh3_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Adjudicated amount

</td><td>

Currency

</td><td>

Adjusted amount paid for the service by the primary payer.

</td></tr><tr><td>

Billed DRG code

</td><td>

String

</td><td>

Diagnosis Related Group \(DRG\) code for the billed diagnosis-related group.

</td></tr><tr><td>

Claim amount

</td><td>

Currency

</td><td>

Original amount submitted with the claim.

</td></tr><tr><td>

Date accepted

</td><td>

Date

</td><td>

Date when the claim was accepted by the payer organization.

</td></tr><tr><td>

Date adjudicated

</td><td>

Date

</td><td>

Date when the claim was adjudicated for the payment.

</td></tr><tr><td>

Date paid

</td><td>

Date

</td><td>

Date when the claim was paid by the payer organization.

</td></tr><tr><td>

Date submitted

</td><td>

Date

</td><td>

Date when the claim was submitted to the payer organization.

</td></tr><tr><td>

Fee reduction amount

</td><td>

Currency

</td><td>

Difference between the original claim amount and the adjusted paid amount.

</td></tr><tr><td>

Medical record number

</td><td>

String

</td><td>

Medical Record Number \(MRN\) of the patient as entered in the electronic medical records \(EMR\) system.

</td></tr><tr><td>

Member plan

</td><td>

Reference

</td><td>

Member plan associated with the patient.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name to identify the claim header.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the claim header.

 The value is auto-generated and is incremented every time you add a new claim header to an instance. The initial value for the **Number** field is CLAIMHDR00001001.

**Note:** To customize the number, define the auto-numbering format for the Claim header \[sn\_hcls\_claim\_header\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Paid amount

</td><td>

Currency

</td><td>

Amount to be paid by the patient.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Patient on whose behalf the claim was submitted.

</td></tr><tr><td>

Patient account number

</td><td>

String

</td><td>

Patient account number as entered in the EMR system.

</td></tr><tr><td>

Patient payable amount

</td><td>

Currency

</td><td>

Amount for which the patient is responsible.

</td></tr><tr><td>

Payer

</td><td>

Reference

</td><td>

Name of the company listed as a payer organization.

</td></tr><tr><td>

Preauthorization header

</td><td>

Reference

</td><td>

Associated pre-authorization request.

</td></tr><tr><td>

Remarks

</td><td>

String

</td><td>

Comments or additional information about the claim.

</td></tr><tr><td>

Service provider

</td><td>

Reference

</td><td>

Practitioner who provided the service to the patient.

</td></tr><tr><td>

Service provider id

</td><td>

String

</td><td>

Identifier of the practitioner who provided the product or service to the patient.

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

Status of the claim.

 The following statuses are available by default:

-   Active
-   Cancelled
-   Denied
-   Draft
-   Entered in error
-   In hold
-   Paid
-   Suspended

 For more information about the available statuses, see [claim statuses](http://hl7.org/fhir/2016sep/codesystem-claim-status.html) defined in the FHIR specifications.

</td></tr><tr><td>

Transaction control number

</td><td>

String

</td><td>

Unique identifier of the claim in the payer system.

</td></tr><tr><td>

Type

</td><td>

Choice list

</td><td>

Type of the claim.

 The following types are available by default:

-   Institutional
-   Oral
-   Pharmacy
-   Professional
-   Vision

 For more information about the available claim types, see [claim types](https://www.hl7.org/fhir/valueset-claim-type.html) defined in the FHIR specifications.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

