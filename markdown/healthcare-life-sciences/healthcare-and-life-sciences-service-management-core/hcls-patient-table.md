---
title: Patient table
description: The Patient \[sn\_hcls\_patient\] table stores the details of a patient in your healthcare organization.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Patient table

The Patient \[sn\_hcls\_patient\] table stores the details of a patient in your healthcare organization.

## Key features

-   Extends the Consumer profile \[sn\_csm\_consumer\_profile\] table.
-   Stores details of a patient, the central object in the Healthcare and Life Sciences data model.
-   Stores basic patient information including first name, last name, date of birth, gender, primary and secondary emails, home, work and mobile phones.
-   Includes the consumer attribute associated with the patient that is a reference to the Consumer \[csm\_consumer\] table. A Consumer record is automatically created when a patient is created in the Patient \[sn\_hcls\_patient\] table.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_rkd_g4t_mpb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Birth place

</td><td>

Reference

</td><td>

Birth place of the patient.

</td></tr><tr><td>

Date of birth

</td><td>

String

</td><td id="patient-dob">

Birth date of the patient.

</td></tr><tr><td>

Deceased

</td><td>

True/False

</td><td>

Option to indicate the patient is deceased.

</td></tr><tr><td>

Deceased date/time

</td><td>

Date/Time

</td><td>

Date and time of patient's death.

</td></tr><tr><td>

Ethnicity

</td><td>

Choice list

</td><td id="patient-ethnic">

Ethnic group the patient identifies with.

 The following types are available by default:

-   Hispanic or Latino
-   Not Hispanic or Latino
-   Unable to report due to do policy/law

</td></tr><tr><td>

First name

</td><td>

String

</td><td id="patient-fn">

First name of the patient.

</td></tr><tr><td>

Gender

</td><td>

Choice list

</td><td id="patient-gender">

Gender of the patient.

 The following types are available by default:

-   Female
-   Male
-   Non binary
-   Not disclosed
-   Other

</td></tr><tr><td>

Guarantor id

</td><td>

String

</td><td id="patient-guarantor">

Identifier that applies to a person who is responsible for paying all charges for services ordered on behalf of the patient

</td></tr><tr><td>

Home phone

</td><td>

String

</td><td id="patient-hp">

Home phone number of the patient.

</td></tr><tr><td>

Interpreter required

</td><td>

True/False

</td><td>

Option to indicate that an interpreter is needed during patient interactions.

</td></tr><tr><td>

Is DOB estimated

</td><td>

True/False

</td><td>

Option to indicate the date of birth \(DOB\) of the patient is an estimated value.

</td></tr><tr><td>

Language code

</td><td>

Reference

</td><td>

Represents the preferred language of interaction for the patient.

</td></tr><tr><td>

Last name

</td><td>

String

</td><td id="patient-ln">

Last name of the patient.

</td></tr><tr><td>

Marital status

</td><td>

Choice list

</td><td>

Marital status of the patient.

</td></tr><tr><td>

Middle name

</td><td>

String

</td><td>

Middle name of the patient.

</td></tr><tr><td>

Mobile phone

</td><td>

String

</td><td id="patient-mp">

Mobile phone number of the patient.

</td></tr><tr><td>

Occupation

</td><td>

String

</td><td>

Occupation of the patient.

</td></tr><tr><td>

Name

</td><td>

String

</td><td id="patient-name">

Name to identify the patient.

</td></tr><tr><td>

Number

</td><td>

String

</td><td>

Alpha-numeric profile identifier of the patient.

 The value is auto-generated and is incremented every time you add a new patient to an instance. The initial value for the **Number** field is PAT00001001.

**Note:** To customize the number, define the auto-numbering format for the Patient \[sn\_hcls\_patient\] table. For more information, see [Add auto-numbering records in a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AutoNumberingRecordsInATable.md).

</td></tr><tr><td>

Preferred communication channel

</td><td>

Choice list

</td><td id="patient-pcm-channel">

Patient's preferred communication channel, including email, phone, or chat.

 The value is dependent on the value entered in the Preferred communication method field.

</td></tr><tr><td>

Preferred communication method

</td><td>

Choice list

</td><td id="patient-pcm">

Patient's preferred communication method, including email, text, or phone.

</td></tr><tr><td>

Prefix

</td><td>

String

</td><td id="patient-prefix">

Part of the patient name that is acquired as a title due to academic, legal, employment or nobility status, and that appears at the start of the name.

 For example, Mr. or Mrs.

</td></tr><tr><td>

Primary email

</td><td>

String

</td><td id="patient-email">

Email address of the patient to which any correspondence is sent.

</td></tr><tr><td>

Race

</td><td>

Choice list

</td><td id="patient-race">

Race of the patient.

 The following types are available by default:

-   American Indian or Alaska Native
-   Asian
-   Black or African American
-   Native Hawaiian or Other Pacific Islander
-   Other Race

Unable to report due to do policy/law

-   White

</td></tr><tr><td>

Research consent given

</td><td>

True/False

</td><td>

Option to indicate that the patient has given consent to take part in research programs.

</td></tr><tr><td>

Secondary email

</td><td>

String

</td><td id="patient-email-second">

Alternative email address of the patient.

</td></tr><tr><td>

SMS consent given

</td><td>

True/False

</td><td>

Option to indicate that the patient has given consent to be communicated with via SMS. Protected health information is shared only if indicated.

</td></tr><tr><td>

Source

</td><td>

Reference

</td><td>

Source system details of an external healthcare system in a ServiceNow instance.

</td></tr><tr><td>

Suffix

</td><td>

String

</td><td id="patient-suffix">

Part of the patient name that is acquired as a title due to academic, legal, employment or nobility status, and that appears at the end of the name.

 For example, MD or PhD.

</td></tr><tr><td>

Work phone

</td><td>

String

</td><td id="patient-wp">

Work phone number of the patient.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

