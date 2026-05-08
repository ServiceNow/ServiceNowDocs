---
title: Configure a privacy policy for managing patient consent
description: Configure a privacy policy for effectively managing patient and member consent to a healthcare request.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Determining the consent management process for patients, Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure a privacy policy for managing patient consent

Configure a privacy policy for effectively managing patient and member consent to a healthcare request.

## Before you begin

Role required: sn\_hcls.admin or admin

## Procedure

1.  Navigate to **All** &gt; **HCLS Service Management** &gt; **Administration** &gt; **Privacy Policy**.

2.  In the Policies list, click **New**.

3.  On the form, fill in the fields.

<table id="table_lq3_tdh_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Alpha-numeric profile identifier of the policy.

 The value is auto-generated and is incremented every time you add a new policy to your ServiceNow instance. The initial value for the **Number** field is POL00001000.

**Note:** To customize the number, define the auto-numbering format for the Policy \[sn\_hcls\_policy\] table. For more information, see Add auto-numbering records in a table.

</td></tr><tr><td>

Policy category

</td><td>

This field should be set to **Registration**.

</td></tr><tr><td>

Policy type

</td><td>

Type of the policy.

 A policy is one of the following types:

-   **Standard**: A policy that doesn't require a consent form to be signed by a patient.
-   **Document template**: A policy that requires a consent form to be signed by a patient.

With the Document template policy type, a to-do item is created for the patient to sign the consent form.

</td></tr><tr><td>

Validity duration \(in days\)

</td><td>

Number of days the policy is valid for after a patient signs the policy.

</td></tr><tr><td>

Active

</td><td>

Option for enabling the privacy policy.

</td></tr><tr><td>

Scope

</td><td>

Type of consent included in the policy.For privacy consent, select **Privacy consent**. Else, this field should be left empty.

</td></tr><tr><td>

Document template

</td><td>

Document template to generate standard letters or documents associated with the policy.

 This field is used only when the [Policy type](hcls-config-policy-consent.md#policy_type) field is set to **Document template**.

 **Note:** You can associate only one active policy with a document template.

 For more information, see [Configure document templates for Healthcare and Life Sciences Service Management Core](../concept/hcls-config-doc-templates.md).

</td></tr><tr><td>

External policy link

</td><td>

External reference to the policy included in a consent scope.

</td></tr><tr><td>

Policy name

</td><td>

Name to identify the policy.

</td></tr><tr><td>

Policy content

</td><td>

Content of the policy that should be read and accepted by the Patient Portal users at the time of registration.

</td></tr></tbody>
</table>4.  Click **Submit**.


