---
title: Enable users to enroll for Password Reset
description: To enable users to enroll for the Password Reset program, you specify a UI macro that takes the user through the enrollment process and a script that processes the enrollment data that the user entered. The base system includes a functioning macro and script.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable users to enroll for Password Reset

To enable users to enroll for the Password Reset program, you specify a UI macro that takes the user through the enrollment process and a script that processes the enrollment data that the user entered. The base system includes a functioning macro and script.

## Before you begin

Role required: password\_reset\_admin

## About this task

To enable users to enroll, you configure settings for the verification type that your Password Reset process is based on.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Extensions** &gt; **Verification Types**.

2.  Click the verification type for the verification that your Password Reset process uses.

    The verification type for each base-system verification is identified in [Password Reset verifications](../../login/concept/c_PWRVerifications.md).

3.  On the **Verification Types** page, specify the following settings:

    |Field|Description|
    |-----|-----------|
    |Automatic enrollment|Clear the check box to disable automatic enrollment.|
    |Enrollment UI|Enrollment UI macro that takes the user through the enrollment process.|
    |Enrollment processor|Enrollment processor script that processes enrollment data.|

4.  Repeat the procedure for all verifications that your Password Reset process uses.


## Enabling user enrollment

This example verification type uses the pwd\_enroll\_sms\_ui enrollment UI macro and the PwdEnrollSMSProcessor enrollment processor script.

![Verification type](../image/VerificationTypeExample.png "Verification type")

A verification type must also define a verification UI macro and a corresponding verification processor script. The example uses the pwd\_verify\_sms\_uiverification UI macro and the PwdVerifySMSProcessor verification processor script.

![UI macro](../image/VerificationTypeSMSUIMacro.png "Verification UI macro")

![Verification processor](../image/VerificationTypeSMSProcessor.png "Verification processor script")

**Parent Topic:**[Configure your Password Reset process](../../login/task/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Calculating the security score for password reset process](../../login/reference/pwd-reset-process-recommend.md)

[Configure password expiration reminder](../../login/task/password-reset-expiration-setup.md)

[Credential stores for Password Reset](../../login/concept/c_CredentialStores.md)

[Password Reset verifications](../../login/concept/c_PWRVerifications.md)

[Configure your Password Reset process to auto-enroll users](configure-auto-enroll-for-pwd-reset.md)

[Configure Password Reset properties](../../login/task/t_SetPwdResetProps.md)

[Send email to remind users to enroll for Password Reset](../../login/task/config-pwd-reset-enroll-reminder.md)

[Configure the required strength for passwords](../../login/task/config-pwd-strength-rqmts.md)

[Specify lockout for failed login attempts](t_LockoutForFailedLogins.md)

[Configure Google reCAPTCHA for the password reset process](../../login/task/t_ConfigureGoogleRecaptcha.md)

