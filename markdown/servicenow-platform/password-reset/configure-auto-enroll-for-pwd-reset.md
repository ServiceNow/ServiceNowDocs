---
title: Configure your Password Reset process to auto-enroll users
description: To simplify management, many organizations auto-enroll users in the Password Reset program. Every base-system verification type enables you to specify automatic enrollment for your process.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure your Password Reset process to auto-enroll users

To simplify management, many organizations auto-enroll users in the Password Reset program. Every base-system verification type enables you to specify automatic enrollment for your process.

## Before you begin

Role required: password\_reset\_admin or admin

## About this task

To enable automatic enrollment, you configure settings for the verification type that your Password Reset process is based on.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Extensions** &gt; **Verification Types**.

2.  Click the verification type for the verification that your Password Reset process uses.

    The verification type for each base-system verification is identified in [Password Reset verifications](../../login/concept/c_PWRVerifications.md).

3.  On the **Verification Types** page, specify the following settings:

<table id="table_p5w_mgz_h1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enrollment check

</td><td>

Script that determines whether a user is enrolled for verification. **Note:** For automatic enrollment to work, the **Enrollment check** script must return true. This may require additional setup by the admin to ensure that the preconditions are met. For example, for the **SMS Code** verification type, records must be populated in particular tables.

 If no script is specified when **Automatic Enrollment** is selected, a default script is provided.

</td></tr><tr><td>

Automatic enrollment

</td><td>

Select the check box to auto-enroll users. **Note:** If **Automatic enrollment** is not selected, then you must provide an enrollment UI macro and enrollment processor script as described in [Create a custom Password Reset verification type](../../login/task/create-verification-type.md).

</td></tr></tbody>
</table>4.  Repeat the procedure for all verifications that your Password Reset process uses.


**Parent Topic:**[Configure your Password Reset process](../../login/task/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Configure password expiration reminder](../../login/task/password-reset-expiration-setup.md)

[Credential stores for Password Reset](../../login/concept/c_CredentialStores.md)

[Password Reset verifications](../../login/concept/c_PWRVerifications.md)

[Enable users to enroll for Password Reset](configure-user-enroll-for-pwd-reset.md)

[Configuring Password Reset properties](../../login/task/t_SetPwdResetProps.md)

[Send email to remind users to enroll for Password Reset](../../login/task/config-pwd-reset-enroll-reminder.md)

[Configure the required strength for passwords](../../login/task/config-pwd-strength-rqmts.md)

[Specify lockout for failed login attempts](t_LockoutForFailedLogins.md)

[Configure Google reCAPTCHA for the password reset process](../../login/task/t_ConfigureGoogleRecaptcha.md)

