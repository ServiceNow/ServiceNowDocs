---
title: Allergy intolerance table
description: The Allergy intolerance \[sn\_hcls\_allergy\] table stores the information about a clinical assessment of an allergy or intolerance; a propensity, or a potential risk to an individual, to have an adverse reaction on future exposure to the specified substance, or class of substance.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Allergy intolerance table

The Allergy intolerance \[sn\_hcls\_allergy\] table stores the information about a clinical assessment of an allergy or intolerance; a propensity, or a potential risk to an individual, to have an adverse reaction on future exposure to the specified substance, or class of substance.

## Key features

-   Stores any allergy or intolerance associated with a patient.
-   Includes the allergy code, type, category, criticality, clinical status, date recorded, and date of onset.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_gsz_dbb_npb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Age of onset

</td><td>

String

</td><td>

Age at which an individual first experience the allergy or intolerance.

</td></tr><tr><td>

Allergy intolerance code

</td><td>

Reference

</td><td>

Identifier of the allergy or intolerance.

</td></tr><tr><td>

Category

</td><td>

Choice list

</td><td>

Category of an identified substance associated with the allergy or intolerance.

 The following categories are available by default:

-   Biological
-   Environment
-   Food
-   Medication

 For more information about the available categories, see [allergy intolerance categories](https://www.hl7.org/fhir/valueset-allergy-intolerance-category.html) defined in the FHIR specifications.

</td></tr><tr><td>

Clinical status

</td><td>

Choice list

</td><td>

Status of the allergy or intolerance under clinical trial.

 The following statuses are available by default:

-   Active
-   Inactive
-   Resolved

 For more information about the available statuses, see [allergy intolerance clinical statuses](https://www.hl7.org/fhir/valueset-allergyintolerance-clinical.html) defined in the FHIR specifications.

</td></tr><tr><td>

Criticality

</td><td>

Choice list

</td><td>

Estimate of the potential clinical harm or seriousness of a reaction to an identified substance.

 The following types are available by default:

-   High
-   Low
-   Unable to access

 For more information about the available types, see [allergy intolerance criticality types](https://www.hl7.org/fhir/valueset-allergy-intolerance-criticality.html) defined in the FHIR specifications.

</td></tr><tr><td>

Date of onset

</td><td>

Date/Time

</td><td>

Date and time that the allergy or intolerance began.

</td></tr><tr><td>

Date recorded

</td><td>

Date/Time

</td><td>

Date the first version of the allergy or intolerance was recorded into the application.

</td></tr><tr><td>

Encounter

</td><td>

Reference

</td><td>

Healthcare event during which this allergy intolerance was asserted.

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

Alpha-numeric profile identifier of the allergy intolerance.

 The value is auto-generated and is incremented every time you add a new allergy or intolerance to your ServiceNow instance. The initial value for the **Number** field is ALLR00001001.

**Note:** To customize the number, define the auto-numbering format for the Allergy intolerance \[sn\_hcls\_allergy\] table. For more information, see Add auto-numbering records in a table.

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Patient who has the allergy or intolerance.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Type

</td><td>

Choice list

</td><td>

Underlying physiological mechanism for a reaction risk.

 The following types are available by default:

-   Allergy
-   Intolerance

 For more information about the available types, see [allergy intolerance types](https://www.hl7.org/fhir/valueset-allergy-intolerance-type.html) defined in the FHIR specifications.

</td></tr><tr><td>

Verification status

</td><td>

Choice list

</td><td>

Assertion about certainty associated with a propensity or potential risk of a reaction to the identified substance.

 The following statuses are available by default:

-   Confirmed
-   Entered in error
-   Refuted
-   Unconfirmed

 For more information about the available statuses, see [allergy intolerance verification statuses](https://www.hl7.org/fhir/valueset-allergyintolerance-verification.html) defined in the FHIR specifications.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

