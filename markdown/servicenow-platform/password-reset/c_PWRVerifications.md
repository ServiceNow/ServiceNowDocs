---
title: Password Reset verifications
description: Each verification specifies the method and process for verifying the identity of the user that is requesting a password reset.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset verifications

Each verification specifies the method and process for verifying the identity of the user that is requesting a password reset.

## Verifications included with Password Reset

The Password Reset application includes the following verifications in the base system. You can create a verification based on either a base-system verification or a verification type \(a template\).

**Note:** The Password Reset Windows Application doesn’t support custom verifications.

<table id="table_mxh_lbz_f1b"><tbody><tr><td>

QA verification

</td><td>

Implements a self-service Password Reset model with questions that are included with the base system or custom questions that the admin defines. While enrolling for the process, the user decides which questions to provide answers for. Questions are presented in the language that the user requested during login.When a user requests a password reset, the system poses a specified number of the questions that the user selected during enrollment. The user must answer all questions correctly to verify their identity.

![QA verification on the Verify page.](../image/verify-enduser-page.png "QA verification on the Verify page")

 For information on the user enrollment experience, see [Enroll for the Password Reset program using questions and answers](../task/t_EnrollUsingASecurityQuestion.md).

 This verification is based on the **Security Questions** verification type.

</td></tr><tr><td>

Email verification

</td><td>

This verification relies on auto-generated code numbers. You typically implement email verification as a self-service Password Reset model.When a user requests a password reset, the system sends a verification code to an email address that the user authorized during enrollment. To verify identity, the user then submits the code on the Password Reset Verify page.

For information on the user enrollment experience, see [Enroll for the Password Reset program using emailed codes](../task/enroll-email-verification.md).

The Password Reset Windows Application supports email verification.

This verification is based on the **Email Code** verification type.

By default, a six-digit email verification code is sent to the user through email. The code expires in 10 minutes. Users can attempt to send another code after two minutes. A maximum of 10 email verification codes can be sent to a user in one day.

</td></tr><tr><td>

SMS verification

</td><td>

Implements a self-service or service desk-assisted Password Reset model that relies on auto-generated code numbers. When a user requests a password reset, the system sends a code to an SMS-capable device that the user has authorized. To verify identity, the user then submits the code on the Password Reset Verify page.

You can use the ServiceNow Notify feature to send the codes.

For information on the user enrollment experience, see [Enroll for the Password Reset program using SMS codes](../task/t_EnrollUsingSMS.md).

This verification is based on the **SMS Code** verification type.

When users enroll for email or SMS verification on the Password Reset Enrollment page, they get a code to verify their email address or device. After the users enter the code and select **Verify**, an associated record is automatically created in the Password Reset Enrollment for Verifications \[pwd\_enrollment\] table even before they select **Submit**.

By default, a six-digit verification code is sent to the user's mobile device. The code expires in five minutes. Users can attempt to send another SMS verification code to the device after two minutes. A maximum of 10 codes can be sent to a particular device in one day.

**Note:** While the record is created automatically in the Password Reset Enrollment for Verifications \[pwd\_enrollment\] table for the email or SMS verification, the associated enrollment check script doesn’t get processed unless users select **Submit**.

</td></tr><tr><td>

Authenticator verification

</td><td>

Password Reset model that relies on auto-generated code numbers. Users typically implement authenticator verification as a self-service Password Reset model.When a user requests a password reset, the user reads a code from the authenticator app on a device that the user has paired. To verify identity, the user then submits the code on the Password Reset Verify page.

 For information on the user enrollment experience, see [Enroll for the Password Reset program using an authenticator](../task/authenticator-app-verification.md).

 The Password Reset Windows Application supports Google Authenticator verification.

 This verification is based on the authenticator verification type.

</td></tr><tr><td>

Personal Data — Confirm Email Address

</td><td>

Implements a self-service Password Reset model that relies on user information that is available in the user profile on the instance.This verification is based on the **Personal Data Confirmation** verification type.

**Note:** Users can't configure this verification for the processes with the active public access.

</td></tr><tr><td>

Personal Data — Enter User Name

</td><td>

Implements a self-service Password Reset model that relies on user information that is available in the user profile on the instance.This verification is based on the **Personal Data** verification type.

</td></tr><tr><td>

Soft PIN Verification

</td><td>

Implements a self-service Password Reset model that relies on a Soft PIN that's a six-digit number. Users can enroll for the Soft PIN verification for a process and reset the Soft PIN. ServiceNow® Virtual Agent supports the Soft PIN verification method.

</td></tr></tbody>
</table>-   **[Personal data identification types and confirmation type verifications](c_PersonalDataAndPDConfirmVerifs.md)**  
Personal data verifications allow users to verify their identity by providing answers to questions that are generated from personal information stored in the User table `[sys_user]`.
-   **[SMS Code Verification type for Password Reset](c_SMSCodeTypeVerifications.md)**  
Using the Simple Message Service \(SMS\) Code Verification type, a user can verify identity with the help of any SMS-enabled device, like a cell phone that accepts text messages. When a user requests password reset, the system sends a numerical code to the device and the user then enters the code on the Password Reset Verification page.
-   **[Specify the number of required security questions](../task/t_SecurityQuestionTypeVerif.md)**  
When designing a Security Questions verification for Password Reset, you can specify the number of questions to display when users enroll. You can also specify the number to display when a user is verifying identity while resetting the password.

**Parent Topic:**[Configure your Password Reset process](../task/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Calculating the security score for password reset process](../reference/pwd-reset-process-recommend.md)

[Configure password expiration reminder](../task/password-reset-expiration-setup.md)

[Credential stores for Password Reset](c_CredentialStores.md)

[Configure your Password Reset process to auto-enroll users](../../security/task/configure-auto-enroll-for-pwd-reset.md)

[Enable users to enroll for Password Reset](../../security/task/configure-user-enroll-for-pwd-reset.md)

[Configure Password Reset properties](../task/t_SetPwdResetProps.md)

[Send email to remind users to enroll for Password Reset](../task/config-pwd-reset-enroll-reminder.md)

[Configure the required strength for passwords](../task/config-pwd-strength-rqmts.md)

[Specify lockout for failed login attempts](../../security/task/t_LockoutForFailedLogins.md)

[Configure Google reCAPTCHA for the password reset process](../task/t_ConfigureGoogleRecaptcha.md)

[Create a custom Password Reset verification](../task/t_CreatePWRVerFromVerType.md)

[Create a Password Reset verification from an existing verification](../task/t_CreatePWRVerFromBaseVer.md)

