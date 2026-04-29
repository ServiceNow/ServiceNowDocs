---
title: Practitioner table
description: The Practitioner \[sn\_hcls\_practitioner\] table stores the details of a practitioner in your healthcare organization.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Practitioner table

The Practitioner \[sn\_hcls\_practitioner\] table stores the details of a practitioner in your healthcare organization.

## Key features

-   Models a healthcare practitioner data object.
-   Includes the name, gender, date of birth, and contact information like phone numbers and emails of practitioners.
-   Includes a reference to the sys\_user entry for a practitioner to log in to a ServiceNow instance to perform tasks.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_rkd_g4t_mpb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

True/False

</td><td>

Option to indicate that the practitioner is associated with your healthcare organization.

</td></tr><tr><td>

City

</td><td>

String

</td><td>

City in which the practitioner is located.

</td></tr><tr><td>

Country

</td><td>

String

</td><td>

Country in which the practitioner is located.

</td></tr><tr><td>

Date of birth

</td><td>

Date

</td><td>

Birth date of the practitioner.

</td></tr><tr><td>

District

</td><td>

String

</td><td>

District of the city in which the practitioner is located.

</td></tr><tr><td>

Effective from

</td><td>

Date

</td><td>

Start date of the period during which the practitioner is authorized to perform in the location.

</td></tr><tr><td>

Effective until

</td><td>

Date

</td><td>

End date of the period during which the practitioner is authorized to perform in the location.

</td></tr><tr><td>

Ethnicity

</td><td>

Choice list

</td><td>

Ethnic group the practitioner identifies with.

 The following types are available by default:

-   Hispanic or Latino
-   Not Hispanic or Latino
-   Unable to report due to do policy/law

</td></tr><tr><td>

First name

</td><td>

String

</td><td>

First name of the practitioner.

</td></tr><tr><td>

Gender

</td><td>

Choice list

</td><td>

Gender of the practitioner.

 The following types are available by default:

-   Female
-   Male
-   Non binary
-   Not disclosed
-   Other

</td></tr><tr><td>

Home phone

</td><td>

String

</td><td>

Home phone number of the practitioner.

</td></tr><tr><td>

Last name

</td><td>

String

</td><td>

Last name of the practitioner.

</td></tr><tr><td>

Mobile phone

</td><td>

String

</td><td>

Mobile phone number of the practitioner.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name to identify the practitioner.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the practitioner.

 The value is auto-generated and is incremented every time you add a new practitioner to an instance. The initial value for the **Number** field is PRACT00001001.

**Note:** To customize the number, define the auto-numbering format for the Practitioner \[sn\_hcls\_practitioner\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Practitioner id or NPI

</td><td>

String

</td><td>

Identifier that applies to the person in the practitioner role.

</td></tr><tr><td>

Prefix

</td><td>

String

</td><td>

Part of the practitioner name that is acquired as a title due to academic, legal, employment or nobility status, and that appears at the start of the name.

 For example, Doctor or Dr.

</td></tr><tr><td>

Primary email

</td><td>

String

</td><td>

Email address of the practitioner to which any correspondence is sent.

</td></tr><tr><td>

Race

</td><td>

Choice list

</td><td>

Race of the practitioner.

 The following types are available by default:

-   American Indian or Alaska Native
-   Asian
-   Black or African American
-   Native Hawaiian or Other Pacific Islander
-   Other Race

Unable to report due to do policy/law

-   White

</td></tr><tr><td>

Secondary email

</td><td>

String

</td><td>

Alternative email address of the practitioner.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

State or province

</td><td>

String

</td><td>

State or province in which the practitioner is located.

</td></tr><tr><td>

Street address

</td><td>

String

</td><td>

Mailing street address of the practitioner.

</td></tr><tr><td>

Suffix

</td><td>

String

</td><td>

Part of the practitioner name that is acquired as a title due to academic, legal, employment or nobility status, and that appears at the end of the name.

 For example, M.D. \(Physician\)

</td></tr><tr><td>

Work email

</td><td>

String

</td><td>

Email address of the practitioner associated with the practitioner's business profile.

</td></tr><tr><td>

Work phone

</td><td>

String

</td><td>

Work phone number of the practitioner.

</td></tr><tr><td>

Zip or Postal code

</td><td>

String

</td><td>

ZIP or postal code for the practitioner.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

