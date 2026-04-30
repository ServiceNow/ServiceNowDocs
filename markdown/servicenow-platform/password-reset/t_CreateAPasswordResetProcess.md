---
title: Configure your Password Reset process
description: To implement the process, you configure credentials, verification methods and settings, and enrollment settings. You also specify to which users the process applies.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure your Password Reset process

To implement the process, you configure credentials, verification methods and settings, and enrollment settings. You also specify to which users the process applies.

## Before you begin

Role required: password\_reset\_admin or admin

1.  Be sure to [Plan your Password Reset processes](t_PlanPasswordReset.md).
2.  Create the credential store record for user names and passwords that are managed.

    **Note:** For LDAP integrations: If the Active Directory settings require users to reset the password when logging in, the results depend on the installed Password Reset plugin.

    -   The Password Reset plugin cannot change an AD password. End users will not be able to log in to the instance.
    -   The Self Service Password Reset plugin depends on the Password Reset Basic plugin. Self service is intended for password reset only on the local ServiceNow instance and cannot change an AD password. In order to change AD password, you must install the **Microsoft AD spoke for Password Reset**.
    -   The Password Reset Windows App \(com.glideapp.password\_reset\_desktop\) plugin supports changing the AD password.
3.  Define the verifications that the process can use.
4.  Configure Password Reset to auto-enroll users or to enable users to enroll for the program. See [Configure your Password Reset process to auto-enroll users](../../security/task/configure-auto-enroll-for-pwd-reset.md) and [Enable users to enroll for Password Reset](../../security/task/configure-user-enroll-for-pwd-reset.md).

## About this task

A Password Reset process consists of the following elements:

-   The credential store that contains user login credentials.
-   Optionally, the user groups that are authorized to use the Password Reset process.
-   The verifications that verify the identity of the requesting user and that enable the service desk agents to authorize reset of the password. \(Verifications are implemented by script includes.\)
-   Process strength configuration that helps view the security score of the process. You see the score in digits and colors based on the verification methods you select for the process. If enabled, notifications can be sent for potential configuration improvements to the process. If there are any deviations between the maximum attainable and current scores, an email with an actionable list of recommendations to improve the configuration is sent.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Processes**.

2.  Click **New** and then specify a meaningful **Name** and **Description** for the process.

3.  Select the **Credential store** that contains the user credentials that the process applies to.

4.  Specify the process that you are defining: Select the **Password reset** check box, the **Password change** check box, or both check boxes.

5.  Specify the **Apply to all users** setting.

    |**Setting of the Apply to all users check box**|Result|
    |-----------------------------------------------|------|
    |**Selected**|All users use the process that you are defining. This setting is useful only if all users have access to the authentication methods that are defined in this process.|
    |**Not selected**|Only the users in the groups that you specify use the process. You specify the groups in the **Groups** related list.|

    For more information about the fields on the Password Reset Process form, see [Password Reset Process form](../reference/configure-password-reset-form.md).

6.  For Password Reset, configure settings on the **Password Reset Details** tab.

    For information about the settings and fields on the **Password Reset Details** tab, see [Description of the fields on the **Password Reset Details** tab](../reference/configure-password-reset-form.md#table_qmr_mpk_sr).

7.  For Password Reset, configure settings of interest on the **Advanced** tab.

    For information about the fields on the **Advanced** tab, see [Description of the fields on the **Advanced** tab](../reference/configure-password-reset-form.md#table_alq_tgk_xvb).

8.  For Password Reset, fill in any fields of interest on the **Enrollment Reminder** tab.

9.  Save your changes on the Password Reset Process form.

    The form refreshes, and additional related lists appear.

10. From the **Password Reset Process Verifications** related list, select one or more verifications.

11. From the **Password Reset Process Groups** related list, select the user groups that use the process that you are defining.

    The **Password Reset Process Groups** related list appears only if the **Apply to all users** check box is not selected.

12. Save the record and then select the **Active** check box to enable the Password Reset process that you configured.

    The check box is available only after the record has been saved.

13. Click **Update**.

14. Navigate to **Password Reset** &gt; **Properties** to set the properties that configure the Password Reset experience for end users.


-   **[Configure password expiration reminder](password-reset-expiration-setup.md)**  
You can configure the password reset expiration reminder feature to send notifications to change or reset a user’s password whenever it is going to expire.
-   **[Credential stores for Password Reset](../concept/c_CredentialStores.md)**  
Credential stores hold user information such as user names and passwords that can be used as login credentials. Examples include the User table \[sys\_user\] or an Active Directory server.
-   **[Password Reset verifications](../concept/c_PWRVerifications.md)**  
Each verification specifies the method and process for verifying the identity of the user that is requesting a password reset.
-   **[Configure your Password Reset process to auto-enroll users](../../security/task/configure-auto-enroll-for-pwd-reset.md)**  
To simplify management, many organizations auto-enroll users in the Password Reset program. Every base-system verification type enables you to specify automatic enrollment for your process.
-   **[Enable users to enroll for Password Reset](../../security/task/configure-user-enroll-for-pwd-reset.md)**  
To enable users to enroll for the Password Reset program, you specify a UI macro that takes the user through the enrollment process and a script that processes the enrollment data that the user entered. The base system includes a functioning macro and script.
-   **[Configuring Password Reset properties](t_SetPwdResetProps.md)**  
You can specify properties that configure the Password Reset experience for end users.
-   **[Send email to remind users to enroll for Password Reset](config-pwd-reset-enroll-reminder.md)**  
 You can automatically send messages that remind users to enrolled in the Password Reset process. You specify the text of the message and can configure the messages to repeat at intervals.
-   **[Configure the required strength for passwords](config-pwd-strength-rqmts.md)**  
The password that a user defines must meet certain requirements — for example, it must contain at least 12 characters, it must include a numeral, and so on. You can configure the requirements as needed for your organization.
-   **[Specify lockout for failed login attempts](../../security/task/t_LockoutForFailedLogins.md)**  
The system provides inactive script actions that enable you to specify the number of failed login attempts before a user account is locked and to reset the count after a successful login.
-   **[Configure Google reCAPTCHA for the password reset process](t_ConfigureGoogleRecaptcha.md)**  
To use the Google reCAPTCHA service, instances that are running on a domain other than `service-now.com` require an API key pair from Google.

**Parent Topic:**[Configuring Password Reset](../concept/password-reset-admin-guide.md)

**Related topics**  


[Plan your Password Reset processes](t_PlanPasswordReset.md)

[Configure the required strength for passwords](config-pwd-strength-rqmts.md)

