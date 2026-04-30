---
title: Healthcare code set table
description: The Healthcare code set \[sn\_hcls\_code\_set\] table stores the details of code sets available in your ServiceNow instance.
locale: en-US
release: xanadu
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Healthcare and Life Sciences data model tables, Healthcare and Life Sciences Service Management Core reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Healthcare code set table

The Healthcare code set \[sn\_hcls\_code\_set\] table stores the details of code sets available in your ServiceNow instance.

## Key features

-   Enables HL7-based data tables including healthcare specialties, services, procedures, encounters.
-   Enables grouping of all HL7 data into code sets with attributes type, code, and name.
-   By default, supports the following HL7-based data tables:
    -   [Care specialty](https://www.hl7.org/fhir/valueset-c80-practice-codes.html)
    -   [Condition](https://www.hl7.org/fhir/valueset-condition-code.html)
    -   [Observation](https://www.hl7.org/fhir/valueset-observation-codes.html)
    -   [Procedure](https://www.hl7.org/fhir/valueset-procedure-code.html)
    -   [Allergy intolerance](https://www.hl7.org/fhir/valueset-allergyintolerance-code.html)
    -   [Encounter](https://www.hl7.org/fhir/valueset-encounter-type.html)
    -   [Body site](https://www.hl7.org/fhir/valueset-body-site.html)
    -   [Service type](https://www.hl7.org/fhir/valueset-service-type.html)
    -   [Service category](https://www.hl7.org/fhir/valueset-service-category.html)
    -   [Priority](https://www.hl7.org/fhir/valueset-request-priority.html)
    -   [Medication code](https://www.hl7.org/fhir/valueset-medication-codes.html)
    -   [Medication form code](https://www.hl7.org/FHIR/valueset-medication-form-codes.html)
    -   [Practitioner type](https://www.hl7.org/fhir/valueset-practitioner-role.html)

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_whb_q5s_mpb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Code

</td><td>

String

</td><td>

Code value including symbols, expressions, or both.

</td></tr><tr><td>

Code system ID

</td><td>

String

</td><td>

Identifier of the system that holds the code set.

</td></tr><tr><td>

Code system name

</td><td>

String

</td><td>

Name of the system that holds the code set.

</td></tr><tr><td>

External identifier

</td><td>

String

</td><td>

Identifier of the record in an electronic medical record \(EMR\) system.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name to identify the code.

</td></tr><tr><td>

Type

</td><td>

Choice list

</td><td>

Common language including set of identifiers, names, and codes for identifying health measurements, observations, and documents.

 The following types are available by default:

-   Allergy Intolerance
-   Body site
-   Care specialty
-   Condition
-   Encounter
-   Language code
-   Medication code
-   Medication form code
-   Observation
-   Practitioner type
-   Procedure
-   Priority
-   Service category
-   Service type

 For more information about the available code sets, see [value sets all types](https://www.hl7.org/fhir/R4/valueset-all-types.html) defined in the FHIR specifications.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

