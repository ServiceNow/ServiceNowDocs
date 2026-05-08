---
title: Configure a checklist for Patient Support Services
description: Configure a checklist for a Patient Support Services program as an informal list of questions or tasks used as a reminder for the completion of an enrollment request.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure a checklist for Patient Support Services

Configure a checklist for a Patient Support Services program as an informal list of questions or tasks used as a reminder for the completion of an enrollment request.

## Before you begin

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Role required: admin

## About this task

The checklist feature is available with the Checklist plugin \(com.glide.ui.checklist\). As an administrator, you can create a checklist such as an eligibility checklist for a program or a training completion checklist for a nurse educator and associate them with a Patient Support Services program.

With the Patient Support Services application, the following checklists are available for use:

-   Eligibility Checklist: A sample checklist for determining the eligibility of a patient for a Patient Support Services program.
-   Nurse educator checklist: A sample checklist for conducting a training task. By default, this checklist is assigned to the Nurse Training Support group.

Alternatively, you can create a checklist using the Checklist formatter. For more information, see Create a checklist.

## Procedure

1.  Navigate to **All** &gt; **Patient Support Services** &gt; **Administration** &gt; **Checklist**.

2.  Either configure an existing checklist or create a new one.

    -   Select an existing checklist template.
    -   Create new checklist template by clicking **New**.
3.  On the form, verify the default field values for an existing checklist or fill in the values for a custom configuration.

<table id="table_k5p_mpz_crb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the checklist template

</td></tr><tr><td>

User

</td><td>

User who created the template.

</td></tr><tr><td>

Group

</td><td>

Group who can use the checklist template.

**Note:** Only members of the selected group and the user who created the checklist can use the checklist as a template. Leaving this field empty prevents anyone but the template creator from using the checklist template.

</td></tr><tr><td>

Template

</td><td>

JSON representation of the checklist.

</td></tr></tbody>
</table>4.  Save your changes.

    -   Save a new checklist by clicking **Submit**.
    -   Save the changes to an existing checklist by clicking **Update**.

## What to do next

Associate the checklist with a Patient Support Services program. For more information, see [Configuring a program for Patient Support Services](../concept/pss-program-services-setup.md).

