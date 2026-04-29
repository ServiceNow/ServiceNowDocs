---
title: Calculating the security score for password reset process
description: The security score of the password reset process is a critical metric for the password reset administrators to assess the strength and configuration of the password reset process.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Calculating the security score for password reset process

The security score of the password reset process is a critical metric for the password reset administrators to assess the strength and configuration of the password reset process.

## Password reset calculation

The password reset process score provides a quantitative measure of how well the process is configured to protect against unauthorized access and confirm that only legitimate users can reset their passwords. The score is based on the following categories:

-   Identification score \(Max: 20 points\)
-   Verification score \(Max: 40 points\)
-   Configuration score \(Max: 20 points\)
-   Password policy score \(Max: 20 points\)

## Identification score

To increase your identification score, you must enable multiple identification methods. If you’re currently using only one method, such as a username, adding another method like an email can increase your score by approximately five points. Additionally, enabling CAPTCHA adds 10 points to your score and help to prevent the bots from exploiting the password reset flow.

## Verification score

To achieve a high score, you must use at least two verification methods with medium or high security levels. Each method adds up to 15 points \(medium\) or 25 points \(high\).

For the custom verification types, you must assign the security level. By default the custom verification is set as **low**.

## Configuration score

To optimize your score, enable either the Email/SMS Password Reset URL or auto-generate passwords. If neither is enabled, the score is set at 10 points. Enabling either of these options fetches 20 points.

## Password Policy Score

To maximize your Password Policy Score, enable the Password Policy on the Credential Store if it isn’t active. Implement the Enforce History Policy to prevent users from reusing their last five passwords as defined in the **password\_history\_limit** property. Use a **High** strength password policy and enable the following settings:

**Send password reset process security score notification** is a weekly job that send reminders to the password admin about the score and recommendations to improve the score. An email notification is sent to the Process Owners of all the active processes if **Enable security score notification** option is selected in Password Reset Process form.

**Parent Topic:**[Configure your Password Reset process](../task/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Configure password expiration reminder](../task/password-reset-expiration-setup.md)

[Credential stores for Password Reset](../concept/c_CredentialStores.md)

[Password Reset verifications](../concept/c_PWRVerifications.md)

[Configure your Password Reset process to auto-enroll users](../../security/task/configure-auto-enroll-for-pwd-reset.md)

[Enable users to enroll for Password Reset](../../security/task/configure-user-enroll-for-pwd-reset.md)

[Configure Password Reset properties](../task/t_SetPwdResetProps.md)

[Send email to remind users to enroll for Password Reset](../task/config-pwd-reset-enroll-reminder.md)

[Configure the required strength for passwords](../task/config-pwd-strength-rqmts.md)

[Specify lockout for failed login attempts](../../security/task/t_LockoutForFailedLogins.md)

[Configure Google reCAPTCHA for the password reset process](../task/t_ConfigureGoogleRecaptcha.md)

