---
title: Configuring Patient Support Services
description: Set up the Patient Support Services application to complete enrollment activities associated with a patient service program.
locale: en-US
release: zurich
product: Patient Support Services
classification: patient-support-services
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 4
breadcrumb: [Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configuring Patient Support Services

Set up the Patient Support Services application to complete enrollment activities associated with a patient service program.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

**Note:** The Patient Support Services application is based on the Patient Support Services data model that extends the [Healthcare and Life Sciences data model](hcls-serv-mgmt-core.md) and stores all enrollment requests in the Enrollment case \[sn\_patientservice\_enroll\_case\] table.

The following table provides an overview of the configuration tasks required for Patient Support Services.

<table id="table_ksw_gpr_4nb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Install Patient Support Services](../task/pss-install-app.md).

</td><td>

Install the Patient Support Services application to work on patient support services.

</td></tr><tr><td>

[Assign roles for Patient Support Services users](../task/pss-assign-roles.md).

</td><td>

Assign roles to control access to features, capabilities, and data in the Patient Support Services application.

</td></tr><tr><td>

[Use the Patient Support Services data model](pss-data-model.md).

</td><td>

Use Patient Support Services tables to store the data related to enrollment requests.

</td></tr><tr><td>

[Approve restricted caller access privileges for Patient Support Services.](pss-approve-rca.md)

</td><td>

Approve restricted caller access \(RCA\) privileges for accessing document templates from the Patient Support Services application.

</td></tr><tr><td>

[Configure an enrollment request form](pss-enroll-form-config.md).

</td><td>

Configure an enrollment request form to enable patients or practitioners enroll into Patient Support Services programs offered by a healthcare organization.

</td></tr><tr><td>

[Configure the submission flow of the enrollment request form](../task/pss-ext-point-enrollment-form.md).

</td><td>

Use scripted extension points to decide what records are created or updated after an enrollment request form is submitted.

</td></tr><tr><td>

[Determine who can conduct training tasks](../task/pss-nurse-ts-group.md).

</td><td>

Add users who can conduct the trainings for Patient Support Services to the Nurse Training Support assignment group.

</td></tr><tr><td>

[Configure an appointment booking setting](pss-appt-booking-setup.md#).

</td><td>

Enable patients to book an appointment for the training tasks conducted within the Patient Support Services application

</td></tr><tr><td>

[Configure a program](pss-program-services-setup.md).

</td><td>

Enable your patients to enroll to a program in the Patient Support Services application.

</td></tr><tr><td>

[Configure a checklist for a program.](../task/pss-config-checklist.md)

</td><td>

Configure a checklist for a Patient Support Services program as an informal list of questions or tasks used as a reminder for the completion of an enrollment request.

</td></tr><tr><td>

[Configure the auto-generation of documents](pss-config-doc-decisions.md).

</td><td>

Define the conditions for auto-generating documents for an enrollment request.

</td></tr><tr><td>

[Add a to-dos menu item to patient portal](pss-config-to-do.md).

</td><td>

Configure the patient portal to add a menu item that lists all to-do items for enrollment request tasks.

</td></tr><tr><td>

[Configure a playbook for Patient Support Services](pss-config-playbook.md).

</td><td>

Configure a playbook to provide step-by-step guidance for resolving enrollment cases.

</td></tr><tr><td>

[Configure a Patient Support Services email notification](pss-config-emails.md).

</td><td>

Configure the email notifications sent to patients about Patient Support Services programs.

</td></tr><tr><td>

[Determine additional user profiles](pss-connector-contributor.md).

</td><td>

Determine who can act as an agent connector or contributor for enrollment cases in the Patient Support Services application.

</td></tr><tr><td>

[Set up the process for contributors to create an enrollment case](pss-case-contributor.md).

</td><td>

Set up the process for creating enrollment cases on a service portal.

</td></tr></tbody>
</table>