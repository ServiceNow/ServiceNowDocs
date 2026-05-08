---
title: Password Reset Process form
description: Description of the fields on the Password Reset Process form.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Password Reset reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset Process form

Description of the fields on the Password Reset Process form.

<table id="table_yrq_b1k_zzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Security score

</td><td>

View the security score in digits. As the security score changes, the color of the field changes.The following are three ranges of the security score:

-   0 to 40: The color is red and the security is low.
-   40 to 75: The color is orange and the security is medium.
-   76 to 100: The color is green and the security is high.

</td></tr><tr><td>

Enable security score notification

</td><td>

Send security score notifications to process owners.If this field is selected, a weekly scheduled job sends emails containing the security score for all the active public processes.

**Note:** The email notifications aren't sent for the service-desk processes and the processes for which only Change Password is configured.

</td></tr><tr><td>

Process owner

</td><td>

Designate one or more users as owners for the process you're creating. You can add only the users with the password reset admin role to this field.If you select **Enable security score notification**, the Process owner field becomes a required field.

</td></tr></tbody>
</table>**Note:** The Process Strength Configuration section is displayed only when you select the **Public access** check box in the **Password Reset Details** tab.

<table id="table_qmr_mpk_sr"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Public access

</td><td>

The check box is available only when **Password reset** is selected.

 -   Select the check box to enable a self-service process with public user access to the Password Reset or Password Change form through a URL.
-   Clear the check box to define a Service desk-assisted process in which only service desk agents can reset a password at the request of a user.

</td></tr><tr><td>

Public URL

</td><td>

The field is available only when **Public access** is selected.

 URL of the page where users go to reset or change the password. The value from the URL suffix field is appended to the URL when you tab out of the URL suffix field. For the Default self-service Password Reset process, this value must be `/$pwd_reset.do?sysparm_url=ss_default`.

</td></tr><tr><td>

URL suffix

</td><td>

The field is available only when **Public access** is selected.

 Suffix used to create a unique URL for the Password Reset or Password Change form.

</td></tr><tr><td>

Display CAPTCHA

</td><td>

The check box is available only when **Public access** is selected.

Select the check box to display a CAPTCHA on the user identification page. The Password Reset application uses Google reCAPTCHA as the default CAPTCHA service. See [Configure Google reCAPTCHA for the password reset process](../task/t_ConfigureGoogleRecaptcha.md).

 **Note:** The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA.

 Because on-premises instances do not have access to the internet, the instances cannot use the Google reCAPTCHA service. Set the **password\_reset.captcha.google.enabled** system property to **false** for on-premises instances.

 To use the base system CAPTCHA, change the **password\_reset.captcha.google.enabled** system property to false.

</td></tr><tr><td>

Identification type

</td><td>

Method that the user employs to claim identity for the public Password Reset or Password Change process. Any selection overrides the default identification that is associated with the process. The base system includes the Email and Username Identification identification types. You can create a custom identification type \(some knowledge of JavaScript is recommended\).

 See [Personal data identification types and confirmation type verifications](../concept/c_PersonalDataAndPDConfirmVerifs.md).

</td></tr><tr><td>

Redirect URL

</td><td>

