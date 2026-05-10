---
title: Specify lockout for failed login attempts
description: The system provides inactive script actions that enable you to specify the number of failed login attempts before a user account is locked and to reset the count after a successful login.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Specify lockout for failed login attempts

The system provides inactive script actions that enable you to specify the number of failed login attempts before a user account is locked and to reset the count after a successful login.

## Before you begin

Role required: password\_reset\_admin

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Script Actions** to view or activate the scripts.

    **Note:** Starting with the Kingston release, following a zBoot, the script actions **SNC User Lockout Check with Auto Unlock** and **SNC User Clear** are activated.

    To learn more about properties that affect failed login attempts, see [Managing failed login attempts \(instance security hardening\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-managing-failed-login-attempts.md) in the Instance Security Hardening Settings.

<table id="table_yzs_qcf_g1b"><thead><tr><th>

Script action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SNC User Lockout Check with Auto Unlock

</td><td>

-   Uses the value of the glide.user.max\_unlock\_attempts property to set the limit for failed login attempts.
-   Unlocks the user account after the time period that is specified for the glide.user.unlock\_timeout\_in\_mins property. If no value is specified, then the system unlocks the user account after the default period of 15 minutes.


</td></tr><tr><td>

SNC User Lockout Check

</td><td>

Tracks the number of failed login attempts and locks the user account after a specified number of failed login attempts \(default: 5\).

</td></tr><tr><td>

SNC User Clear

</td><td>

Updates the user record after a successful login: Resets the number of failed login attempts and updates the date of the last login.

</td></tr></tbody>
</table>
## What to do next

Each time a user attempts to log in, the action is recorded in an event log. You can view a log of failed login attempts.

1.  Navigate to **System Policy** &gt; **Event Logs**.
2.  Filter for **login.failed** in the **Name** field. You can view the attempted login name, date, and IP address logged for the attempt.

**Parent Topic:**[Configure your Password Reset process](../../login/task/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Calculating the security score for password reset process](../../login/reference/pwd-reset-process-recommend.md)

[Configure password expiration reminder](../../login/task/password-reset-expiration-setup.md)

[Credential stores for Password Reset](../../login/concept/c_CredentialStores.md)

[Password Reset verifications](../../login/concept/c_PWRVerifications.md)

[Configure your Password Reset process to auto-enroll users](configure-auto-enroll-for-pwd-reset.md)

[Enable users to enroll for Password Reset](configure-user-enroll-for-pwd-reset.md)

[Configure Password Reset properties](../../login/task/t_SetPwdResetProps.md)

[Send email to remind users to enroll for Password Reset](../../login/task/config-pwd-reset-enroll-reminder.md)

[Configure the required strength for passwords](../../login/task/config-pwd-strength-rqmts.md)

[Configure Google reCAPTCHA for the password reset process](../../login/task/t_ConfigureGoogleRecaptcha.md)

