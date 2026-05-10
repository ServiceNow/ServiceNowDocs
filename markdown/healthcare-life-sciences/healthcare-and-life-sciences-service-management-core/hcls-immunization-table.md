---
title: Immunization table
description: The Immunization \[sn\_hcls\_immunization\] table stores the information about an event of a patient being administered a vaccine or a record of an immunization as reported by a patient, a clinician, or another party.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Immunization table

The Immunization \[sn\_hcls\_immunization\] table stores the information about an event of a patient being administered a vaccine or a record of an immunization as reported by a patient, a clinician, or another party.

## Key features

-   Extends the Install base item \[sn\_install\_base\_item\] table to store immunization details.
-   Stores all immunization data associated with a patient, including the vaccine received, administered date, recommended doses, dose number, location where it was administered, practitioner who administered it, and the condition for which the vaccine was given.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administered by

</td><td>

Reference

</td><td>

Practitioner who administered the patient.

</td></tr><tr><td>

Administration route

</td><td>

Choice list

</td><td>

Route by which the vaccine was administered.

 The following routes are available by default:

-   Intradermal
-   Intramuscular
-   Intravenous
-   Nasal
-   Oral
-   Percutaneous
-   Subcutaneous
-   Transdermal

 For more information about the available routes, see [immunization routes](https://www.hl7.org/fhir/DSTU2/valueset-medication-admin-status.html) defined in the FHIR specifications.

</td></tr><tr><td>

Body site

</td><td>

Choice list

</td><td>

Body site at which the vaccine was administered.

 The following body sites are available by default:

-   Left arm
-   Left deltoid
-   Left gluteus medius
-   Left lower forearm
-   Left thigh
-   Left vastus lateralis
-   Right arm
-   Right deltoid
-   Right thigh
-   Right gluteus medius
-   Right lower forearm
-   Right vastus lateralis

 For more information about the body sites, see [immunization sites](https://www.hl7.org/implement/standards/fhir/2015Jan/valueset-immunization-site.html) defined in the FHIR specifications.

</td></tr><tr><td>

Date administered

</td><td>

Date/Time

</td><td>

Date and time when the vaccine was administered.

</td></tr><tr><td>

Dose number

</td><td>

Integer

</td><td>

Dose sequence number within the vaccine series.

</td></tr><tr><td>

Dose quantity

</td><td>

String

</td><td>

Quantity of dose given to the patient.

</td></tr><tr><td>

Encounter

</td><td>

Reference

</td><td>

Encounter the immunization was part of.

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

Service delivery location in which the vaccine was or was to be administered.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the immunization.

 The value is auto-generated and is incremented every time you add a new immunization to your ServiceNow instance. The initial value for the **Number** field is IMM00001001.

**Note:** To customize the number, define the auto-numbering format for the Immunization \[sn\_hcls\_immunization\] table. For more information, see [Add auto-numbering records in a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AutoNumberingRecordsInATable.md).

</td></tr><tr><td>

Observation

</td><td>

Reference

</td><td>

Observation associated with the immunization.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Patient who received the vaccine and is being administered.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Vaccine product

</td><td>

Reference

</td><td>

Vaccine product sold to the patient who is being administered.

</td></tr><tr><td>

Recommended doses

</td><td>

Integer

</td><td>

Recommended number of doses to achieve immunity.

</td></tr><tr><td>

Status

</td><td>

Choice list

</td><td>

Status of the immunization.

 The following statuses are available by default:

-   Completed
-   Incorrect entry
-   Not done

 For more information about the available statuses, see [immunization statuses](https://www.hl7.org/fhir/valueset-immunization-status.html) defined in the FHIR specifications.

</td></tr><tr><td>

Status reason

</td><td>

String

</td><td>

Explanation why a vaccine was not administered.

</td></tr><tr><td>

Target disease

</td><td>

Reference

</td><td>

Vaccine preventable disease the dose is being administered for.

</td></tr><tr><td>

Vaccine expiry date

</td><td>

Date

</td><td>

Date when the vaccine product expires.

</td></tr><tr><td>

Vaccine lot number

</td><td>

String

</td><td>

Lot number of the vaccine product.

</td></tr><tr><td>

Vaccine manufacturer

</td><td>

String

</td><td>

Manufacturer of the vaccine product.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