URL to go to after a successfully resetting a password — typically, the URL of the original login page. Enter a complete path, including the protocol \(for example, https://myDomain.myURL.com\). If the path is under the same domain as the **Public URL**, then start the path with the / character.

</td></tr><tr><td>

Minimum verifications

</td><td>

Number of verifications that a user must successfully submit to reset the password. If the number exceeds the number of required verifications, then the user must submit enough additional optional verifications to meet the number specified for **Minimum verifications**.

 **Note:** Each user must submit all mandatory verifications regardless of the number specified.

 By default, during the password reset process, the system presents optional verifications to the user based on the **Order** values for the verifications. If you selected **Allow user to choose from optional verifications**, then the Verification page presents all optional verifications to the user. The user then selects the appropriate number of verifications. In this example, the **Minimum verifications** value is `1`. Because no mandatory verifications are configured, the user can choose an optional verification.

 Also, see **Allow user to choose from optional verifications**.

</td></tr><tr><td>

Allow user to choose from optional verifications

</td><td>

Select the check box to enable a user, on the Verifications page during the process of resetting the password, to select which optional verifications to use. The choice of optional verifications appears only if the **Minimum verifications** setting is greater than the number of mandatory verifications. The number that you specify for **Minimum verifications** determines how many optional verifications that the user is allowed to select.

 In the example, the **Minimum verifications** setting is **2** and there are no mandatory verifications. The user has selected two optional verifications, so cannot select a third verification.![User chooses which optional verifications to use](../image/select-optional-verifications.png)

</td></tr><tr><td>

Email/SMS Password Reset URL

</td><td>

Select the check box to enable users to reset the password by clicking a link in an email that the instance sends to them. This is the secured method of resetting a password. If configured, the instance also sends the URL to the users through SMS on mobile devices. By default, the self-service Password Reset processes enable this option. When you select this option, the **Auto-generate password** check box is not available. See Example: The default self-service Password Reset process for an outline of the process that is enabled by default.

 If you don’t select the **Email/SMS Password Reset URL** option and try to save the record, you get a message that suggests you select the verification options to configure with secure verification.

You can’t set the QA verification as the only verification for this process as the process becomes less secure. You must either enable the **Email/SMS Password Reset URL** option or configure this process with multi-factor authentication. Also, you can’t configure the process only with personal data and QA verifications. You must configure any other verification along with these two.

If you still don’t select the **Email/SMS Password Reset URL** option with a weak security verification configuration, it might allow unauthenticated users to reset any user’s password using any user ID or email address.

</td></tr><tr><td>

Enable account unlock

</td><td>

This check box is available only when **Password reset** is selected.

 Select the check box to allow user accounts on credential stores to be unlocked without resetting the password.

 **Note:** Not supported by the default self-service Password Reset process.

</td></tr><tr><td>

Unlock user account

</td><td>

Select the check box to unlock user accounts on credential stores after a password reset.

</td></tr><tr><td>

Auto-generate password

</td><td>

Select the check box to auto-generate a new password for the user. When this check box is selected, you must select the **Email/SMS password** or **Display password** check box, or both. This setting is useful for Service Desk assisted processes.

This check box is available only when:-   The **Password reset** check box is selected.
-   The **Email/SMS Password Reset URL** check box is cleared.

 **Note:** If you use the credential store on your local ServiceNow instance or an Active Directory credential store: Clear the check box to enable the **Enforce history policy** option for a credential store. See [Configure the connection to a credential store for the Password Reset processes](../task/t_CreateACredentialStore.md).

</td></tr><tr><td>

User must reset password

</td><td>

This check box is available only when **Auto-generate password** is selected.

 Select the check box to require users to reset their password immediately after logging in with the auto-generated password.

**Note:** Users whose credentials are held in the local ServiceNow instance credential store are prompted to change their password the first time that they log in. Users whose credentials are held in an Active Directory credential store are not prompted to change their passwords in the instance. Such users must change their passwords from a computer on the domain.

</td></tr><tr><td>

Display password

</td><td>

This check box is available only when **Auto-generate password** is selected.

Select the check box to display the new password on the screen. In a self-service process, the password appears on the user screen. In a service desk-assisted process, the password appears on the service desk agent screen.

</td></tr><tr><td>

Email/SMS password

</td><td>

This check box is available only when **Auto-generate password** is selected.

 Select the check box to email or SMS the new password to the user. The setting is useful in both self-service and Service Desk assisted processes. The setting can add a layer of security by requiring that users access their email or SMS to view the password. In a Service Desk assisted process, sending password through email or SMS to users ensures that only the user requesting the password reset can view the password.

</td></tr></tbody>
</table><table id="table_cmx_2jc_fbb"><thead><tr><th>

List

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verifications

</td><td>

One or more verifications that the Password Reset process uses. See [Password Reset verifications](../concept/c_PWRVerifications.md).The Verifications related list is available only after the record has been saved.

</td></tr><tr><td>

Groups

</td><td>

ServiceNow user groups to associate with the Password Reset process.The Groups related list is available only after the record has been saved and if the **Apply to all users** check box is cleared.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Entry UI macro|UI macro that displays a customized message to users when they access the initial Password Reset screen.|
|Success UI macro|UI macro that displays a customized message to users on the final Password Reset screen when their password is successfully reset.|
|Failure UI macro|UI macro that displays a customized message to users on the final Password Reset screen when their password reset fails.|
|Post reset script|Script include that performs actions after the Password Reset process completes whether the outcome is success or failure. For more information on customizing post processor scripts, see the **Post reset** script category as described in [Password Reset extension script categories](../concept/pw-reset-extension-script.md).|
|Header UI macro or Footer UI macro|Macros that add a header or footer to customize the appearance of the pages that end users work in while resetting a password \(the Identify, Verify, and Reset pages. See [Add a custom header or footer to the user pages for Password Reset](../task/customize-user-reset-pages.md).|

**Related topics**  


[Configure your Password Reset process](../task/t_CreateAPasswordResetProcess.md)

