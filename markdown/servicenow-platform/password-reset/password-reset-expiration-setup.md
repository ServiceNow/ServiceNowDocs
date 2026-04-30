---
title: Configure password expiration reminder
description: You can configure the password reset expiration reminder feature to send notifications to change or reset a user’s password whenever it is going to expire.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure password expiration reminder

You can configure the password reset expiration reminder feature to send notifications to change or reset a user’s password whenever it is going to expire.

## Before you begin

You must enable the **pwd\_reset.enable.password\_expiration\_reminder** property to configure password expiration reminder. By default, this property is turned off.

Role required: admin

## About this task

Configure password expiration reminder for any credential stores, such as Microsoft Active Directory, Windows Active Directory, and Okta Active Directory.

**Note:** Password expiration reminder doesn’t support the local ServiceNow credential store.

After configuring password expiration reminder, notifications are sent to users by different channels, such as emails, text messages, or actionable virtual agent notifications. Users get an option to reset or change the password through notifications, such as a link that users can select to reset or change the password.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Processes**.

2.  On the Password Reset Process page, select the process for which you want to configure password expiration.

3.  On the form for the selected process, select the **Password Expiration Configuration** tab.

4.  Select the **Send expiration reminder** option.

5.  On the form, fill in the fields.

    For information about the fields on the Password Expiration Configuration form, see [Password Expiration Configuration form](../reference/password-expiration-configuration-form.md).

6.  Save the form.

    After enabling password expiration reminder for a process, a sync expiration data scheduled job runs after an hour. The scheduled job creates records in the password expiration table for every user entitled for that process. The schedule job creates records for the process for which you configured password expiration and users who belong to this process.

    If you find that the data in the password expiration table is not in sync, select **Sync Expiration data** to sync the data. Otherwise, the sync is an automated process.

    **Note:** After you select **Sync Expiration data**, the scheduled job runs after an hour. The **Sync Expiration data** button appears only for those processes that are active and the processes for which the **Send expiration reminder** option is selected.


-   **[View scheduled jobs](view-scheduled-jobs.md)**  
You can view scheduled jobs for the process that you configured password expiration for. When you configure password expiration for a process, two scheduled jobs are created automatically.
-   **[View a password expiration table](view-pwd-exp-table.md)**  
You can view a password expiration table and validate whether a record is created in it.

**Parent Topic:**[Configure your Password Reset process](t_CreateAPasswordResetProcess.md)

**Related topics**  


[Credential stores for Password Reset](../concept/c_CredentialStores.md)

[Password Reset verifications](../concept/c_PWRVerifications.md)

[Configure your Password Reset process to auto-enroll users](../../security/task/configure-auto-enroll-for-pwd-reset.md)

[Enable users to enroll for Password Reset](../../security/task/configure-user-enroll-for-pwd-reset.md)

[Configuring Password Reset properties](t_SetPwdResetProps.md)

[Send email to remind users to enroll for Password Reset](config-pwd-reset-enroll-reminder.md)

[Configure the required strength for passwords](config-pwd-strength-rqmts.md)

[Specify lockout for failed login attempts](../../security/task/t_LockoutForFailedLogins.md)

[Configure Google reCAPTCHA for the password reset process](t_ConfigureGoogleRecaptcha.md)

[System properties for password expiration](../reference/password-expiration-system-properties.md)

