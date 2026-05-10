---
title: Claim line table
description: The Claim line \[sn\_hcls\_claim\_line\] table stores the details of the items pertaining to a claim header.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Claim line table

The Claim line \[sn\_hcls\_claim\_line\] table stores the details of the items pertaining to a claim header.

## Key features

-   Stores the items pertaining to a claim header.
-   Includes the payer, provider control number, line title, line number, parent claim, line status, associated procedure, location, practitioner, service start and end dates, various amounts, and codes.

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

Adjusted amount paid for the service associated with the claim line.

</td></tr><tr><td>

Claim

</td><td>

Reference

</td><td>

Original claim associated with the claim line.

</td></tr><tr><td>

Code modifier

</td><td>

String

</td><td>

Modifier that helps further describe a procedure code without changing its definition.

</td></tr><tr><td>

Comments

</td><td>

String

</td><td>

Additional information about the clam line.

</td></tr><tr><td>

Days/Units

</td><td>

String

</td><td>

Number of days or units of the service provided.

</td></tr><tr><td>

Exception codes

</td><td>

String

</td><td>

Exception codes associated with the claim line.

</td></tr><tr><td>

Fee reduction

</td><td>

Currency

</td><td>

Difference between the original claim amount and the adjusted paid amount.

</td></tr><tr><td>

Line number

</td><td>

String

</td><td>

Sequential number to distinguish the service submitted in a claim.

</td></tr><tr><td>

Line status

</td><td>

Choice list

</td><td>

Status of the claim line rather than the entire claim.

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

Line title

</td><td>

String

</td><td>

Name to identify the claim line.

</td></tr><tr><td>

Location

</td><td>

Reference

</td><td>

Location where the service was performed.

</td></tr><tr><td>

National drug code

</td><td>

String

</td><td>

Code of the drug included in the service as identified in the National Drug Code \(NDC\) billing guidelines.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the claim line.

 The value is auto-generated and is incremented every time you add a new claim line to an instance. The initial value for the **Number** field is CLAIMLN00001001.

**Note:** To customize the number, define the auto-numbering format for the Claim line \[sn\_hcls\_claim\_line\] table. For more information, see [Add auto-numbering records in a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AutoNumberingRecordsInATable.md).

</td></tr><tr><td>

Original transaction control number

</td><td>

String

</td><td>

Unique identifier of the original claim in the payer system.

</td></tr><tr><td>

Paid amount

</td><td>

Currency

</td><td>

Total amount paid or the service associated with the claim line.

</td></tr><tr><td>

Procedure code

</td><td>

Reference

</td><td>

Code to identify the specific procedure associated with the claim. Code is based on the Current Procedural Terminology \(CPT\) or Healthcare Common Procedure Coding System \(HCPCS\) coding system.

 For more information about the available codes, see [procedure codes](https://www.hl7.org/fhir/valueset-procedure-code.html) defined in the FHIR specifications.

</td></tr><tr><td>

Provider control number

</td><td>

String

</td><td>

Number assigned to the service by the service provider for tracking and billing purposes.

</td></tr><tr><td>

Revenue code

</td><td>

String

</td><td>

Revenue grouping code associated with the claim line.

</td></tr><tr><td>

Service end date

</td><td>

Date

</td><td>

Service end date for the claim line.

</td></tr><tr><td>

Service price

</td><td>

Currency

</td><td>

Price of the service associated with the claim line.

</td></tr><tr><td>

Service provider

</td><td>

Reference

</td><td>

Practitioner who provided the service to the patient.

</td></tr><tr><td>

Service start date

</td><td>

Date

</td><td>

Service start date for the claim line.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Tooth code

</td><td>

String

</td><td>

Code of the tooth on which service was performed.

 Applies to dental providers only.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

