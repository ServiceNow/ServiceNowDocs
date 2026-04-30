---
title: Add a custom registration form field
description: You can add custom fields in the user self-registration form.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring a user registration configuration for external users, Self-register to ServiceNow instance, Authentication, Access Management]
---

# Add a custom registration form field

You can add custom fields in the user self-registration form.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **External User Self-Registration** &gt; **User Registration Configurations**.

2.  Open the record for the required user registration configuration.

3.  Navigate to the end of the Registration Form Fields section and click **Insert a new row...**.

4.  Enter the field name under the **Label** column and click check mark.

    A new row is added with the default values. You can configure the custom registration form field based on your requirements.

<table id="table_vpn_vsd_rlb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

The field name which appears on the registration form.

</td></tr><tr><td>

Type

</td><td>

The type of the user interface element. Following are the supported types: -   Single line text
-   Email
-   Date
-   Date/time
-   Yes/No
-   Wide Single Line Text
-   Multiple Choice
-   Select Box


</td></tr><tr><td>

Display in Registration Form

</td><td>

Option to display the field in the registration form.

</td></tr><tr><td>

Order

</td><td>

The sequence in which the form fields appear on the registration form. The field with the lowest order value appears first and the field with the highest order value is appears last. The default value is 10,000.

</td></tr><tr><td>

Mandatory

</td><td>

Option to make a field mandatory on the registration form.

</td></tr><tr><td>

Validation only field

</td><td>

Option to use a field only for validation purposes. For example, registration code. When set to true, this field is not saved in the User Table \(sys\_user\).

</td></tr></tbody>
</table>5.  Save or Update the changes.


