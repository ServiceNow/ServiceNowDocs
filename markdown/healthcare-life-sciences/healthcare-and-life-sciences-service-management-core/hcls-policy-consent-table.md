---
title: Policy consent table
description: The Policy consent \[sn\_hcls\_policy\_consent\] table stores the details of a consent accepted by a patient or a household member on behalf of the patient.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Policy consent table

The Policy consent \[sn\_hcls\_policy\_consent\] table stores the details of a consent accepted by a patient or a household member on behalf of the patient.

## Key features

-   Includes the consent number and date, patient name, policy type, status, and whether the consent was signed by a household member.
-   Refers to the Policy \[sn\_hcls\_policy\], Healthcare organization \[sn\_hcls\_organization\], Healthcare case \[sn\_hcls\_case\],and Patient \[sn\_hcls\_patient\] tables.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_rdz_dhp_xrb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case

</td><td>

Reference

</td><td>

Healthcare case associated with the policy.

</td></tr><tr><td>

Consent date

</td><td>

Date/Time

</td><td>

Date and time when the consent was accepted.

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

Alpha-numeric profile identifier of the consent.

 The value is auto-generated and is incremented every time you add a new consent to your ServiceNow instance. The initial value for the **Number** field is CON00001000.

**Note:** To customize the number, define the auto-numbering format for the Policy consent \[sn\_hcls\_policy\_consent\] table. For more information, see [Add auto-numbering records in a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AutoNumberingRecordsInATable.md).

</td></tr><tr><td>

Patient

</td><td>

Reference

</td><td>

Individual establishing their personal consent.

</td></tr><tr><td>

Policy

</td><td>

Reference

</td><td>

Policy covered by the consent.

</td></tr><tr><td id="policy-status">

Status

</td><td>

Choice list

</td><td>

Status of a consent.

 The following statuses are available by default:

-   Active
-   Draft
-   Inactive
-   Proposed
-   Rejected

 For more information about the available categories, see [consent state value set](https://www.hl7.org/fhir/valueset-consent-state-codes.html) defined in the FHIR specifications.

</td></tr><tr><td>

Signed by household member

</td><td>

True/False

</td><td>

Option to indicate that the consent was provided by a household member of the patient.

</td></tr><tr><td>

Valid until

</td><td>

Date

</td><td>

Date until which the policy is valid for a patient. The valid until date is calculated based on validity duration of the policy after the date on which the consent was given.

 **Note:** The [**Status**](hcls-policy-consent-table.md#policy-status) field value is updated as active or inactive based on the **Valid until** date.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

