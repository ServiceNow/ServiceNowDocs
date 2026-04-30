---
title: Policy table
description: The Policy \[sn\_hcls\_policy\] table stores the details of a policy shared with patients in the Healthcare and Life Sciences applications.
locale: en-US
release: zurich
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Policy table

The Policy \[sn\_hcls\_policy\] table stores the details of a policy shared with patients in the Healthcare and Life Sciences applications.

## Key features

-   Includes the consent number and date, patient name, policy type, status, and whether the consent was signed by a household member.
-   Refers to the Document Template \[sn\_doc\_template\] table.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_rdz_dhp_xrb"><thead><tr><th>

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

Option to indicate that the policy is in use.

</td></tr><tr><td>

Document template

</td><td>

Reference

</td><td id="hcls-policy-doc-template">

Document template to generate standard letters or documents associated with the policy.

 This field is used only when the [Policy type](#policy_type) field is set to **Document template**.

 **Note:** You can associate only one active policy with a document template.

 For more information, see [Configure document templates for Healthcare and Life Sciences Service Management Core](../concept/hcls-config-doc-templates.md).

</td></tr><tr><td>

External policy link

</td><td>

URL

</td><td id="hcls-policy-external">

External reference to the policy included in a consent scope.

</td></tr><tr><td>

Number

</td><td>

String

</td><td id="hcls-policy-number">

Alpha-numeric profile identifier of the policy.

 The value is auto-generated and is incremented every time you add a new policy to your ServiceNow instance. The initial value for the **Number** field is POL00001000.

**Note:** To customize the number, define the auto-numbering format for the Policy \[sn\_hcls\_policy\] table. For more information, see [Add auto-numbering records in a table](https://www.servicenow.com/docs/access?context=t_AutoNumberingRecordsInATable&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Policy category

</td><td>

Choice list

</td><td id="hcls-policy-category">

Category of a policy.

 The following categories are available by default:

-   Registration
-   Advance care directive
-   Do not resuscitate
-   Emergency only
-   Health care directive
-   Notice of privacy practices
-   Information disclosure
-   Patient consent
-   Privacy policy acknowledgment document
-   Privacy policy organization document

 For more information about the available categories, see [consent category value set](https://www.hl7.org/fhir/valueset-consent-category.html) defined in the FHIR specifications.

</td></tr><tr><td>

Policy name

</td><td>

String

</td><td id="hcls-policy-name">

Name to identify the policy.

</td></tr><tr><td>

Policy type

</td><td>

String

</td><td id="hcls-policy-type">

Type of the policy.

 A policy is one of the following types:

-   **Standard**: A policy that doesn't require a consent form to be signed by a patient.
-   **Document template**: A policy that requires a consent form to be signed by a patient.

With the Document template policy type, a to-do item is created for the patient to sign the consent form.


</td></tr><tr><td>

Scope

</td><td>

Choice list

</td><td id="hcls-policy-scope">

Type of consent included in the policy.

 The following scope types are available by default:

-   Advance care directive
-   Research
-   Privacy consent
-   Treatment

 For more information about the available scopes, see [consent scope value set](https://www.hl7.org/fhir/valueset-consent-scope.html) defined in the FHIR specifications.

</td></tr><tr><td>

Validity duration \(in days\)

</td><td>

String

</td><td id="hcls-policy-validity">

Number of days the policy is valid for after a patient signs the policy.

</td></tr></tbody>
</table>